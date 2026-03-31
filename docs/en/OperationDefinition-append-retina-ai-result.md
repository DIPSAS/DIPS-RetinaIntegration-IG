# Retina Append AI Result Operation - RetinaIntegration v0.7.0

## OperationDefinition: Retina Append AI Result Operation 

 
OperationDefinition for appending retina AI results to an existing DiagnosticReport. 

### Overview

The `$append-retina-ai-result` operation is used to add AI analysis results to an existing DiagnosticReport. This operation is invoked bye the regional integration platform after the AI system has analyzed retinal images.

### Example

See [RetinaAppendAIResultOperation-Example](Parameters-RetinaAppendAIResultOperation-Example.json.md) for a an example of the parameters.

### Usage

Add AI result to an examination using the following operation:

```
[baseUrl]/DiagnosticReport/[id]/$append-retina-ai-result

```

`[id]` is the identifier UUID (Universally Unique Identifier), sometimes referred to as a GUID, of the DiagnosticReport, a.k.a examination, to update.



## Resource Content

```json
{
  "resourceType" : "OperationDefinition",
  "id" : "append-retina-ai-result",
  "url" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result",
  "version" : "0.7.0",
  "name" : "AppendRetinaAIResult",
  "title" : "Retina Append AI Result Operation",
  "status" : "draft",
  "kind" : "operation",
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
  "description" : "OperationDefinition for appending retina AI results to an existing DiagnosticReport.",
  "purpose" : "Append results from AI analysis of retina images to a existing DiagnosticReport",
  "code" : "append-retina-ai-result",
  "resource" : ["DiagnosticReport"],
  "system" : false,
  "type" : false,
  "instance" : true,
  "parameter" : [{
    "name" : "sectraStudyId",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Sectra study ID for the retinal images that were analyzed.",
    "type" : "string"
  },
  {
    "name" : "conclusion",
    "use" : "in",
    "min" : 1,
    "max" : "1",
    "documentation" : "Conclusion indicating the next step. MUST be a single code from the 1000 series. If the validation parameter is set to true, the next step will always be manual grading.",
    "type" : "CodeableConcept"
  },
  {
    "name" : "daysUntilNextExamination",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Number of days until next examination. Only included if the conclusion code indicates that the next step is a new examination.",
    "type" : "integer"
  },
  {
    "name" : "leftDiabeticRetinopathy",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Left eye diabetic retinopathy evaluation, a decimal between 0.0 and 5.0",
    "type" : "decimal"
  },
  {
    "name" : "leftDiabeticMacularEdema",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Left eye diabetic macular edema evaluation. True if diabetic macular edema is present.",
    "type" : "boolean"
  },
  {
    "name" : "rightDiabeticRetinopathy",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Right eye diabetic retinopathy evaluation, a decimal between 0.0 and 5.0",
    "type" : "decimal"
  },
  {
    "name" : "rightDiabeticMacularEdema",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Right eye diabetic macular edema evaluation. True if diabetic macular edema is present.",
    "type" : "boolean"
  },
  {
    "name" : "rightEyeImage",
    "use" : "in",
    "min" : 0,
    "max" : "*",
    "documentation" : "Right eye images used in the AI analysis. MUST conform to RetinaImageParameter profile.",
    "type" : "Observation",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-parameter"]
  },
  {
    "name" : "leftEyeImage",
    "use" : "in",
    "min" : 0,
    "max" : "*",
    "documentation" : "Left eye images used in the AI analysis. MUST conform to RetinaImageParameter profile.",
    "type" : "Observation",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-image-parameter"]
  },
  {
    "name" : "aiDevice",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "AI Device that performed the analysis. Includes AI product name, algorithm version and protocol version.",
    "type" : "Device",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device"]
  },
  {
    "name" : "performedDateTime",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Date and time when the retinal AI analysis was performed.",
    "type" : "dateTime"
  },
  {
    "name" : "cameraDevice",
    "use" : "in",
    "min" : 0,
    "max" : "1",
    "documentation" : "Camera device used to capture the retinal images.",
    "type" : "Device",
    "targetProfile" : ["http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-camera-device"]
  },
  {
    "name" : "fullReport",
    "use" : "in",
    "min" : 1,
    "max" : "1",
    "documentation" : "Technical details for further reference about the AI grading.",
    "type" : "Attachment"
  },
  {
    "name" : "validation",
    "use" : "in",
    "min" : 1,
    "max" : "1",
    "documentation" : "Set true if the AI result is for validation purposes only and will not be used in clinical decision making.",
    "type" : "boolean"
  }]
}

```
