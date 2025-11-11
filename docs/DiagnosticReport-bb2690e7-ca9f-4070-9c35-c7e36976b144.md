# Notification From DIPS - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Notification From DIPS**

## Example DiagnosticReport: Notification From DIPS

Profile: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)

## Bildediagnostikk 

| | |
| :--- | :--- |
| Identifiers | [RetinaExaminationIdentifierSystem](NamingSystem-retina-examination-id.md)/e72b0645-e761-4b50-abf9-1e9e2231273b`http://sectra.no/identifiers`/MMA94126079 |

**Report Details**



## Resource Content

```json
{
  "resourceType" : "DiagnosticReport",
  "id" : "bb2690e7-ca9f-4070-9c35-c7e36976b144",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaDiagnosticReport"
    ]
  },
  "extension" : [
    {
      "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/tiltaksstatus-forrige-undersokelse-extension",
      "valueCodeableConcept" : {
        "coding" : [
          {
            "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/tiltakstatus-nesteundersokelse-cs",
            "code" : "3002",
            "display" : "Ny fotokontroll (sekundærgradering)"
          }
        ]
      }
    }
  ],
  "identifier" : [
    {
      "system" : "http://dips.no/fhir/NamingSystem/retina-examination-id",
      "value" : "e72b0645-e761-4b50-abf9-1e9e2231273b"
    },
    {
      "system" : "http://sectra.no/identifiers",
      "value" : "MMA94126079"
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
