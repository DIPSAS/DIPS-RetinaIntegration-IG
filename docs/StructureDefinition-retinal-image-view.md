# Retinal Image View - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retinal Image View**

## Extension: Retinal Image View 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/retinal-image-view | *Version*:0.6.0 |
| Draft as of 2026-02-03 | *Computable Name*:RetinalImageView |

The centering or anatomical focus of a retinal image.

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retinal-image-view)

### Formal Views of Extension Content

 [Description of Profiles, Differentials, Snapshots, and how the XML and JSON presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-retinal-image-view.csv), [Excel](StructureDefinition-retinal-image-view.xlsx), [Schematron](StructureDefinition-retinal-image-view.sch) 

#### Terminology Bindings

#### Constraints



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retinal-image-view",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retinal-image-view",
  "version" : "0.6.0",
  "name" : "RetinalImageView",
  "title" : "Retinal Image View",
  "status" : "draft",
  "date" : "2026-02-03T09:57:13+01:00",
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
  "description" : "The centering or anatomical focus of a retinal image.",
  "fhirVersion" : "4.0.1",
  "mapping" : [
    {
      "identity" : "rim",
      "uri" : "http://hl7.org/v3",
      "name" : "RIM Mapping"
    }
  ],
  "kind" : "complex-type",
  "abstract" : false,
  "context" : [
    {
      "type" : "element",
      "expression" : "ImagingStudy.series.instance"
    }
  ],
  "type" : "Extension",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Extension",
  "derivation" : "constraint",
  "differential" : {
    "element" : [
      {
        "id" : "Extension",
        "path" : "Extension",
        "short" : "Retinal Image View",
        "definition" : "The centering or anatomical focus of a retinal image."
      },
      {
        "id" : "Extension.extension",
        "path" : "Extension.extension",
        "max" : "0"
      },
      {
        "id" : "Extension.url",
        "path" : "Extension.url",
        "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retinal-image-view"
      },
      {
        "id" : "Extension.value[x]",
        "path" : "Extension.value[x]",
        "type" : [
          {
            "code" : "CodeableConcept"
          }
        ],
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-view-vs"
        }
      }
    ]
  }
}

```
