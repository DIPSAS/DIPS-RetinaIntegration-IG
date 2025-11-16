# Grading Cautions - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Grading Cautions**

## CodeSystem: Grading Cautions (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/grading-caution-cs | *Version*:0.1.3 |
| Draft as of 2025-11-16 | *Computable Name*:GradingCautionCodeSystem |

 
Cautions to consider when grading examinations. (5000-series) 

 This Code system is referenced in the content logical definition of the following value sets: 

* [VidereForlopValueSet](ValueSet-videre-forlop-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "grading-caution-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/grading-caution-cs",
  "version" : "0.1.3",
  "name" : "GradingCautionCodeSystem",
  "title" : "Grading Cautions",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-11-16T16:39:43+01:00",
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
  "description" : "Cautions to consider when grading examinations. (5000-series)",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 1,
  "concept" : [
    {
      "code" : "5001",
      "display" : "Ønsker ikke KI-svar",
      "definition" : "Fotograf har huket av 'Ønsker ikke KI-svar'."
    }
  ]
}

```
