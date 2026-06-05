# Retina Cautions - RetinaIntegration v0.9.0

## ValueSet: Retina Cautions 

 
Special considerations or cautions for grading this examination (5000-series). 

 **References** 

* [Cautions](StructureDefinition-cautions-extension.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-caution-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-caution-vs",
  "version" : "0.9.0",
  "name" : "RetinaCautionValueSet",
  "title" : "Retina Cautions",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-07",
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
  "description" : "Special considerations or cautions for grading this examination (5000-series).",
  "compose" : {
    "include" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-caution-cs"
    }]
  }
}

```
