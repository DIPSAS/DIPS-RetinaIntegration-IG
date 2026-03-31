# RetinaImageQualityAssessment-Example-right - RetinaIntegration v0.7.0

## Example Observation: RetinaImageQualityAssessment-Example-right

Language: en

Profile: [Retina Image Quality Assessment](StructureDefinition-retina-image-quality-asessment.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-ns.md)/f1e2d3c4-b5a6-7890-abcd-ef1234567890

**status**: Final

**code**: Computer assisted image analysis for image quality

**effective**: 2025-11-30 10:21:00+0000

**value**: Good

**bodySite**: Høyre retina



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaImageQualityAssessment-Example-right",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-quality-asessment"]
  },
  "language" : "en",
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
    "value" : "f1e2d3c4-b5a6-7890-abcd-ef1234567890"
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
      "code" : "2001",
      "display" : "Good"
    }]
  },
  "bodySite" : {
    "coding" : [{
      "system" : "http://snomed.info/sct",
      "code" : "5597008",
      "display" : "Retina of right eye"
    }],
    "text" : "Høyre retina"
  }
}

```
