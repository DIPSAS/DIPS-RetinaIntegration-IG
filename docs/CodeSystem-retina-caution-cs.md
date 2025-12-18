# Retina Cautions - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Cautions**

## CodeSystem: Retina Cautions 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-caution-cs | *Version*:0.5.0 |
| Draft as of 2025-12-02 | *Computable Name*:RetinaCautionCodeSystem |

 
Cautions to consider when grading examinations (5000-series). 

 This Code system is referenced in the content logical definition of the following value sets: 

* [RetinaCautionValueSet](ValueSet-retina-caution-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-caution-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-caution-cs",
  "version" : "0.5.0",
  "name" : "RetinaCautionCodeSystem",
  "title" : "Retina Cautions",
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
  "description" : "Cautions to consider when grading examinations (5000-series).",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 1,
  "concept" : [
    {
      "code" : "5001",
      "display" : "Ønsker ikke KI-svar",
      "definition" : "Patient has told photographer that they do not want an AI-based grading result."
    }
  ]
}

```
