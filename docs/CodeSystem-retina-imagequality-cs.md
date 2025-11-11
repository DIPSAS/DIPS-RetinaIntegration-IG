# Image Quality - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Image Quality**

## CodeSystem: Image Quality (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-imagequality-cs | *Version*:0.1.3 |
| Active as of 2025-11-11 | *Computable Name*:RetinaImageQualityCodesystem |

 
Image quality as interpreted by an AI solution. (2000-series) 

 This Code system is referenced in the content logical definition of the following value sets: 

* [RetinaImageQualityValueSet](ValueSet-retina-imagequality-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-imagequality-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-imagequality-cs",
  "version" : "0.1.3",
  "name" : "RetinaImageQualityCodesystem",
  "title" : "Image Quality",
  "status" : "active",
  "experimental" : true,
  "date" : "2025-11-11T17:38:50+01:00",
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
  "description" : "Image quality as interpreted by an AI solution. (2000-series)",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 4,
  "concept" : [
    {
      "code" : "2001",
      "display" : "Good",
      "definition" : "This means that the AI solution has been able to extract sufficient information from an image so it can be used in an automated assessment for DR that may return eye-level results if a sufficient amount and types of images of that eye are present."
    },
    {
      "code" : "2002",
      "display" : "Barely gradable",
      "definition" : "This means that the AI solution has been able to extract sufficient information from an image so it can be used in an automated assessment for DR that may return patient-level results indicating possibly presence of DR if a sufficient amount and types of images of the patient's eye(s) are present. In the implementation in HSØ, DR and DME values will never be returend in the API from examinations based on image quality where at least one image has the label 'barely gradable'. The API will then return no value together with a dataAbsentReason."
    },
    {
      "code" : "2003",
      "display" : "Not gradable",
      "definition" : "This means that the AI solution has not been able to extract sufficient information from an image so it can be used in an automated assessment for DR. In the implementation in HSØ, DR and DME values will never be returend in the API from examinations based on image quality where at least one image has the label 'not gradable'. The API will then return no value together with a dataAbsentReason."
    },
    {
      "code" : "2004",
      "display" : "Missing",
      "definition" : "This may come from the absence of expected images or other reasons. This value will for instance be returned on an expected image with optic disc centration if the AI solution does not return any image documentation of this category. Use: This can be used by a receiving system for documentation or use in other business logics."
    }
  ]
}

```
