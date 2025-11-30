# Initial Instructions - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Initial Instructions**

## Extension: Initial Instructions (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/initial-instructions-extension | *Version*:0.2.0 |
| Active as of 2025-11-30 | *Computable Name*:InitialInstructionsExtension |

Initial routing instruction and optional cautions for grading this examination (4000-series and 5000-series).

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Extension: [Bundle/Bundle-SinglExamination-Example](Bundle-Bundle-SinglExamination-Example.md), [Bundle/Bundle-TwoExaminations-Example](Bundle-Bundle-TwoExaminations-Example.md), [DiagnosticReport/RetinaDiagnosticReport-Example-PendingAI](DiagnosticReport-RetinaDiagnosticReport-Example-PendingAI.md), [DiagnosticReport/RetinaDiagnosticReport-Example](DiagnosticReport-RetinaDiagnosticReport-Example.md) and [DiagnosticReport/bb2690e7-ca9f-4070-9c35-c7e36976b144](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/initial-instructions-extension)

### Formal Views of Extension Content

 [Description of Profiles, Differentials, Snapshots, and how the XML and JSON presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-initial-instructions-extension.csv), [Excel](StructureDefinition-initial-instructions-extension.xlsx), [Schematron](StructureDefinition-initial-instructions-extension.sch) 

#### Terminology Bindings

#### Constraints



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "initial-instructions-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/initial-instructions-extension",
  "version" : "0.2.0",
  "name" : "InitialInstructionsExtension",
  "title" : "Initial Instructions",
  "status" : "active",
  "experimental" : true,
  "date" : "2025-11-30T22:57:21+01:00",
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
  "description" : "Initial routing instruction and optional cautions for grading this examination (4000-series and 5000-series).",
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
        "short" : "Initial Instructions",
        "definition" : "Initial routing instruction and optional cautions for grading this examination (4000-series and 5000-series)."
      },
      {
        "id" : "Extension.extension",
        "path" : "Extension.extension",
        "max" : "0"
      },
      {
        "id" : "Extension.url",
        "path" : "Extension.url",
        "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/initial-instructions-extension"
      },
      {
        "id" : "Extension.value[x]",
        "path" : "Extension.value[x]",
        "type" : [
          {
            "code" : "CodeableConcept"
          }
        ],
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-initial-instructions-vs"
        }
      }
    ]
  }
}

```
