# AI Product Name - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **AI Product Name**

## Extension: AI Product Name (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-productname-extension | *Version*:0.1.3 |
| Draft as of 2025-11-16 | *Computable Name*:KIProductName |

Name of the AI product used for analysis.

For documentation of AI product used in automated analysis of retinal images for the purpose of grading images for diabetic rethinopathy.

Origin: AI solution.

Content: String with name of AI product.

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)
* Examples for this Extension: [Bundle/BundleWithSingleExaminationAndAI-Example](Bundle-BundleWithSingleExaminationAndAI-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/ki-productname-extension)

### Formal Views of Extension Content

 [Description of Profiles, Differentials, Snapshots, and how the XML and JSON presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-ki-productname-extension.csv), [Excel](StructureDefinition-ki-productname-extension.xlsx), [Schematron](StructureDefinition-ki-productname-extension.sch) 

#### Constraints



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "ki-productname-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-productname-extension",
  "version" : "0.1.3",
  "name" : "KIProductName",
  "title" : "AI Product Name",
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
  "description" : "Name of the AI product used for analysis.",
  "purpose" : "For documentation of AI product used in automated analysis of retinal images for the purpose of grading images for diabetic rethinopathy.\n\nOrigin: AI solution.\n\nContent: String with name of AI product.",
  "fhirVersion" : "4.0.1",
  "mapping" : [
    {
      "identity" : "rim",
      "uri" : "http://hl7.org/v3",
      "name" : "RIM Mapping"
    }
  ],
  "kind" : "complex-type",
  "abstract" : false,
  "context" : [
    {
      "type" : "element",
      "expression" : "DiagnosticReport"
    }
  ],
  "type" : "Extension",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Extension",
  "derivation" : "constraint",
  "differential" : {
    "element" : [
      {
        "id" : "Extension",
        "path" : "Extension",
        "short" : "AI Product Name",
        "definition" : "Name of the AI product used for analysis."
      },
      {
        "id" : "Extension.extension",
        "path" : "Extension.extension",
        "max" : "0"
      },
      {
        "id" : "Extension.url",
        "path" : "Extension.url",
        "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-productname-extension"
      },
      {
        "id" : "Extension.value[x]",
        "path" : "Extension.value[x]",
        "min" : 1,
        "type" : [
          {
            "code" : "string"
          }
        ]
      }
    ]
  }
}

```
