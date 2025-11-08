# NO Kodeverk 8660 - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **NO Kodeverk 8660**

## CodeSystem: NO Kodeverk 8660 

| | |
| :--- | :--- |
| *Official URL*:http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660 | *Version*:0.1.3 |
| Draft as of 2025-11-08 | *Computable Name*:NOKodeverk8660 |

 
Tjenestetyper. Benyttes primært i forbindelse med rekvisisjoner og svarrapporter innenfor lab og røntgen. 

 This Code system is referenced in the content logical definition of the following value sets: 

* [DiagnosticReportCodes](ValueSet-diagnosticreport-codes-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "no-kodeverk-8660",
  "url" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660",
  "version" : "0.1.3",
  "name" : "NOKodeverk8660",
  "title" : "NO Kodeverk 8660",
  "status" : "draft",
  "experimental" : false,
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
  "description" : "Tjenestetyper. Benyttes primært i forbindelse med rekvisisjoner og svarrapporter innenfor lab og røntgen.",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 7,
  "concept" : [
    {
      "code" : "B",
      "display" : "Bildediagnostikk"
    },
    {
      "code" : "B06",
      "display" : "Nukleærmedisin"
    },
    {
      "code" : "L",
      "display" : "Laboratoriefag"
    },
    {
      "code" : "L02",
      "display" : "Transfusjonsmedisin og immunologi"
    },
    {
      "code" : "L03",
      "display" : "Medisinsk biokjemi"
    },
    {
      "code" : "L04",
      "display" : "Medisinsk mikrobiologi"
    },
    {
      "code" : "L06",
      "display" : "Patologi"
    }
  ]
}

```
