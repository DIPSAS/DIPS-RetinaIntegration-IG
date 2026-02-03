# RetinaDiabeticRetinopathyFinding-Example-left - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaDiabeticRetinopathyFinding-Example-left**

## Example Observation: RetinaDiabeticRetinopathyFinding-Example-left

Profile: [Retina Diabetic Retinopathy Finding](StructureDefinition-retina-diabetic-retinopathy-finding.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-ns.md)/d4e5f6a7-b8c9-0123-def4-567890abcdef

**status**: Final

**code**: Diabetic retinopathy

**effective**: 2025-11-30 10:21:00+0000

**value**: 3

**bodySite**: Venstre retina



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaDiabeticRetinopathyFinding-Example-left",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-retinopathy-finding"
    ]
  },
  "identifier" : [
    {
      "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
      "value" : "d4e5f6a7-b8c9-0123-def4-567890abcdef"
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
    "value" : 3
  },
  "bodySite" : {
    "coding" : [
      {
        "system" : "http://snomed.info/sct",
        "code" : "58443009",
        "display" : "Retina of left eye"
      }
    ],
    "text" : "Venstre retina"
  }
}

```
