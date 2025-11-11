# Retina DiagnosticReport - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina DiagnosticReport**

## Resource Profile: Retina DiagnosticReport ( Experimental ) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaDiagnosticReport | *Version*:0.1.3 |
| Draft as of 2025-11-11 | *Computable Name*:DIPSRetinaIntegrationDiagnosticReport |

 
This diagnostic report for the grading of a retina screening examination. 

 
The purpose of RetinaIntegrationDiagnosticReport is for a client to examine the state of a retina screening examination grading. This includes documenting which observations were made (e.g., fundus photography, OCT), any laboratory results relevant to the examination (e.g., HbA1c), and the results of AI analysis or manual grading for diabetic retinopathy (DR) and diabetic macular edema (DME). Additionally, it captures metadata about the examination, such as identifiers, image quality, and recommended follow-up actions. 

**Usages:**

* Examples for this Profile: [DiagnosticReport/bb2690e7-ca9f-4070-9c35-c7e36976b144](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md)
* CapabilityStatements using this Profile: [CapabilityStatement[http://dips.no/fhir/RetinaIntegration/CapabilityStatement/DIPSRetinaCapabilityStatement|0.1.3]](CapabilityStatement-DIPSRetinaCapabilityStatement.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/RetinaDiagnosticReport)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-RetinaDiagnosticReport.csv), [Excel](StructureDefinition-RetinaDiagnosticReport.xlsx), [Schematron](StructureDefinition-RetinaDiagnosticReport.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "RetinaDiagnosticReport",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaDiagnosticReport",
  "version" : "0.1.3",
  "name" : "DIPSRetinaIntegrationDiagnosticReport",
  "title" : "Retina DiagnosticReport",
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
  "description" : "This diagnostic report for the grading of a retina screening examination.",
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
        "id" : "DiagnosticReport.extension:retinaImageQualityExtension",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "retinaImageQualityExtension",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagequality-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:kiProductName",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "kiProductName",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-productname-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:kiVersionAlgoritme",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "kiVersionAlgoritme",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-versjon-algoritme-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:kiFristNesteUndersokelse",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "kiFristNesteUndersokelse",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/frist-nesteundersokelse-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:kiProtokoll",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "kiProtokoll",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/ki-protokoll-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:videreForlop",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "videreForlop",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/videre-forlop-extension"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.extension:forrigeUndersokelse",
        "path" : "DiagnosticReport.extension",
        "sliceName" : "forrigeUndersokelse",
        "min" : 1,
        "max" : "1",
        "type" : [
          {
            "code" : "Extension",
            "profile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/tiltaksstatus-forrige-undersokelse-extension"
            ]
          }
        ]
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
        "id" : "DiagnosticReport.identifier:sectraStudyId",
        "path" : "DiagnosticReport.identifier",
        "sliceName" : "sectraStudyId",
        "short" : "Sectra Study Identifier",
        "definition" : "Uniquely identify a study within the Sectra system.",
        "comment" : "There may be multiple Sectra Study Identifiers if the report is associated with multiple imaging studies. If there are no Sectra studies it is not possible for AI to grade the examination.",
        "min" : 0,
        "max" : "*"
      },
      {
        "id" : "DiagnosticReport.identifier:sectraStudyId.system",
        "path" : "DiagnosticReport.identifier.system",
        "min" : 1,
        "patternUri" : "http://sectra.no/identifiers"
      },
      {
        "id" : "DiagnosticReport.identifier:retinaExaminationId",
        "path" : "DiagnosticReport.identifier",
        "sliceName" : "retinaExaminationId",
        "short" : "Retina Examination Identifier",
        "definition" : "Identifies the retina examination in RetinaIntegration.",
        "min" : 1,
        "max" : "1"
      },
      {
        "id" : "DiagnosticReport.identifier:retinaExaminationId.system",
        "path" : "DiagnosticReport.identifier.system",
        "min" : 1,
        "patternUri" : "http://dips.no/fhir/NamingSystem/retina-examination-id"
      },
      {
        "id" : "DiagnosticReport.code",
        "path" : "DiagnosticReport.code",
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
        "id" : "DiagnosticReport.result:fundusFotografiObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "fundusFotografiObservation",
        "short" : "Optional Fundus Photography Observation.",
        "definition" : "An optional observation indicating that fundus photography was performed.",
        "comment" : "This slice is used to explicitly document when fundus photography has been performed during a retina screening examination. The observation should use the code CKDP10 from the Norwegian code system.",
        "requirements" : "Used to track and document the completion of fundus photography procedures within the retina screening workflow.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/fundus-foto-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:octObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "octObservation",
        "short" : "Optional OCT Observation",
        "definition" : "An optional observation indicating that Optical Coherence Tomography (OCT) was performed.",
        "comment" : "This slice is used to explicitly document when OCT has been performed during a retina screening examination. The observation should use the code CKFX16 from the Norwegian code system.",
        "requirements" : "Used to track and document the completion of OCT procedures within the retina screening workflow.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/oct-observation"
            ]
          }
        ]
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
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/hba1c-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:drRightEyeObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "drRightEyeObservation",
        "short" : "Optional Diabetic Retinopathy Right Eye Observation",
        "definition" : "An optional observation containing diabetic retinopathy assessment results for the right eye. This observation documents AI-analyzed or manually graded findings related to diabetic retinopathy severity in the right eye.",
        "comment" : "This slice is used to document diabetic retinopathy findings specifically for the right eye. The observation should use the SNOMED CT code 4855003 for diabetic retinopathy.",
        "requirements" : "Essential for tracking diabetic retinopathy progression and severity in the right eye for appropriate clinical decision making and follow-up scheduling.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/dr-right-eye-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:drLeftEyeObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "drLeftEyeObservation",
        "short" : "Optional Diabetic Retinopathy Left Eye Observation",
        "definition" : "An optional observation containing diabetic retinopathy assessment results for the left eye. This observation documents AI-analyzed or manually graded findings related to diabetic retinopathy severity in the left eye.",
        "comment" : "This slice is used to document diabetic retinopathy findings specifically for the left eye. The observation should use the SNOMED CT code 4855003 for diabetic retinopathy.",
        "requirements" : "Essential for tracking diabetic retinopathy progression and severity in the left eye for appropriate clinical decision making and follow-up scheduling.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/dr-left-eye-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:dmeRightEyeObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "dmeRightEyeObservation",
        "short" : "Optional Diabetic Macular Edema Right Eye Observation",
        "definition" : "An optional observation containing diabetic macular edema assessment results for the right eye. This observation documents AI-analyzed or manually graded findings related to diabetic macular edema presence in the right eye.",
        "comment" : "This slice is used to document diabetic macular edema findings specifically for the right eye. The observation should use the SNOMED CT code 312912001 for diabetic macular edema.",
        "requirements" : "Critical for identifying and monitoring diabetic macular edema in the right eye, which requires prompt treatment to prevent vision loss.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/dme-right-eye-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.result:dmeLeftEyeObservation",
        "path" : "DiagnosticReport.result",
        "sliceName" : "dmeLeftEyeObservation",
        "short" : "Optional Diabetic Macular Edema Left Eye Observation",
        "definition" : "An optional observation containing diabetic macular edema assessment results for the left eye. This observation documents AI-analyzed or manually graded findings related to diabetic macular edema presence in the left eye.",
        "comment" : "This slice is used to document diabetic macular edema findings specifically for the left eye. The observation should use the SNOMED CT code 312912001 for diabetic macular edema.",
        "requirements" : "Critical for identifying and monitoring diabetic macular edema in the left eye, which requires prompt treatment to prevent vision loss.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/dme-left-eye-observation"
            ]
          }
        ]
      },
      {
        "id" : "DiagnosticReport.conclusionCode",
        "path" : "DiagnosticReport.conclusionCode",
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusioncode-vs"
        }
      }
    ]
  }
}

```
