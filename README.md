# Awesome taxonomyzoo list

A zoo of taxonomies for labelling domain names (as in [DNS](https://en.wikipedia.org/wiki/Domain_Name_System)) and IP addresses.


This repository collects and documents known taxonomies in the field of IT-Security ("Cyber") as well as internet wide research.
A taxonomy is a way of (potentially) labelling objects and giving them meaning. These labels are not exclusive. An object MAY have multiple labels and be categorized by multiple taxonomies.
Specifically, objects in this context are DNS domain names and/or IP addresses.

The list of taxonomies contains: 

  * the taxonomy name
  * a link to where it is defined (source)
  * an estimate for suitability for our use case of DNS names/IP addresses.

Naturally, this list will never be complete nor exhaustive. Therefore, we encourage receiving pull requests.

# Examples

  * The DHS (as in Dept. of Homeland Security) published a [taxonomy](https://github.com/MISP/misp-taxonomies/blob/master/dhs-ciip-sectors/machinetag.json) for labeling critical infrastructure industry sectors
  * The DNS Low Content domains: lists types of low content (e.g. parking domains, apache default web page, empty web page, etc.) domains
  
  
  
# Rules for labelling objects

1. Domain names or IP addresses MAY be labelled by one or more taxonomies.
2. A taxonomy is always represented as a triplet ``prefix:tag=value``. See the [MISP taxonomies](https://github.com/MISP/misp-taxonomies) explanation page
3. A taxonomy MUST be representable in the [machine-tags](https://github.com/MISP/misp-taxonomies) readable format
4. a taxonomy which is to be considered useful for DNS names or IP addresses SHOULD be stable. A label assignment SHOULD be stable and not change frequently (e.g. once per quarter or year)
5. There are two ways for assigning labels: a) manually or b) automatically. The latter implies that a taxonomy MUST only be used if the assignment of labels can be done by an algorithm with high success rates (and low false positive rates). Otherwise we consider a taxonomy *non-actionable*.


  
# The list

| Name               | Description    | actionable? | automatic classification  |  stable?        | Link           | 
|:-------------------|:---------------|:-----------:|:--------------------------|:----------------|:---------------|
| DHS CIIP           | Dept. of Homeland Security Critical Infrastructure Sectors list | ? | | Y | https://github.com/MISP/misp-taxonomies/blob/master/dhs-ciip-sectors/machinetag.json |
| RSIT               | Reference Security Incident Taxonomy | partly | | no, usually cleaned up quickly | https://github.com/MISP/misp-taxonomies/blob/master/rsit/machinetag.json|
