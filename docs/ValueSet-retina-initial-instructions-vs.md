# Retina Initial Instructions - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Initial Instructions**

## ValueSet: Retina Initial Instructions (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/ValueSet/retina-initial-instructions-vs | *Version*:0.2.0 |
| Draft as of 2025-11-30 | *Computable Name*:InitialInstructionsValueSet |

 
Initial routing decisions and cautions for grading this examination (1000-series and 5000-series). 

 
The diagnostic report will include the inital routing decision the photographer made when capturing the images, as well as any cautions that should be considered by the graders when performing the grading of the examination. 

 **References** 

* [Initial Instructions](StructureDefinition-initial-instructions-extension.md)

### Logical Definition (CLD)

 

### Expansion

This value set contains 4 concepts

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
  "id" : "retina-initial-instructions-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-initial-instructions-vs",
  "version" : "0.2.0",
  "name" : "InitialInstructionsValueSet",
  "title" : "Retina Initial Instructions",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-11-30T22:57:21+01:00",
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
  "description" : "Initial routing decisions and cautions for grading this examination (1000-series and 5000-series).",
  "purpose" : "The diagnostic report will include the inital routing decision the photographer made when capturing the images, \r\nas well as any cautions that should be considered by the graders when performing the grading of the examination.",
  "compose" : {
    "include" : [
      {
        "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs",
        "concept" : [
          {
            "code" : "1001",
            "display" : "KI-gradering (basert på nåværende bilder)"
          },
          {
            "code" : "1002",
            "display" : "Primærgradering (basert på nåværende bilder)"
          },
          {
            "code" : "1003",
            "display" : "Sekundærgradering (basert på nåværende bilder)"
          }
        ]
      },
      {
        "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-caution-cs"
      }
    ]
  }
}

```
