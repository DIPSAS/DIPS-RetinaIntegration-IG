# Retina examination identifier NamingSystem - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina examination identifier NamingSystem**

## NamingSystem: Retina examination identifier NamingSystem 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-examination-id | *Version*:0.1.3 |
| Active as of 2025-10-19 | *Computable Name*:RetinaExaminationIdentifierSystem |

 
A naming system for retina examination identifiers used by DIPS integration services. 

### Summary

| | |
| :--- | :--- |
| Defining URL | http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-examination-id |
| Version | 0.1.3 |
| Name | RetinaExaminationIdentifierSystem |
| Status | active |
| Definition | A naming system for retina examination identifiers used by DIPS integration services. |
| Publisher | DIPS AS |

### Identifiers

* **Type**: URI
  * **Value**: http://dips.no/fhir/NamingSystem/retina-examination-id
  * **Preferred**: true



## Resource Content

```json
{
  "resourceType" : "NamingSystem",
  "id" : "retina-examination-id",
  "extension" : [
    {
      "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.url",
      "valueUri" : "http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-examination-id"
    },
    {
      "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.version",
      "valueString" : "0.1.3"
    }
  ],
  "name" : "RetinaExaminationIdentifierSystem",
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
  "description" : "A naming system for retina examination identifiers used by DIPS integration services.",
  "uniqueId" : [
    {
      "type" : "uri",
      "value" : "http://dips.no/fhir/NamingSystem/retina-examination-id",
      "preferred" : true
    }
  ]
}

```
