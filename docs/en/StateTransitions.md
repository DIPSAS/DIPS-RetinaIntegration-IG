#  - RetinaIntegration v0.9.0

## 

# States and state transitions

The **state** of an examination is determined by the `DiagnosticReport.conclusionCode` (1000 series).

* If the previous examination concluded with 1005, the current examination should go directly to secondary grading.
* Patients are allowed to refuse AI-assisted grading.
* A conclusion from the AI integrator that is based on AI grading requires at least one gradable eye grading result.
* Validation only: If the update is for validation only, the state will be substituted with according to the process rules.

If the AI integrator specifies a transition that does not conform to these rules, the API will ignore or substitute the status and return a warning.

In addition to setting status, all input from the AI integrator is persisted in EyeCare.

How to read the table:

1. The first column is the current state of the examination in EyeCare application
1. The next column is the desired new state received in the`conclusion`parameter
1. The Guard Condition column are rules that may alter what the next state will be, starting from top and going downward
1. The Next State column is the actual next state. It may be differen than the desired state depending on the guard rules.
1. A Warning in the Success / Warning column indicates that the outcome is not exactly what the AI integrator indicated.
1. The Notes column is a description that may be used in the API respons.

## State Transition Table

| | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1001 | 1002 | Previous examination is 1005 | 1003 | Warning | Substitute 1002 with 1003 because the previous examination concluded with 1005. |
| 1001 | 1002 | Valdiation only | 1002 | Success |   |
| 1001 | 1002 | None | 1002 | Success |   |
| 1001 | 1003 | Previous examination is 1005 | 1003 | Success |   |
| 1001 | 1003 | Validation only | 1002 | Success | Substitute 1003 with 1002 because input was only for validation. |
| 1001 | 1003 | Patient refused AI | 1002 | Warning | Substitute 1003 with 1002 because patient refused AI. |
| 1001 | 1003 | No gradable grading | 1002 | Warning | Substitute 1003 with 1002 because the payload does not indicate successful grading. |
| 1001 | 1003 | None | 1003 | Success | Examinations skips primary grading and goes to secondary grading. |
| 1001 | 1004 | Previous examination is 1005 | 1003 | Warning | Substitute 1004 with 1003 because the previous examination concluded with 1005. |
| 1001 | 1004 | Validation only | 1002 | Success | Substitute 1004 with 1002 because input was only for validation. |
| 1001 | 1004 | Patient refused AI | 1002 | Warning | Substitute 1004 with 1002 because the patient has refused AI. |
| 1001 | 1004 | No gradable grading | 1002 | Warning | Substitute 1004 with 1002 because the payload does not indicate successful grading. |
| 1001 | 1004 | None | 1004 | Success | New screening examination in X months. This is the happy case which will have most of the traffic. |
| 1002 | 1002 | None | 1002 | Success |   |
| 1002 | 1003 | Patient refused AI | 1002 | Warning | Substitute 1003 with 1002 because the patient has refused AI. |
| 1002 | 1003 | Validation only | 1002 | Success | Substitue 1003 with 1002 because input was only for validation. |
| 1002 | 1003 | None | 1003 | Success | Examination was awaiting primary grading but AI integrator wants it to go to secondary grading. |
| 1002 | 1004 | Previous examination is 1005 | 1003 | Warning | Substitute 1004 with 1003 because previous examination concluded with 1005. |
| 1002 | 1004 | Validation only | 1002 | Success | Substitute 1004 with 1002 because input was only for validation |
| 1002 | 1004 | Patient refused AI | 1002 | Warning | Substitute 1004 with 1002 because the patient has refused AI. |
| 1002 | 1004 | No gradable grading | 1002 | Warning | Substitute 1004 with 1002 because the payload does not indicate successful grading. |
| 1002 | 1004 | None | 1004 | Success | Transferred from primary grading to new screening examination in X months. |
| 1003 | 1002 | Illegal transition | 1003 | Warning | Substitute 1002 with 1003 because regression from secondary to primary grading is not allowed. |
| 1003 | 1003 | None | 1003 | Success |   |
| 1003 | 1004 | Illegal transition | 1003 | Warning | Substitute 1004 with 1003 the examination was awaiting secondary grading. |
| 1004, 1005, 1006, 1007 | Same as current | None | Same as current | Success | Storing result on finalized examination without changing state. |
| 1004, 1005, 1006, 1007 | Different than current | None | Same as current | Warning | Substituting desired state with current state because current state is final. |

## State Catalog

These are the states that an examination may be in, as determined by the conclusion code.

| | | | | |
| :--- | :--- | :--- | :--- | :--- |
| 1001 | Await AI | Retina photo is taken | Input from AI integrator is received, or manual grading is done. | No |
| 1002 | Await primary grading | Photographer ordered primary grading | Primary grading is done | No |
| 1003 | Await secondary grading | Ordered in EyeCare by primary grader | Secondary grading was done, or previous examination ordered directly to secondary grading. | No |
| 1004 | New examination in X months | Ordered in EyeCare |   | Yes |
| 1005 | New examination in X months directly to secondary grading | Ordered in EyeCare |   | Yes |
| 1006 | Pause screening program | Ordered in EyeCare |   | Yes |
| 1007 | Terminate screening program | Ordered in EyeCare |   | Yes |

## Event Catalog for the AI integrator

These are the states the AI integrator is allowed to set as target state if the desired state is different that the current state.

| | | | |
| :--- | :--- | :--- | :--- |
| 1002 | Primary grading current examination | Optional AI evaluation | AI is not able to grade pictures |
| 1003 | Secondary grading current examination | Optional AI evaluation | AI grading indicates that something is wrong. |
| 1004 | New screening examination in X months | Gradable AI grading, recall interval | No need for further grading in this examination. |

## Global Rules

* The append operation is not idempotent. A given examination may only receive one successful AI integrator update.

