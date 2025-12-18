# Retina Conclusion - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Conclusion**

## CodeSystem: Retina Conclusion 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs | *Version*:0.5.0 |
| Draft as of 2025-12-02 | *Computable Name*:RetinaConclusionCodeSystem |

 
Codes for the current or final conclusion of the grading process (1000-series). 

 This Code system is referenced in the content logical definition of the following value sets: 

* [RetinaDiagnosticReportConclusionCodeValueSet](ValueSet-retina-conclusion-code-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-conclusion-code-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
  "version" : "0.5.0",
  "name" : "RetinaConclusionCodeSystem",
  "title" : "Retina Conclusion",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-02",
  "publisher" : "DIPS AS",
  "contact" : [
    {
      "name" : "DIPS AS",
      "telecom" : [
        {
          "system" : "url",
          "value" : "http://dips.no/"
        },
        {
          "system" : "email",
          "value" : "teamsolsiden@dips.no"
        }
      ]
    }
  ],
  "description" : "Codes for the current or final conclusion of the grading process (1000-series).",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 6,
  "concept" : [
    {
      "code" : "1001",
      "display" : "KI-gradering (basert på nåværende bilder)",
      "definition" : "This examination is waiting to be graded by the AI system."
    },
    {
      "code" : "1002",
      "display" : "Primærgradering (basert på nåværende bilder)",
      "definition" : "This examinations is waiting to be graded by a primary grader."
    },
    {
      "code" : "1003",
      "display" : "Sekundærgradering (basert på nåværende bilder)",
      "definition" : "This examination is waiting to be graded by a secondary grader."
    },
    {
      "code" : "1004",
      "display" : "Ny fotokontroll (primærgradering)",
      "definition" : "Patient should be scheduled for a new routine eye examination graded by primary grader or AI."
    },
    {
      "code" : "1005",
      "display" : "Ny fotokontroll (sekundærgradering)",
      "definition" : "Patient should be scheduled for a new routine eye examination but graded by secondary grader."
    },
    {
      "code" : "1006",
      "display" : "Øyelegeundersøkelse (grunnet diabetisk retinopati)",
      "definition" : "Patient is leaving the screening program and should be referred to an ophthalmologist for further examination due to findings of diabetic retinopathy."
    }
  ]
}

```
