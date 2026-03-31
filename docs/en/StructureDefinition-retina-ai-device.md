# Retina AI Device - RetinaIntegration v0.7.0

## Resource Profile: Retina AI Device 

 
AI device/software system used for automated retina screening analysis. 

**Usages:**

* Examples for this Profile: [Device/RetinaAIDevice-Example](Device-RetinaAIDevice-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-ai-device)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-retina-ai-device.csv), [Excel](../StructureDefinition-retina-ai-device.xlsx), [Schematron](../StructureDefinition-retina-ai-device.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-ai-device",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device",
  "version" : "0.7.0",
  "name" : "RetinaAIDevice",
  "title" : "Retina AI Device",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-02",
  "publisher" : "DIPS AS",
  "contact" : [{
    "name" : "DIPS AS",
    "telecom" : [{
      "system" : "url",
      "value" : "http://dips.no/"
    },
    {
      "system" : "email",
      "value" : "teamsolsiden@dips.no"
    }]
  }],
  "description" : "AI device/software system used for automated retina screening analysis.",
  "purpose" : "The AI system that performs grading of the images.",
  "fhirVersion" : "4.0.1",
  "mapping" : [{
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
    "identity" : "udi",
    "uri" : "http://fda.gov/UDI",
    "name" : "UDI Mapping"
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Device",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Device",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Device",
      "path" : "Device"
    },
    {
      "id" : "Device.implicitRules",
      "path" : "Device.implicitRules",
      "max" : "0"
    },
    {
      "id" : "Device.modifierExtension",
      "path" : "Device.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Device.status",
      "path" : "Device.status",
      "max" : "0"
    },
    {
      "id" : "Device.deviceName",
      "path" : "Device.deviceName",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Device.deviceName.modifierExtension",
      "path" : "Device.deviceName.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Device.deviceName.name",
      "path" : "Device.deviceName.name",
      "short" : "AI Product Name",
      "definition" : "The commercial or product name of the AI system (e.g., 'AwesomeAI for Retina')."
    },
    {
      "id" : "Device.deviceName.type",
      "path" : "Device.deviceName.type",
      "short" : "Device Name Type: model-name",
      "patternCode" : "model-name"
    },
    {
      "id" : "Device.version",
      "path" : "Device.version",
      "slicing" : {
        "discriminator" : [{
          "type" : "value",
          "path" : "type"
        }],
        "rules" : "open"
      },
      "min" : 1
    },
    {
      "id" : "Device.version.modifierExtension",
      "path" : "Device.version.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Device.version:algorithmVersion",
      "path" : "Device.version",
      "sliceName" : "algorithmVersion",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Device.version:algorithmVersion.modifierExtension",
      "path" : "Device.version.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Device.version:algorithmVersion.type",
      "path" : "Device.version.type",
      "min" : 1,
      "patternCodeableConcept" : {
        "coding" : [{
          "code" : "model-number"
        }]
      }
    },
    {
      "id" : "Device.version:algorithmVersion.type.id",
      "path" : "Device.version.type.id",
      "max" : "0"
    },
    {
      "id" : "Device.version:algorithmVersion.type.extension",
      "path" : "Device.version.type.extension",
      "max" : "0"
    },
    {
      "id" : "Device.version:algorithmVersion.type.text",
      "path" : "Device.version.type.text",
      "max" : "0"
    },
    {
      "id" : "Device.version:algorithmVersion.value",
      "path" : "Device.version.value",
      "short" : "Algorithm Version",
      "definition" : "The version identifier of the AI algorithm used for analysis (e.g., 'v2.1.0')."
    },
    {
      "id" : "Device.version:protocol",
      "path" : "Device.version",
      "sliceName" : "protocol",
      "min" : 0,
      "max" : "1"
    },
    {
      "id" : "Device.version:protocol.modifierExtension",
      "path" : "Device.version.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Device.version:protocol.type",
      "path" : "Device.version.type",
      "short" : "Protocol Type: software",
      "min" : 1,
      "patternCodeableConcept" : {
        "coding" : [{
          "code" : "software"
        }]
      }
    },
    {
      "id" : "Device.version:protocol.type.id",
      "path" : "Device.version.type.id",
      "max" : "0"
    },
    {
      "id" : "Device.version:protocol.type.extension",
      "path" : "Device.version.type.extension",
      "max" : "0"
    },
    {
      "id" : "Device.version:protocol.type.text",
      "path" : "Device.version.type.text",
      "max" : "0"
    },
    {
      "id" : "Device.version:protocol.value",
      "path" : "Device.version.value",
      "short" : "AI Protocol",
      "definition" : "The analysis protocol used by the AI algorithm for this examination (e.g., 'Standard protocol')."
    }]
  }
}

```
