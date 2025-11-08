# Retina observation identifier NamingSystem - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina observation identifier NamingSystem**

## NamingSystem: Retina observation identifier NamingSystem 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-observation-id | *Version*:0.1.3 |
| Active as of 2025-10-19 | *Computable Name*:RetinaObservationIdentifierSystem |

 
A naming system for retina observation identifiers used by DIPS integration services. 

### Summary

| | |
| :--- | :--- |
| Defining URL | http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-observation-id |
| Version | 0.1.3 |
| Name | RetinaObservationIdentifierSystem |
| Status | active |
| Definition | A naming system for retina observation identifiers used by DIPS integration services. |
| Publisher | DIPS AS |

### Identifiers

* **Type**: URI
  * **Value**: http://dips.no/fhir/NamingSystem/retina-observation-id
  * **Preferred**: true



## Resource Content

```json
{
  "resourceType" : "NamingSystem",
  "id" : "retina-observation-id",
  "extension" : [
    {
      "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.url",
      "valueUri" : "http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-observation-id"
    },
    {
      "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.version",
      "valueString" : "0.1.3"
    }
  ],
  "name" : "RetinaObservationIdentifierSystem",
  "status" : "active",
  "kind" : "identifier",
  "date" : "2025-10-19T00:00:00Z",
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
  "description" : "A naming system for retina observation identifiers used by DIPS integration services.",
  "uniqueId" : [
    {
      "type" : "uri",
      "value" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
      "preferred" : true
    }
  ]
}

```
