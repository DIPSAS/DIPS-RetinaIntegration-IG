# Retina Observation Id - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Observation Id**

## NamingSystem: Retina Observation Id 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-observation-id | *Version*:0.2.0 |
| Active as of 2025-10-19 | *Computable Name*:RetinaObservationIdentifierSystem |

 
A naming system for observation identifiers in RetinaIntegration. 

### Summary

| | |
| :--- | :--- |
| Defining URL | http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-observation-id |
| Version | 0.2.0 |
| Name | RetinaObservationIdentifierSystem |
| Status | active |
| Definition | A naming system for observation identifiers in RetinaIntegration. |
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
      "valueString" : "0.2.0"
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
  "description" : "A naming system for observation identifiers in RetinaIntegration.",
  "uniqueId" : [
    {
      "type" : "uri",
      "value" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
      "preferred" : true
    }
  ]
}

```
