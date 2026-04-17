# RetinaImagingStudy-registered-Example - RetinaIntegration v0.8.0

## Example ImagingStudy: RetinaImagingStudy-registered-Example

Language: en

Profile: [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

**identifier**: [RetinaImagingStudyIdentifierSystem](NamingSystem-retina-imaging-study-ns.md)/MMA94126079

**status**: Registered

**subject**: Identifier: `urn:oid:2.16.578.1.12.4.1.4.1`/01015549145



## Resource Content

```json
{
  "resourceType" : "ImagingStudy",
  "id" : "RetinaImagingStudy-registered-Example",
  "meta" : {
    "profile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagingstudy"]
  },
  "language" : "en",
  "identifier" : [{
    "system" : "http://dips.no/fhir/RetinaIntegration/sectra-image-study-id",
    "value" : "MMA94126079"
  }],
  "status" : "registered",
  "subject" : {
    "identifier" : {
      "system" : "urn:oid:2.16.578.1.12.4.1.4.1",
      "value" : "01015549145"
    }
  }
}

```
