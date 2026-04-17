# Retina Body Site - RetinaIntegration v0.8.0

## ValueSet: Retina Body Site 

 
Body site codes for retinal observations (right or left retina). 

 **References** 

* [Retina Diabetic Macular Edema Finding](StructureDefinition-retina-diabetic-macular-edema-finding.md)
* [Retina Diabetic Retinopathy Finding](StructureDefinition-retina-diabetic-retinopathy-finding.md)
* [Retina Image Quality Assessment](StructureDefinition-retina-image-quality-asessment.md)
* [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-body-site-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-body-site-vs",
  "version" : "0.8.0",
  "name" : "RetinaBodySiteValueSet",
  "title" : "Retina Body Site",
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
  "description" : "Body site codes for retinal observations (right or left retina).",
  "compose" : {
    "include" : [{
      "system" : "http://snomed.info/sct",
      "concept" : [{
        "code" : "5597008",
        "display" : "Retina of right eye"
      },
      {
        "code" : "58443009",
        "display" : "Retina of left eye"
      }]
    }]
  }
}

```
