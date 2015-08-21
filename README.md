# A RESTful Application Programming Interface for AMWA's AS-02

**This is work in progress, it will change and has not been adequately reviewed.**

* [AMWA](http://www.amwa.tv) WIP: 2
* Category: Work in progress - candidate Proposed Specification
* Author: [R. I. Cartwright](<richard.cartwright@quantel.com>), [Quantel Ltd](http://www.quantel.com/)
* Date: July 2015
* License: [Apache 2.0](../master/LICENSE.TXT), see [NOTICE](../master/NOTICE.TXT) 
* [IPR Policy](http://www.amwa.tv/about/policies/AMWA_IPR_Policy_V3.0.pdf): [Quantel contribution form](../master/RFC2_Quantel_Contribution.pdf)

## Abstract

A RESTful API (AMWA interface specification) for the creation, reading, updating and deleting of [AS-02] bundles and the 
assets that they contain. The aim of the API is that it makes the use of and testing of AS-02-based applications more efficient 
by separating the concerns of storing and retrieving media data from the mechanics of the underlying store, enabling the originally 
intended versioning workflows. 

## Introduction

A RESTful API (AMWA interface specification) for the creation, reading, updating and deleting of [AS-02] bundles and the assets 
that they contain. The aim of the API is that it makes the use of and testing of [AS-02]-based applications more efficient by 
separating the concerns of storing and retrieving media data from the mechanics of the underlying store, enabling the originally 
intended versioning workflows. The API will provide:

* an interface that abstracts developers from the detail of working with the underlying byte formats of MXF files and maintaining 
  manifest files, loosely coupling the AS-02 application and store;
* a means to dynamically change bundles by growing files, adding new audio tracks, working with vendor-specific data in the extras 
  folder;
* support for common read and write operations over units of essence - such as frames, samples and timecodes - and metadata 
  structures, providing a stateless view into what is stored inside the MXF files.

A common interface at this level provides a new media-rich interoperability point between applications and storage, where that storage 
can be interchanged between local disk, tiered storage, distributed file systems (e.g. GPFS) or object storage. As a REST API, the interface 
can take advantage of Internet-scaling techniques such as web caches and/or load balancing.

## Specification Method

The API is specified and documented using the [RAML Specification] v0.8.
The specification is contained in file ["as02.raml"](../master/as02.raml).
    	
The RAML specification makes use of [XML Schema] and [JSON LD Schema].

## Acknowledgements

The author would like to thank the board and members of the AMWA and members of the AMWA RFC Committee for their assistance during
the experimental phase of development of the new AMWA process. 

## References

> Work out how to format these.

```
[AS-02]: http://www.amwa.tv/downloads/specifications/AMWA-AS-02-10-2011-11-18_MXF_Versioning.pdf
[RAML Specification]: http://raml.org/spec.html
[XML Schema]: http://www.w3.org/TR/xmlschema11-1/
[JSON LD Schema]: https://developers.google.com/schemas/formats/json-ld
```

[AS-02]: http://www.amwa.tv/downloads/specifications/AMWA-AS-02-10-2011-11-18_MXF_Versioning.pdf
[RAML Specification]: http://raml.org/spec.html
[XML Schema]: http://www.w3.org/TR/xmlschema11-1/
[JSON LD Schema]: https://developers.google.com/schemas/formats/json-ld

## Authors' Addresses

> Use two spaces at the end of each line to request a linebreak.

Dr Richard Cartwright  
Quantel Ltd  
Turnpike Road  
Newbury  
Berkshire  
RG14 2NX  
<richard.cartwright@quantel.com>

## Appendix: Links to useful tools

The following tools were used in the preparation of this specification:

* [RAML API Designer](https://github.com/mulesoft/api-designer)
* [raml2html](https://github.com/kevinrenskers/raml2html)
* [JSON Schema Lint](http://jsonschemalint.com/draft4/#")
* [JSON Lint](http://jsonlint.com/)

