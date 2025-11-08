# Observation for retina screening - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Observation for retina screening**

## Resource Profile: Observation for retina screening 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaObservation | *Version*:0.1.3 |
| Draft as of 2025-11-08 | *Computable Name*:DIPSRetinaIntegrationObservation |

 
This is observations connected to RetinaDiagnosticReport 

**Usages:**

* Derived from this Profile: [Diabetic Macular Edema Left Eye Observation](StructureDefinition-dme-left-eye-observation.md), [Diabetic Macular Edema Right Eye Observation](StructureDefinition-dme-right-eye-observation.md), [Diabetic Retinopathy Left Eye Observation](StructureDefinition-dr-left-eye-observation.md), [Diabetic Retinopathy Right Eye Observation](StructureDefinition-dr-right-eye-observation.md)...Show 3 more,[FundusFotografiObservation](StructureDefinition-fundus-foto-observation.md),[HbA1cObservation](StructureDefinition-hba1c-observation.md)and[OCTObservation](StructureDefinition-oct-observation.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/RetinaObservation)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-RetinaObservation.csv), [Excel](StructureDefinition-RetinaObservation.xlsx), [Schematron](StructureDefinition-RetinaObservation.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "RetinaObservation",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaObservation",
  "version" : "0.1.3",
  "name" : "DIPSRetinaIntegrationObservation",
  "title" : "Observation for retina screening",
  "status" : "draft",
  "date" : "2025-11-08T17:39:22+01:00",
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
  "description" : "This is observations connected to RetinaDiagnosticReport",
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
      }
    ]
  }
}

```
