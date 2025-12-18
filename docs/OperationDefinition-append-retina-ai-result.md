# Retina Append AI Result Operation - RetinaIntegration v0.5.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Append AI Result Operation**

## OperationDefinition: Retina Append AI Result Operation 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result | *Version*:0.5.0 |
| Draft as of 2025-12-18 | *Computable Name*:AppendRetinaAIResult |

 
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

#### Observation Resources

These observations contain the AI's clinical findings.

There are three observations for each eye.

The effectiveTime is repeated in each observation, because that is FHIR best practice.

* **rightDiabeticRetinopathyFinding**, **rightDiabeticMacularEdemaFinding**, **rightImageQualityAssessment**
* **leftDiabeticRetinopathyFinding**, **leftDiabeticMacularEdemaFinding**, **leftImageQualityAssessment**

#### Conclusion

* **conclusionCode** (1..1): Overall conclusion code for the analysis
* **daysUntilNextExamination** (0..1): Recommended days until next examination

#### AI Metadata (1..1 required)

Required information about the AI system and analysis:

* **aiDevice** (1..1): The AI device that performed the analysis in the `device` element. We assume that alle the observations are performed by the same AI device. (TODO: Verify this assumption.)
* **fullReport** (1..1): Complete report of AI and supporting system an Attachment.
* **metaTags** (0..*): Workflow tags, such as `VALIDATION` to indicate data for validation review

### Example

See [RetinaAppendAIResultOperation-Example](Parameters-RetinaAppendAIResultOperation-Example.md) for a complete example of the operation parameters.



## Resource Content

```json
{
  "resourceType" : "OperationDefinition",
  "id" : "append-retina-ai-result",
  "url" : "http://dips.no/fhir/RetinaIntegration/OperationDefinition/append-retina-ai-result",
  "version" : "0.5.0",
  "name" : "AppendRetinaAIResult",
  "title" : "Retina Append AI Result Operation",
  "status" : "draft",
  "kind" : "operation",
  "date" : "2025-12-18T07:21:20+01:00",
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
      "documentation" : "Sectra study identifier for the retinal images that were analyzed. System: http://dips.no/fhir/RetinaIntegration/sectra-image-study-id",
      "type" : "Identifier"
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
      "name" : "aiDevice",
      "use" : "in",
      "min" : 1,
      "max" : "1",
      "documentation" : "AI Device that performed the analysis. MUST conform to RetinaAIDevice profile (http://dips.no/fhir/RetinaIntegration/StructureDefinition/retina-ai-device). Should include deviceName with AI product name, and version elements for algorithm version and protocol.",
      "type" : "Device"
    },
    {
      "name" : "rightDiabeticRetinopathyFinding",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Right eye diabetic retinopathy finding. MUST conform to RetinaDiabeticRetinopathyFinding profile with bodySite set to right eye (SNOMED CT: 5597008).",
      "type" : "Observation"
    },
    {
      "name" : "rightDiabeticMacularEdemaFinding",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Right eye diabetic macular edema finding. MUST conform to RetinaDiabeticMacularEdemaFinding profile with bodySite set to right eye (SNOMED CT: 5597008).",
      "type" : "Observation"
    },
    {
      "name" : "rightImageQualityAssessment",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Right eye image quality assessment. MUST conform to RetinaImageQualityAssessment profile with bodySite set to right eye (SNOMED CT: 5597008).",
      "type" : "Observation"
    },
    {
      "name" : "leftDiabeticRetinopathyFinding",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Left eye diabetic retinopathy finding. MUST conform to RetinaDiabeticRetinopathyFinding profile with bodySite set to left eye (SNOMED CT: 58443009).",
      "type" : "Observation"
    },
    {
      "name" : "leftDiabeticMacularEdemaFinding",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Left eye diabetic macular edema finding. MUST conform to RetinaDiabeticMacularEdemaFinding profile with bodySite set to left eye (SNOMED CT: 58443009).",
      "type" : "Observation"
    },
    {
      "name" : "leftImageQualityAssessment",
      "use" : "in",
      "min" : 0,
      "max" : "1",
      "documentation" : "Left eye image quality assessment. MUST conform to RetinaImageQualityAssessment profile with bodySite set to left eye (SNOMED CT: 58443009).",
      "type" : "Observation"
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
