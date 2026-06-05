# RetinaAppendAIResultOperation-Example - RetinaIntegration v0.9.0

## Example Parameters: RetinaAppendAIResultOperation-Example



## Resource Content

```json
{
  "resourceType" : "Parameters",
  "id" : "RetinaAppendAIResultOperation-Example",
  "parameter" : [{
    "name" : "sectraStudyId",
    "valueString" : "MMA94126079"
  },
  {
    "name" : "conclusion",
    "valueCodeableConcept" : {
      "coding" : [{
        "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
        "code" : "1004",
        "display" : "Ny fotokontroll (primærgradering)"
      }]
    }
  },
  {
    "name" : "monthsUntilNextExamination",
    "valueInteger" : 6
  },
  {
    "name" : "leftGradability",
    "valueCode" : "good-gradability"
  },
  {
    "name" : "rightGradability",
    "valueCode" : "good-gradability"
  },
  {
    "name" : "rightDiabeticRetinopathy",
    "valueDecimal" : 0
  },
  {
    "name" : "rightDiabeticMacularEdema",
    "valueBoolean" : false
  },
  {
    "name" : "leftDiabeticRetinopathy",
    "valueDecimal" : 1.4
  },
  {
    "name" : "leftDiabeticMacularEdema",
    "valueBoolean" : false
  },
  {
    "name" : "rightEyeImage",
    "resource" : {
      "resourceType" : "Observation",
      "id" : "RetinaImageParameter-Example-right-input-1",
      "status" : "final",
      "code" : {
        "coding" : [{
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs",
          "code" : "6001",
          "display" : "Macula centered"
        },
        {
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-quality-cs",
          "code" : "2001",
          "display" : "Good"
        }]
      }
    }
  },
  {
    "name" : "rightEyeImage",
    "resource" : {
      "resourceType" : "Observation",
      "id" : "RetinaImageParameter-Example-right-input-2",
      "status" : "final",
      "code" : {
        "coding" : [{
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs",
          "code" : "6002",
          "display" : "Optic disc centered"
        },
        {
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-quality-cs",
          "code" : "2002",
          "display" : "Barely gradable"
        }]
      }
    }
  },
  {
    "name" : "leftEyeImage",
    "resource" : {
      "resourceType" : "Observation",
      "id" : "RetinaImageParameter-Example-left-input-1",
      "status" : "final",
      "code" : {
        "coding" : [{
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs",
          "code" : "6001",
          "display" : "Macula centered"
        },
        {
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-quality-cs",
          "code" : "2003",
          "display" : "Not gradable"
        }]
      }
    }
  },
  {
    "name" : "leftEyeImage",
    "resource" : {
      "resourceType" : "Observation",
      "id" : "RetinaImageParameter-Example-left-input-2",
      "status" : "final",
      "code" : {
        "coding" : [{
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-view-cs",
          "code" : "6002",
          "display" : "Optic disc centered"
        },
        {
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-image-quality-cs",
          "code" : "2004",
          "display" : "Missing"
        }]
      }
    }
  },
  {
    "name" : "aiDevice",
    "resource" : {
      "resourceType" : "Device",
      "id" : "RetinaAIDevice-input",
      "meta" : {
        "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device"]
      },
      "deviceName" : [{
        "name" : "AwesomeAI for Retina",
        "type" : "model-name"
      }],
      "version" : [{
        "type" : {
          "coding" : [{
            "code" : "model-number"
          }]
        },
        "value" : "v2.1.0"
      },
      {
        "type" : {
          "coding" : [{
            "code" : "software"
          }]
        },
        "value" : "Standard protocol"
      }]
    }
  },
  {
    "name" : "performedDateTime",
    "valueDateTime" : "2026-03-31T10:00:00+01:00"
  },
  {
    "name" : "cameraDevice",
    "resource" : {
      "resourceType" : "Device",
      "id" : "RetinaCameraDevice-input",
      "meta" : {
        "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-camera-device"]
      },
      "serialNumber" : "SN123456789",
      "deviceName" : [{
        "name" : "AAK_TOPCON2",
        "type" : "user-friendly-name"
      },
      {
        "name" : "Topcon NW500",
        "type" : "manufacturer-name"
      }]
    }
  },
  {
    "name" : "fullReport",
    "valueAttachment" : {
      "contentType" : "text/plain",
      "data" : "SGVsbG8sIEZISVIhIFRoaXMgZmlsZSBjb250YWlucyB0aGUgZnVsbCByZXBvcnQgb2YgdGhlIEFpIGFuYWx5c2lzLg==",
      "title" : "Full report"
    }
  },
  {
    "name" : "validation",
    "valueBoolean" : true
  }]
}

```
