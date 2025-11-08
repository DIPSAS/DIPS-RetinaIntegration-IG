# BundleWithSinglExamination-Example - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **BundleWithSinglExamination-Example**

## Example Bundle: BundleWithSinglExamination-Example

Bundle BundleWithSinglExamination-Example of type searchset

-------

Entry 1

Search:Mode = match

Resource DiagnosticReport:

> 

Profile: [DiagnosticReport for Retinascreening](StructureDefinition-RetinaDiagnosticReport.md)

## Bildediagnostikk 

| | |
| :--- | :--- |
| Subject | Pasient Eksempel Female, DoB: 1970-01-01 ( urn:oid:2.16.578.1.12.4.1.4.1#01015549145) |
| Identifiers | [RetinaExaminationIdentifierSystem](NamingSystem-retina-examination-id.md)/6d2f4dbc-5f03-46e0-a302-606ae889df45`http://sectra.no/identifiers`/MMA94126079 |

**Report Details**

* **Code**: [HbA1c](Bundle-BundleWithSinglExamination-Example.md#Observation_ObservationGlukose-1)
  * **Value**: 63.2
  * **Flags**: Final
  * **When For**: 2025-06-06 10:30:00+0000
* **Code**: [Fundusfotografi](Bundle-BundleWithSinglExamination-Example.md#Observation_ObservationPhoto-1)
  * **Value**: true
  * **Flags**: Final
  * **When For**: 
* **Code**: [Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk](Bundle-BundleWithSinglExamination-Example.md#Observation_ObservationOCT-1)
  * **Value**: true
  * **Flags**: Final
  * **When For**: 


-------

Entry 2

Search:Mode = include

Resource Observation:

> 

Profile: [Observation for retina screening](StructureDefinition-RetinaObservation.md)

**identifier**:[RetinaObservationIdentifierSystem](NamingSystem-retina-observation-id.md)/78772631-5e7f-4c2a-8c45-42ada291b1a4**status**: Final**code**:HbA1c**effective**: 2025-06-06 10:30:00+0000**value**: 63.2

-------

Entry 3

Search:Mode = include

Resource Observation:

> 

Profile: [Observation for retina screening](StructureDefinition-RetinaObservation.md)

**identifier**:[RetinaObservationIdentifierSystem](NamingSystem-retina-observation-id.md)/eb8ef81c-d8a5-4656-b44d-2f9b86a16903**status**: Final**code**:Fundusfotografi**value**: true

-------

Entry 4

Search:Mode = include

Resource Observation:

> 

Profile: [Observation for retina screening](StructureDefinition-RetinaObservation.md)

**identifier**:[RetinaObservationIdentifierSystem](NamingSystem-retina-observation-id.md)/96f8e5bb-41be-4dae-bcc3-833b01b050ab**status**: Final**code**:Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk**value**: true



## Resource Content

```json
{
  "resourceType" : "Bundle",
  "id" : "BundleWithSinglExamination-Example",
  "type" : "searchset",
  "total" : 1,
  "entry" : [
    {
      "resource" : {
        "resourceType" : "DiagnosticReport",
        "id" : "DiagnosticReportWithoutAI-1",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaDiagnosticReport"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"DiagnosticReport_DiagnosticReportWithoutAI-1\"> </a><p class=\"res-header-id\"><b>Generated Narrative: DiagnosticReport DiagnosticReportWithoutAI-1</b></p><a name=\"DiagnosticReportWithoutAI-1\"> </a><a name=\"hcDiagnosticReportWithoutAI-1\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-RetinaDiagnosticReport.html\">DiagnosticReport for Retinascreening</a></p></div><h2><span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660 B}\">Bildediagnostikk</span> </h2><table class=\"grid\"><tr><td>Subject</td><td>Pasient Eksempel  Female, DoB: 1970-01-01 ( urn:oid:2.16.578.1.12.4.1.4.1#01015549145)</td></tr><tr><td>Identifiers</td><td> <a href=\"NamingSystem-retina-examination-id.html\" title=\"A naming system for retina examination identifiers used by DIPS integration services.\">RetinaExaminationIdentifierSystem</a>/6d2f4dbc-5f03-46e0-a302-606ae889df45 <code>http://sectra.no/identifiers</code>/MMA94126079</td></tr></table><p><b>Report Details</b></p><table class=\"grid\"><tr><td><b>Code</b></td><td><b>Value</b></td><td><b>Flags</b></td><td><b>When For</b></td></tr><tr><td><a href=\"Bundle-BundleWithSinglExamination-Example.html#Observation_ObservationGlukose-1\"><span title=\"Codes:{http://snomed.info/sct 167491000202108}\">HbA1c</span></a></td><td>63.2</td><td>Final</td><td>2025-06-06 10:30:00+0000</td></tr><tr><td><a href=\"Bundle-BundleWithSinglExamination-Example.html#Observation_ObservationPhoto-1\"><span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275 CKDP10}\">Fundusfotografi</span></a></td><td>true</td><td>Final</td><td/></tr><tr><td><a href=\"Bundle-BundleWithSinglExamination-Example.html#Observation_ObservationOCT-1\"><span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275 CKFX16}\">Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk</span></a></td><td>true</td><td>Final</td><td/></tr></table></div>"
        },
        "extension" : [
          {
            "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/tiltaksstatus-forrige-undersokelse-extension",
            "valueCodeableConcept" : {
              "coding" : [
                {
                  "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/tiltakstatus-nesteundersokelse-cs",
                  "code" : "3003",
                  "display" : "Ingen registrert tidligere undersøkelser"
                }
              ]
            }
          }
        ],
        "identifier" : [
          {
            "system" : "http://dips.no/fhir/NamingSystem/retina-examination-id",
            "value" : "6d2f4dbc-5f03-46e0-a302-606ae889df45"
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
        },
        "subject" : {
          "reference" : "Patient/cdp1123123",
          "identifier" : {
            "system" : "urn:oid:2.16.578.1.12.4.1.4.1",
            "value" : "01015549145"
          }
        },
        "result" : [
          {
            "reference" : "Observation/ObservationGlukose-1"
          },
          {
            "reference" : "Observation/ObservationPhoto-1"
          },
          {
            "reference" : "Observation/ObservationOCT-1"
          }
        ]
      },
      "search" : {
        "mode" : "match"
      }
    },
    {
      "resource" : {
        "resourceType" : "Observation",
        "id" : "ObservationGlukose-1",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaObservation"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"Observation_ObservationGlukose-1\"> </a><p class=\"res-header-id\"><b>Generated Narrative: Observation ObservationGlukose-1</b></p><a name=\"ObservationGlukose-1\"> </a><a name=\"hcObservationGlukose-1\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-RetinaObservation.html\">Observation for retina screening</a></p></div><p><b>identifier</b>: <a href=\"NamingSystem-retina-observation-id.html\" title=\"A naming system for retina observation identifiers used by DIPS integration services.\">RetinaObservationIdentifierSystem</a>/78772631-5e7f-4c2a-8c45-42ada291b1a4</p><p><b>status</b>: Final</p><p><b>code</b>: <span title=\"Codes:{http://snomed.info/sct 167491000202108}\">HbA1c</span></p><p><b>effective</b>: 2025-06-06 10:30:00+0000</p><p><b>value</b>: 63.2</p></div>"
        },
        "identifier" : [
          {
            "system" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
            "value" : "78772631-5e7f-4c2a-8c45-42ada291b1a4"
          }
        ],
        "status" : "final",
        "code" : {
          "coding" : [
            {
              "system" : "http://snomed.info/sct",
              "code" : "167491000202108",
              "display" : "HbA1c"
            }
          ]
        },
        "effectiveDateTime" : "2025-06-06T10:30:00Z",
        "valueQuantity" : {
          "value" : 63.2
        }
      },
      "search" : {
        "mode" : "include"
      }
    },
    {
      "resource" : {
        "resourceType" : "Observation",
        "id" : "ObservationPhoto-1",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaObservation"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"Observation_ObservationPhoto-1\"> </a><p class=\"res-header-id\"><b>Generated Narrative: Observation ObservationPhoto-1</b></p><a name=\"ObservationPhoto-1\"> </a><a name=\"hcObservationPhoto-1\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-RetinaObservation.html\">Observation for retina screening</a></p></div><p><b>identifier</b>: <a href=\"NamingSystem-retina-observation-id.html\" title=\"A naming system for retina observation identifiers used by DIPS integration services.\">RetinaObservationIdentifierSystem</a>/eb8ef81c-d8a5-4656-b44d-2f9b86a16903</p><p><b>status</b>: Final</p><p><b>code</b>: <span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275 CKDP10}\">Fundusfotografi</span></p><p><b>value</b>: true</p></div>"
        },
        "identifier" : [
          {
            "system" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
            "value" : "eb8ef81c-d8a5-4656-b44d-2f9b86a16903"
          }
        ],
        "status" : "final",
        "code" : {
          "coding" : [
            {
              "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
              "code" : "CKDP10",
              "display" : "Fundusfotografi"
            }
          ]
        },
        "valueBoolean" : true
      },
      "search" : {
        "mode" : "include"
      }
    },
    {
      "resource" : {
        "resourceType" : "Observation",
        "id" : "ObservationOCT-1",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaObservation"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"Observation_ObservationOCT-1\"> </a><p class=\"res-header-id\"><b>Generated Narrative: Observation ObservationOCT-1</b></p><a name=\"ObservationOCT-1\"> </a><a name=\"hcObservationOCT-1\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-RetinaObservation.html\">Observation for retina screening</a></p></div><p><b>identifier</b>: <a href=\"NamingSystem-retina-observation-id.html\" title=\"A naming system for retina observation identifiers used by DIPS integration services.\">RetinaObservationIdentifierSystem</a>/96f8e5bb-41be-4dae-bcc3-833b01b050ab</p><p><b>status</b>: Final</p><p><b>code</b>: <span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275 CKFX16}\">Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk</span></p><p><b>value</b>: true</p></div>"
        },
        "identifier" : [
          {
            "system" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
            "value" : "96f8e5bb-41be-4dae-bcc3-833b01b050ab"
          }
        ],
        "status" : "final",
        "code" : {
          "coding" : [
            {
              "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
              "code" : "CKFX16",
              "display" : "Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk"
            }
          ]
        },
        "valueBoolean" : true
      },
      "search" : {
        "mode" : "include"
      }
    }
  ]
}

```
