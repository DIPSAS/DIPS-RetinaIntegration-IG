# RetinaDiagnosticReport-Notification-Example - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaDiagnosticReport-Notification-Example**

## Example DiagnosticReport: RetinaDiagnosticReport-Notification-Example

Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

## Bildediagnostikk 

| | |
| :--- | :--- |
| Identifier | [RetinaExaminationIdentifierSystem](NamingSystem-retina-examination-id.md)/e72b0645-e761-4b50-abf9-1e9e2231273b |

**Report Details**



## Resource Content

```json
{
  "resourceType" : "DiagnosticReport",
  "id" : "bb2690e7-ca9f-4070-9c35-c7e36976b144",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report"
    ]
  },
  "extension" : [
    {
      "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/previous-examination-conclusion-extension",
      "valueCodeableConcept" : {
        "coding" : [
          {
            "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs",
            "code" : "1004",
            "display" : "Ny fotokontroll (primærgradering)"
          }
        ]
      }
    },
    {
      "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/initial-instructions-extension",
      "valueCodeableConcept" : {
        "coding" : [
          {
            "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs",
            "code" : "1001",
            "display" : "KI-gradering (basert på nåværende bilder)"
          }
        ]
      }
    }
  ],
  "identifier" : [
    {
      "system" : "http://dips.no/fhir/NamingSystem/retina-examination-id",
      "value" : "e72b0645-e761-4b50-abf9-1e9e2231273b"
    }
  ],
  "status" : "preliminary",
  "code" : {
    "coding" : [
      {
        "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660",
        "code" : "B",
        "display" : "Bildediagnostikk"
      }
    ]
  }
}

```
