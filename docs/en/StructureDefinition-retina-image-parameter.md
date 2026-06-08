# Retina Image Parameter - RetinaIntegration v0.9.1

## Resource Profile: Retina Image Parameter 

 
A structure describing an image for use in a operation. 

**Usages:**

* Examples for this Profile: [Observation/RetinaImageParameter-Example](Observation-RetinaImageParameter-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/dips.fhir.retinaintegration|current/StructureDefinition/StructureDefinition-retina-image-parameter.json)

### Formal Views of Profile Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-retina-image-parameter.csv), [Excel](../StructureDefinition-retina-image-parameter.xlsx), [Schematron](../StructureDefinition-retina-image-parameter.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "retina-image-parameter",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-parameter",
  "version" : "0.9.1",
  "name" : "RetinaImageParameter",
  "title" : "Retina Image Parameter",
  "status" : "draft",
  "experimental" : false,
  "date" : "2026-01-19",
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
  "description" : "A structure describing an image for use in a operation.",
  "purpose" : "An Image parameter MUST consist of two codes: one for image quality (2000 series) and one for image view (6000 series).",
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
      "id" : "Observation.implicitRules",
      "path" : "Observation.implicitRules",
      "max" : "0"
    },
    {
      "id" : "Observation.modifierExtension",
      "path" : "Observation.modifierExtension",
      "max" : "0"
    },
    {
      "id" : "Observation.identifier",
      "path" : "Observation.identifier",
      "max" : "0"
    },
    {
      "id" : "Observation.code",
      "path" : "Observation.code",
      "short" : "Image quality as assessed by AI (2000-series) and image view (6000-series).",
      "binding" : {
        "strength" : "required",
        "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-image-parameter-vs"
      }
    },
    {
      "id" : "Observation.effective[x]",
      "path" : "Observation.effective[x]",
      "max" : "0"
    }]
  }
}

```
