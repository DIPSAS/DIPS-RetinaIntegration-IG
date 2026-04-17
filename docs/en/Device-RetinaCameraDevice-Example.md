# RetinaCameraDevice-Example - RetinaIntegration v0.8.0

## Example Device: RetinaCameraDevice-Example

Language: en

Profile: [Retina Camera Device](StructureDefinition-retina-camera-device.md)

**serialNumber**: SN123456789

> **deviceName****name**: AAK_TOPCON2**type**: User Friendly name

> **deviceName****name**: Topcon NW500**type**: Manufacturer name



## Resource Content

```json
{
  "resourceType" : "Device",
  "id" : "RetinaCameraDevice-Example",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-camera-device"]
  },
  "language" : "en",
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

```
