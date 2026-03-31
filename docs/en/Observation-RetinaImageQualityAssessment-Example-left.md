# RetinaImageQualityAssessment-Example-left - RetinaIntegration v0.7.0

## Example Observation: RetinaImageQualityAssessment-Example-left

Language: en

Profile: [Retina Image Quality Assessment](StructureDefinition-retina-image-quality-asessment.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-ns.md)/a0b9c8d7-e6f5-4321-0987-6543210fedcb

**status**: Final

**code**: Computer assisted image analysis for image quality

**effective**: 2025-11-30 10:21:00+0000

**value**: Barely gradable

**bodySite**: Venstre retina



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaImageQualityAssessment-Example-left",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-quality-asessment"]
  },
  "language" : "en",
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
    "value" : "a0b9c8d7-e6f5-4321-0987-6543210fedcb"
  }],
  "status" : "final",
  "code" : {
    "coding" : [{
      "system" : "http://snomed.info/sct",
      "code" : "133887000",
      "display" : "Computer assisted image analysis for image quality"
    }]
  },
  "effectiveDateTime" : "2025-11-30T10:21:00Z",
  "valueCodeableConcept" : {
    "coding" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-quality-cs",
      "code" : "2002",
      "display" : "Barely gradable"
    }]
  },
  "bodySite" : {
    "coding" : [{
      "system" : "http://snomed.info/sct",
      "code" : "58443009",
      "display" : "Retina of left eye"
    }],
    "text" : "Venstre retina"
  }
}

```
