# Videre forløp etter fotografering - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Videre forløp etter fotografering**

## CodeSystem: Videre forløp etter fotografering (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/videre-forlop-cs | *Version*:0.1.3 |
| Draft as of 2025-11-08 | *Computable Name*:VidereForlopCodeSystem |

 
Koder basert på hva fotografen velger i skjema. 

 This Code system is referenced in the content logical definition of the following value sets: 

* [VidereForlopValueSet](ValueSet-videre-forlop-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "videre-forlop-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/videre-forlop-cs",
  "version" : "0.1.3",
  "name" : "VidereForlopCodeSystem",
  "title" : "Videre forløp etter fotografering",
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
  "description" : "Koder basert på hva fotografen velger i skjema.",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 3,
  "concept" : [
    {
      "code" : "4001",
      "display" : "KI-gradering"
    },
    {
      "code" : "4002",
      "display" : "Primærgradering manuell"
    },
    {
      "code" : "4003",
      "display" : "Sekundærgradering manuell"
    }
  ]
}

```
