# DIPSRetinaAppendOperationDefinition - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **DIPSRetinaAppendOperationDefinition**

## OperationDefinition: DIPSRetinaAppendOperationDefinition 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result | *Version*:0.1.3 |
| Active as of 2025-11-15 | *Computable Name*:AppendRetinaAIResult |

 
OperationDefinition for appending retina AI results to existing DiagnosticReport. See AddAIResultOperation for an example of the input parameters. 

 
Append results from AI analysis of retina images to a existing DiagnosticReport 

URL: [base]/DiagnosticReport/[id]/$append-retina-ai-result

### Parameters

* **Use**: IN
  * **Name**: dme-right-eye
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [Observation](http://hl7.org/fhir/R4/observation.html)
  * **Binding**: 
  * **Documentation**: Diabetisk makulaødem høyre øye
* **Use**: IN
  * **Name**: dr-right-eye
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [Observation](http://hl7.org/fhir/R4/observation.html)
  * **Binding**: 
  * **Documentation**: Diabetisk retinopati høyre øye
* **Use**: IN
  * **Name**: dme-left-eye
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [Observation](http://hl7.org/fhir/R4/observation.html)
  * **Binding**: 
  * **Documentation**: Diabetisk makulaødem venstre øye
* **Use**: IN
  * **Name**: dr-left-eye
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [Observation](http://hl7.org/fhir/R4/observation.html)
  * **Binding**: 
  * **Documentation**: Diabetisk retinopati venstre øye
* **Use**: IN
  * **Name**: days-until-next-examination
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [integer](http://hl7.org/fhir/R4/datatypes.html#integer)
  * **Binding**: 
  * **Documentation**: Number of days until next examination, stored in extension http://dips.no/fhir/StructureDefinition/frist-nesteundersokelse-extension
* **Use**: IN
  * **Name**: ki-product-name
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [string](http://hl7.org/fhir/R4/datatypes.html#string)
  * **Binding**: 
  * **Documentation**: Name of the AI product, stored in extension http://dips.no/fhir/StructureDefinition/ki-productname-extension
* **Use**: IN
  * **Name**: ki-version-algorithm
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [string](http://hl7.org/fhir/R4/datatypes.html#string)
  * **Binding**: 
  * **Documentation**: Version of the AI algorithm, stored in extension http://dips.no/fhir/StructureDefinition/ki-versjon-algoritme-extension
* **Use**: IN
  * **Name**: ki-protocol
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [string](http://hl7.org/fhir/R4/datatypes.html#string)
  * **Binding**: 
  * **Documentation**: Protocol of the AI analysis, stored in extension http://dips.no/fhir/StructureDefinition/ki-protokoll-extension
* **Use**: IN
  * **Name**: effectiveTime
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [dateTime](http://hl7.org/fhir/R4/datatypes.html#dateTime)
  * **Binding**: 
  * **Documentation**: Time when the AI analysis was performed
* **Use**: IN
  * **Name**: full-ki-report
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [Attachment](http://hl7.org/fhir/R4/datatypes.html#Attachment)
  * **Binding**: 
  * **Documentation**: Full report from the AI analysis, stored in presentedForm of the DiagnosticReport
* **Use**: IN
  * **Name**: imageDescriptions
  * **Scope**: 
  * **Cardinality**: 1..*
  * **Type**: [ImagingStudy](http://hl7.org/fhir/R4/imagingstudy.html)
  * **Binding**: 
  * **Documentation**: Descriptions of the images, diagnosticreport.imagingStudy
* **Use**: IN
  * **Name**: conclusionCode
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept)
  * **Binding**: 
  * **Documentation**: Conclusion code for the AI analysis, added to DiagnosticReport.conclusionCode



## Resource Content

```json
{
  "resourceType" : "OperationDefinition",
  "id" : "append-retina-ai-result",
  "url" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result",
  "version" : "0.1.3",
  "name" : "AppendRetinaAIResult",
  "status" : "active",
  "kind" : "operation",
  "date" : "2025-11-15T17:14:08+01:00",
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
  "description" : "OperationDefinition for appending retina AI results to existing DiagnosticReport. See AddAIResultOperation for an example of the input parameters.",
  "purpose" : "Append results from AI analysis of retina images to a existing DiagnosticReport",
  "code" : "append-retina-ai-result",
  "resource" : ["DiagnosticReport"],
  "system" : false,
  "type" : false,
  "instance" : true,
  "parameter" : [
    {
      "name" : "dme-right-eye",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Diabetisk makulaødem høyre øye",
      "type" : "Observation"
    },
    {
      "name" : "dr-right-eye",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Diabetisk retinopati høyre øye",
      "type" : "Observation"
    },
    {
      "name" : "dme-left-eye",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Diabetisk makulaødem venstre øye",
      "type" : "Observation"
    },
    {
      "name" : "dr-left-eye",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Diabetisk retinopati venstre øye",
      "type" : "Observation"
    },
    {
      "name" : "days-until-next-examination",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Number of days until next examination, stored in extension http://dips.no/fhir/StructureDefinition/frist-nesteundersokelse-extension",
      "type" : "integer"
    },
    {
      "name" : "ki-product-name",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Name of the AI product, stored in extension http://dips.no/fhir/StructureDefinition/ki-productname-extension",
      "type" : "string"
    },
    {
      "name" : "ki-version-algorithm",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Version of the AI algorithm, stored in extension http://dips.no/fhir/StructureDefinition/ki-versjon-algoritme-extension",
      "type" : "string"
    },
    {
      "name" : "ki-protocol",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Protocol of the AI analysis, stored in extension http://dips.no/fhir/StructureDefinition/ki-protokoll-extension",
      "type" : "string"
    },
    {
      "name" : "effectiveTime",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Time when the AI analysis was performed",
      "type" : "dateTime"
    },
    {
      "name" : "full-ki-report",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Full report from the AI analysis, stored in presentedForm of the DiagnosticReport",
      "type" : "Attachment"
    },
    {
      "name" : "imageDescriptions",
      "use" : "in",
      "min" : 1,
      "max" : "*",
      "documentation" : "Descriptions of the images, diagnosticreport.imagingStudy",
      "type" : "ImagingStudy"
    },
    {
      "name" : "conclusionCode",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Conclusion code for the AI analysis, added to DiagnosticReport.conclusionCode",
      "type" : "CodeableConcept"
    }
  ]
}

```
