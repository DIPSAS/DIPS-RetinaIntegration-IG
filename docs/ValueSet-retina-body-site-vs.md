# Retina Body Site - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Body Site**

## ValueSet: Retina Body Site 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/ValueSet/retina-body-site-vs | *Version*:0.6.0 |
| Draft as of 2025-12-02 | *Computable Name*:RetinaBodySiteValueSet |

 
Body site codes for retinal observations (right or left retina). 

 **References** 

* [Retina Diabetic Macular Edema Finding](StructureDefinition-retina-diabetic-macular-edema-finding.md)
* [Retina Diabetic Retinopathy Finding](StructureDefinition-retina-diabetic-retinopathy-finding.md)
* [Retina Image Quality Assessment](StructureDefinition-retina-image-quality-asessment.md)
* [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

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
  "id" : "retina-body-site-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-body-site-vs",
  "version" : "0.6.0",
  "name" : "RetinaBodySiteValueSet",
  "title" : "Retina Body Site",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-02",
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
  "description" : "Body site codes for retinal observations (right or left retina).",
  "compose" : {
    "include" : [
      {
        "system" : "http://snomed.info/sct",
        "concept" : [
          {
            "code" : "5597008",
            "display" : "Retina of right eye"
          },
          {
            "code" : "58443009",
            "display" : "Retina of left eye"
          }
        ]
      }
    ]
  }
}

```
