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
| [DIPSRetinaAppendOperationDefinition](OperationDefinition-append-retina-ai-result.md) | OperationDefinition for appending retina AI results to existing DiagnosticReport |

### Structures: Resource Profiles 

These define constraints on FHIR resources for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Diabetic Macular Edema Left Eye Observation](StructureDefinition-dme-left-eye-observation.md) | Observation for diabetic macular edema findings in the left eye |
| [Diabetic Macular Edema Right Eye Observation](StructureDefinition-dme-right-eye-observation.md) | Observation for diabetic macular edema findings in the right eye |
| [Diabetic Retinopathy Left Eye Observation](StructureDefinition-dr-left-eye-observation.md) | Observation for diabetic retinopathy findings in the left eye |
| [Diabetic Retinopathy Right Eye Observation](StructureDefinition-dr-right-eye-observation.md) | Observation for diabetic retinopathy findings in the right eye |
| [DiagnosticReport for Retinascreening](StructureDefinition-RetinaDiagnosticReport.md) | This report contains the results from a retina screening examination. |
| [FundusFotografiObservation](StructureDefinition-fundus-foto-observation.md) |  |
| [HbA1cObservation](StructureDefinition-hba1c-observation.md) |  |
| [OCTObservation](StructureDefinition-oct-observation.md) |  |
| [Observation for retina screening](StructureDefinition-RetinaObservation.md) | This is observations connected to RetinaDiagnosticReport |

### Structures: Extension Definitions 

These define constraints on FHIR data types for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Frist neste undersøkelse](StructureDefinition-frist-nesteundersokelse-extension.md) |  |
| [Image Quality](StructureDefinition-retina-imagequality-extension.md) | A coded extension representing the quality of a diagnostic image |
| [KI Product Name extension](StructureDefinition-ki-productname-extension.md) |  |
| [KI protokoll](StructureDefinition-ki-protokoll-extension.md) |  |
| [KI versjon algoritme](StructureDefinition-ki-versjon-algoritme-extension.md) |  |
| [Neste skritt i forløpet.](StructureDefinition-videre-forlop-extension.md) | Angir videre forløp |
| [Titaksstaus forrige undersøkelse Retina](StructureDefinition-tiltaksstatus-forrige-undersokelse-extension.md) | Angir om et tiltak er primært eller sekundært |

### Terminology: Value Sets 

These define sets of codes used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Conclusion Code ValueSet for Retinascreening](ValueSet-retina-conclusioncode-vs.md) | Allowed conclusion codes for DiagnosticReport |
| [Image Quality ValueSet for Retinascreening](ValueSet-retina-imagequality-vs.md) | Image quality as interpreted by an AI solution. |
| [Rapport for Retina-screening](ValueSet-diagnosticreport-codes-vs.md) | Rapporttype bildediagnsotikk fra Volven 8660 |
| [Verdisett for tiltaksstatus neste undersøkelse](ValueSet-tiltaksstatus-forrigeUndersokelse-vs.md) | Verdisett som beskriver verdier for forløpsstatus for neste undersøkelse for Retinascreening |
| [Verdisett for videre forløpsstudie](ValueSet-videre-forlop-vs.md) | Verdisett som beskriver videre forløp for Retinascreening. |

### Terminology: Code Systems 

These define new code systems used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Image Quality CodeSystem for Retinascreening](CodeSystem-retina-imagequality-cs.md) | Image quality as interpreted by an AI solution. |
| [Kodeverk for konklusjon etter KI-anlyse](CodeSystem-retina-conclusioncode-cs.md) | Verdisett som beskriver verdier for forløpsstatus for neste undersøkelse for Retinascreening etter KI |
| [NO Kodeverk 8660](CodeSystem-no-kodeverk-8660.md) | Tjenestetyper. Benyttes primært i forbindelse med rekvisisjoner og svarrapporter innenfor lab og røntgen. |
| [Verdisett for tiltaksstatus neste undersøkelse](CodeSystem-tiltakstatus-nesteundersokelse-cs.md) | Verdisett som beskriver verdier for forløpsstatus for neste undersøkelse for Retinascreening |
| [Videre forløp etter fotografering](CodeSystem-videre-forlop-cs.md) | Koder basert på hva fotografen velger i skjema. |

### Terminology: Naming Systems 

These define identifier and/or code system identities used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Retina examination identifier NamingSystem](NamingSystem-retina-examination-id.md) | NamingSystem that documents the canonical URL used for retina-examination-id identifiers in DIPS. |
| [Retina observation identifier NamingSystem](NamingSystem-retina-observation-id.md) | NamingSystem that documents the canonical URL used for retina-observation-id identifiers in DIPS. |

### Example: Example Instances 

These are example instances that show what data produced and consumed by systems conforming with this implementation guide might look like.

| | |
| :--- | :--- |
| [AddAIResultOperation](Parameters-AddAIResultOperation.md) | Example request from client to append AI results to existing DiagnosticReport |
| [BundleWithSinglExamination-Example](Bundle-BundleWithSinglExamination-Example.md) | Result of query for a specific examination idfentified by ID containing no AI result. |
| [BundleWithSingleExaminationAndAI-Example](Bundle-BundleWithSingleExaminationAndAI-Example.md) | Example response containing a single diagnostic report containing AI result. |
| [BundleWithTwoExaminations-Example](Bundle-BundleWithTwoExaminations-Example.md) | Result of query for examinations between two dates, not containing AI result. Note: The resource references in this example are not correct. |
| [NotificationFromDIPS-Example](DiagnosticReport-bb2690e7-ca9f-4070-9c35-c7e36976b144.md) | Notifikasjon fra DIPS |
| [Patient-cdp1123122](Patient-cdp1123122.md) |  |
| [Patient-cdp1123123](Patient-cdp1123123.md) |  |

