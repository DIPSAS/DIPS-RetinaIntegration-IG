# Retina Conclusion Codes - RetinaIntegration v0.9.1

## CodeSystem: Retina Conclusion Codes 

 
Codes for the current or final conclusion of the grading process (1000-series). 

This Code system is referenced in the definition of the following value sets:

* [RetinaAppendAIConlusionValueSet](ValueSet-retina-append-ai-conclusion-vs.md)
* [RetinaDiagnosticReportConclusionCodeValueSet](ValueSet-retina-conclusion-code-vs.md)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-conclusion-code-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusion-code-cs",
  "version" : "0.9.1",
  "name" : "RetinaConclusionCodeSystem",
  "title" : "Retina Conclusion Codes",
  "status" : "draft",
  "experimental" : false,
  "date" : "2026-06-05",
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
  "description" : "Codes for the current or final conclusion of the grading process (1000-series).",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 7,
  "concept" : [{
    "code" : "1001",
    "display" : "KI-gradering (basert på nåværende bilder)",
    "definition" : "This examination is waiting to be graded by the AI system.",
    "designation" : [{
      "language" : "x-eyecare",
      "value" : "EY12"
    }]
  },
  {
    "code" : "1002",
    "display" : "Primærgradering (basert på nåværende bilder)",
    "definition" : "This examinations is waiting to be graded by a primary grader.",
    "designation" : [{
      "language" : "x-eyecare",
      "value" : "EY11"
    }]
  },
  {
    "code" : "1003",
    "display" : "Sekundærgradering (basert på nåværende bilder)",
    "definition" : "This examination is waiting to be graded by a secondary grader.",
    "designation" : [{
      "language" : "x-eyecare",
      "value" : "EY01"
    }]
  },
  {
    "code" : "1004",
    "display" : "Ny fotokontroll (primærgradering)",
    "definition" : "Patient should be scheduled for a new routine eye examination graded by primary grader or AI.",
    "designation" : [{
      "language" : "x-eyecare",
      "value" : "EY02"
    }]
  },
  {
    "code" : "1005",
    "display" : "Ny fotokontroll (sekundærgradering)",
    "definition" : "Patient should be scheduled for a new routine eye examination but graded by secondary grader.",
    "designation" : [{
      "language" : "x-eyecare",
      "value" : "EY04"
    }]
  },
  {
    "code" : "1006",
    "display" : "Oppfølging i programmet settes på vent",
    "definition" : "Participation in the screening program is put on hold.",
    "designation" : [{
      "language" : "x-eyecare",
      "value" : "EY24"
    }]
  },
  {
    "code" : "1007",
    "display" : "Oppfølging i programmet avsluttes",
    "definition" : "Patient is discharged from the screening program.",
    "designation" : [{
      "language" : "x-eyecare",
      "value" : "EY25"
    }]
  }]
}

```
