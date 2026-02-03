# Query By Date Operation - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Query By Date Operation**

## OperationDefinition: Query By Date Operation 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/OperationDefinition/retina-by-date | *Version*:0.6.0 |
| Draft as of 2026-02-03 | *Computable Name*:RetinaQueryByDate |

 
Operation to query for retina diagnostic reports within a specified date range and optionally filter for reports pending AI analysis. 

The `retina-by-date` is a custom query operation that is easier to use than the general FHIR query. (And our general GET does not )

### Retrieve all reports between to dates

To retrieve all diagnostic reports for one day regardless of the status of the report use this URL:

```
[baseurl]/DiagnosticReport/$retina-by-date?start=2025-10-02&end=2025-10-03&_include=DiagnosticReport:result

```

### Retrieve reports pending AI

To retrieve reports where it is possible to do the operation [append AI result](OperationDefinition-append-retina-ai-result.md), add the optional parameter `pendingAI`.

```
[baseurl]/DiagnosticReport/$retina-by-date?start=2025-10-02&end=2025-10-03&pendingAI=true&_include=DiagnosticReport:result

```

### Notes:

Only GET works through the DIPS FHIR facade (the fhirr4-service).

Passing the [query parameters in the body](Parameters-RetinaQueryByDate-Example.json.md) in a POST only works directly at retinaintegration-service.

There is no need to specify the profile `_profile=RetinaDiagnosticReport` when using this query operation.



## Resource Content

```json
{
  "resourceType" : "OperationDefinition",
  "id" : "retina-by-date",
  "url" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/retina-by-date",
  "version" : "0.6.0",
  "name" : "RetinaQueryByDate",
  "title" : "Query By Date Operation",
  "status" : "draft",
  "kind" : "query",
  "date" : "2026-02-03T09:57:13+01:00",
  "publisher" : "DIPS AS",
  "contact" : [
    {
      "name" : "DIPS AS",
      "telecom" : [
        {
          "system" : "url",
          "value" : "http://dips.no/"
        },
        {
          "system" : "email",
          "value" : "teamsolsiden@dips.no"
        }
      ]
    }
  ],
  "description" : "Operation to query for retina diagnostic reports within a specified date range and optionally filter for reports pending AI analysis.",
  "affectsState" : false,
  "code" : "retina-by-date",
  "resource" : ["DiagnosticReport"],
  "system" : false,
  "type" : true,
  "instance" : false,
  "parameter" : [
    {
      "name" : "start",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Optional start of the date range for the query. If not provided, the query will return reports from the earliest available date up to the end date.",
      "type" : "dateTime"
    },
    {
      "name" : "end",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Optional end of the date range for the query. If not provided, the query will return reports from the start date up to the latest available date.",
      "type" : "dateTime"
    },
    {
      "name" : "pendingAI",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Optional parameter. If present, the query will only return reports that are pending AI analysis. In a GET request, the parameter can be provided without a value (e.g., `&pendingAI`).",
      "type" : "boolean"
    }
  ]
}

```
