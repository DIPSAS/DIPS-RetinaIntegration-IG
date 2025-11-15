# HbA1c Observation - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **HbA1c Observation**

## Resource Profile: HbA1c Observation 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/hba1c-observation | *Version*:0.1.3 |
| Draft as of 2025-11-15 | *Computable Name*:HbA1cObservation |

 
HbA1c level as reported by patient prior to retina examination. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/hba1c-observation)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-hba1c-observation.csv), [Excel](StructureDefinition-hba1c-observation.xlsx), [Schematron](StructureDefinition-hba1c-observation.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "hba1c-observation",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/hba1c-observation",
  "version" : "0.1.3",
  "name" : "HbA1cObservation",
  "title" : "HbA1c Observation",
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
  "description" : "HbA1c level as reported by patient prior to retina examination.",
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
              "code" : "167491000202108"
            }
          ]
        }
      }
    ]
  }
}

```
