# RetinaEyeObservation-input-left - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaEyeObservation-input-left**

## Example Observation: RetinaEyeObservation-input-left

Profile: [Retina Eye Observation](StructureDefinition-retina-eye-observation.md)

**status**: Final

**code**: Retinal examination

**effective**: 2025-09-30 12:00:00+0000

**bodySite**: Venstre retina

> **component****code**:Diabetic retinopathy**dataAbsentReason**:Not asked

> **component****code**:Diabetic macular edema**value**: true



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaEyeObservation-input-left",
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
        "code" : "58443009",
        "display" : "Retina of left eye"
      }
    ],
    "text" : "Venstre retina"
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
      "dataAbsentReason" : {
        "coding" : [
          {
            "system" : "http://terminology.hl7.org/CodeSystem/data-absent-reason",
            "code" : "not-asked",
            "display" : "Not asked"
          }
        ]
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
