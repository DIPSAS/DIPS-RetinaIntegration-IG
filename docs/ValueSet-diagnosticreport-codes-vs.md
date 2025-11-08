# Rapport for Retina-screening - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Rapport for Retina-screening**

## ValueSet: Rapport for Retina-screening (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/ValueSet/diagnosticreport-codes-vs | *Version*:0.1.3 |
| Draft as of 2025-11-08 | *Computable Name*:DiagnosticReportCodes |

 
Rapporttype bildediagnsotikk fra Volven 8660 

 **References** 

* [DiagnosticReport for Retinascreening](StructureDefinition-RetinaDiagnosticReport.md)

### Logical Definition (CLD)

* Include all codes defined in [`http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660`](CodeSystem-no-kodeverk-8660.md)version 📦0.1.3

 

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
  "id" : "diagnosticreport-codes-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/diagnosticreport-codes-vs",
  "version" : "0.1.3",
  "name" : "DiagnosticReportCodes",
  "title" : "Rapport for Retina-screening",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-11-08T17:39:22+01:00",
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
  "description" : "Rapporttype bildediagnsotikk fra Volven 8660",
  "compose" : {
    "include" : [
      {
        "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660"
      }
    ]
  }
}

```
