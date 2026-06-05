# Retina Camera Device - RetinaIntegration v0.9.0

## Resource Profile: Retina Camera Device ( Experimental ) 

 
Description of the camera device used for taking retinal images. 

### Overview

This profile constrains the FHIR [Device](https://www.hl7.org/fhir/R4/device.html) resource to represent the retinal camera used to capture fundus images as part of the retinopathy screening workflow.

### Device Names

Two device names are required:

| | | |
| :--- | :--- | :--- |
| `userFriendlyName` | `user-friendly-name` | The name used by clinical staff to identify the camera, e.g. as shown in the EHR worklist. |
| `manufacturerName` | `manufacturer-name` | Concatenation of manufacturer name and model name as received from the AI system (derived from DICOM tags). Used for validation, not displayed to clinical staff. |

### Serial Number

The serial number from the manufacturer that is printed on the device. The serial number (`serialNumber`) is required and must uniquely identify the physical camera unit.

**Usages:**

* Examples for this Profile: [Device/RetinaCameraDevice-Example](Device-RetinaCameraDevice-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/dips.fhir.retinaintegration|current/StructureDefinition/StructureDefinition-retina-camera-device.json)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-retina-camera-device.csv), [Excel](../StructureDefinition-retina-camera-device.xlsx), [Schematron](../StructureDefinition-retina-camera-device.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-camera-device",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-camera-device",
  "version" : "0.9.0",
  "name" : "RetinaCameraDevice",
  "title" : "Retina Camera Device",
  "status" : "draft",
  "experimental" : true,
  "date" : "2026-03-31",
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
  "description" : "Description of the camera device used for taking retinal images.",
  "purpose" : "Description of the camera device used for taking retinal images.",
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
      "id" : "Device.modifierExtension",
      "path" : "Device.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Device.serialNumber",
      "path" : "Device.serialNumber",
      "short" : "Serial number of the physical camera.",
      "definition" : "The unique serial number assigned by the manufacturer to this specific physical unit. Used to distinguish individual devices when multiple cameras of the same model are in use.",
      "min" : 1
    },
    {
      "id" : "Device.deviceName",
      "path" : "Device.deviceName",
      "slicing" : {
        "discriminator" : [{
          "type" : "value",
          "path" : "type"
        }],
        "rules" : "open"
      },
      "min" : 2
    },
    {
      "id" : "Device.deviceName.modifierExtension",
      "path" : "Device.deviceName.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Device.deviceName:userFriendlyName",
      "path" : "Device.deviceName",
      "sliceName" : "userFriendlyName",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Device.deviceName:userFriendlyName.name",
      "path" : "Device.deviceName.name",
      "short" : "Human-readable name of the device as used in clinical context",
      "definition" : "The name by which clinical staff refer to this device, e.g. as displayed in Arena and in worklists."
    },
    {
      "id" : "Device.deviceName:userFriendlyName.type",
      "path" : "Device.deviceName.type",
      "short" : "User-friendly name",
      "patternCode" : "user-friendly-name"
    },
    {
      "id" : "Device.deviceName:manufacturerName",
      "path" : "Device.deviceName",
      "sliceName" : "manufacturerName",
      "min" : 1,
      "max" : "1"
    },
    {
      "id" : "Device.deviceName:manufacturerName.name",
      "path" : "Device.deviceName.name",
      "short" : "Manufacturer's name and manufacturer's model name for the device.",
      "definition" : "The name of the manufacturer and the official model name as defined by the manufacturer. This is a combination of two tags in the DICOM message. The AI system concatenates these values. Used for validation purposes. Not displayed to clinical staff."
    },
    {
      "id" : "Device.deviceName:manufacturerName.type",
      "path" : "Device.deviceName.type",
      "short" : "Manufacturer name and model name",
      "patternCode" : "manufacturer-name"
    }]
  }
}

```
