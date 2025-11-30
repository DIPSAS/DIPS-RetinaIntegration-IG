# RetinaEyeObservation-Example-right - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaEyeObservation-Example-right**

## Example Observation: RetinaEyeObservation-Example-right

Profile: [Retina Eye Observation](StructureDefinition-retina-eye-observation.md)

**identifier**: [RetinaObservationIdentifierSystem](NamingSystem-retina-observation-id.md)/ed4ea83b-de33-4ba2-8289-02d2ac75b736

**status**: Final

**code**: Retinal examination

**effective**: 2025-11-30 10:21:00+0000

**bodySite**: Høyre retina

**device**: [Device](Device-RetinaAIDevice-Example.md)

> **component****code**:Diabetic retinopathy**value**: 5

> **component****code**:Diabetic macular edema**value**: true

> **component****code**:Computer assisted image analysis for image quality**value**:Good



## Resource Content

```json
{
  "resourceType" : "Observation",
  "id" : "RetinaEyeObservation-Example-right",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation"
    ]
  },
  "identifier" : [
    {
      "system" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
      "value" : "ed4ea83b-de33-4ba2-8289-02d2ac75b736"
    }
  ],
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
  "effectiveDateTime" : "2025-11-30T10:21:00Z",
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
  "device" : {
    "reference" : "Device/RetinaAIDevice-Example"
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
    },
    {
      "code" : {
        "coding" : [
          {
            "system" : "http://snomed.info/sct",
            "code" : "133887000",
            "display" : "Computer assisted image analysis for image quality"
          }
        ]
      },
      "valueCodeableConcept" : {
        "coding" : [
          {
            "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-imagequality-cs",
            "code" : "2001",
            "display" : "Good"
          }
        ]
      }
    }
  ]
}

```
