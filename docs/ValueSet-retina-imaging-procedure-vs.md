# Retina Imaging Procedures - RetinaIntegration v0.6.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Retina Imaging Procedures**

## ValueSet: Retina Imaging Procedures 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/ValueSet/retina-imaging-procedure-vs | *Version*:0.6.0 |
| Draft as of 2025-12-02 | *Computable Name*:RetinaImagingProcedureValueSet |

 
Valid procedure codes for Retina imaging studies. Contains two Norwegian procedure codes from no-kodeverk-7275: CKDP10 for fundus photography and CKFX16 for OCT imaging of the eye fundus using light-wave based technique. 

 
This ValueSet constrains the procedureCode element in RetinaImagingStudy to only allow the two imaging modalities used in diabetic retinopathy screening programs: fundus photography for capturing retinal images and OCT for detailed structural examination of the retina and macula. 

 **References** 

* [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

### Logical Definition (CLD)

 

### Expansion

No Expansion for this valueset (not supported by Publication Tooling)

-------

 Explanation of the columns that may appear on this page: 

| | |
| :--- | :--- |
| Level | A few code lists that FHIR defines are hierarchical - each code is assigned a level. In this scheme, some codes are under other codes, and imply that the code they are under also applies |
| System | The source of the definition of the code (when the value set draws in codes defined elsewhere) |
| Code | The code (used as the code in the resource instance) |
| Display | The display (used in the*display*element of a[Coding](http://hl7.org/fhir/R4/datatypes.html#Coding)). If there is no display, implementers should not simply display the code, but map the concept into their application |
| Definition | An explanation of the meaning of the concept |
| Comments | Additional notes about how to use the code |



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-imaging-procedure-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-imaging-procedure-vs",
  "version" : "0.6.0",
  "name" : "RetinaImagingProcedureValueSet",
  "title" : "Retina Imaging Procedures",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-02",
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
  "description" : "Valid procedure codes for Retina imaging studies. Contains two Norwegian procedure codes from no-kodeverk-7275: CKDP10 for fundus photography and CKFX16 for OCT imaging of the eye fundus using light-wave based technique.",
  "purpose" : "This ValueSet constrains the procedureCode element in RetinaImagingStudy to only allow the two imaging modalities used in diabetic retinopathy screening programs: fundus photography for capturing retinal images and OCT for detailed structural examination of the retina and macula.",
  "compose" : {
    "include" : [
      {
        "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
        "concept" : [
          {
            "code" : "CKDP10",
            "display" : "Fundusfotografi"
          },
          {
            "code" : "CKFX16",
            "display" : "Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk"
          }
        ]
      }
    ]
  }
}

```
