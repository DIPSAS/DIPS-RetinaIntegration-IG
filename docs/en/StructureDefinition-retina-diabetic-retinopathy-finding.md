# Retina Diabetic Retinopathy Finding - RetinaIntegration v0.8.0

## Resource Profile: Retina Diabetic Retinopathy Finding ( Experimental ) 

 
Observation profile for documenting findings related to diabetic retinopathy (DR) in retina examinations. 

**Usages:**

* Refer to this Profile: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Profile: [Observation/RetinaDiabeticRetinopathyFinding-Example-left](Observation-RetinaDiabeticRetinopathyFinding-Example-left.md) and [Observation/RetinaDiabeticRetinopathyFinding-Example-right](Observation-RetinaDiabeticRetinopathyFinding-Example-right.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/retina-diabetic-retinopathy-finding)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-retina-diabetic-retinopathy-finding.csv), [Excel](../StructureDefinition-retina-diabetic-retinopathy-finding.xlsx), [Schematron](../StructureDefinition-retina-diabetic-retinopathy-finding.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-diabetic-retinopathy-finding",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-diabetic-retinopathy-finding",
  "version" : "0.8.0",
  "name" : "RetinaDiabeticRetinopathyFinding",
  "title" : "Retina Diabetic Retinopathy Finding",
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
  "description" : "Observation profile for documenting findings related to diabetic retinopathy (DR) in retina examinations.",
  "purpose" : "The DR severity component uses a Quantity value representing the severity level of diabetic retinopathy:\n\n<table class=\"codes\">\n<tr><th>Value</th><th>Description</th></tr>\n<tr><td>[0.0 1.0></td><td>Ingen synlig diabetisk retinopati (DR)</td></tr>\n<tr><td>[1.0 2.0></td><td>Mild non-proliferativ DR</td></tr>\n<tr><td>[2.0 3.0></td><td>Moderat non-proliferativ DR</td></tr>\n<tr><td>[3.0 4.0></td><td>Alvorlig non-proliferativ DR</td></tr>\n<tr><td>≥ 4.0</td><td>Proliferativ DR</td></tr>\n</table>\n\nTODO: Consider this: Should we use a CodeableConcept with a coding for each severity level, in addition to the Quantity value? \nSusggested LOINC 11504-0 \"Diabetic retinopathy severity\" with answer list LL5321-4 with standardized severity levels. ",
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
          "code" : "4855003",
          "display" : "Diabetic retinopathy"
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
      "id" : "Observation.value[x]:valueQuantity",
      "path" : "Observation.value[x]",
      "sliceName" : "valueQuantity",
      "short" : "Severity of diabetic retinopathy (0.0 - 5.0)",
      "definition" : "Quantitative assessment of diabetic retinopathy severity on a scale from 0.0 to 5.0.",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "Quantity"
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
