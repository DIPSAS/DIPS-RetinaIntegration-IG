# OCT Observation - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **OCT Observation**

## Resource Profile: OCT Observation 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/oct-observation | *Version*:0.1.3 |
| Draft as of 2025-11-11 | *Computable Name*:OCTObservation |

 
Wether Optical Coherence Tomography (OCT) was performed or not. Will be true if OCT was performed. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/oct-observation)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-oct-observation.csv), [Excel](StructureDefinition-oct-observation.xlsx), [Schematron](StructureDefinition-oct-observation.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "oct-observation",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/oct-observation",
  "version" : "0.1.3",
  "name" : "OCTObservation",
  "title" : "OCT Observation",
  "status" : "draft",
  "date" : "2025-11-11T17:38:50+01:00",
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
  "description" : "Wether Optical Coherence Tomography (OCT) was performed or not. Will be true if OCT was performed.",
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
              "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
              "code" : "CKFX16"
            }
          ]
        }
      }
    ]
  }
}

```
