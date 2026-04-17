# Previous Examination Conclusion - RetinaIntegration v0.8.0

## Extension: Previous Examination Conclusion (Experimental) 

The conclusion from the previous examination (1000 series). If this is the first examination, this extension is not present.

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Extension: [Bundle/Bundle-TwoExaminations-Example](Bundle-Bundle-TwoExaminations-Example.md), [DiagnosticReport/RetinaDiagnosticReport-Example](DiagnosticReport-RetinaDiagnosticReport-Example.md) and [DiagnosticReport/bb2690e7-ca9f-4070-9c35-c7e36976b144](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/previous-examination-conclusion-extension)

### Formal Views of Extension Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-previous-examination-conclusion-extension.csv), [Excel](../StructureDefinition-previous-examination-conclusion-extension.xlsx), [Schematron](../StructureDefinition-previous-examination-conclusion-extension.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "previous-examination-conclusion-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/previous-examination-conclusion-extension",
  "version" : "0.8.0",
  "name" : "PreviousExaminationConclusionExtension",
  "title" : "Previous Examination Conclusion",
  "status" : "active",
  "experimental" : true,
  "date" : "2026-04-17T16:52:07+02:00",
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
  "description" : "The conclusion from the previous examination (1000 series). If this is the first examination, this extension is not present.",
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
      "short" : "Previous Examination Conclusion",
      "definition" : "The conclusion from the previous examination (1000 series). If this is the first examination, this extension is not present."
    },
    {
      "id" : "Extension.extension",
      "path" : "Extension.extension",
      "max" : "0"
    },
    {
      "id" : "Extension.url",
      "path" : "Extension.url",
      "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/previous-examination-conclusion-extension"
    },
    {
      "id" : "Extension.value[x]",
      "path" : "Extension.value[x]",
      "type" : [{
        "code" : "Coding"
      }],
      "binding" : {
        "strength" : "required",
        "valueSet" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusion-code-vs"
      }
    }]
  }
}

```
