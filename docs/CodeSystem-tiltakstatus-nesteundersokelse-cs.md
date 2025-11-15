# Next Examination - RetinaIntegration v0.1.3

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Next Examination**

## CodeSystem: Next Examination (Experimental) 

| | |
| :--- | :--- |
| *Official URL*:http://dips.no/fhir/RetinaIntegration/CodeSystem/tiltakstatus-nesteundersokelse-cs | *Version*:0.1.3 |
| Draft as of 2025-11-15 | *Computable Name*:TiltakStatusForrigeUndersokelseCodeSystem |

 
Next step for this patient is a new examination. (3000-series) 

 This Code system is referenced in the content logical definition of the following value sets: 

* [TiltaksstatusForrigeUndersokelseValueSet](ValueSet-tiltaksstatus-forrigeUndersokelse-vs.md)



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "tiltakstatus-nesteundersokelse-cs",
  "url" : "http://dips.no/fhir/RetinaIntegration/CodeSystem/tiltakstatus-nesteundersokelse-cs",
  "version" : "0.1.3",
  "name" : "TiltakStatusForrigeUndersokelseCodeSystem",
  "title" : "Next Examination",
  "status" : "draft",
  "experimental" : true,
  "date" : "2025-11-15T17:14:08+01:00",
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
  "description" : "Next step for this patient is a new examination. (3000-series)",
  "caseSensitive" : true,
  "content" : "complete",
  "count" : 3,
  "concept" : [
    {
      "code" : "3001",
      "display" : "Ny fotokontroll (primærgradering)"
    },
    {
      "code" : "3002",
      "display" : "Ny fotokontroll (sekundærgradering)"
    },
    {
      "code" : "3003",
      "display" : "Ingen registrert tidligere undersøkelser"
    }
  ]
}

```
