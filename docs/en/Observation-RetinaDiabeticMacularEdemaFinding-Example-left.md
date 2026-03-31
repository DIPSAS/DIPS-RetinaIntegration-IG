# RetinaDiabeticMacularEdemaFinding-Example-left - RetinaIntegration v0.7.0

## Example Observation: RetinaDiabeticMacularEdemaFinding-Example-left

Language: en

Profile: [Retina Diabetic Macular Edema Finding](StructureDefinition-retina-diabetic-macular-edema-finding.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-ns.md)/b1c2d3e4-f5a6-7890-abcd-ef1234567890

**status**: Final

**code**: Diabetic macular edema

**effective**: 2025-11-30 10:21:00+0000

**value**: false

**bodySite**: Venstre retina



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaDiabeticMacularEdemaFinding-Example-left",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-macular-edema-finding"]
  },
  "language" : "en",
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
    "value" : "b1c2d3e4-f5a6-7890-abcd-ef1234567890"
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
  "valueBoolean" : false,
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
