# AI Algorithm Version - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **AI Algorithm Version**

## Extension: AI Algorithm Version (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-versjon-algoritme-extension | *Version*:0.1.3 |
| Draft as of 2025-11-16 | *Computable Name*:KIVersionAlgoritme |

Version of the AI algorithm used for analysis.

For documentation of the algorithm version used by the AI product in automated analysis of retinal images for the purpose of grading images for diabetic rethinopathy.

Origin: AI solution.

Content: String with AI product's algorithm version.

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)
* Examples for this Extension: [Bundle/BundleWithSingleExaminationAndAI-Example](Bundle-BundleWithSingleExaminationAndAI-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/ki-versjon-algoritme-extension)

### Formal Views of Extension Content

 [Description of Profiles, Differentials, Snapshots, and how the XML and JSON presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-ki-versjon-algoritme-extension.csv), [Excel](StructureDefinition-ki-versjon-algoritme-extension.xlsx), [Schematron](StructureDefinition-ki-versjon-algoritme-extension.sch) 

#### Constraints



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "ki-versjon-algoritme-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-versjon-algoritme-extension",
  "version" : "0.1.3",
  "name" : "KIVersionAlgoritme",
  "title" : "AI Algorithm Version",
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
  "description" : "Version of the AI algorithm used for analysis.",
  "purpose" : "For documentation of the algorithm version used by the AI product in automated analysis of retinal images for the purpose of grading images for diabetic rethinopathy.\n\nOrigin: AI solution.\n\nContent: String with AI product's algorithm version.",
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
        "short" : "AI Algorithm Version",
        "definition" : "Version of the AI algorithm used for analysis."
      },
      {
        "id" : "Extension.extension",
        "path" : "Extension.extension",
        "max" : "0"
      },
      {
        "id" : "Extension.url",
        "path" : "Extension.url",
        "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-versjon-algoritme-extension"
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
