# Retina Conclusion - RetinaIntegration v0.8.1

## ValueSet: Retina Conclusion 

 
Codes describing the current or final conclusion of the examination (1000-series). 

 **References** 

* [Previous Examination Conclusion](StructureDefinition-previous-examination-conclusion-extension.md)
* [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)

### Logical Definition (CLD)

 

### Expansion

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-conclusion-code-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-conclusion-code-vs",
  "version" : "0.8.1",
  "name" : "RetinaDiagnosticReportConclusionCodeValueSet",
  "title" : "Retina Conclusion",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-05",
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
  "description" : "Codes describing the current or final conclusion of the examination (1000-series).",
  "compose" : {
    "include" : [{
      "system" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs"
    }]
  }
}

```
