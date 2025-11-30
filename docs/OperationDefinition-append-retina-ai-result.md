# Retina Append AI Result Operation - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Append AI Result Operation**

## OperationDefinition: Retina Append AI Result Operation 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result | *Version*:0.2.0 |
| Draft as of 2025-11-30 | *Computable Name*:AppendRetinaAIResult |

 
OperationDefinition for appending retina AI results to an existing DiagnosticReport. 

 
Append results from AI analysis of retina images to a existing DiagnosticReport 

### Overview

The `$append-retina-ai-result` operation is used to add AI analysis results to an existing DiagnosticReport. This operation is invoked after an AI system has analyzed retinal images and needs to submit its findings back to the DIPS system.

### Usage

```
POST {baseUrl}/DiagnosticReport/{id}/$append-retina-ai-result

```

Where `{id}` is the identifier of the DiagnosticReport to update.

### Parameters Overview

The operation accepts multiple types of parameters organized into logical groups:

#### Input references

* **sectraStudyId** (1..1): The image study that was input for the AI system

#### Observation Resources (0..1 each)

These observations contain the AI's clinical findings:

* **rightEye**: Combined observation for the right eye with DR and DME as components.
* **leftEye**: Combined observation for the left eye with DR and DME as components.
* **imageDescriptions** (1..*): ImagingStudy resources describing the analyzed images

#### Conclusion

* **conclusionCode** (1..1): Overall conclusion code for the analysis
* **daysUntilNextExamination** (0..1): Recommended days until next examination

#### AI Metadata (1..1 required)

Required information about the AI system and analysis:

* **aiDevice** (1..1): The AI device that performed the analysis in the `device` element. We assume that alle the observations (the EyeObservations gradings) are performed by the same AI device. (TODO: Verify this assumption.)
* **effectiveTime** (1..1): When the AI analysis was performed
* **fullReport** (1..1): Complete report of AI and supporting system an Attachment.
* **metaTags** (0..*): Workflow tags, such as `VALIDATION` to indicate data for validation review

### Example

See [RetinaAppendAIResultOperation-Example](Parameters-RetinaAppendAIResultOperation-Example.md) for a complete example of the operation parameters.

URL: [base]/DiagnosticReport/[id]/$append-retina-ai-result

### Parameters

