# Retina CapabilityStatement - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina CapabilityStatement**

## CapabilityStatement: Retina CapabilityStatement 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CapabilityStatement/RetinaCapabilityStatement | *Version*:0.6.0 |
| Active as of 2025-09-30 | *Computable Name*: |

 
CapabilityStatement for DIPS Retina Integration FHIR API. 

 [Raw OpenAPI-Swagger Definition file](RetinaCapabilityStatement.openapi.json) | [Download](RetinaCapabilityStatement.openapi.json) 



## Resource Content

```json
{
  "resourceType" : "CapabilityStatement",
  "id" : "RetinaCapabilityStatement",
  "url" : "http://dips.no/fhir/RetinaIntegration/CapabilityStatement/RetinaCapabilityStatement",
  "version" : "0.6.0",
  "title" : "Retina CapabilityStatement",
  "status" : "active",
  "date" : "2025-09-30T12:00:00Z",
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
  "description" : "CapabilityStatement for DIPS Retina Integration FHIR API.",
  "kind" : "instance",
  "implementation" : {
    "description" : "DIPS retinaintegration-service"
  },
  "fhirVersion" : "4.0.1",
  "format" : ["xml", "json"],
  "rest" : [
    {
      "mode" : "server",
      "resource" : [
        {
          "type" : "DiagnosticReport",
          "profile" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report",
          "interaction" : [
            {
              "code" : "read"
            }
          ],
          "searchInclude" : ["DiagnosticReport:patient", "DiagnosticReport:result"]
        }
      ],
      "operation" : [
        {
          "name" : "AppendRetinaAIResult",
          "definition" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result",
          "documentation" : "Append results from AI analysis of retina images to a existing DiagnosticReport"
        }
      ]
    }
  ]
}

```
