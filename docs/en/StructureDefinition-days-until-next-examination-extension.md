# Days Until Next Examination - RetinaIntegration v0.7.0

## Extension: Days Until Next Examination (Experimental) 

Number of days until next examination.

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* Examples for this Extension: [DiagnosticReport/RetinaDiagnosticReport-Example](DiagnosticReport-RetinaDiagnosticReport-Example.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/dips.fhir.retinaintegration|current/StructureDefinition/days-until-next-examination-extension)

### Formal Views of Extension Content

 [Description Differentials, Snapshots, and other representations](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](../StructureDefinition-days-until-next-examination-extension.csv), [Excel](../StructureDefinition-days-until-next-examination-extension.xlsx), [Schematron](../StructureDefinition-days-until-next-examination-extension.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "days-until-next-examination-extension",
  "url" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/days-until-next-examination-extension",
  "version" : "0.7.0",
  "name" : "DaysUntilNextExamination",
  "title" : "Days Until Next Examination",
  "status" : "draft",
  "experimental" : true,
  "date" : "2026-03-31T17:09:32+02:00",
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
  "description" : "Number of days until next examination.",
  "purpose" : "The number indicates a clinically decided time interval between current retinal examination and next retinal examination based on a risk assessment of the patient during the current retinal examination. \n\nContent: String with a number. The number indicates number of days. The counting of the number of days starts at the date images of the patient's retinas are taken. The end date of the counting is the clinical deadline indicated for the next examination.\n\n1 year counts as 365 days, 2 years counts as 730 days. Used by the EMR to set correct deadline date in the patient's planned contact so that the patient will be recalled within the deadline. \n\nFor documentation of a clinically decided time interval between current retinal examination and next retinal examination based on a risk assessment of the patient during the current retinal examination. Origin: Lookup in National Norwegian clinical guidelines for diabetic retinopathy screening [National Norwegian clinical guidelines for diabetic retinopathy screening](https://www.legeforeningen.no/contentassets/c7fccca0ee554d7d80fd8c4818cdd739/godkjente-retningslinjer-for-screening-for-diabetisk-retinopati-05.11.2022.pdf) based on the patient's relevant dataset.",
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
      "short" : "Days Until Next Examination",
      "definition" : "Number of days until next examination."
    },
    {
      "id" : "Extension.extension",
      "path" : "Extension.extension",
      "max" : "0"
    },
    {
      "id" : "Extension.url",
      "path" : "Extension.url",
      "fixedUri" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/days-until-next-examination-extension"
    },
    {
      "id" : "Extension.value[x]",
      "path" : "Extension.value[x]",
      "min" : 1,
      "type" : [{
        "code" : "integer"
      }]
    }]
  }
}

```
