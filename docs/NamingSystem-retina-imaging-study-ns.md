# Retina ImagingStudy Identifier System - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina ImagingStudy Identifier System**

## NamingSystem: Retina ImagingStudy Identifier System 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-imaging-study-ns | *Version*:0.5.0 |
| Active as of 2025-12-17 | *Computable Name*:RetinaImagingStudyIdentifierSystem |

 
A naming system for imaging study identifiers in RetinaIntegration using GUIDs for internally and external Sectra image studies. 



## Resource Content

```json
{
  "resourceType" : "NamingSystem",
  "id" : "retina-imaging-study-ns",
  "extension" : [
    {
      "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.url",
      "valueUri" : "http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-imaging-study-ns"
    },
    {
      "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.version",
      "valueString" : "0.5.0"
    }
  ],
  "name" : "RetinaImagingStudyIdentifierSystem",
  "status" : "active",
  "kind" : "identifier",
  "date" : "2025-12-17",
  "publisher" : "DIPS AS",
  "contact" : [
    {
      "name" : "DIPS AS",
      "telecom" : [
        {
          "system" : "url",
          "value" : "http://dips.no/"
        },
        {
          "system" : "email",
          "value" : "teamsolsiden@dips.no"
        }
      ]
    }
  ],
  "description" : "A naming system for imaging study identifiers in RetinaIntegration using GUIDs for internally and external Sectra image studies.",
  "uniqueId" : [
    {
      "type" : "uri",
      "value" : "http://dips.no/fhir/RetinaIntegration/imaging-study-id",
      "preferred" : true,
      "comment" : "The imaging study ID will uniquely identify imaging studies. Identifier values are GUIDs in the format: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
    },
    {
      "type" : "uri",
      "value" : "http://dips.no/fhir/RetinaIntegration/sectra-image-study-id",
      "preferred" : false,
      "comment" : "Sectra image study id. This is an identifier assigned by Sectra, e.g., `MMA94126079`"
    }
  ]
}

```
