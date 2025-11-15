# Next Examination Previous Examination - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Next Examination Previous Examination**

## Extension: Next Examination Previous Examination (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/tiltaksstatus-forrige-undersokelse-extension | *Version*:0.1.3 |
| Active as of 2025-11-15 | *Computable Name*:RetinaTiltaksstausForrigeUndersokelseExtension |

The next step in the screening process after the previous examination. (3000-series)

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)
* Examples for this Extension: [Bundle/BundleWithSinglExamination-Example](Bundle-BundleWithSinglExamination-Example.md), [Bundle/BundleWithSingleExaminationAndAI-Example](Bundle-BundleWithSingleExaminationAndAI-Example.md), [Bundle/BundleWithTwoExaminations-Example](Bundle-BundleWithTwoExaminations-Example.md) and [DiagnosticReport/bb2690e7-ca9f-4070-9c35-c7e36976b144](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/tiltaksstatus-forrige-undersokelse-extension)

### Formal Views of Extension Content

 [Description of Profiles, Differentials, Snapshots, and how the XML and JSON presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-tiltaksstatus-forrige-undersokelse-extension.csv), [Excel](StructureDefinition-tiltaksstatus-forrige-undersokelse-extension.xlsx), [Schematron](StructureDefinition-tiltaksstatus-forrige-undersokelse-extension.sch) 

#### Terminology Bindings

#### Constraints



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "tiltaksstatus-forrige-undersokelse-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/tiltaksstatus-forrige-undersokelse-extension",
  "version" : "0.1.3",
  "name" : "RetinaTiltaksstausForrigeUndersokelseExtension",
  "title" : "Next Examination Previous Examination",
  "status" : "active",
  "experimental" : true,
  "date" : "2025-11-15T17:14:08+01:00",
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
  "description" : "The next step in the screening process after the previous examination. (3000-series)",
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
        "short" : "Next Examination Previous Examination",
        "definition" : "The next step in the screening process after the previous examination. (3000-series)"
      },
      {
        "id" : "Extension.extension",
        "path" : "Extension.extension",
        "max" : "0"
      },
      {
        "id" : "Extension.url",
        "path" : "Extension.url",
        "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/tiltaksstatus-forrige-undersokelse-extension"
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
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/tiltaksstatus-forrigeUndersokelse-vs"
        }
      }
    ]
  }
}

```
