# Artifacts Summary - RetinaIntegration v0.5.0

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
| [Retina Diabetic Macular Edema Finding](StructureDefinition-retina-diabetic-macular-edema-finding.md) | Observation profile for documenting findings related to diabetic macular edema (DME) in retina examinations. |
| [Retina Diabetic Retinopathy Finding](StructureDefinition-retina-diabetic-retinopathy-finding.md) | Observation profile for documenting findings related to diabetic retinopathy (DR) in retina examinations. |
| [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md) | Diagnostic report for the grading process of a single examination which is part of a screening program. |
| [Retina HbA1c Observation](StructureDefinition-retina-hba1c-observation.md) | HbA1c level as reported by patient prior to retina examination. |
| [Retina Image Quality Assessment](StructureDefinition-retina-image-quality-asessment.md) | The image quality as assesed by AI (2000-series). |
| [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md) | Profile for imaging studies related to retina examinations, including fundus photography and OCT imaging. |

### Structures: Extension Definitions 

These define constraints on FHIR data types for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Cautions](StructureDefinition-cautions-extension.md) | Special considerations or cautions for grading this examination (5000-series). |
| [Days Until Next Examination](StructureDefinition-days-until-next-examination-extension.md) | Number of days until next examination. |
| [Previous Examination Conclusion](StructureDefinition-previous-examination-conclusion-extension.md) | The conclusion from the previous examination (1000 series). If this is the first examination, this extension is not present. |
| [Retinal Image View](StructureDefinition-retinal-image-view.md) | The centering or anatomical focus of a retinal image. |

### Terminology: Value Sets 

These define sets of codes used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina Body Site](ValueSet-retina-body-site-vs.md) | Body site codes for retinal observations (right or left retina). |
| [Retina Cautions](ValueSet-retina-caution-vs.md) | Special considerations or cautions for grading this examination (5000-series). |
| [Retina Conclusion](ValueSet-retina-conclusion-code-vs.md) | Codes describing the current or final conclusion of the examination (1000-series). |
| [Retina Image Quality](ValueSet-retina-image-quality-vs.md) | Image quality as assessed by AI (2000-series). |
| [Retina Image View](ValueSet-retina-image-view-vs.md) | Codes describing the centering used when capturing retinal images, such as macula-centered or optic disc-centered (6000-series). |
| [Retina Imaging Procedures](ValueSet-retina-imaging-procedure-vs.md) | Valid procedure codes for Retina imaging studies. Contains two Norwegian procedure codes from no-kodeverk-7275: CKDP10 for fundus photography and CKFX16 for OCT imaging of the eye fundus using light-wave based technique. |

### Terminology: Code Systems 

These define new code systems used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina Cautions](CodeSystem-retina-caution-cs.md) | Cautions to consider when grading examinations (5000-series). |
| [Retina Conclusion](CodeSystem-retina-conclusion-code-cs.md) | Codes for the current or final conclusion of the grading process (1000-series). |
| [Retina Image Quality](CodeSystem-retina-image-quality-cs.md) | Image quality as assessed by AI solution (2000-series). |
| [Retina Image View](CodeSystem-retina-image-view-cs.md) | Codes describing the centering used when capturing retinal images (6000-series). |

### Terminology: Naming Systems 

These define identifier and/or code system identities used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina DiagnosticReport Identifier System](NamingSystem-retina-diagnostic-report-ns.md) | IDs to identify retina diagnostic reports. |
| [Retina ImagingStudy Identifier System](NamingSystem-retina-imaging-study-ns.md) | IDs identifying imaging studies associated with a diagnostic report. Includes both internal GUIDs and Sectra image study IDs. |
| [Retina Observation Identifier System](NamingSystem-retina-observation-ns.md) | IDs identifying observations associated with a diagnostic report. |

### Example: Example Instances 

These are example instances that show what data produced and consumed by systems conforming with this implementation guide might look like.

| | |
| :--- | :--- |
| [Bundle-SingleExamination-Example](Bundle-Bundle-SingleExamination-Example.md) | A bundle containing a single DiagnosticReport with a single ImagingStudy awaiting AI result without any previous examination and without andy cautions. |
| [Bundle-TwoExaminations-Example](Bundle-Bundle-TwoExaminations-Example.md) | A bundle containing two DiagnosticReports with their corresponding ImagingStudies and HbA1cObservations. One DiagnosticReport has a previous examination and cautions, while the other does not. One report has two ImagingStudies. |
| [RetinaAIDevice-Example](Device-RetinaAIDevice-Example.md) | AI device that performed the automated retina analysis. |
| [RetinaAppendAIResultOperation-Example](Parameters-RetinaAppendAIResultOperation-Example.md) | Example request from client to append AI results to existing DiagnosticReport. |
| [RetinaCameraDevice-Example](Device-RetinaCameraDevice-Example.md) | TODO: Camera profile not defined yet. Camera device not used yet. |
| [RetinaDiabeticMacularEdemaFinding-Example-left](Observation-RetinaDiabeticMacularEdemaFinding-Example-left.md) | Left eye diabetic macular edema finding example. |
| [RetinaDiabeticMacularEdemaFinding-Example-right](Observation-RetinaDiabeticMacularEdemaFinding-Example-right.md) | Right eye diabetic macular edema finding example. |
| [RetinaDiabeticRetinopathyFinding-Example-left](Observation-RetinaDiabeticRetinopathyFinding-Example-left.md) | Left eye diabetic retinopathy finding example. |
| [RetinaDiabeticRetinopathyFinding-Example-right](Observation-RetinaDiabeticRetinopathyFinding-Example-right.md) | Right eye diabetic retinopathy finding example. |
| [RetinaDiagnosticReport-Example](DiagnosticReport-RetinaDiagnosticReport-Example.md) | Example after AI result is appended. Both eyes. |
| [RetinaDiagnosticReport-Example-PendingAI](DiagnosticReport-RetinaDiagnosticReport-Example-PendingAI.md) | Example of DiagnosticReport pending AI result. Does not have a previous examination. |
| [RetinaDiagnosticReport-Notification-Example](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md) | Notification from DIPS to external system that new retina examination is ready for AI grading. |
| [RetinaHbA1cObservation-Example](Observation-RetinaHbA1cObservation-Example.md) | HbA1c level observation example. |
| [RetinaImageQualityAssessment-Example-left](Observation-RetinaImageQualityAssessment-Example-left.md) | Left eye image quality assessment example. |
| [RetinaImageQualityAssessment-Example-right](Observation-RetinaImageQualityAssessment-Example-right.md) | Right eye image quality assessment example. |
| [RetinaImagingStudy-available-Example](ImagingStudy-RetinaImagingStudy-available-Example.md) | An 'available' ImagingStudy updated by AI system. |
| [RetinaImagingStudy-registered-Example](ImagingStudy-RetinaImagingStudy-registered-Example.md) | A 'registered' ImagingStudy awaiting AI grading. |

