# RetinaDiagnosticReport-Notification-Example - RetinaIntegration v0.7.0

## Example DiagnosticReport: RetinaDiagnosticReport-Notification-Example

Language: en

Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

## Fundusfotografi 

| | |
| :--- | :--- |
| Identifier | [RetinaDiagnosticReportIdentifierSystem](NamingSystem-retina-diagnostic-report-ns.md)/e72b0645-e761-4b50-abf9-1e9e2231273b |

**Report Details**

**Coded Conclusions:**

* KI-gradering (basert på nåværende bilder)



## Resource Content

```json
{
  "resourceType" : "DiagnosticReport",
  "id" : "bb2690e7-ca9f-4070-9c35-c7e36976b144",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report"]
  },
  "language" : "en",
  "extension" : [{
    "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/previous-examination-conclusion-extension",
    "valueCoding" : {
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
      "code" : "1004",
      "display" : "Ny fotokontroll (primærgradering)"
    }
  }],
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/examination-id",
    "value" : "e72b0645-e761-4b50-abf9-1e9e2231273b"
  }],
  "status" : "preliminary",
  "code" : {
    "coding" : [{
      "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
      "code" : "CKDP10",
      "display" : "Fundusfotografi"
    },
    {
      "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
      "code" : "CKFX16",
      "display" : "Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk"
    }]
  },
  "conclusionCode" : [{
    "coding" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
      "code" : "1001",
      "display" : "KI-gradering (basert på nåværende bilder)"
    }]
  }]
}

```
