# Retina Conclusion - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Conclusion**

## ValueSet: Retina Conclusion 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusion-code-vs | *Version*:0.5.0 |
| Draft as of 2025-12-05 | *Computable Name*:RetinaDiagnosticReportConclusionCodeValueSet |

 
Codes describing the current or final conclusion of the examination (1000-series). 

 **References** 

* [Previous Examination Conclusion](StructureDefinition-previous-examination-conclusion-extension.md)
* [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

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
  "id" : "retina-conclusion-code-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusion-code-vs",
  "version" : "0.5.0",
  "name" : "RetinaDiagnosticReportConclusionCodeValueSet",
  "title" : "Retina Conclusion",
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
  "description" : "Codes describing the current or final conclusion of the examination (1000-series).",
  "compose" : {
    "include" : [
      {
        "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs"
      }
    ]
  }
}

```
