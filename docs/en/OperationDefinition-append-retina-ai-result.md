# Retina Append AI Result Operation - RetinaIntegration v0.8.1

## OperationDefinition: Retina Append AI Result Operation 

 
OperationDefinition for appending retina AI results to an existing DiagnosticReport. 

### Overview

The `$append-retina-ai-result` operation is used to add AI analysis results to an existing DiagnosticReport. This operation is invoked by the regional integration platform after the AI system has analyzed retinal images.

### Example

See [RetinaAppendAIResultOperation-Example](Parameters-RetinaAppendAIResultOperation-Example.json.md) for an example of the parameters.

### Usage

Add AI result to an examination using the following operation:

```
[baseUrl]/DiagnosticReport/[id]/$append-retina-ai-result

```

`[id]` is the identifier UUID (Universally Unique Identifier), sometimes referred to as a GUID, of the DiagnosticReport, a.k.a examination, to update.

### Business rules

`422 Unprocessable Entity` with a OperationOutcome of issue of type BusinessRule is returned if the request fails to comply with one of the following business rules.

Many of the parameters are optional, but there are rules governing the combination of some of the parameters:

1. If current status of the examination is not[1001](CodeSystem-retina-conclusion-code-cs.md#retina-conclusion-code-cs-1001)(Waiting to be graded by AI) the update is not allowed.
1. If no eye evaluations are provided`conclusion`can only be[1002](CodeSystem-retina-conclusion-code-cs.md#retina-conclusion-code-cs-1002)(Primary grading based on current images) or[1003](CodeSystem-retina-conclusion-code-cs.md#retina-conclusion-code-cs-1002)(Secondary grading based on current images).
1. If`conclusion`is[1004](CodeSystem-retina-conclusion-code-cs.md#retina-conclusion-code-cs-1004)(New examination primary grading) or[1005](CodeSystem-retina-conclusion-code-cs.md#retina-conclusion-code-cs-1005)(New examination secondary grading) then parameter`monthsUntilNextExamination`must be specified.

### Conflict

`409 Conflict` is returned in the following cases:

1. The examination already has an AI grading
1. The`sectraStudyId`is linked to another examination

### HTTP response codes

| | |
| :--- | :--- |
| 204 No Content | The operation completed successfully and the DiagnosticReport was updated. |
| 400 Bad Request | The request was malformed or contained invalid parameters. |
| 401 Unauthorized | The server was not able to authenticate the user so authorization could not be done. |
| 403 Forbidden | The user is not authorized to use the API. |
| 404 Not Found | No DiagnosticReport with the given`[id]`was found. |
| 409 Conflict | DiagnosticReport`[id]`already has a grading, or`sectraStudyId`already used. |
| 422 Unprocessable Entity | The request was well-formed but violated business rules (e.g. missing required parameter combinations). |
| 500 Internal Server Error | An unexpected server-side error occurred. |



## Resource Content

```json
{
  "resourceType" : "OperationDefinition",
  "id" : "append-retina-ai-result",
  "url" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result",
  "version" : "0.8.1",
  "name" : "AppendRetinaAIResult",
  "title" : "Retina Append AI Result Operation",
  "status" : "draft",
  "kind" : "operation",
  "date" : "2026-05-08T13:22:39+02:00",
  "publisher" : "DIPS AS",
  "contact" : [{
    "name" : "DIPS AS",
    "telecom" : [{
      "system" : "url",
      "value" : "http://dips.no/"
    },
    {
      "system" : "email",
      "value" : "teamsolsiden@dips.no"
    }]
  }],
  "description" : "OperationDefinition for appending retina AI results to an existing DiagnosticReport.",
  "purpose" : "Append results from AI analysis of retina images to a existing DiagnosticReport",
  "code" : "append-retina-ai-result",
  "resource" : ["DiagnosticReport"],
  "system" : false,
  "type" : false,
  "instance" : true,
  "parameter" : [{
    "name" : "sectraStudyId",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Sectra study ID for the retinal images that were analyzed.",
    "type" : "string"
  },
  {
    "name" : "conclusion",
    "use" : "in",
    "min" : 1,
    "max" : "1",
    "documentation" : "Conclusion indicating the next step. MUST be a single code from the 1000 series. If the validation parameter is set to true, the next step will always be manual grading.",
    "type" : "CodeableConcept",
    "binding" : {
      "strength" : "required",
      "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusion-code-vs"
    }
  },
  {
    "name" : "monthsUntilNextExamination",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "The recall interval in months until the patient's next examination. Only included if the conclusion is a new examination. Value must be a positive integer greater than 1",
    "type" : "integer"
  },
  {
    "name" : "leftGradability",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Gradability of the left eye for AI analysis. Must be a single code from the Retina AI Gradability ValueSet.",
    "type" : "code",
    "binding" : {
      "strength" : "required",
      "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-ai-gradability-vs"
    }
  },
  {
    "name" : "rightGradability",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Gradability of the right eye for AI analysis. Must be a single code from the Retina AI Gradability ValueSet.",
    "type" : "code",
    "binding" : {
      "strength" : "required",
      "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-ai-gradability-vs"
    }
  },
  {
    "name" : "leftDiabeticRetinopathy",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Left eye diabetic retinopathy evaluation, a decimal between 0.0 and 5.0",
    "type" : "decimal"
  },
  {
    "name" : "leftDiabeticMacularEdema",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Left eye diabetic macular edema evaluation. True if diabetic macular edema is present.",
    "type" : "boolean"
  },
  {
    "name" : "rightDiabeticRetinopathy",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Right eye diabetic retinopathy evaluation, a decimal between 0.0 and 5.0",
    "type" : "decimal"
  },
  {
    "name" : "rightDiabeticMacularEdema",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Right eye diabetic macular edema evaluation. True if diabetic macular edema is present.",
    "type" : "boolean"
  },
  {
    "name" : "rightEyeImage",
    "use" : "in",
    "min" : 0,
    "max" : "*",
    "documentation" : "Right eye images used in the AI analysis. MUST conform to RetinaImageParameter profile.",
    "type" : "Observation",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-parameter"]
  },
  {
    "name" : "leftEyeImage",
    "use" : "in",
    "min" : 0,
    "max" : "*",
    "documentation" : "Left eye images used in the AI analysis. MUST conform to RetinaImageParameter profile.",
    "type" : "Observation",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-parameter"]
  },
  {
    "name" : "aiDevice",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "AI Device that performed the analysis. Includes AI product name, algorithm version and protocol version.",
    "type" : "Device",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device"]
  },
  {
    "name" : "performedDateTime",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Date and time when the retinal AI analysis was performed.",
    "type" : "dateTime"
  },
  {
    "name" : "cameraDevice",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Camera device used to capture the retinal images.",
    "type" : "Device",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-camera-device"]
  },
  {
    "name" : "fullReport",
    "use" : "in",
    "min" : 1,
    "max" : "1",
    "documentation" : "Technical details for further reference about the AI grading.",
    "type" : "Attachment"
  },
  {
    "name" : "validation",
    "use" : "in",
    "min" : 1,
    "max" : "1",
    "documentation" : "Set true if the AI result is for validation purposes only and will not be used in clinical decision making.",
    "type" : "boolean"
  }]
}

```
