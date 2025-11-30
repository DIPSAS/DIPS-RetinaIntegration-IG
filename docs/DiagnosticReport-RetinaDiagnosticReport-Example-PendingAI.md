# RetinaDiagnosticReport-Example-PendingAI - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaDiagnosticReport-Example-PendingAI**

## Example DiagnosticReport: RetinaDiagnosticReport-Example-PendingAI

Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

## Bildediagnostikk 

| | |
| :--- | :--- |
| Subject | Unable to get Patient Details |
| Identifier | [RetinaExaminationIdentifierSystem](NamingSystem-retina-examination-id.md)/6d2f4dbc-5f03-46e0-a302-606ae889df45 |

**Report Details**

* **Code**: [HbA1c](Observation-RetinaHbA1cObservation-Example.md)
  * **Value**: 63.2
  * **Flags**: Final
  * **When For**: 2025-11-29 10:30:00+0000



## Resource Content

```json
{
  "resourceType" : "DiagnosticReport",
  "id" : "RetinaDiagnosticReport-Example-PendingAI",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report"
    ]
  },
  "extension" : [
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
      "value" : "6d2f4dbc-5f03-46e0-a302-606ae889df45"
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
  },
  "subject" : {
    "identifier" : {
      "system" : "urn:oid:2.16.578.1.12.4.1.4.1",
      "value" : "01015549145"
    }
  },
  "result" : [
    {
      "reference" : "Observation/RetinaHbA1cObservation-Example"
    }
  ],
  "imagingStudy" : [
    {
      "reference" : "ImagingStudy/RetinaImagingStudy-registered-Example"
    }
  ]
}

```
