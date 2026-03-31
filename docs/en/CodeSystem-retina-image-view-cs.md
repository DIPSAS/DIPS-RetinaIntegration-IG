# Retina Image View - RetinaIntegration v0.7.0

## CodeSystem: Retina Image View 

 
Codes describing the centering used when capturing retinal images (6000-series). 

This Code system is referenced in the definition of the following value sets:

* [RetinaImageViewValueSet](ValueSet-retina-image-view-vs.md)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-image-view-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs",
  "version" : "0.7.0",
  "name" : "RetinaImageViewCodeSystem",
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
  "description" : "Codes describing the centering used when capturing retinal images (6000-series).",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 2,
  "concept" : [{
    "code" : "6001",
    "display" : "Macula centered",
    "definition" : "Retinal image centered on the macula."
  },
  {
    "code" : "6002",
    "display" : "Optic disc centered",
    "definition" : "Retinal image centered on the optic disc."
  }]
}

```
