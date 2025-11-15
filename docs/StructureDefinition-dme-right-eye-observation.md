# Diabetic Macular Edema Right Eye Observation - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Diabetic Macular Edema Right Eye Observation**

## Resource Profile: Diabetic Macular Edema Right Eye Observation 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/dme-right-eye-observation | *Version*:0.1.3 |
| Draft as of 2025-11-15 | *Computable Name*:DMERightEyeObservation |

 
Observation for diabetic macular edema findings in the right eye. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/dme-right-eye-observation)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-dme-right-eye-observation.csv), [Excel](StructureDefinition-dme-right-eye-observation.xlsx), [Schematron](StructureDefinition-dme-right-eye-observation.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "dme-right-eye-observation",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/dme-right-eye-observation",
  "version" : "0.1.3",
  "name" : "DMERightEyeObservation",
  "title" : "Diabetic Macular Edema Right Eye Observation",
  "status" : "draft",
  "date" : "2025-11-15T17:14:08+01:00",
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
  "description" : "Observation for diabetic macular edema findings in the right eye.",
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
  "baseDefinition" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaObservation",
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
              "code" : "312912001"
            }
          ]
        }
      },
      {
        "id" : "Observation.bodySite",
        "path" : "Observation.bodySite",
        "patternCodeableConcept" : {
          "coding" : [
            {
              "system" : "http://snomed.info/sct",
              "code" : "5597008",
              "display" : "Retina of right eye"
            }
          ]
        }
      }
    ]
  }
}

```
