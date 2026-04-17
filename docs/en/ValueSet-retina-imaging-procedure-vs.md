# Retina Imaging Procedures - RetinaIntegration v0.8.0

## ValueSet: Retina Imaging Procedures 

 
Valid procedure codes for Retina imaging studies. Contains two Norwegian procedure codes from no-kodeverk-7275: CKDP10 for fundus photography and CKFX16 for OCT imaging of the eye fundus using light-wave based technique. 

 **References** 

* [Retina DiagnosticReport](StructureDefinition-retina-diagnostic-report.md)
* [Retina ImagingStudy](StructureDefinition-retina-imagingstudy.md)

### Logical Definition (CLD)

 

### Expansion

No Expansion for this valueset (Unknown Code System)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "retina-imaging-procedure-vs",
  "url" : "http://dips.no/fhir/RetinaIntegration/ValueSet/retina-imaging-procedure-vs",
  "version" : "0.8.0",
  "name" : "RetinaImagingProcedureValueSet",
  "title" : "Retina Imaging Procedures",
  "status" : "draft",
  "experimental" : false,
  "date" : "2025-12-02",
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
  "description" : "Valid procedure codes for Retina imaging studies. Contains two Norwegian procedure codes from no-kodeverk-7275: CKDP10 for fundus photography and CKFX16 for OCT imaging of the eye fundus using light-wave based technique.",
  "purpose" : "This ValueSet constrains the procedureCode element in RetinaImagingStudy to only allow the two imaging modalities used in diabetic retinopathy screening programs: fundus photography for capturing retinal images and OCT for detailed structural examination of the retina and macula.",
  "compose" : {
    "include" : [{
      "system" : "http://ehelse.no/fhir/CodeSystem/no-kodeverk-7275",
      "concept" : [{
        "code" : "CKDP10",
        "display" : "Fundusfotografi"
      },
      {
        "code" : "CKFX16",
        "display" : "Undersøkelse av øyenbunnsstruktur med lysbølgebasert teknikk"
      }]
    }]
  }
}

```
