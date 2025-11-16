# Grading Conclusion - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Grading Conclusion**

## CodeSystem: Grading Conclusion (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs | *Version*:0.1.3 |
| Draft as of 2025-11-16 | *Computable Name*:RetinaConclusionCodesystem |

 
Codes describing where the external client has landed in its assessment of the examination. (1000-series) 

 This Code system is referenced in the content logical definition of the following value sets: 

* [RetinaConclusionCodeValueset](ValueSet-retina-conclusioncode-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-conclusioncode-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs",
  "version" : "0.1.3",
  "name" : "RetinaConclusionCodesystem",
  "title" : "Grading Conclusion",
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
  "description" : "Codes describing where the external client has landed in its assessment of the examination. (1000-series)",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 3,
  "concept" : [
    {
      "code" : "1001",
      "display" : "Grading completed"
    },
    {
      "code" : "1002",
      "display" : "To primary grading"
    },
    {
      "code" : "1003",
      "display" : "To secondary grading"
    }
  ]
}

```
