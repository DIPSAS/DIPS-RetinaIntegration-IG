# Retina Image Parameter ValueSet - RetinaIntegration v0.7.0

## ValueSet: Retina Image Parameter ValueSet 

 
Includes codes for both image quality and image view. 

 **References** 

* [Retina Image Parameter](StructureDefinition-retina-image-parameter.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-image-parameter-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-parameter-vs",
  "version" : "0.7.0",
  "name" : "RetinaImageParameterValueSet",
  "title" : "Retina Image Parameter ValueSet",
  "status" : "draft",
  "experimental" : false,
  "date" : "2026-01-20",
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
  "description" : "Includes codes for both image quality and image view.",
  "compose" : {
    "include" : [{
      "valueSet" : ["http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-quality-vs"]
    },
    {
      "valueSet" : ["http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-view-vs"]
    }]
  }
}

```
