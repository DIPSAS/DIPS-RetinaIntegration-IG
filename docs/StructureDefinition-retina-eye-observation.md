# Retina Eye Observation - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Eye Observation**

## Resource Profile: Retina Eye Observation ( Experimental ) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation | *Version*:0.2.0 |
| Draft as of 2025-11-30 | *Computable Name*:RetinaEyeObservation |

 
The result of AI grading for one eye. The bodySite element identifies which eye (right or left). 

 
The DR severity component uses a Quantity value representing the severity level of diabetic retinopathy: 

* Value: [0.0 1.0>
  * Description: Ingen synlig diabetisk retinopati (DR)
* Value: [1.0 2.0>
  * Description: Mild non-proliferativ DR
* Value: [2.0 3.0>
  * Description: Moderat non-proliferativ DR
* Value: [3.0 4.0>
  * Description: Alvorlig non-proliferativ DR
* Value: ≥ 4.0
  * Description: Proliferativ DR

 
TODO: Consider this: Should we use a CodeableConcept with a coding for each severity level, in addition to the Quantity value? Susggested LOINC 11504-0 "Diabetic retinopathy severity" with answer list LL5321-4 with standardized severity levels. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Profile: [Observation/RetinaEyeObservation-Example-left](Observation-RetinaEyeObservation-Example-left.md), [Observation/RetinaEyeObservation-Example-right](Observation-RetinaEyeObservation-Example-right.md), [Observation/RetinaEyeObservation-input-left](Observation-RetinaEyeObservation-input-left.md) and [Observation/RetinaEyeObservation-input-right](Observation-RetinaEyeObservation-input-right.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-eye-observation)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-retina-eye-observation.csv), [Excel](StructureDefinition-retina-eye-observation.xlsx), [Schematron](StructureDefinition-retina-eye-observation.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-eye-observation",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation",
  "version" : "0.2.0",
  "name" : "RetinaEyeObservation",
  "title" : "Retina Eye Observation",
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
  "description" : "The result of AI grading for one eye. The bodySite element identifies which eye (right or left).",
  "purpose" : "The DR severity component uses a Quantity value representing the severity level of diabetic retinopathy:\n\n<table class=\"codes\">\n<tr><th>Value</th><th>Description</th></tr>\n<tr><td>[0.0 1.0></td><td>Ingen synlig diabetisk retinopati (DR)</td></tr>\n<tr><td>[1.0 2.0></td><td>Mild non-proliferativ DR</td></tr>\n<tr><td>[2.0 3.0></td><td>Moderat non-proliferativ DR</td></tr>\n<tr><td>[3.0 4.0></td><td>Alvorlig non-proliferativ DR</td></tr>\n<tr><td>≥ 4.0</td><td>Proliferativ DR</td></tr>\n</table>\n\nTODO: Consider this: Should we use a CodeableConcept with a coding for each severity level, in addition to the Quantity value? \nSusggested LOINC 11504-0 \"Diabetic retinopathy severity\" with answer list LL5321-4 with standardized severity levels. ",
  "fhirVersion" : "4.0.1",
  "mapping" : [
    {
      "identity" : "workflow",
      "uri" : "http://hl7.org/fhir/workflow",
      "name" : "Workflow Pattern"
    },
    {
      "identity" : "sct-concept",
      "uri" : "http://snomed.info/conceptdomain",
      "name" : "SNOMED CT Concept Domain Binding"
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
    },
    {
      "identity" : "sct-attr",
      "uri" : "http://snomed.org/attributebinding",
      "name" : "SNOMED CT Attribute Binding"
    }
  ],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Observation",
  "baseDefinition" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-observation",
  "derivation" : "constraint",
  "differential" : {
    "element" : [
      {
        "id" : "Observation",
        "path" : "Observation"
      },
      {
        "id" : "Observation.code",
        "path" : "Observation.code",
        "patternCodeableConcept" : {
          "coding" : [
            {
              "system" : "http://snomed.info/sct",
              "code" : "134395001",
              "display" : "Diabetic retinopathy screening"
            }
          ]
        }
      },
      {
        "id" : "Observation.bodySite",
        "path" : "Observation.bodySite",
        "short" : "Which eye (right or left retina)",
        "definition" : "Identifies whether this observation is for the right eye (SNOMED CT: 5597008) or left eye (SNOMED CT: 58443009).",
        "min" : 1,
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-body-site-vs"
        }
      },
      {
        "id" : "Observation.device",
        "path" : "Observation.device",
        "short" : "AI device that performed the analysis.",
        "definition" : "Reference to the AI Device resource that performed the automated analysis producing this observation.",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : [
              "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device"
            ]
          }
        ]
      },
      {
        "id" : "Observation.component",
        "path" : "Observation.component",
        "slicing" : {
          "discriminator" : [
            {
              "type" : "value",
              "path" : "code"
            }
          ],
          "rules" : "open"
        },
        "min" : 2
      },
      {
        "id" : "Observation.component:drComponent",
        "path" : "Observation.component",
        "sliceName" : "drComponent",
        "short" : "DR severity (0.0 - 5.0)",
        "min" : 1,
        "max" : "1"
      },
      {
        "id" : "Observation.component:drComponent.code",
        "path" : "Observation.component.code",
        "patternCodeableConcept" : {
          "coding" : [
            {
              "system" : "http://snomed.info/sct",
              "code" : "4855003",
              "display" : "Diabetic retinopathy"
            }
          ]
        }
      },
      {
        "id" : "Observation.component:drComponent.value[x]",
        "path" : "Observation.component.value[x]",
        "type" : [
          {
            "code" : "Quantity"
          }
        ]
      },
      {
        "id" : "Observation.component:dmeComponent",
        "path" : "Observation.component",
        "sliceName" : "dmeComponent",
        "short" : "DME presence (yes/no)",
        "min" : 1,
        "max" : "1"
      },
      {
        "id" : "Observation.component:dmeComponent.code",
        "path" : "Observation.component.code",
        "patternCodeableConcept" : {
          "coding" : [
            {
              "system" : "http://snomed.info/sct",
              "code" : "312912001",
              "display" : "Diabetic macular edema"
            }
          ]
        }
      },
      {
        "id" : "Observation.component:dmeComponent.value[x]",
        "path" : "Observation.component.value[x]",
        "type" : [
          {
            "code" : "boolean"
          }
        ]
      },
      {
        "id" : "Observation.component:imageQuality",
        "path" : "Observation.component",
        "sliceName" : "imageQuality",
        "short" : "Image quality as assessed by AI. (2000-series)",
        "definition" : "Quality of the retinal image for this eye as assessed by the AI solution.",
        "min" : 0,
        "max" : "1"
      },
      {
        "id" : "Observation.component:imageQuality.code",
        "path" : "Observation.component.code",
        "patternCodeableConcept" : {
          "coding" : [
            {
              "system" : "http://snomed.info/sct",
              "code" : "133887000",
              "display" : "Computer assisted image analysis for image quality"
            }
          ]
        }
      },
      {
        "id" : "Observation.component:imageQuality.value[x]",
        "path" : "Observation.component.value[x]",
        "type" : [
          {
            "code" : "CodeableConcept"
          }
        ],
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-imagequality-vs"
        }
      }
    ]
  }
}

```
