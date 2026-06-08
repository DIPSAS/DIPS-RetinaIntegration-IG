# RetinaAIDevice-Example - RetinaIntegration v0.9.1

## Example Device: RetinaAIDevice-Example

Profile: [Retina AI Device](StructureDefinition-retina-ai-device.md)

### DeviceNames

| | | |
| :--- | :--- | :--- |
| - | **Name** | **Type** |
| * | ACME Retina AI | Model name |

> **version****type**: model-number**value**: v2.1.0

> **version****type**: software**value**: Standard protocol



## Resource Content

```json
{
  "resourceType" : "Device",
  "id" : "RetinaAIDevice-Example",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device"]
  },
  "deviceName" : [{
    "name" : "ACME Retina AI",
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

```
