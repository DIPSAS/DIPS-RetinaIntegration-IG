# Retina Image Quality Assessment - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Image Quality Assessment**

## Resource Profile: Retina Image Quality Assessment ( Experimental ) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-quality-asessment | *Version*:0.5.0 |
| Draft as of 2025-12-02 | *Computable Name*:RetinaImageQualityAssessment |

 
The image quality as assesed by AI (2000-series). 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Profile: [Observation/RetinaImageQualityAssessment-Example-left](Observation-RetinaImageQualityAssessment-Example-left.md) and [Observation/RetinaImageQualityAssessment-Example-right](Observation-RetinaImageQualityAssessment-Example-right.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-image-quality-asessment)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-retina-image-quality-asessment.csv), [Excel](StructureDefinition-retina-image-quality-asessment.xlsx), [Schematron](StructureDefinition-retina-image-quality-asessment.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-image-quality-asessment",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-quality-asessment",
  "version" : "0.5.0",
  "name" : "RetinaImageQualityAssessment",
  "title" : "Retina Image Quality Assessment",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-12-02",
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
  "description" : "The image quality as assesed by AI (2000-series).",
  "fhirVersion" : "4.0.1",
  "mapping" : [
    {
      "identity" : "workflow",
      "uri" : "http://hl7.org/fhir/workflow",
      "name" : "Workflow Pattern"
    },
    {
      "identity" : "sct-concept",
      "uri" : "http://snomed.info/conceptdomain",
      "name" : "SNOMED CT Concept Domain Binding"
    },
    {
      "identity" : "v2",
      "uri" : "http://hl7.org/v2",
      "name" : "HL7 v2 Mapping"
    },
    {
      "identity" : "rim",
      "uri" : "http://hl7.org/v3",
      "name" : "RIM Mapping"
    },
    {
      "identity" : "w5",
      "uri" : "http://hl7.org/fhir/fivews",
      "name" : "FiveWs Pattern Mapping"
    },
    {
      "identity" : "sct-attr",
      "uri" : "http://snomed.org/attributebinding",
      "name" : "SNOMED CT Attribute Binding"
    }
  ],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Observation",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Observation",
  "derivation" : "constraint",
  "differential" : {
    "element" : [
      {
        "id" : "Observation",
        "path" : "Observation"
      },
      {
        "id" : "Observation.code",
        "path" : "Observation.code",
        "patternCodeableConcept" : {
          "coding" : [
            {
              "system" : "http://snomed.info/sct",
              "code" : "133887000",
              "display" : "Computer assisted image analysis for image quality"
            }
          ]
        }
      },
      {
        "id" : "Observation.value[x]",
        "path" : "Observation.value[x]",
        "slicing" : {
          "discriminator" : [
            {
              "type" : "type",
              "path" : "$this"
            }
          ],
          "ordered" : false,
          "rules" : "open"
        }
      },
      {
        "id" : "Observation.value[x]:valueCodeableConcept",
        "path" : "Observation.value[x]",
        "sliceName" : "valueCodeableConcept",
        "short" : "Image quality as assessed by AI (2000-series).",
        "definition" : "Quality assessment of the retinal image from the 2000-series codes.",
        "min" : 0,
        "max" : "1",
        "type" : [
          {
            "code" : "CodeableConcept"
          }
        ],
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-quality-vs"
        }
      },
      {
        "id" : "Observation.bodySite",
        "path" : "Observation.bodySite",
        "short" : "Which eye (right or left retina)",
        "definition" : "Identifies whether this observation is for the right eye (SNOMED CT: 5597008) or left eye (SNOMED CT: 58443009).",
        "min" : 1,
        "binding" : {
          "strength" : "required",
          "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-body-site-vs"
        }
      }
    ]
  }
}

```
