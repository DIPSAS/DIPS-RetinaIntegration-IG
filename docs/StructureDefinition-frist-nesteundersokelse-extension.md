# Deadline Next Examination - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Deadline Next Examination**

## Extension: Deadline Next Examination (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/frist-nesteundersokelse-extension | *Version*:0.1.3 |
| Draft as of 2025-11-11 | *Computable Name*:KIFristNesteUndersokelse |

Number of days until next examination.

The number indicates a clinically decided time interval between current retinal examination and next retinal examination based on a risk assessment of the patient during the current retinal examination.

Content: String with a number. The number indicates number of days. The counting of the number of days starts at the date images of the patient's retinas are taken. The end date of the counting is the clinical deadline indicated for the next examination.

1 year counts as 365 days, 2 years counts as 730 days. Used by the EMR to set correct deadline date in the patient's planned contact so that the patient will be recalled within the deadline.

For documentation of a clinically decided time interval between current retinal examination and next retinal examination based on a risk assessment of the patient during the current retinal examination. Origin: Lookup in National Norwegian clinical guidelines for diabetic retinopathy screening [National Norwegian clinical guidelines for diabetic retinopathy screening](https://www.legeforeningen.no/contentassets/c7fccca0ee554d7d80fd8c4818cdd739/godkjente-retningslinjer-for-screening-for-diabetisk-retinopati-05.11.2022.pdf) based on the patient's relevant dataset.

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)
* Examples for this Extension: [Bundle/BundleWithSingleExaminationAndAI-Example](Bundle-BundleWithSingleExaminationAndAI-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/frist-nesteundersokelse-extension)

### Formal Views of Extension Content

 [Description of Profiles, Differentials, Snapshots, and how the XML and JSON presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-frist-nesteundersokelse-extension.csv), [Excel](StructureDefinition-frist-nesteundersokelse-extension.xlsx), [Schematron](StructureDefinition-frist-nesteundersokelse-extension.sch) 

#### Constraints



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "frist-nesteundersokelse-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/frist-nesteundersokelse-extension",
  "version" : "0.1.3",
  "name" : "KIFristNesteUndersokelse",
  "title" : "Deadline Next Examination",
  "status" : "draft",
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
  "description" : "Number of days until next examination.",
  "purpose" : "The number indicates a clinically decided time interval between current retinal examination and next retinal examination based on a risk assessment of the patient during the current retinal examination. \n\nContent: String with a number. The number indicates number of days. The counting of the number of days starts at the date images of the patient's retinas are taken. The end date of the counting is the clinical deadline indicated for the next examination.\n\n1 year counts as 365 days, 2 years counts as 730 days. Used by the EMR to set correct deadline date in the patient's planned contact so that the patient will be recalled within the deadline. \n\nFor documentation of a clinically decided time interval between current retinal examination and next retinal examination based on a risk assessment of the patient during the current retinal examination. Origin: Lookup in National Norwegian clinical guidelines for diabetic retinopathy screening [National Norwegian clinical guidelines for diabetic retinopathy screening](https://www.legeforeningen.no/contentassets/c7fccca0ee554d7d80fd8c4818cdd739/godkjente-retningslinjer-for-screening-for-diabetisk-retinopati-05.11.2022.pdf) based on the patient's relevant dataset.",
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
        "short" : "Deadline Next Examination",
        "definition" : "Number of days until next examination."
      },
      {
        "id" : "Extension.extension",
        "path" : "Extension.extension",
        "max" : "0"
      },
      {
        "id" : "Extension.url",
        "path" : "Extension.url",
        "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/frist-nesteundersokelse-extension"
      },
      {
        "id" : "Extension.value[x]",
        "path" : "Extension.value[x]",
        "min" : 1,
        "type" : [
          {
            "code" : "integer"
          }
        ]
      }
    ]
  }
}

```
