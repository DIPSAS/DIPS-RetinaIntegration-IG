# RetinaAppendAIResultOperation-Example - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaAppendAIResultOperation-Example**

## Example Parameters: RetinaAppendAIResultOperation-Example

## Parameters



## Resource Content

```json
{
  "resourceType" : "Parameters",
  "id" : "RetinaAppendAIResultOperation-Example",
  "parameter" : [
    {
      "name" : "sectraStudyId",
      "valueIdentifier" : {
        "system" : "http://sectra.no/identifiers",
        "value" : "MMA94126079"
      }
    },
    {
      "name" : "rightEye",
      "resource" : {
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
    },
    {
      "name" : "leftEye",
      "resource" : {
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
    },
    {
      "name" : "conclusion",
      "valueCodeableConcept" : {
        "coding" : [
          {
            "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs",
            "code" : "1004",
            "display" : "Ny fotokontroll (primærgradering)"
          }
        ]
      }
    },
    {
      "name" : "daysUntilNextExamination",
      "valueInteger" : 180
    },
    {
      "name" : "effectiveTime",
      "valueDateTime" : "2025-09-30T12:00:00Z"
    },
    {
      "name" : "aiDevice",
      "resource" : {
        "resourceType" : "Device",
        "id" : "RetinaAIDevice-input",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device"
          ]
        },
        "deviceName" : [
          {
            "name" : "AwesomeAI for Retina",
            "type" : "model-name"
          }
        ],
        "version" : [
          {
            "type" : {
              "coding" : [
                {
                  "code" : "model-number"
                }
              ]
            },
            "value" : "v2.1.0"
          },
          {
            "type" : {
              "coding" : [
                {
                  "code" : "software"
                }
              ]
            },
            "value" : "Standard protocol"
          }
        ]
      }
    },
    {
      "name" : "fullReport",
      "valueAttachment" : {
        "contentType" : "text/plain",
        "data" : "Base64binary",
        "title" : "Full report"
      }
    },
    {
      "name" : "metaTags",
      "valueCoding" : {
        "system" : "http://terminology.hl7.org/CodeSystem/v3-ActReason",
        "code" : "VALIDATION",
        "display" : "validation review"
      }
    }
  ]
}

```
