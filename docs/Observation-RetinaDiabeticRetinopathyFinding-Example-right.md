# RetinaDiabeticRetinopathyFinding-Example-right - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaDiabeticRetinopathyFinding-Example-right**

## Example Observation: RetinaDiabeticRetinopathyFinding-Example-right

Profile: [Retina Diabetic Retinopathy Finding](StructureDefinition-retina-diabetic-retinopathy-finding.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-ns.md)/e5f6a7b8-c901-2345-6789-0abcdef12345

**status**: Final

**code**: Diabetic retinopathy

**effective**: 2025-11-30 10:21:00+0000

**value**: 4

**bodySite**: Høyre retina



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaDiabeticRetinopathyFinding-Example-right",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-retinopathy-finding"
    ]
  },
  "identifier" : [
    {
      "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
      "value" : "e5f6a7b8-c901-2345-6789-0abcdef12345"
    }
  ],
  "status" : "final",
  "code" : {
    "coding" : [
      {
        "system" : "http://snomed.info/sct",
        "code" : "4855003",
        "display" : "Diabetic retinopathy"
      }
    ]
  },
  "effectiveDateTime" : "2025-11-30T10:21:00Z",
  "valueQuantity" : {
    "value" : 4
  },
  "bodySite" : {
    "coding" : [
      {
        "system" : "http://snomed.info/sct",
        "code" : "5597008",
        "display" : "Retina of right eye"
      }
    ],
    "text" : "Høyre retina"
  }
}

```
