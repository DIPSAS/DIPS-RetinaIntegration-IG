# Retina DiagnosticReport - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina DiagnosticReport**

## Resource Profile: Retina DiagnosticReport ( Experimental ) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report | *Version*:0.2.0 |
| Draft as of 2025-11-30 | *Computable Name*:RetinaDiagnosticReport |

 
Diagnostic report for the grading process of a single examination which is part of a screening program. 

 
The purpose of RetinaIntegrationDiagnosticReport is for a client to examine the state of a retina screening examination grading. This includes documenting which observations were made (e.g., fundus photography, OCT), any laboratory results relevant to the examination (e.g., HbA1c), and the results of AI analysis or manual grading for diabetic retinopathy (DR) and diabetic macular edema (DME). Additionally, it captures metadata about the examination, such as identifiers, image quality, and recommended follow-up actions. 

**Usages:**

* Examples for this Profile: [DiagnosticReport/RetinaDiagnosticReport-Example-PendingAI](DiagnosticReport-RetinaDiagnosticReport-Example-PendingAI.md), [DiagnosticReport/RetinaDiagnosticReport-Example](DiagnosticReport-RetinaDiagnosticReport-Example.md) and [DiagnosticReport/bb2690e7-ca9f-4070-9c35-c7e36976b144](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md)
* CapabilityStatements using this Profile: [Retina CapabilityStatement](CapabilityStatement-RetinaCapabilityStatement.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-diagnostic-report)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-retina-diagnostic-report.csv), [Excel](StructureDefinition-retina-diagnostic-report.xlsx), [Schematron](StructureDefinition-retina-diagnostic-report.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-diagnostic-report",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report",
  "version" : "0.2.0",
  "name" : "RetinaDiagnosticReport",
  "title" : "Retina DiagnosticReport",
  "status" : "draft",
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
  "description" : "Diagnostic report for the grading process of a single examination which is part of a screening program.",
  "purpose" : "The purpose of RetinaIntegrationDiagnosticReport is for a client to examine the state of a retina screening examination grading. This includes documenting which observations were made (e.g., fundus photography, OCT), any laboratory results relevant to the examination (e.g., HbA1c), and the results of AI analysis or manual grading for diabetic retinopathy (DR) and diabetic macular edema (DME). Additionally, it captures metadata about the examination, such as identifiers, image quality, and recommended follow-up actions.",
  "fhirVersion" : "4.0.1",
  "mapping" : [
    {
      "identity" : "workflow",
      "uri" : "http://hl7.org/fhir/workflow",
      "name" : "Workflow Pattern"
    },
    {
      "identity" : "v2",
      "uri" : "http://hl7.org/v2",
      "name" : "HL7 v2 Mapping"
    },
    {
      "identity" : "rim",
      "uri" : "http://hl7.org/v3",
      "name" : "RIM Mapping"
    },
    {
      "identity" : "w5",
      "uri" : "http://hl7.org/fhir/fivews",
      "name" : "FiveWs Pattern Mapping"
    }
  ],
  "kind" : "resource",
  "abstract" : false,
  "type" : "DiagnosticReport",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/DiagnosticReport",
  "derivation" : "constraint",
  "differential" : {
    "element" : [
      {
        "id" : "DiagnosticReport",
        "path" : "DiagnosticReport"
      },
      {
        "id" : "DiagnosticReport.implicitRules",
        "path" : "DiagnosticReport.implicitRules",
        "max" : "0"
      },
      {
        "id" : "DiagnosticReport.extension",
        "path" : "DiagnosticReport.extension",
        "slicing" : {
          "discriminator" : [
            {
              "type" : "value",
              "path" : "url"
            }
          ],
          "ordered" : false,
          "rules" : "open"
        },
        "min" : 1
      },
      {
        "id" : "DiagnosticReport.extension:daysUntilNextExamination",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "daysUntilNextExamination",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/days-until-next-examination-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:initialInstructions",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "initialInstructions",
        "min" : 1,
        "max" : "*",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/initial-instructions-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:previousExaminationConclusion",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "previousExaminationConclusion",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/previous-examination-conclusion-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.modifierExtension",
        "path" : "DiagnosticReport.modifierExtension",
        "max" : "0"
      },
      {
        "id" : "DiagnosticReport.identifier",
        "path" : "DiagnosticReport.identifier",
        "slicing" : {
          "discriminator" : [
            {
              "type" : "value",
              "path" : "system"
            }
          ],
          "rules" : "open"
        },
        "min" : 1
      },
      {
        "id" : "DiagnosticReport.identifier:retinaExaminationId",
        "path" : "DiagnosticReport.identifier",
        "sliceName" : "retinaExaminationId",
        "short" : "Retina Examination Identifier (GUID)",
        "definition" : "Identifies the retina examination in RetinaIntegration. Value must be a valid GUID in format: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        "min" : 1,
        "max" : "1",
        "example" : [
          {
            "label" : "UUID Identifier",
            "valueIdentifier" : {
              "system" : "http://dips.no/fhir/NamingSystem/retina-examination-id",
              "value" : "550e8400-e29b-41d4-a716-446655440000"
            }
          }
        ]
      },
      {
        "id" : "DiagnosticReport.identifier:retinaExaminationId.use",
        "path" : "DiagnosticReport.identifier.use",
        "max" : "0"
      },
      {
        "id" : "DiagnosticReport.identifier:retinaExaminationId.system",
        "path" : "DiagnosticReport.identifier.system",
        "min" : 1,
        "patternUri" : "http://dips.no/fhir/NamingSystem/retina-examination-id"
      },
      {
        "id" : "DiagnosticReport.identifier:retinaExaminationId.value",
        "path" : "DiagnosticReport.identifier.value",
        "short" : "Unique identifier for the examination (GUID)",
        "min" : 1
      },
      {
        "id" : "DiagnosticReport.status",
        "path" : "DiagnosticReport.status",
        "short" : "Status of the diagnostic report: registered | partial | final",
        "definition" : "Use 'preliminary' when the examination is created and awaiting AI/manual grading. \r\nUse 'final' when grading is complete."
      },
      {
        "id" : "DiagnosticReport.code",
        "path" : "DiagnosticReport.code",
        "short" : "Fixed code: Bildediagnostikk",
        "patternCodeableConcept" : {
          "coding" : [
            {
              "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660",
              "code" : "B",
              "display" : "Bildediagnostikk"
            }
          ]
        }
      },
      {
        "id" : "DiagnosticReport.performer",
        "path" : "DiagnosticReport.performer",
        "max" : "0"
      },
      {
        "id" : "DiagnosticReport.resultsInterpreter",
        "path" : "DiagnosticReport.resultsInterpreter",
        "max" : "0"
      },
      {
        "id" : "DiagnosticReport.result",
        "path" : "DiagnosticReport.result",
        "slicing" : {
          "discriminator" : [
            {
              "type" : "profile",
              "path" : "resolve()"
            }
          ],
          "rules" : "open"
        }
      },
      {
        "id" : "DiagnosticReport.result:hbA1cObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "hbA1cObservation",
        "short" : "Optional HbA1c Laboratory Result",
        "definition" : "An optional observation containing HbA1c laboratory results. This observation provides important context for diabetic retinopathy assessment by documenting the patient's glycemic control status at the time of retinal examination. This value is reported by the user before the examination begins.",
        "comment" : "This slice is used to include HbA1c laboratory values that provide clinical context for retinal screening. The observation should use the SNOMED CT code 167491000202108 for HbA1c.",
        "requirements" : "HbA1c values provide essential clinical context for interpreting retinal screening results and determining appropriate follow-up intervals in diabetic retinopathy management.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-hba1c-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:eyeObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "eyeObservation",
        "short" : "Optional Eye Assessment (Right or Left)",
        "definition" : "An optional observation containing diabetic retinopathy and macular edema assessment results for one eye. This observation uses components to document both DR severity and DME presence. The bodySite element identifies which eye (right or left).",
        "comment" : "This slice contains a multi-component observation for one eye with DR severity and DME presence as separate components. Up to two instances can be present (one for each eye).",
        "requirements" : "Essential for tracking diabetic retinopathy and macular edema for appropriate clinical decision making and follow-up scheduling.",
        "min" : 0,
        "max" : "2",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.imagingStudy",
        "path" : "DiagnosticReport.imagingStudy",
        "short" : "Reference to imaging studies containing retinal images.",
        "definition" : "References to ImagingStudy resources that contain the retinal images analyzed for this examination.",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagingstudy"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.conclusion",
        "path" : "DiagnosticReport.conclusion",
        "max" : "0"
      },
      {
        "id" : "DiagnosticReport.conclusionCode",
        "path" : "DiagnosticReport.conclusionCode",
        "short" : "Conclusion codes summarizing the findings of the retina examination.",
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusioncode-vs"
        }
      }
    ]
  }
}

```
