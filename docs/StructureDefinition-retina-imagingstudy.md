# Retina ImagingStudy - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina ImagingStudy**

## Resource Profile: Retina ImagingStudy ( Experimental ) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagingstudy | *Version*:0.2.0 |
| Draft as of 2025-11-30 | *Computable Name*:RetinaImagingStudy |

 
Profile for imaging studies related to retina examinations, including fundus photography and OCT imaging. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Profile: [ImagingStudy/RetinaImagingStudy-available-Example](ImagingStudy-RetinaImagingStudy-available-Example.md) and [ImagingStudy/RetinaImagingStudy-registered-Example](ImagingStudy-RetinaImagingStudy-registered-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-imagingstudy)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-retina-imagingstudy.csv), [Excel](StructureDefinition-retina-imagingstudy.xlsx), [Schematron](StructureDefinition-retina-imagingstudy.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-imagingstudy",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-imagingstudy",
  "version" : "0.2.0",
  "name" : "RetinaImagingStudy",
  "title" : "Retina ImagingStudy",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-11-30T22:57:21+01:00",
  "publisher" : "DIPS AS",
  "contact" : [
    {
      "name" : "DIPS AS",
      "telecom" : [
        {
          "system" : "url",
          "value" : "http://dips.no/"
        },
        {
          "system" : "email",
          "value" : "teamsolsiden@dips.no"
        }
      ]
    }
  ],
  "description" : "Profile for imaging studies related to retina examinations, including fundus photography and OCT imaging.",
  "fhirVersion" : "4.0.1",
  "mapping" : [
    {
      "identity" : "workflow",
      "uri" : "http://hl7.org/fhir/workflow",
      "name" : "Workflow Pattern"
    },
    {
      "identity" : "rim",
      "uri" : "http://hl7.org/v3",
      "name" : "RIM Mapping"
    },
    {
      "identity" : "dicom",
      "uri" : "http://nema.org/dicom",
      "name" : "DICOM Tag Mapping"
    },
    {
      "identity" : "w5",
      "uri" : "http://hl7.org/fhir/fivews",
      "name" : "FiveWs Pattern Mapping"
    },
    {
      "identity" : "v2",
      "uri" : "http://hl7.org/v2",
      "name" : "HL7 v2 Mapping"
    }
  ],
  "kind" : "resource",
  "abstract" : false,
  "type" : "ImagingStudy",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/ImagingStudy",
  "derivation" : "constraint",
  "differential" : {
    "element" : [
      {
        "id" : "ImagingStudy",
        "path" : "ImagingStudy"
      },
      {
        "id" : "ImagingStudy.implicitRules",
        "path" : "ImagingStudy.implicitRules",
        "max" : "0"
      },
      {
        "id" : "ImagingStudy.modifierExtension",
        "path" : "ImagingStudy.modifierExtension",
        "max" : "0"
      },
      {
        "id" : "ImagingStudy.identifier",
        "path" : "ImagingStudy.identifier",
        "slicing" : {
          "discriminator" : [
            {
              "type" : "value",
              "path" : "system"
            }
          ],
          "rules" : "open"
        },
        "min" : 1,
        "mustSupport" : true
      },
      {
        "id" : "ImagingStudy.identifier:sectraStudyId",
        "path" : "ImagingStudy.identifier",
        "sliceName" : "sectraStudyId",
        "short" : "Sectra Study Identifier.",
        "definition" : "Unique identifier for the imaging study in the Sectra Media Archive system.",
        "min" : 1,
        "max" : "1",
        "mustSupport" : true
      },
      {
        "id" : "ImagingStudy.identifier:sectraStudyId.use",
        "path" : "ImagingStudy.identifier.use",
        "max" : "0"
      },
      {
        "id" : "ImagingStudy.identifier:sectraStudyId.system",
        "path" : "ImagingStudy.identifier.system",
        "min" : 1,
        "patternUri" : "http://sectra.no/identifiers"
      },
      {
        "id" : "ImagingStudy.status",
        "path" : "ImagingStudy.status",
        "short" : "Status of the imaging study: registered | available.",
        "mustSupport" : true
      },
      {
        "id" : "ImagingStudy.subject",
        "path" : "ImagingStudy.subject",
        "short" : "Patient who is the subject of the imaging study.",
        "type" : [
          {
            "code" : "Reference",
            "targetProfile" : ["http://hl7.org/fhir/StructureDefinition/Patient"]
          }
        ]
      },
      {
        "id" : "ImagingStudy.procedureCode",
        "path" : "ImagingStudy.procedureCode",
        "short" : "Type of imaging procedure performed: fundus photography | OCT.",
        "mustSupport" : true,
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-imaging-procedure-vs"
        }
      },
      {
        "id" : "ImagingStudy.series",
        "path" : "ImagingStudy.series",
        "short" : "We don't have any more information about the image series in this version of the API.",
        "max" : "0"
      }
    ]
  }
}

```
