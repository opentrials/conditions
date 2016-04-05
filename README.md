# Condition Databases

[![Gitter](https://img.shields.io/gitter/room/opentrials/chat.svg)](https://gitter.im/opentrials/chat)
[![Issues](https://img.shields.io/badge/issue-tracker-orange.svg)](https://github.com/opentrials/opentrials/issues)
[![Docs](https://img.shields.io/badge/docs-latest-blue.svg)](http://docs.opentrials.net/en/latest/developers/)

A Data Package which is a database of public and private sources of
information on health conditions related to clinical trials.

How will we take info from these multiple resources to create a new, normalized list of health conditions?

Normalized lists of health conditions have been created by the Unified
Medical Language System
(https://www.nlm.nih.gov/research/umls/quickstart.html).  The UMLS
maps between various “controlled vocabularies” e.g. MeSH, SNOMED-CT
and ICD-10.  This is free to use, but come with license terms.

My recommendation as a first pass is to adopt MeSH as the primary
database of health condition terms.  It is freely downloadable as XML.
It is directly used by ClinicalTrials.gov and therefore will cover a
large amount of the clinical trials we will have in OpenTrials.

As an example, the CT.gov trial NCT02640105 has the following XML bits:

```xml
<condition>Cluster Headache</condition>
...
<condition_browse>
    <!-- CAUTION:  
The following MeSH terms are assigned with an imperfect algorithm  
    -->
    <mesh_term>Cluster Headache</mesh_term>
    <mesh_term>Headache</mesh_term>
</condition_browse>
```

We can look up “Cluster Headache” in the [MeSH database](https://www.nlm.nih.gov/cgi/mesh/2016/MB_cgi?term=cluster%20headache):




