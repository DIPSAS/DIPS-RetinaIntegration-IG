# Retina Caution Codes - RetinaIntegration v0.9.0

## CodeSystem: Retina Caution Codes 

 
Cautions to consider when grading examinations (5000-series). 

This Code system is referenced in the definition of the following value sets:

* [RetinaCautionValueSet](ValueSet-retina-caution-vs.md)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-caution-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-caution-cs",
  "version" : "0.9.0",
  "name" : "RetinaCautionCodeSystem",
  "title" : "Retina Caution Codes",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-02",
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
  "description" : "Cautions to consider when grading examinations (5000-series).",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 1,
  "concept" : [{
    "code" : "5001",
    "display" : "Ønsker ikke KI-svar",
    "definition" : "Patient has told photographer that they do not want an AI-based grading result."
  }]
}

```
