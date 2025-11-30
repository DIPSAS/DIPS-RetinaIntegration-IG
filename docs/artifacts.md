# Artifacts Summary - RetinaIntegration v0.2.0

* [**Table of Contents**](toc.md)
* **Artifacts Summary**

## Artifacts Summary

This page provides a list of the FHIR artifacts defined as part of this implementation guide.

### Behavior: Capability Statements 

The following artifacts define the specific capabilities that different types of systems are expected to have in order to comply with this implementation guide. Systems conforming to this implementation guide are expected to declare conformance to one or more of the following capability statements.

| | |
| :--- | :--- |
| [Retina CapabilityStatement](CapabilityStatement-RetinaCapabilityStatement.md) | CapabilityStatement for DIPS Retina Integration FHIR API. |

### Behavior: Operation Definitions 

These are custom operations that can be supported by and/or invoked by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina Append AI Result Operation](OperationDefinition-append-retina-ai-result.md) | OperationDefinition for appending retina AI results to an existing DiagnosticReport. |

### Structures: Abstract Profiles 

These are profiles on resources or data types that describe patterns used by other profiles, but cannot be instantiated directly. I.e. instances can conform to profiles **based** on these abstract profiles but do not declare conformance to the abstract profiles themselves.

| | |
| :--- | :--- |
| [Retina Observation](StructureDefinition-retina-observation.md) | Base observation profile for observations connected to RetinaDiagnosticReport. |

### Structures: Resource Profiles 

These define constraints on FHIR resources for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina AI Device](StructureDefinition-retina-ai-device.md) | AI device/software system used for automated retina screening analysis. |
| [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md) | Diagnostic report for the grading process of a single examination which is part of a screening program. |
| [Retina Eye Observation](StructureDefinition-retina-eye-observation.md) | The result of AI grading for one eye. The bodySite element identifies which eye (right or left). |
| [Retina HbA1c Observation](StructureDefinition-retina-hba1c-observation.md) | HbA1c level as reported by patient prior to retina examination. |
| [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md) | Profile for imaging studies related to retina examinations, including fundus photography and OCT imaging. |

### Structures: Extension Definitions 

These define constraints on FHIR data types for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Days Until Next Examination](StructureDefinition-days-until-next-examination-extension.md) | Number of days until next examination. |
| [Initial Instructions](StructureDefinition-initial-instructions-extension.md) | Initial routing instruction and optional cautions for grading this examination (4000-series and 5000-series). |
| [Previous Examination Conclusion](StructureDefinition-previous-examination-conclusion-extension.md) | The conclusion from the previous examination (1000 series). If this is the first examination, this extension is not present. |

### Terminology: Value Sets 

These define sets of codes used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina Body Site](ValueSet-retina-body-site-vs.md) | Body site codes for retinal observations (right or left retina). |
| [Retina Conclusion](ValueSet-retina-conclusioncode-vs.md) | Codes describing the current or final conclusion of the examination (1000-series). |
| [Retina Image Quality](ValueSet-retina-imagequality-vs.md) | Image quality as assessed by AI (2000-series). |
| [Retina Imaging Procedures](ValueSet-retina-imaging-procedure-vs.md) | Valid procedure codes for Retina imaging studies. Contains two Norwegian procedure codes from no-kodeverk-7275: CKDP10 for fundus photography and CKFX16 for OCT imaging of the eye fundus using light-wave based technique. |
| [Retina Initial Instructions](ValueSet-retina-initial-instructions-vs.md) | Initial routing decisions and cautions for grading this examination (1000-series and 5000-series). |

### Terminology: Code Systems 

These define new code systems used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina Cautions](CodeSystem-retina-caution-cs.md) | Cautions to consider when grading examinations (5000-series). |
| [Retina Conclusion](CodeSystem-retina-conclusioncode-cs.md) | Codes for the current or final conclusion of the grading process (1000-series). |
| [Retina Image Quality](CodeSystem-retina-imagequality-cs.md) | Image quality as asessed by AI solution (2000-series). |

### Terminology: Naming Systems 

These define identifier and/or code system identities used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina Examination Id](NamingSystem-retina-examination-id.md) | ID identifying an examination. |
| [Retina Observation Id](NamingSystem-retina-observation-id.md) | ID identifying an observation associated with an examination. |

### Example: Example Instances 

These are example instances that show what data produced and consumed by systems conforming with this implementation guide might look like.

| | |
| :--- | :--- |
| [Bundle-SinglExamination-Example](Bundle-Bundle-SinglExamination-Example.md) | Result of query for a specific examination idfentified by ID containing no AI result. |
| [Bundle-TwoExaminations-Example](Bundle-Bundle-TwoExaminations-Example.md) | Result of query for examinations between two dates, not containing AI result. |
| [RetinaAIDevice-Example](Device-RetinaAIDevice-Example.md) | AI device that performed the automated retina analysis. |
| [RetinaAIDevice-input](Device-RetinaAIDevice-input.md) | AI device used for this analysis. |
| [RetinaAppendAIResultOperation-Example](Parameters-RetinaAppendAIResultOperation-Example.md) | Example request from client to append AI results to existing DiagnosticReport. |
| [RetinaCameraDevice-Example](Device-RetinaCameraDevice-Example.md) | TODO: Camera profile not defined yet. Camera device not used yet. |
| [RetinaDiagnosticReport-Example](DiagnosticReport-RetinaDiagnosticReport-Example.md) | Example after AI result is appended. Only one eye. |
| [RetinaDiagnosticReport-Example-PendingAI](DiagnosticReport-RetinaDiagnosticReport-Example-PendingAI.md) | Example of DiagnosticReport pending AI result. Does not have a previous examination. |
| [RetinaDiagnosticReport-Notification-Example](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md) | Notification from DIPS to external system that new retina examination is ready for AI grading. |
| [RetinaEyeObservation-Example-left](Observation-RetinaEyeObservation-Example-left.md) | Left eye assessment with DR, DME and image quality components. |
| [RetinaEyeObservation-Example-right](Observation-RetinaEyeObservation-Example-right.md) | Right eye assessment with DR, DME and image quality components. |
| [RetinaEyeObservation-input-left](Observation-RetinaEyeObservation-input-left.md) | Left eye assessment with DR and DME components. TODO: Why is 'not-asked' used in this example? |
| [RetinaEyeObservation-input-right](Observation-RetinaEyeObservation-input-right.md) | Right eye assessment with DR and DME components. |
| [RetinaHbA1cObservation-Example](Observation-RetinaHbA1cObservation-Example.md) | HbA1c level observation example. |
| [RetinaImagingStudy-available-Example](ImagingStudy-RetinaImagingStudy-available-Example.md) | An 'available' ImagingStudy updated by AI system. |
| [RetinaImagingStudy-registered-Example](ImagingStudy-RetinaImagingStudy-registered-Example.md) | A 'registered' ImagingStudy awaiting AI grading. |

