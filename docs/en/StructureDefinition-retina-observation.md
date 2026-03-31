# Retina Observation - RetinaIntegration v0.7.0

## Resource Profile: Retina Observation ( Abstract ) 

 
Base observation profile for observations connected to RetinaDiagnosticReport. 

**Usages:**

* Derived from this Profile: [Retina HbA1c Observation](StructureDefinition-retina-hba1c-observation.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-observation)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-retina-observation.csv), [Excel](../StructureDefinition-retina-observation.xlsx), [Schematron](../StructureDefinition-retina-observation.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-observation",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-observation",
  "version" : "0.7.0",
  "name" : "RetinaObservation",
  "title" : "Retina Observation",
  "status" : "draft",
  "experimental" : false,
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
  "description" : "Base observation profile for observations connected to RetinaDiagnosticReport.",
  "purpose" : "This profile is not to be instantiated directly. It is a base profile for other observation profiles.",
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
  "abstract" : true,
  "type" : "Observation",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Observation",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Observation",
      "path" : "Observation"
    },
    {
      "id" : "Observation.identifier",
      "path" : "Observation.identifier",
      "slicing" : {
        "discriminator" : [{
          "type" : "value",
          "path" : "system"
        }],
        "rules" : "open"
      }
    },
    {
      "id" : "Observation.identifier:retinaObservationId",
      "path" : "Observation.identifier",
      "sliceName" : "retinaObservationId",
      "short" : "Retina Observation Identifier (GUID)",
      "definition" : "Unique identifier for the observation within RetinaIntegration. Value must be a valid GUID in format: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
      "min" : 0,
      "max" : "1",
      "example" : [{
        "label" : "UUID Identifier",
        "valueIdentifier" : {
          "system" : "http://dips.no/fhir/RetinaIntegration/observation-id",
          "value" : "8367e10c-ee7f-4a42-8bdd-44f628ab0a6f"
        }
      }]
    },
    {
      "id" : "Observation.identifier:retinaObservationId.system",
      "path" : "Observation.identifier.system",
      "min" : 1,
      "patternUri" : "http://dips.no/fhir/RetinaIntegration/observation-id"
    },
    {
      "id" : "Observation.identifier:retinaObservationId.value",
      "path" : "Observation.identifier.value",
      "min" : 1
    }]
  }
}

```
