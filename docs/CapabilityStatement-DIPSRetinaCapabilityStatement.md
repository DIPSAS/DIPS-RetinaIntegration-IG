# DIPSRetinaCapabilityStatement - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **DIPSRetinaCapabilityStatement**

## CapabilityStatement: DIPSRetinaCapabilityStatement 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CapabilityStatement/DIPSRetinaCapabilityStatement | *Version*:0.1.3 |
| Active as of 2025-09-30 | *Computable Name*: |

 
CapabilityStatement for DIPS Retinaflyt 

 [Raw OpenAPI-Swagger Definition file](DIPSRetinaCapabilityStatement.openapi.json) | [Download](DIPSRetinaCapabilityStatement.openapi.json) 

## 

* Implementation Guide Version: 0.1.3 
* FHIR Version: 4.0.1 
* Supported Formats: `xml`, `json`
* Published on: 2025-09-30 12:00:00+0000 
* Published by: DIPS AS 

> **Note to Implementers: FHIR Capabilities**Any FHIR capability may be 'allowed' by the system unless explicitly marked as 'SHALL NOT'. A few items are marked as MAY in the Implementation Guide to highlight their potential relevance to the use case.

## FHIR RESTful Capabilities

### Mode: server

Summary of System-wide Operations


### Capabilities by Resource/Profile

#### Summary

The summary table lists the resources that are part of this configuration, and for each resource it lists:

* The relevant profiles (if any)
* The interactions supported by each resource (**R**ead, **S**earch, **U**pdate, and **C**reate, are always shown, while **VR**ead, **P**atch, **D**elete, **H**istory on **I**nstance, or **H**istory on **T**ype are only present if at least one of the resources has support for them.
* The required, recommended, and some optional search parameters (if any).
* The linked resources enabled for `_include`
* The other resources enabled for `_revinclude`
* The operations on the resource (if any)

| | | | | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| [DiagnosticReport](#DiagnosticReport1-1) | [http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaDiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md) | y |  |  |  |  | `DiagnosticReport:patient`,`DiagnosticReport:result` |  |  |

-------

#### Resource Conformance: supported DiagnosticReport

Base System Profile

[DiagnosticReport for Retinascreening](StructureDefinition-RetinaDiagnosticReport.md)

Profile Conformance

**SHALL**

Reference Policy

Interaction summary

* Supports `read`.



## Resource Content

```json
{
  "resourceType" : "CapabilityStatement",
  "id" : "DIPSRetinaCapabilityStatement",
  "url" : "http://dips.no/fhir/RetinaIntegration/CapabilityStatement/DIPSRetinaCapabilityStatement",
  "version" : "0.1.3",
  "status" : "active",
  "date" : "2025-09-30T12:00:00Z",
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
  "description" : "CapabilityStatement for DIPS Retinaflyt",
  "kind" : "instance",
  "implementation" : {
    "description" : "DIPS retinaintegration-service"
  },
  "fhirVersion" : "4.0.1",
  "format" : ["xml", "json"],
  "rest" : [
    {
      "mode" : "server",
      "resource" : [
        {
          "type" : "DiagnosticReport",
          "profile" : "http://dips.no/fhir/RetinaIntegration/StructureDefinition/RetinaDiagnosticReport",
          "interaction" : [
            {
              "code" : "read"
            }
          ],
          "searchInclude" : ["DiagnosticReport:patient", "DiagnosticReport:result"]
        }
      ],
      "operation" : [
        {
          "name" : "AppendRetinaAIResult",
          "definition" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result",
          "documentation" : "Append results from AI analysis of retina images to a existing DiagnosticReport"
        }
      ]
    }
  ]
}

```
