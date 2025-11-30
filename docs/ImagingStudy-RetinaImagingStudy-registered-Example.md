# RetinaImagingStudy-registered-Example - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **RetinaImagingStudy-registered-Example**

## Example ImagingStudy: RetinaImagingStudy-registered-Example

Profile: [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

**identifier**: `http://sectra.no/identifiers`/MMA94126079

**status**: Registered

**subject**: Identifier: `urn:oid:2.16.578.1.12.4.1.4.1`/01015549145

**procedureCode**: Fundusfotografi



## Resource Content

```json
{
  "resourceType" : "ImagingStudy",
  "id" : "RetinaImagingStudy-registered-Example",
  "meta" : {
    "profile" : [
      "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagingstudy"
    ]
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
}

```
