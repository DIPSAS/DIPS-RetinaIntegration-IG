# RetinaHbA1cObservation-Example - RetinaIntegration v0.7.0

## Example Observation: RetinaHbA1cObservation-Example

Language: en

Profile: [Retina HbA1c Observation](StructureDefinition-retina-hba1c-observation.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-ns.md)/a7f3e821-9c4d-4f2a-b5e6-8d3c7a1f9b42

**status**: Final

**code**: HbA1c

**effective**: 2025-11-29 10:30:00+0000

**value**: 63.2



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaHbA1cObservation-Example",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-hba1c-observation"]
  },
  "language" : "en",
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
    "value" : "a7f3e821-9c4d-4f2a-b5e6-8d3c7a1f9b42"
  }],
  "status" : "final",
  "code" : {
    "coding" : [{
      "system" : "http://snomed.info/sct",
      "code" : "167491000202108",
      "display" : "HbA1c"
    }]
  },
  "effectiveDateTime" : "2025-11-29T10:30:00Z",
  "valueQuantity" : {
    "value" : 63.2
  }
}

```
