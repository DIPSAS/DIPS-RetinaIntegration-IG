# Retina Image View - RetinaIntegration v0.9.1

## ValueSet: Retina Image View 

 
Codes describing the centering used when capturing retinal images, such as macula-centered or optic disc-centered (6000-series). 

 **References** 

* Included into [RetinaImageParameterValueSet](ValueSet-retina-image-parameter-vs.md)
* [Retinal Image View](StructureDefinition-retinal-image-view.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-image-view-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-view-vs",
  "version" : "0.9.1",
  "name" : "RetinaImageViewValueSet",
  "title" : "Retina Image View",
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
  "description" : "Codes describing the centering used when capturing retinal images, such as macula-centered or optic disc-centered (6000-series).",
  "purpose" : "We have discussed including the actual DICOM codes from the camera, or another standard code system, but have not yet identified suitable codes for this purpose. Therefore, we have created our own code system and value set for the centering of retinal images.",
  "compose" : {
    "include" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs"
    }]
  }
}

```
