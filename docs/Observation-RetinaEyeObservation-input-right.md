# RetinaEyeObservation-input-right - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaEyeObservation-input-right**

## Example Observation: RetinaEyeObservation-input-right

Profile: [Retina Eye Observation](StructureDefinition-retina-eye-observation.md)

**status**: Final

**code**: Retinal examination

**effective**: 2025-09-30 12:00:00+0000

**bodySite**: Høyre retina

> **component****code**:Diabetic retinopathy**value**: 5

> **component****code**:Diabetic macular edema**value**: true



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaEyeObservation-input-right",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation"
    ]
  },
  "status" : "final",
  "code" : {
    "coding" : [
      {
        "system" : "http://snomed.info/sct",
        "code" : "134395001",
        "display" : "Diabetic retinopathy screening"
      }
    ],
    "text" : "Retinal examination"
  },
  "effectiveDateTime" : "2025-09-30T12:00:00Z",
  "bodySite" : {
    "coding" : [
      {
        "system" : "http://snomed.info/sct",
        "code" : "5597008",
        "display" : "Retina of right eye"
      }
    ],
    "text" : "Høyre retina"
  },
  "component" : [
    {
      "code" : {
        "coding" : [
          {
            "system" : "http://snomed.info/sct",
            "code" : "4855003",
            "display" : "Diabetic retinopathy"
          }
        ]
      },
      "valueQuantity" : {
        "value" : 5
      }
    },
    {
      "code" : {
        "coding" : [
          {
            "system" : "http://snomed.info/sct",
            "code" : "312912001",
            "display" : "Diabetic macular edema"
          }
        ]
      },
      "valueBoolean" : true
    }
  ]
}

```
