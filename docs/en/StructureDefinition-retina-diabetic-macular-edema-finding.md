# Retina Diabetic Macular Edema Finding - RetinaIntegration v0.9.0

## Resource Profile: Retina Diabetic Macular Edema Finding ( Experimental ) 

 
Observation profile for documenting findings related to diabetic macular edema (DME) in retina examinations. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Profile: [Observation/RetinaDiabeticMacularEdemaFinding-Example-left](Observation-RetinaDiabeticMacularEdemaFinding-Example-left.md) and [Observation/RetinaDiabeticMacularEdemaFinding-Example-right](Observation-RetinaDiabeticMacularEdemaFinding-Example-right.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/dips.fhir.retinaintegration|current/StructureDefinition/StructureDefinition-retina-diabetic-macular-edema-finding.json)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-retina-diabetic-macular-edema-finding.csv), [Excel](../StructureDefinition-retina-diabetic-macular-edema-finding.xlsx), [Schematron](../StructureDefinition-retina-diabetic-macular-edema-finding.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-diabetic-macular-edema-finding",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-macular-edema-finding",
  "version" : "0.9.0",
  "name" : "RetinaDiabeticMacularEdemaFinding",
  "title" : "Retina Diabetic Macular Edema Finding",
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
  "description" : "Observation profile for documenting findings related to diabetic macular edema (DME) in retina examinations.",
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
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Observation",
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
          "code" : "312912001",
          "display" : "Diabetic macular edema"
        }]
      }
    },
    {
      "id" : "Observation.value[x]",
      "path" : "Observation.value[x]",
      "slicing" : {
        "discriminator" : [{
          "type" : "type",
          "path" : "$this"
        }],
        "ordered" : false,
        "rules" : "open"
      }
    },
    {
      "id" : "Observation.value[x]:valueBoolean",
      "path" : "Observation.value[x]",
      "sliceName" : "valueBoolean",
      "short" : "DME presence (yes/no)",
      "definition" : "Indicates whether diabetic macular edema is present (true) or not (false).",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "boolean"
      }]
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
    }]
  }
}

```
