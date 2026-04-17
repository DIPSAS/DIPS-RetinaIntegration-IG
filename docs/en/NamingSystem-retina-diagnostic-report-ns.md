# Retina DiagnosticReport Identifier System - RetinaIntegration v0.8.0

## NamingSystem: Retina DiagnosticReport Identifier System 

 
A naming system for identifying Retina DiagnosticReports using GUIDs. An examination ID is used to uniquely identify the single Retina DiagnosticReport for that examination. 



## Resource Content

```json
{
  "resourceType" : "NamingSystem",
  "id" : "retina-diagnostic-report-ns",
  "extension" : [{
    "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.url",
    "valueUri" : "http://dips.no/fhir/RetinaIntegration/NamingSystem/retina-diagnostic-report-ns"
  },
  {
    "url" : "http://hl7.org/fhir/5.0/StructureDefinition/extension-NamingSystem.version",
    "valueString" : "0.8.0"
  }],
  "name" : "RetinaDiagnosticReportIdentifierSystem",
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
  "description" : "A naming system for identifying Retina DiagnosticReports using GUIDs. An examination ID is used to uniquely identify the single Retina DiagnosticReport for that examination.",
  "uniqueId" : [{
    "type" : "uri",
    "value" : "http://dips.no/fhir/RetinaIntegration/examination-id",
    "preferred" : true,
    "comment" : "The examination ID will uniquely identify the diagnostic report for an examination. Identifier values are GUIDs in the format: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
  }]
}

```
