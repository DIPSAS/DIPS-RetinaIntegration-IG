# Retina AI Integration Conclusion - RetinaIntegration v0.9.1

## ValueSet: Retina AI Integration Conclusion 

 
Goal states applicable for AI integration conclusions. 

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
  "id" : "retina-append-ai-conclusion-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-append-ai-conclusion-vs",
  "version" : "0.9.1",
  "name" : "RetinaAppendAIConlusionValueSet",
  "title" : "Retina AI Integration Conclusion",
  "status" : "draft",
  "experimental" : false,
  "date" : "2026-06-04",
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
  "description" : "Goal states applicable for AI integration conclusions.",
  "compose" : {
    "include" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
      "concept" : [{
        "code" : "1002",
        "display" : "Primærgradering (basert på nåværende bilder)"
      },
      {
        "code" : "1003",
        "display" : "Sekundærgradering (basert på nåværende bilder)"
      },
      {
        "code" : "1004",
        "display" : "Ny fotokontroll (primærgradering)"
      }]
    }]
  }
}

```
