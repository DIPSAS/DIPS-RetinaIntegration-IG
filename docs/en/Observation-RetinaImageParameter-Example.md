# RetinaImageParameter-Example - RetinaIntegration v0.7.0

## Example Observation: RetinaImageParameter-Example

Language: en

Profile: [Retina Image Parameter](StructureDefinition-retina-image-parameter.md)

**status**: Final

**code**: Macula centered



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaImageParameter-Example",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-parameter"]
  },
  "language" : "en",
  "status" : "final",
  "code" : {
    "coding" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs",
      "code" : "6001",
      "display" : "Macula centered"
    },
    {
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-quality-cs",
      "code" : "2001",
      "display" : "Good"
    }]
  }
}

```
