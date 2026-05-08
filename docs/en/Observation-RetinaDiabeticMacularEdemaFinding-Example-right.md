# RetinaDiabeticMacularEdemaFinding-Example-right - RetinaIntegration v0.8.1

## Example Observation: RetinaDiabeticMacularEdemaFinding-Example-right

Profile: [Retina Diabetic Macular Edema Finding](StructureDefinition-retina-diabetic-macular-edema-finding.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-ns.md)/c3d4e5f6-a7b8-9012-cdef-1234567890ab

**status**: Final

**code**: Diabetic macular edema

**effective**: 2025-11-30 10:21:00+0000

**value**: true

**bodySite**: Høyre retina



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaDiabeticMacularEdemaFinding-Example-right",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-macular-edema-finding"]
  },
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
    "value" : "c3d4e5f6-a7b8-9012-cdef-1234567890ab"
  }],
  "status" : "final",
  "code" : {
    "coding" : [{
      "system" : "http://snomed.info/sct",
      "code" : "312912001",
      "display" : "Diabetic macular edema"
    }]
  },
  "effectiveDateTime" : "2025-11-30T10:21:00Z",
  "valueBoolean" : true,
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
