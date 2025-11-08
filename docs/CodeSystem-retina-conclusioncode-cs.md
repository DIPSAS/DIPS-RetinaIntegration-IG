# Kodeverk for konklusjon etter KI-anlyse - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Kodeverk for konklusjon etter KI-anlyse**

## CodeSystem: Kodeverk for konklusjon etter KI-anlyse (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs | *Version*:0.1.3 |
| Draft as of 2025-11-08 | *Computable Name*:RetinaConclusionCodesystem |

 
Verdisett som beskriver verdier for forløpsstatus for neste undersøkelse for Retinascreening etter KI 

 This Code system is referenced in the content logical definition of the following value sets: 

* [RetinaConclusionCodeValueset](ValueSet-retina-conclusioncode-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "retina-conclusioncode-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/retina-conclusioncode-cs",
  "version" : "0.1.3",
  "name" : "RetinaConclusionCodesystem",
  "title" : "Kodeverk for konklusjon etter KI-anlyse",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-11-08T17:39:22+01:00",
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
  "description" : "Verdisett som beskriver verdier for forløpsstatus for neste undersøkelse for Retinascreening etter KI",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 3,
  "concept" : [
    {
      "code" : "1001",
      "display" : "Ferdig etter KI"
    },
    {
      "code" : "1002",
      "display" : "Til manuell primærgradering etter KI"
    },
    {
      "code" : "1003",
      "display" : "Til sekundærgradering etter KI"
    }
  ]
}

```
