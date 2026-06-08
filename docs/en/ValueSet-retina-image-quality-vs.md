# Retina Image Quality - RetinaIntegration v0.9.1

## ValueSet: Retina Image Quality 

 
Image quality as assessed by AI (2000-series). 

 **References** 

* Included into [RetinaImageParameterValueSet](ValueSet-retina-image-parameter-vs.md)
* [Retina Image Quality Assessment](StructureDefinition-retina-image-quality-asessment.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-image-quality-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-quality-vs",
  "version" : "0.9.1",
  "name" : "RetinaImageQualityValueSet",
  "title" : "Retina Image Quality",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-05",
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
  "description" : "Image quality as assessed by AI (2000-series).",
  "purpose" : "For documentation of image quality as assessed by an AI solution.",
  "compose" : {
    "include" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-quality-cs"
    }]
  }
}

```
