# Retina DiagnosticReport - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina DiagnosticReport**

## Resource Profile: Retina DiagnosticReport 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report | *Version*:0.6.0 |
| Draft as of 2025-12-08 | *Computable Name*:RetinaDiagnosticReport |

 
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
  "version" : "0.6.0",
  "name" : "RetinaDiagnosticReport",
  "title" : "Retina DiagnosticReport",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-08",
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
        }
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
        "id" : "DiagnosticReport.extension:cautions",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "cautions",
        "min" : 0,
        "max" : "*",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/cautions-extension"
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
              "system" : "http://dips.no/fhir/RetinaIntegration/examination-id",
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
        "patternUri" : "http://dips.no/fhir/RetinaIntegration/examination-id"
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
        "short" : "Retina imaging procedure(s) performed: fundus photography and/or OCT",
        "definition" : "The type(s) of retinal imaging procedure(s) the photographer has indicated shall be performed.",
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-imaging-procedure-vs"
        }
      },
      {
        "id" : "DiagnosticReport.subject",
        "path" : "DiagnosticReport.subject",
        "short" : "Reference to the patient",
        "definition" : "A reference to the patient. The patient's identifier MUST be one of the official Norwegian patient identifier systems: Fødselsnummer (urn:oid:2.16.578.1.12.4.1.4.1), D-nummer (urn:oid:2.16.578.1.12.4.1.4.2), or Felles hjelpenummer (urn:oid:2.16.578.1.12.4.1.4.3).",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : ["http://hl7.org/fhir/StructureDefinition/Patient"]
          }
        ],
        "example" : [
          {
            "label" : "Patient with Fødselsnummer",
            "valueReference" : {
              "reference" : "Patient/cdp1000807",
              "identifier" : {
                "system" : "urn:oid:2.16.578.1.12.4.1.4.1",
                "value" : "15076500565"
              }
            }
          },
          {
            "label" : "Patient with D-nummer",
            "valueReference" : {
              "reference" : "Patient/cdp1004445",
              "identifier" : {
                "system" : "urn:oid:2.16.578.1.12.4.1.4.2",
                "value" : "41018512345"
              }
            }
          },
          {
            "label" : "Patient with Felles Hjelpenummer",
            "valueReference" : {
              "identifier" : {
                "system" : "urn:oid:2.16.578.1.12.4.1.4.3",
                "value" : "11223344556"
              }
            }
          }
        ]
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
        "id" : "DiagnosticReport.result:dmeFinding",
        "path" : "DiagnosticReport.result",
        "sliceName" : "dmeFinding",
        "short" : "Optional DME Findings (up to 2: left and/or right eye). Use bodySite element to distinguish left vs right eye.",
        "min" : 0,
        "max" : "2",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-macular-edema-finding"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:drFinding",
        "path" : "DiagnosticReport.result",
        "sliceName" : "drFinding",
        "short" : "Optional DR Findings (up to 2: left and/or right eye). Use bodySite element to distinguish left vs right eye.",
        "min" : 0,
        "max" : "2",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-retinopathy-finding"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:imageQuality",
        "path" : "DiagnosticReport.result",
        "sliceName" : "imageQuality",
        "short" : "Optional Image Quality Observations (up to 2: left and/or right eye). Use bodySite element to distinguish left vs right eye.",
        "min" : 0,
        "max" : "2",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-quality-asessment"
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
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusion-code-vs"
        }
      }
    ]
  }
}

```
