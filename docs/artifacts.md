# Artifacts Summary - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* **Artifacts Summary**

## Artifacts Summary

This page provides a list of the FHIR artifacts defined as part of this implementation guide.

### Behavior: Capability Statements 

The following artifacts define the specific capabilities that different types of systems are expected to have in order to comply with this implementation guide. Systems conforming to this implementation guide are expected to declare conformance to one or more of the following capability statements.

| | |
| :--- | :--- |
| [DIPSRetinaCapabilityStatement](CapabilityStatement-DIPSRetinaCapabilityStatement.md) | CapabilityStatement for DIPS Retinaflyt |

### Behavior: Operation Definitions 

These are custom operations that can be supported by and/or invoked by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [DIPSRetinaAppendOperationDefinition](OperationDefinition-append-retina-ai-result.md) | OperationDefinition for appending retina AI results to existing DiagnosticReport. See AddAIResultOperation for an example of the input parameters. |

### Structures: Resource Profiles 

These define constraints on FHIR resources for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Diabetic Macular Edema Left Eye Observation](StructureDefinition-dme-left-eye-observation.md) | Observation for diabetic macular edema findings in the left eye. |
| [Diabetic Macular Edema Right Eye Observation](StructureDefinition-dme-right-eye-observation.md) | Observation for diabetic macular edema findings in the right eye. |
| [Diabetic Retinopathy Left Eye Observation](StructureDefinition-dr-left-eye-observation.md) | Observation for diabetic retinopathy findings in the left eye. |
| [Diabetic Retinopathy Right Eye Observation](StructureDefinition-dr-right-eye-observation.md) | Observation for diabetic retinopathy findings in the right eye. |
| [Fundus Photography Observation](StructureDefinition-fundus-foto-observation.md) | Wether fundus photography was performed or not. Will be true if fundus photos where taken. |
| [HbA1c Observation](StructureDefinition-hba1c-observation.md) | HbA1c level as reported by patient prior to retina examination. |
| [OCT Observation](StructureDefinition-oct-observation.md) | Wether Optical Coherence Tomography (OCT) was performed or not. Will be true if OCT was performed. |
| [Retina DiagnosticReport](StructureDefinition-RetinaDiagnosticReport.md) | This diagnostic report for the grading of a retina screening examination. |
| [Retina Observation](StructureDefinition-RetinaObservation.md) | Observations connected to RetinaDiagnosticReport. |

### Structures: Extension Definitions 

These define constraints on FHIR data types for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [AI Algorithm Version](StructureDefinition-ki-versjon-algoritme-extension.md) | Version of the AI algorithm used for analysis. |
| [AI Product Name](StructureDefinition-ki-productname-extension.md) | Name of the AI product used for analysis. |
| [AI Protocol](StructureDefinition-ki-protokoll-extension.md) | Protocol used by the AI solution for analysis. |
| [Deadline Next Examination](StructureDefinition-frist-nesteundersokelse-extension.md) | Number of days until next examination. |
| [Grading Pending](StructureDefinition-videre-forlop-extension.md) | Next step in grading this examination. (4000-series) |
| [Image Quality](StructureDefinition-retina-imagequality-extension.md) | A coded extension representing the quality of a diagnostic image. |
| [Next Examination Previous Examination](StructureDefinition-tiltaksstatus-forrige-undersokelse-extension.md) | The next step in the screening process after the previous examination. (3000-series) |

### Terminology: Value Sets 

These define sets of codes used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Grading Conclusion](ValueSet-retina-conclusioncode-vs.md) | Codes describing where the external client has landed in its assessment of the examination. (1000-series) |
| [Grading Pending](ValueSet-videre-forlop-vs.md) | Next step in grading this examination. (4000-series and 5000-series) |
| [Image Quality](ValueSet-retina-imagequality-vs.md) | Image quality as interpreted by an AI solution. (2000-series) |
| [Next Examination](ValueSet-tiltaksstatus-forrigeUndersokelse-vs.md) | Next step for this patient is a new examination. (3000-series) |

### Terminology: Code Systems 

These define new code systems used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Grading Cautions](CodeSystem-grading-caution-cs.md) | Cautions to consider when grading examinations. (5000-series) |
| [Grading Conclusion](CodeSystem-retina-conclusioncode-cs.md) | Codes describing where the external client has landed in its assessment of the examination. (1000-series) |
| [Grading Pending](CodeSystem-videre-forlop-cs.md) | Next step in grading this examination. (4000-series) |
| [Image Quality](CodeSystem-retina-imagequality-cs.md) | Image quality as interpreted by an AI solution. (2000-series) |
| [Next Examination](CodeSystem-tiltakstatus-nesteundersokelse-cs.md) | Next step for this patient is a new examination. (3000-series) |

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
| [AddAIResultOperation](Parameters-AddAIResultOperation.md) | Example request from client to append AI results to existing DiagnosticReport |
| [Bundle With Single Examination Containing AI Result](Bundle-BundleWithSingleExaminationAndAI-Example.md) | Example response containing a single diagnostic report containing AI result. |
| [Bundle With Single Examination Without AI Result](Bundle-BundleWithSinglExamination-Example.md) | Result of query for a specific examination idfentified by ID containing no AI result. |
| [Bundle With Two Diagnostic Reports](Bundle-BundleWithTwoExaminations-Example.md) | Result of query for examinations between two dates, not containing AI result. |
| [Notification From DIPS](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md) | Notification from DIPS to external client that new retina examination is ready for grading. |
| [Patient-cdp1123122](Patient-cdp1123122.md) | Example patient 2 |
| [Patient-cdp1123123](Patient-cdp1123123.md) | Example patient 1 |

