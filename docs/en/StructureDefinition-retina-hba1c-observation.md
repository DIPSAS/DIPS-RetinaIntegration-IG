# Retina HbA1c Observation - RetinaIntegration v0.7.0

## Resource Profile: Retina HbA1c Observation ( Experimental ) 

 
HbA1c level as reported by patient prior to retina examination. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Profile: [Observation/RetinaHbA1cObservation-Example](Observation-RetinaHbA1cObservation-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-hba1c-observation)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-retina-hba1c-observation.csv), [Excel](../StructureDefinition-retina-hba1c-observation.xlsx), [Schematron](../StructureDefinition-retina-hba1c-observation.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-hba1c-observation",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-hba1c-observation",
  "version" : "0.7.0",
  "name" : "RetinaHbA1cObservation",
  "title" : "Retina HbA1c Observation",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-12-02",
  "publisher" : "DIPS AS",
  "contact" : [{
    "name" : "DIPS AS",
    "telecom" : [{
      "system" : "url",
      "value" : "http://dips.no/"
    },
    {
      "system" : "email",
      "value" : "teamsolsiden@dips.no"
    }]
  }],
  "description" : "HbA1c level as reported by patient prior to retina examination.",
  "fhirVersion" : "4.0.1",
  "mapping" : [{
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
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Observation",
  "baseDefinition" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-observation",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Observation",
      "path" : "Observation"
    },
    {
      "id" : "Observation.code",
      "path" : "Observation.code",
      "patternCodeableConcept" : {
        "coding" : [{
          "system" : "http://snomed.info/sct",
          "code" : "167491000202108",
          "display" : "HbA1c"
        }]
      }
    }]
  }
}

```