* **Use**: IN
  * **Name**: sectraStudyId
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [Identifier](http://hl7.org/fhir/R4/datatypes.html#Identifier)
  * **Binding**: 
  * **Documentation**: Sectra study identifier for the retinal images that were analyzed. System: http://sectra.no/identifiers (TODO: Is there a more global standard to use for Sectra studyID system?)
* **Use**: IN
  * **Name**: rightEye
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [Observation](http://hl7.org/fhir/R4/observation.html)
  * **Binding**: 
  * **Documentation**: Right eye observation with DR, DME and image quality components. MUST conform to RetinaEyeObservation profile (http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation). BodySite and AI device will be added.
* **Use**: IN
  * **Name**: leftEye
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [Observation](http://hl7.org/fhir/R4/observation.html)
  * **Binding**: 
  * **Documentation**: Left eye observation with DR, DME and image quality components. MUST conform to RetinaEyeObservation profile (http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation). BodySite and AI device will be added.
* **Use**: IN
  * **Name**: conclusion
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept)
  * **Binding**: 
  * **Documentation**: Conclusion code for the AI analysis, added to DiagnosticReport.conclusionCode. MUST use codes from RetinaDiagnosticReportConclusionCodeValueSet (http://dips.no/fhir/RetinaIntegration/ValueSet/retina-diagnosticreport-conclusioncode-vs)
* **Use**: IN
  * **Name**: daysUntilNextExamination
  * **Scope**: 
  * **Cardinality**: 0..1
  * **Type**: [integer](http://hl7.org/fhir/R4/datatypes.html#integer)
  * **Binding**: 
  * **Documentation**: Number of days until next examination, stored in extension http://dips.no/fhir/StructureDefinition/days-until-next-examination-extension
* **Use**: IN
  * **Name**: effectiveTime
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [dateTime](http://hl7.org/fhir/R4/datatypes.html#dateTime)
  * **Binding**: 
  * **Documentation**: Time when the AI analysis was performed
* **Use**: IN
  * **Name**: aiDevice
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [Device](http://hl7.org/fhir/R4/device.html)
  * **Binding**: 
  * **Documentation**: AI Device that performed the analysis. MUST conform to RetinaAIDevice profile (http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device). Should include deviceName with AI product name, and version elements for algorithm version and protocol.
* **Use**: IN
  * **Name**: fullReport
  * **Scope**: 
  * **Cardinality**: 1..1
  * **Type**: [Attachment](http://hl7.org/fhir/R4/datatypes.html#Attachment)
  * **Binding**: 
  * **Documentation**: Technical details for further reference about the AI grading, stored in DiagnosticReport.presentedForm
* **Use**: IN
  * **Name**: metaTags
  * **Scope**: 
  * **Cardinality**: 0..*
  * **Type**: [Coding](http://hl7.org/fhir/R4/datatypes.html#Coding)
  * **Binding**: 
  * **Documentation**: Workflow tags. Add code http://terminology.hl7.org/CodeSystem/v3-ActReason#VALIDATION when data is for validation purposes only and the result from the AI analysis will not be used in clinical decision making.



## Resource Content

```json
{
  "resourceType" : "OperationDefinition",
  "id" : "append-retina-ai-result",
  "url" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result",
  "version" : "0.2.0",
  "name" : "AppendRetinaAIResult",
  "title" : "Retina Append AI Result Operation",
  "status" : "draft",
  "kind" : "operation",
  "date" : "2025-11-30T22:57:21+01:00",
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
  "description" : "OperationDefinition for appending retina AI results to an existing DiagnosticReport.",
  "purpose" : "Append results from AI analysis of retina images to a existing DiagnosticReport",
  "code" : "append-retina-ai-result",
  "resource" : ["DiagnosticReport"],
  "system" : false,
  "type" : false,
  "instance" : true,
  "parameter" : [
    {
      "name" : "sectraStudyId",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Sectra study identifier for the retinal images that were analyzed. System: http://sectra.no/identifiers (TODO: Is there a more global standard to use for Sectra studyID system?)",
      "type" : "Identifier"
    },
    {
      "name" : "rightEye",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Right eye observation with DR, DME and image quality components. MUST conform to RetinaEyeObservation profile (http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation). BodySite and AI device will be added.",
      "type" : "Observation"
    },
    {
      "name" : "leftEye",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Left eye observation with DR, DME and image quality components. MUST conform to RetinaEyeObservation profile (http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-eye-observation). BodySite and AI device will be added.",
      "type" : "Observation"
    },
    {
      "name" : "conclusion",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Conclusion code for the AI analysis, added to DiagnosticReport.conclusionCode. MUST use codes from RetinaDiagnosticReportConclusionCodeValueSet (http://dips.no/fhir/RetinaIntegration/ValueSet/retina-diagnosticreport-conclusioncode-vs)",
      "type" : "CodeableConcept"
    },
    {
      "name" : "daysUntilNextExamination",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Number of days until next examination, stored in extension http://dips.no/fhir/StructureDefinition/days-until-next-examination-extension",
      "type" : "integer"
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
      "name" : "aiDevice",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "AI Device that performed the analysis. MUST conform to RetinaAIDevice profile (http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device). Should include deviceName with AI product name, and version elements for algorithm version and protocol.",
      "type" : "Device"
    },
    {
      "name" : "fullReport",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "Technical details for further reference about the AI grading, stored in DiagnosticReport.presentedForm",
      "type" : "Attachment"
    },
    {
      "name" : "metaTags",
      "use" : "in",
      "min" : 0,
      "max" : "*",
      "documentation" : "Workflow tags. \n    Add code http://terminology.hl7.org/CodeSystem/v3-ActReason#VALIDATION when data is for validation purposes only\n    and the result from the AI analysis will not be used in clinical decision making.",
      "type" : "Coding"
    }
  ]
}

```
