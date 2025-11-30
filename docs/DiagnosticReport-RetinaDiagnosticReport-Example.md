# RetinaDiagnosticReport-Example - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaDiagnosticReport-Example**

## Example DiagnosticReport: RetinaDiagnosticReport-Example

Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

## Bildediagnostikk 

| | |
| :--- | :--- |
| Subject | Unable to get Patient Details |
| When For | 2025-09-30 12:00:00+0000 |
| Identifier | [RetinaExaminationIdentifierSystem](NamingSystem-retina-examination-id.md)/a4ee3f25-405b-4b3a-85ff-f530aedbb5b9 |

**Report Details**

* **Code**: [HbA1c](Observation-RetinaHbA1cObservation-Example.md)
  * **Value**: 63.2
  * **Flags**: Final
  * **When For**: 2025-11-29 10:30:00+0000
* **Code**: [Retinal examination](Observation-RetinaEyeObservation-Example-right.md)(Høyre retina)
  * **Value**: 
  * **Flags**: Final
  * **When For**: 2025-11-30 10:21:00+0000
* **Code**: [Retinal examination](Observation-RetinaEyeObservation-Example-left.md)(Venstre retina)
  * **Value**: 
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
    },
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
      "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/days-until-next-examination-extension",
      "valueInteger" : 365
    }
  ],
  "identifier" : [
    {
      "system" : "http://dips.no/fhir/NamingSystem/retina-examination-id",
      "value" : "a4ee3f25-405b-4b3a-85ff-f530aedbb5b9"
    }
  ],
  "status" : "final",
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
  "effectiveDateTime" : "2025-09-30T12:00:00Z",
  "result" : [
    {
      "reference" : "Observation/RetinaHbA1cObservation-Example"
    },
    {
      "reference" : "Observation/RetinaEyeObservation-Example-right"
    },
    {
      "reference" : "Observation/RetinaEyeObservation-Example-left"
    }
  ],
  "imagingStudy" : [
    {
      "reference" : "ImagingStudy/RetinaImagingStudy-available-Example"
    }
  ],
  "conclusionCode" : [
    {
      "coding" : [
        {
          "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs",
          "code" : "1004",
          "display" : "Ny fotokontroll (primærgradering)"
        }
      ]
    }
  ],
  "presentedForm" : [
    {
      "contentType" : "text/plain",
      "data" : "Base64binary",
      "title" : "Full report"
    }
  ]
}

```
