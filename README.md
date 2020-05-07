# Awesome taxonomyzoo list

A zoo of taxonomies for labelling domain names (as in [DNS](https://en.wikipedia.org/wiki/Domain_Name_System)) and IP addresses.


This repository collects and documents known taxonomies in the field of IT-Security ("Cyber") as well as known taxonomies for internet  research.
A taxonomy is a way of (potentially) labelling objects  (DNS domains or IP addresses) and giving them meaning. These labels are not exclusive. An object MAY have multiple labels and be categorized by multiple taxonomies.
Specifically, objects in this context are DNS domain names and/or IP addresses.

The list of taxonomies contains: 

  * the taxonomy name
  * a short description what it's about
  * a link to where it is defined (source)
  * an estimate for suitability for our use case of DNS names/IP addresses.
  * and some other meta-information

Naturally, this list will never be complete nor exhaustive. Therefore, we encourage your pull requests.

# Examples

  * The DHS (as in Dept. of Homeland Security) published a [taxonomy](https://github.com/MISP/misp-taxonomies/blob/master/dhs-ciip-sectors/machinetag.json) for labeling critical infrastructure industry sectors
  * The DNS Low Content domains: lists types of low content (e.g. parking domains, apache default web page, empty web page, etc.) domains
  
  
  
# Rules for labelling objects

1. Domain names or IP addresses MAY be labelled by one or more taxonomies.
2. A taxonomy is always represented as a triplet ``prefix:tag=value``. See the [MISP taxonomies](https://github.com/MISP/misp-taxonomies) explanation page. "Prefix" is the name of the taxonomy (i.e. a namespace for the tags), "tag" is the tag name (the label we want to assign to the domain or IP, for example: "phishing" for a phishing domain), "value" is optional and MAY further specify details for the tag.
3. A taxonomy MUST be representable in the [machine-tags](https://github.com/MISP/misp-taxonomies) readable format
4. a taxonomy which is to be considered useful for DNS names or IP addresses SHOULD be stable. A tag assignment to an IP address SHOULD be stable and not change frequently (e.g. once per quarter or year) or it should be computable on-the-fly.
5. There are two ways for assigning labels: a) manually or b) automatically. The latter implies that a taxonomy MUST only be used if the assignment of labels can be done by an algorithm with high success rates (and low false positive rates). Otherwise we consider a taxonomy *non-actionable*.

![Machine Tag visual explanation](https://github.com/MISP/misp-taxonomies/blob/master/tools/docs/images/taxonomy-explanation.png)

# Hierarchies for taxonomies

Sometimes taxonomy A is an abstraction of taxonomy B. Example: B==list of industry sectors, A=={ domain represents a private web page or it represents a company}. Obviously B is a sub-specialisation of A.

We decided for now to not represent these hierarchies in order to keep it simple.


  
# The list

| Name               | Description    | actionable? | automatic classification  |  stable?        | Link           | 
|:-------------------|:---------------|:-----------:|:--------------------------|:----------------|:---------------|
| DHS CIIP           | Dept. of Homeland Security Critical Infrastructure Sectors list | ? | | Y | https://github.com/MISP/misp-taxonomies/blob/master/dhs-ciip-sectors/machinetag.json |
| RSIT               | Reference Security Incident Taxonomy | partly | | no, usually cleaned up quickly | https://github.com/MISP/misp-taxonomies/blob/master/rsit/machinetag.json|
|MISP domain abuse   | List of tags for labelling DNS names which have been observed in abuse. Partly also deals with a domain's status (i.e. active, suspended, etc.) | partly | partly | Y | https://github.com/MISP/misp-taxonomies/blob/master/domain-abuse/machinetag.json|
