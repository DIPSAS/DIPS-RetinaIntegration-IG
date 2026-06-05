# Changelog - RetinaIntegration v0.9.0

## Changelog

### Change Log

The changelog gives an overview of the change history of this implementation guide.

### Version 0.9.0-CI (2026-06-05)

* Add state transition table and other documentation to the append-retina-ai-result operation
* Change conclusion code 1006 description to 'pausing screening program for patient'
* Add conclusion code 1007 for 'discharging patient from screening program'
* Add value set retina-append-ai-conclusion-vs limiting changes by the append operation (1000 series)

### Version 0.8.1-CI (2026-05-08)

* Document business rules and HTTP result codes in append operation
* Add Norwegian texts and adjust English text for codes system retina-ai-gradability-cs
* Link `conclusion` parameter to documentation of value set retina-conclusion-code-vs
* Use a decimal value in the leftDiabeticRetinopathy example

### Version 0.8.0-CI (2026-04-17)

* Renamed parameter `daysUntilNextExamination` to `monthsUntilNextExamination`
* Add code system and value set for gradability
* Add parameters leftGradability and rightGradability using gradability codes

### Version 0.7.0-CI (2026-03-31)

* Add optional parameter `cameraDevice` to the append operation.
* Add optional parameter `performedDateTime` for date and time when the retinal AI analysis was performed.
* Make `aiDevice` and `sectraStudyId` optional parameters in append operation.
* Correct small mistakes in diagrams.
* Adjust menu slightly.

### Version 0.6.0-CI (2026-02-03)

* Added query operation `retina-by-date` 
* Parameters `start`, `end` and `pendingAI`
 
* Changes in append operation `append-retina-ai-result` 
* Simplified API using primitive data types
* Added profile RetinaImageParameter for describing images
 
* Added Patient identifier examples to RetinaDiagnosticReport
* Restructured documentation 
* Data in a separate page
* Added report lifecycle state diagram
* Added operations to main menu
 

### Version 0.5.0-CI (2025-12-18)

* Changed DiagnosticReport previousExaminationConclusion extension to only take one Coding, not a CodeableConcept 
* Structure of extension is simplified. See examples.
 
* Correct confusion between naming system ID and the IDs defined by the naming system. 
* In observation identifiers, system `http://dips.no/fhir/NamingSystem/retina-observation-id` is replaced by `http://dips.no/fhir/RetinaIntegration/observation-id`
 
* Add naming system for ImagingStudy. 
* In all ImagingStudy identifiers, system `http://sectra.no/identifiers` is replaced by `http://dips.no/fhir/RetinaIntegration/sectra-image-study-id`
 
* Add patient identifier OID examples to DiagnosticReport profile. 
* There are different OIDs for `Fødeselsnummer`, `D-nummer` and `Felles hjelpenummer.
 
* Add subject references Patient to alle examples.

### Version 0.4.0-CI (Release 2025-12-08)

* Organize images for left and right eye in two series specified by ImagingStudy.Series.bodySite
* Add extension to image instance for specifying 'view', macular or optical disc centring, 6000 series
* Add terminology for image view, macular or optical disc centring, used in image instances (6000 series)
* Let DiagnosticReport.code be the retina imaging procedure(s) requested: fundus photography and/or OCT.
* Add extension 'cautions' for the 5000-series codes to diagnostic report.
* Remove extension 'initialInstructions' as conclusionCode contains the initial workflow step.
* Change id for retina-image-quality value system and code system for consistency.
* Change name to CodeSystem with capital S (best practice).
* Rename and change ID of RetinaConclusionCode code and value system for consistency (best practice).
* Add changelog and specify version on all profiles
* Fix bundle examples for diagnostic reports in `partial` state

### Version 0.3.0-CI (Release 2025-12-02)

#### Drivers for making changes

* Missing description of image quality. This is an Observation base on a the images in an image series
* Need to cluster AI device information into a single object, both in model and in parameter

#### Model changes

* Added device RetinaAIDevice
* Replace meta tag MLTRAINING with VALIDATION
* Added ImagingStudy profile
* Moved sectraIDs from DiagnosticReport to ImagingStudy
* Add optional procedure codes for OCT and Fundus to ImagingStudy
* Remove OCT and Fundus as separate observations
* Replace left and right specific profiles with profiles where bodySite has to be specified
* Add ImageQuality as separate observation (evaluation by AI system)
* Renamed `videreForløp` extension to `initialInstruction`
* Rename RetinaTiltaksstausForrigeUndersokelseExtension to PreviousExaminationConclusionCode
* Rename kiFristNesteUndersokelse to daysUntilNextExamination
* Resource IDs are renamed for consistency
* Consolidated terminology: removed code systems 3000 and 4000 series. Previous conclusion and initial instruction now use 1000 series.
* All ID's are kebab-case

#### Operation changes

* Added AIDevice, replacing KI product name, version algorithm and protocol
* Rename all parameter names to pascal case (FHIR best practice)

#### Documentation

* Added diagram of FHIR model
* Added diagram of systems and users
* Added more examples
* Added camera device example for use in later version
* Added more documentation in english
* Spelling corrected

#### Internal changes

* Reorganized FHIR shorthand files (split large files)

### Version 0.2.0-CI (Release 2025-12-01)

This version was withdrawn. It bundled together all observation of an eye as components in a single observation EyeObservation. This goes against the grain of the FHIR modelling philosophy that the model should be flat. It would severely limit our ability to expand the model in the future.

### Version 0.1.3-CI (Released 2025-11-16)

* Add code system grading-caution-cs (5000 series)

### Version 0.1.3-CI (Released 2025-11-11)

* Add videre-forlop-extension with cods from videre-forlop-cs to examples. Chagnge some titles.

### Version 0.1.3-CI (Released 2025-11-08)

Version 0.1.3 released on new url https://dipsas.github.io/DIPS-RetinaIntegration-IG/

### Version 0.1.3-CI (Released 2025-10-31)

### Version 0.1.2-CI (Release 2025-10-19)

### Version 0.1.1-CI (Release 2025-10-07)

