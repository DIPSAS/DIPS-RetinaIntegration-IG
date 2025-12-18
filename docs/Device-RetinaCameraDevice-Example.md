# RetinaCameraDevice-Example - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaCameraDevice-Example**

## Example Device: RetinaCameraDevice-Example

**identifier**: `http://helse-sorost.no/fhir/NamingSystem/device-ids`/TPNW35634798

### DeviceNames

| | | |
| :--- | :--- | :--- |
| - | **Name** | **Type** |
| * | AK_TOPCON_2 | Model name |

**modelNumber**: NW500



## Resource Content

```json
{
  "resourceType" : "Device",
  "id" : "RetinaCameraDevice-Example",
  "identifier" : [
    {
      "system" : "http://helse-sorost.no/fhir/NamingSystem/device-ids",
      "value" : "TPNW35634798"
    }
  ],
  "deviceName" : [
    {
      "name" : "AK_TOPCON_2",
      "type" : "model-name"
    }
  ],
  "modelNumber" : "NW500"
}

```
