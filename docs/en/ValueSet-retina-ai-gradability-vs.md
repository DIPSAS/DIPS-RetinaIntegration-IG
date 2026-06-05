# Retina AI Gradability - RetinaIntegration v0.9.0

## ValueSet: Retina AI Gradability 

 
Codes indicating whether diagnostic data is suitable for automated AI grading. 

 **References** 

This value set is not used here; it may be used elsewhere (e.g. specifications and/or implementations that use this content)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-ai-gradability-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-ai-gradability-vs",
  "version" : "0.9.0",
  "name" : "RetinaAIGradabilityValueSet",
  "title" : "Retina AI Gradability",
  "status" : "draft",
  "experimental" : false,
  "date" : "2026-04-17",
  "publisher" : "DIPS AS",
  "contact" : [{
    "name" : "DIPS AS",
    "telecom" : [{
      "system" : "url",
      "value" : "http://dips.no/"
    },
    {
      "system" : "email",
      "value" : "teamsolsiden@dips.no"
    }]
  }],
  "description" : "Codes indicating whether diagnostic data is suitable for automated AI grading.",
  "compose" : {
    "include" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-ai-gradability-cs"
    }]
  }
}

```
