# Retina AI Gradability Codes - RetinaIntegration v0.8.0

## CodeSystem: Retina AI Gradability Codes 

 
A set of codes to indicate whether diagnostic data is suitable for automated AI grading. 

This Code system is referenced in the definition of the following value sets:

* [RetinaAIGradabilityValueSet](ValueSet-retina-ai-gradability-vs.md)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-ai-gradability-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-ai-gradability-cs",
  "version" : "0.8.0",
  "name" : "RetinaAIGradabilityCodeSystem",
  "title" : "Retina AI Gradability Codes",
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
  "description" : "A set of codes to indicate whether diagnostic data is suitable for automated AI grading.",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 2,
  "concept" : [{
    "code" : "good-gradability",
    "display" : "Good",
    "definition" : "The data quality is sufficient for it to be processed by an AI grading algorithm."
  },
  {
    "code" : "not-gradable",
    "display" : "Not gradable",
    "definition" : "The data quality is insufficient for it to be processed by an AI grading algorithm."
  }]
}

```
