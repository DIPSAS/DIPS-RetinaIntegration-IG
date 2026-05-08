# Cautions - RetinaIntegration v0.8.1

## Extension: Cautions (Experimental) 

Special considerations or cautions for grading this examination (5000-series).

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Extension: [Bundle/Bundle-TwoExaminations-Example](Bundle-Bundle-TwoExaminations-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/cautions-extension)

### Formal Views of Extension Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-cautions-extension.csv), [Excel](../StructureDefinition-cautions-extension.xlsx), [Schematron](../StructureDefinition-cautions-extension.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "cautions-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/cautions-extension",
  "version" : "0.8.1",
  "name" : "CautionsExtension",
  "title" : "Cautions",
  "status" : "draft",
  "experimental" : true,
  "date" : "2026-05-08T13:22:39+02:00",
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
  "description" : "Special considerations or cautions for grading this examination (5000-series).",
  "fhirVersion" : "4.0.1",
  "mapping" : [{
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  }],
  "kind" : "complex-type",
  "abstract" : false,
  "context" : [{
    "type" : "element",
    "expression" : "DiagnosticReport"
  }],
  "type" : "Extension",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Extension",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Extension",
      "path" : "Extension",
      "short" : "Cautions",
      "definition" : "Special considerations or cautions for grading this examination (5000-series)."
    },
    {
      "id" : "Extension.extension",
      "path" : "Extension.extension",
      "max" : "0"
    },
    {
      "id" : "Extension.url",
      "path" : "Extension.url",
      "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/cautions-extension"
    },
    {
      "id" : "Extension.value[x]",
      "path" : "Extension.value[x]",
      "type" : [{
        "code" : "CodeableConcept"
      }],
      "binding" : {
        "strength" : "required",
        "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-caution-vs"
      }
    }]
  }
}

```
