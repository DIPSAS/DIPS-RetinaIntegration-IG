# RetinaDiagnosticReport-Example - RetinaIntegration v0.8.0

## Example DiagnosticReport: RetinaDiagnosticReport-Example

Language: en

Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

## Fundusfotografi 

| | |
| :--- | :--- |
| Subject | Unable to get Patient Details |
| When For | 2025-09-30 12:00:00+0000 |
| Identifier | [RetinaDiagnosticReportIdentifierSystem](NamingSystem-retina-diagnostic-report-ns.md)/a4ee3f25-405b-4b3a-85ff-f530aedbb5b9 |

**Report Details**

* **Code**: [HbA1c](Observation-RetinaHbA1cObservation-Example.md)
  * **Value**: 63.2
  * **Flags**: Final
  * **When For**: 2025-11-29 10:30:00+0000
* **Code**: [Diabetic macular edema](Observation-RetinaDiabeticMacularEdemaFinding-Example-left.md)(Venstre retina)
  * **Value**: false
  * **Flags**: Final
  * **When For**: 2025-11-30 10:21:00+0000
* **Code**: [Diabetic macular edema](Observation-RetinaDiabeticMacularEdemaFinding-Example-right.md)(Høyre retina)
  * **Value**: true
  * **Flags**: Final
  * **When For**: 2025-11-30 10:21:00+0000
* **Code**: [Diabetic retinopathy](Observation-RetinaDiabeticRetinopathyFinding-Example-left.md)(Venstre retina)
  * **Value**: 3
  * **Flags**: Final
  * **When For**: 2025-11-30 10:21:00+0000
* **Code**: [Diabetic retinopathy](Observation-RetinaDiabeticRetinopathyFinding-Example-right.md)(Høyre retina)
  * **Value**: 4
  * **Flags**: Final
  * **When For**: 2025-11-30 10:21:00+0000
* **Code**: [Computer assisted image analysis for image quality](Observation-RetinaImageQualityAssessment-Example-left.md)(Venstre retina)
  * **Value**: Barely gradable
  * **Flags**: Final
  * **When For**: 2025-11-30 10:21:00+0000
* **Code**: [Computer assisted image analysis for image quality](Observation-RetinaImageQualityAssessment-Example-right.md)(Høyre retina)
  * **Value**: Good
  * **Flags**: Final
  * **When For**: 2025-11-30 10:21:00+0000

**Coded Conclusions:**

* Ny fotokontroll (primærgradering)



## Resource Content

```json
{
  "resourceType" : "DiagnosticReport",
  "id" : "RetinaDiagnosticReport-Example",
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
  },
  {
    "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/days-until-next-examination-extension",
    "valueInteger" : 365
  }],
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/examination-id",
    "value" : "a4ee3f25-405b-4b3a-85ff-f530aedbb5b9"
  }],
  "status" : "final",
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
  "effectiveDateTime" : "2025-09-30T12:00:00Z",
  "result" : [{
    "reference" : "Observation/RetinaHbA1cObservation-Example"
  },
  {
    "reference" : "Observation/RetinaDiabeticMacularEdemaFinding-Example-left"
  },
  {
    "reference" : "Observation/RetinaDiabeticMacularEdemaFinding-Example-right"
  },
  {
    "reference" : "Observation/RetinaDiabeticRetinopathyFinding-Example-left"
  },
  {
    "reference" : "Observation/RetinaDiabeticRetinopathyFinding-Example-right"
  },
  {
    "reference" : "Observation/RetinaImageQualityAssessment-Example-left"
  },
  {
    "reference" : "Observation/RetinaImageQualityAssessment-Example-right"
  }],
  "imagingStudy" : [{
    "reference" : "ImagingStudy/RetinaImagingStudy-available-Example"
  }],
  "conclusionCode" : [{
    "coding" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
      "code" : "1004",
      "display" : "Ny fotokontroll (primærgradering)"
    }]
  }],
  "presentedForm" : [{
    "contentType" : "text/plain",
    "data" : "Base64binary",
    "title" : "Full report"
  }]
}

```
