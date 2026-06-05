# Retina Observation Identifier System - RetinaIntegration v0.9.0

## NamingSystem: Retina Observation Identifier System 

 
A naming system for observation identifiers in RetinaIntegration using GUIDs. 



## Resource Content

```json
{
  "resourceType" : "NamingSystem",
  "id" : "retina-observation-ns",
  "extension" : [{
    "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.url",
    "valueUri" : "http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-observation-ns"
  },
  {
    "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.version",
    "valueString" : "0.9.0"
  }],
  "name" : "RetinaObservationIdentifierSystem",
  "status" : "active",
  "kind" : "identifier",
  "date" : "2025-12-11",
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
  "description" : "A naming system for observation identifiers in RetinaIntegration using GUIDs.",
  "uniqueId" : [{
    "type" : "uri",
    "value" : "http://dips.no/fhir/RetinaIntegration/observation-id",
    "preferred" : true,
    "comment" : "The observation ID will uniquely identify observations. Identifier values are GUIDs in the format: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
  }]
}

```
