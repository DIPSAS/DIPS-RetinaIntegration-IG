# Retina Image View - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Image View**

## ValueSet: Retina Image View 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-view-vs | *Version*:0.6.0 |
| Draft as of 2025-12-05 | *Computable Name*:RetinaImageViewValueSet |

 
Codes describing the centering used when capturing retinal images, such as macula-centered or optic disc-centered (6000-series). 

 
We have discussed including the actual DICOM codes from the camera, or another standard code system, but have not yet identified suitable codes for this purpose. Therefore, we have created our own code system and value set for the centering of retinal images. 

 **References** 

* Included into [RetinaImageParameterValueSet](ValueSet-retina-image-parameter-vs.md)
* [Retinal Image View](StructureDefinition-retinal-image-view.md)

### Logical Definition (CLD)

 

### Expansion

-------

 Explanation of the columns that may appear on this page: 

| | |
| :--- | :--- |
| Level | A few code lists that FHIR defines are hierarchical - each code is assigned a level. In this scheme, some codes are under other codes, and imply that the code they are under also applies |
| System | The source of the definition of the code (when the value set draws in codes defined elsewhere) |
| Code | The code (used as the code in the resource instance) |
| Display | The display (used in the*display*element of a[Coding](http://hl7.org/fhir/R4/datatypes.html#Coding)). If there is no display, implementers should not simply display the code, but map the concept into their application |
| Definition | An explanation of the meaning of the concept |
| Comments | Additional notes about how to use the code |



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-image-view-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-view-vs",
  "version" : "0.6.0",
  "name" : "RetinaImageViewValueSet",
  "title" : "Retina Image View",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-05",
  "publisher" : "DIPS AS",
  "contact" : [
    {
      "name" : "DIPS AS",
      "telecom" : [
        {
          "system" : "url",
          "value" : "http://dips.no/"
        },
        {
          "system" : "email",
          "value" : "teamsolsiden@dips.no"
        }
      ]
    }
  ],
  "description" : "Codes describing the centering used when capturing retinal images, such as macula-centered or optic disc-centered (6000-series).",
  "purpose" : "We have discussed including the actual DICOM codes from the camera, or another standard code system, but have not yet identified suitable codes for this purpose. Therefore, we have created our own code system and value set for the centering of retinal images.",
  "compose" : {
    "include" : [
      {
        "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs"
      }
    ]
  }
}

```
