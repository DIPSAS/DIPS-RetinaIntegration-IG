# Bundle-TwoExaminations-Example - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Bundle-TwoExaminations-Example**

## Example Bundle: Bundle-TwoExaminations-Example

Bundle Bundle-TwoExaminations-Example of type searchset

-------

Entry 1

Search:Mode = match

Resource DiagnosticReport:

> 

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


-------

Entry 2

Search:Mode = include

Resource Observation:

> 

Profile: [Retina HbA1c Observation](StructureDefinition-retina-hba1c-observation.md)

**identifier**:[RetinaObservationIdentifierSystem](NamingSystem-retina-observation-id.md)/a7f3e821-9c4d-4f2a-b5e6-8d3c7a1f9b42**status**: Final**code**:HbA1c**effective**: 2025-11-29 10:30:00+0000**value**: 63.2

-------

Entry 3

Search:Mode = include

Resource ImagingStudy:

> 

Profile: [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

**identifier**:`http://sectra.no/identifiers`/MMA94126079**status**: Registered**subject**: Identifier:`urn:oid:2.16.578.1.12.4.1.4.1`/01015549145

-------

Entry 4

Search:Mode = match

Resource DiagnosticReport:

> 

Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

## Bildediagnostikk 

| | |
| :--- | :--- |
| Subject | Unable to get Patient Details |
| Identifier | [RetinaExaminationIdentifierSystem](NamingSystem-retina-examination-id.md)/9bee5eee-b15d-46b5-913e-d163833d7acd |

**Report Details**

* **Code**: [HbA1c](Bundle-Bundle-TwoExaminations-Example.md#Observation_RetinaHbA1cObservation-2)
  * **Value**: 63.2
  * **Flags**: Final
  * **When For**: 2025-06-06 10:30:00+0000


-------

Entry 5

Search:Mode = include

Resource Observation:

> 

Profile: [Retina HbA1c Observation](StructureDefinition-retina-hba1c-observation.md)

**identifier**:[RetinaObservationIdentifierSystem](NamingSystem-retina-observation-id.md)/718af0c2-794c-4bb0-96f9-365af89b0c08**status**: Final**code**:HbA1c**effective**: 2025-06-06 10:30:00+0000**value**: 63.2

-------

Entry 6

Search:Mode = include

Resource ImagingStudy:

> 

Profile: [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

**identifier**:`http://sectra.no/identifiers`/MMA94126081**status**: Registered**subject**: Identifier:`urn:oid:2.16.578.1.12.4.1.4.1`/01015549144



## Resource Content

```json
{
  "resourceType" : "Bundle",
  "id" : "Bundle-TwoExaminations-Example",
  "type" : "searchset",
  "total" : 3,
  "entry" : [
    {
      "resource" : {
        "resourceType" : "DiagnosticReport",
        "id" : "RetinaDiagnosticReport-Example-PendingAI",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"DiagnosticReport_RetinaDiagnosticReport-Example-PendingAI\"> </a><p class=\"res-header-id\"><b>Generated Narrative: DiagnosticReport RetinaDiagnosticReport-Example-PendingAI</b></p><a name=\"RetinaDiagnosticReport-Example-PendingAI\"> </a><a name=\"hcRetinaDiagnosticReport-Example-PendingAI\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-retina-diagnostic-report.html\">Retina DiagnosticReport</a></p></div><h2><span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660 B}\">Bildediagnostikk</span> </h2><table class=\"grid\"><tr><td>Subject</td><td>Unable to get Patient Details</td></tr><tr><td>Identifier</td><td> <a href=\"NamingSystem-retina-examination-id.html\" title=\"A naming system for examination identifiers in RetinaIntegration.\">RetinaExaminationIdentifierSystem</a>/6d2f4dbc-5f03-46e0-a302-606ae889df45</td></tr></table><p><b>Report Details</b></p><table class=\"grid\"><tr><td><b>Code</b></td><td><b>Value</b></td><td><b>Flags</b></td><td><b>When For</b></td></tr><tr><td><a href=\"Observation-RetinaHbA1cObservation-Example.html\"><span title=\"Codes:{http://snomed.info/sct 167491000202108}\">HbA1c</span></a></td><td>63.2</td><td>Final</td><td>2025-11-29 10:30:00+0000</td></tr></table></div>"
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
      },
      "search" : {
        "mode" : "match"
      }
    },
    {
      "resource" : {
        "resourceType" : "Observation",
        "id" : "RetinaHbA1cObservation-Example",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-hba1c-observation"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"Observation_RetinaHbA1cObservation-Example\"> </a><p class=\"res-header-id\"><b>Generated Narrative: Observation RetinaHbA1cObservation-Example</b></p><a name=\"RetinaHbA1cObservation-Example\"> </a><a name=\"hcRetinaHbA1cObservation-Example\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-retina-hba1c-observation.html\">Retina HbA1c Observation</a></p></div><p><b>identifier</b>: <a href=\"NamingSystem-retina-observation-id.html\" title=\"A naming system for observation identifiers in RetinaIntegration.\">RetinaObservationIdentifierSystem</a>/a7f3e821-9c4d-4f2a-b5e6-8d3c7a1f9b42</p><p><b>status</b>: Final</p><p><b>code</b>: <span title=\"Codes:{http://snomed.info/sct 167491000202108}\">HbA1c</span></p><p><b>effective</b>: 2025-11-29 10:30:00+0000</p><p><b>value</b>: 63.2</p></div>"
        },
        "identifier" : [
          {
            "system" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
            "value" : "a7f3e821-9c4d-4f2a-b5e6-8d3c7a1f9b42"
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
        "effectiveDateTime" : "2025-11-29T10:30:00Z",
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
        "resourceType" : "ImagingStudy",
        "id" : "RetinaImagingStudy-registered-Example",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagingstudy"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"ImagingStudy_RetinaImagingStudy-registered-Example\"> </a><p class=\"res-header-id\"><b>Generated Narrative: ImagingStudy RetinaImagingStudy-registered-Example</b></p><a name=\"RetinaImagingStudy-registered-Example\"> </a><a name=\"hcRetinaImagingStudy-registered-Example\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-retina-imagingstudy.html\">Retina ImagingStudy</a></p></div><p><b>identifier</b>: <code>http://sectra.no/identifiers</code>/MMA94126079</p><p><b>status</b>: Registered</p><p><b>subject</b>: Identifier: <code>urn:oid:2.16.578.1.12.4.1.4.1</code>/01015549145</p><p><b>procedureCode</b>: <span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275 CKDP10}\">Fundusfotografi</span></p></div>"
        },
        "identifier" : [
          {
            "system" : "http://sectra.no/identifiers",
            "value" : "MMA94126079"
          }
        ],
        "status" : "registered",
        "subject" : {
          "identifier" : {
            "system" : "urn:oid:2.16.578.1.12.4.1.4.1",
            "value" : "01015549145"
          }
        },
        "procedureCode" : [
          {
            "coding" : [
              {
                "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
                "code" : "CKDP10",
                "display" : "Fundusfotografi"
              }
            ]
          }
        ]
      },
      "search" : {
        "mode" : "include"
      }
    },
    {
      "resource" : {
        "resourceType" : "DiagnosticReport",
        "id" : "RetinaDiagnosticReport-2",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diagnostic-report"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"DiagnosticReport_RetinaDiagnosticReport-2\"> </a><p class=\"res-header-id\"><b>Generated Narrative: DiagnosticReport RetinaDiagnosticReport-2</b></p><a name=\"RetinaDiagnosticReport-2\"> </a><a name=\"hcRetinaDiagnosticReport-2\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-retina-diagnostic-report.html\">Retina DiagnosticReport</a></p></div><h2><span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-8660 B}\">Bildediagnostikk</span> </h2><table class=\"grid\"><tr><td>Subject</td><td>Unable to get Patient Details</td></tr><tr><td>Identifier</td><td> <a href=\"NamingSystem-retina-examination-id.html\" title=\"A naming system for examination identifiers in RetinaIntegration.\">RetinaExaminationIdentifierSystem</a>/9bee5eee-b15d-46b5-913e-d163833d7acd</td></tr></table><p><b>Report Details</b></p><table class=\"grid\"><tr><td><b>Code</b></td><td><b>Value</b></td><td><b>Flags</b></td><td><b>When For</b></td></tr><tr><td><a href=\"Bundle-Bundle-TwoExaminations-Example.html#Observation_RetinaHbA1cObservation-2\"><span title=\"Codes:{http://snomed.info/sct 167491000202108}\">HbA1c</span></a></td><td>63.2</td><td>Final</td><td>2025-06-06 10:30:00+0000</td></tr></table></div>"
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
                  "code" : "1002",
                  "display" : "Primærgradering (basert på nåværende bilder)"
                }
              ]
            }
          },
          {
            "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/initial-instructions-extension",
            "valueCodeableConcept" : {
              "coding" : [
                {
                  "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-caution-cs",
                  "code" : "5001",
                  "display" : "Ønsker ikke KI-svar"
                }
              ]
            }
          }
        ],
        "identifier" : [
          {
            "system" : "http://dips.no/fhir/NamingSystem/retina-examination-id",
            "value" : "9bee5eee-b15d-46b5-913e-d163833d7acd"
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
            "value" : "01015549144"
          }
        },
        "result" : [
          {
            "reference" : "Observation/RetinaHbA1cObservation-2"
          }
        ],
        "imagingStudy" : [
          {
            "reference" : "ImagingStudy/RetinaImagingStudy-2"
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
        "id" : "RetinaHbA1cObservation-2",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-hba1c-observation"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"Observation_RetinaHbA1cObservation-2\"> </a><p class=\"res-header-id\"><b>Generated Narrative: Observation RetinaHbA1cObservation-2</b></p><a name=\"RetinaHbA1cObservation-2\"> </a><a name=\"hcRetinaHbA1cObservation-2\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-retina-hba1c-observation.html\">Retina HbA1c Observation</a></p></div><p><b>identifier</b>: <a href=\"NamingSystem-retina-observation-id.html\" title=\"A naming system for observation identifiers in RetinaIntegration.\">RetinaObservationIdentifierSystem</a>/718af0c2-794c-4bb0-96f9-365af89b0c08</p><p><b>status</b>: Final</p><p><b>code</b>: <span title=\"Codes:{http://snomed.info/sct 167491000202108}\">HbA1c</span></p><p><b>effective</b>: 2025-06-06 10:30:00+0000</p><p><b>value</b>: 63.2</p></div>"
        },
        "identifier" : [
          {
            "system" : "http://dips.no/fhir/NamingSystem/retina-observation-id",
            "value" : "718af0c2-794c-4bb0-96f9-365af89b0c08"
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
        "resourceType" : "ImagingStudy",
        "id" : "RetinaImagingStudy-2",
        "meta" : {
          "profile" : [
            "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagingstudy"
          ]
        },
        "text" : {
          "status" : "generated",
          "div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\"><a name=\"ImagingStudy_RetinaImagingStudy-2\"> </a><p class=\"res-header-id\"><b>Generated Narrative: ImagingStudy RetinaImagingStudy-2</b></p><a name=\"RetinaImagingStudy-2\"> </a><a name=\"hcRetinaImagingStudy-2\"> </a><div style=\"display: inline-block; background-color: #d9e0e7; padding: 6px; margin: 4px; border: 1px solid #8da1b4; border-radius: 5px; line-height: 60%\"><p style=\"margin-bottom: 0px\"/><p style=\"margin-bottom: 0px\">Profile: <a href=\"StructureDefinition-retina-imagingstudy.html\">Retina ImagingStudy</a></p></div><p><b>identifier</b>: <code>http://sectra.no/identifiers</code>/MMA94126081</p><p><b>status</b>: Registered</p><p><b>subject</b>: Identifier: <code>urn:oid:2.16.578.1.12.4.1.4.1</code>/01015549144</p><p><b>procedureCode</b>: <span title=\"Codes:{http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275 CKDP10}\">Fundusfotografi</span></p></div>"
        },
        "identifier" : [
          {
            "system" : "http://sectra.no/identifiers",
            "value" : "MMA94126081"
          }
        ],
        "status" : "registered",
        "subject" : {
          "identifier" : {
            "system" : "urn:oid:2.16.578.1.12.4.1.4.1",
            "value" : "01015549144"
          }
        },
        "procedureCode" : [
          {
            "coding" : [
              {
                "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
                "code" : "CKDP10",
                "display" : "Fundusfotografi"
              }
            ]
          }
        ]
      },
      "search" : {
        "mode" : "include"
      }
    }
  ]
}

```
