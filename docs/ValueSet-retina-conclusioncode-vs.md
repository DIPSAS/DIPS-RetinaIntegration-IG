# Grading Conclusion - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Grading Conclusion**

## ValueSet: Grading Conclusion (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusioncode-vs | *Version*:0.1.3 |
| Draft as of 2025-11-15 | *Computable Name*:RetinaConclusionCodeValueset |

 
Codes describing where the external client has landed in its assessment of the examination. (1000-series) 

 **References** 

* [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)

### Logical Definition (CLD)

* Include all codes defined in [`http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs`](CodeSystem-retina-conclusioncode-cs.md)version 📦0.1.3

 

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
  "id" : "retina-conclusioncode-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusioncode-vs",
  "version" : "0.1.3",
  "name" : "RetinaConclusionCodeValueset",
  "title" : "Grading Conclusion",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-11-15T17:14:08+01:00",
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
  "description" : "Codes describing where the external client has landed in its assessment of the examination. (1000-series)",
  "compose" : {
    "include" : [
      {
        "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs"
      }
    ]
  }
}

```
