# RetinaDiagnosticReport-Example-PendingAI - RetinaIntegration v0.8.0

## Example DiagnosticReport: RetinaDiagnosticReport-Example-PendingAI

Language: en

Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

## Fundusfotografi 

| | |
| :--- | :--- |
| Subject | Unable to get Patient Details |
| Identifier | [RetinaDiagnosticReportIdentifierSystem](NamingSystem-retina-diagnostic-report-ns.md)/6d2f4dbc-5f03-46e0-a302-606ae889df45 |

**Report Details**

* **Code**: [HbA1c](Observation-RetinaHbA1cObservation-Example.md)
  * **Value**: 63.2
  * **Flags**: Final
  * **When For**: 2025-11-29 10:30:00+0000

**Coded Conclusions:**

* KI-gradering (basert på nåværende bilder)



## Resource Content

```json
{
  "resourceType" : "DiagnosticReport",
  "id" : "RetinaDiagnosticReport-Example-PendingAI",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report"]
  },
  "language" : "en",
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/examination-id",
    "value" : "6d2f4dbc-5f03-46e0-a302-606ae889df45"
  }],
  "status" : "preliminary",
  "code" : {
    "coding" : [{
      "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
      "code" : "CKDP10",
      "display" : "Fundusfotografi"
    }]
  },
  "subject" : {
    "identifier" : {
      "system" : "urn:oid:2.16.578.1.12.4.1.4.1",
      "value" : "01015549145"
    }
  },
  "result" : [{
    "reference" : "Observation/RetinaHbA1cObservation-Example"
  }],
  "imagingStudy" : [{
    "reference" : "ImagingStudy/RetinaImagingStudy-registered-Example"
  }],
  "conclusionCode" : [{
    "coding" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
      "code" : "1001",
      "display" : "KI-gradering (basert på nåværende bilder)"
    }]
  }]
}

```
