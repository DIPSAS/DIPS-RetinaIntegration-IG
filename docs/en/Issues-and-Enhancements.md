#  - RetinaIntegration v0.9.0

## 

### Issues and Future Enhancements

Just some quick notes about the known issues and further enhancements.

### Issues

* VALIDATION tag is missing in the diagrams and model description.

### Enhancements

#### Model the EyeFlow device as Result Integrator Device

Presented in review meeting 2025-12-09

* new Observation for conclusion of the AI-system
* RI-device is performer of the resulting evaluation based on the findings of the AI-device and the blood observation
* RIObservation should store the metaTag, VALIDATION, because it may be different for each evaluation.

This enables:

* Examining what AI conclusion was when it differs from the `DiagnosticReport.conclusionCode`
* Append conclusions for several imaging studies, even if only one of them has been

On the backend we need to store and retrieve the RI-observation.

Positivt til device for integration platform, men det er ikke plattformen som er devicen, det er en integrasjonsapplikasjon, men vi kan ikke kalle den IADevice, for vi har en AIDevice fra før.

AI suggests name: "AI Result Integrator". Let us call it ResultIntegrator or `RIDevice`

RI Device is responsible for the following:

* Matches AI results to the correct DiagnosticReport
* Evaluates the grading
* Consolidates/integrates the data back into the report

