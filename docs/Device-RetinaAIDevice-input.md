# RetinaAIDevice-input - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaAIDevice-input**

## Example Device: RetinaAIDevice-input

Profile: [Retina AI Device](StructureDefinition-retina-ai-device.md)

### DeviceNames

| | | |
| :--- | :--- | :--- |
| - | **Name** | **Type** |
| * | AwesomeAI for Retina | Model name |

> **version****type**:model-number**value**: v2.1.0

> **version****type**:software**value**: Standard protocol



## Resource Content

```json
{
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

```
