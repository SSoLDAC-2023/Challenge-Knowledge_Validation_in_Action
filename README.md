# Challenge: The essence of (digital) Knowledge / Knowledge Validation in Action

## Champions
- Nicholas Nisbet, AEC3 UK Ltd (UK)
- Mathias Bonduel, Neanex (BE)

## Challenge description
The starting point of this challenge is a general contemplation on the essence of “knowledge”, which has occupied philosophers for centuries: what is knowledge, can something ever truly be “known”? E.g. Plato considered knowledge “justified true belief”, consisting of either Facts or Techniques, while Popper modelled scientific knowledge as being falsifiable. Both terms “belief” and “falsifiable” indicate an acceptance that there is a certain degree of uncertainty to knowledge.

This challenge considers the digital consequences of the above-mentioned theories of knowledge. Are semantic statements sufficient to represent “knowledge” in a digital environment; can the truthfulness of these statements be verified/falsified or at least their uncertainty assessed?

Practically, several technologies have been devised over the last decades to digitally model semantic statements about the real world, as well as validating them against a given set of rules. In context of the Semantic Web, statements will be made using the Resource Description Framework, resulting in a directed graph. Querying these graphs happens using the SPARQL Protocol and RDF Query Language, validating them against a set of conditions can be done using the W3C standard SHACL.

Previous research has shown that SHACL is a valid approach towards validation of Linked Building Data. However, currently the creation of SHACL shapes happens manually, requiring a structured workflow, and a thorough understanding of the standard and the vocabularies which are used to create semantic statements. SHACL editors can be applied to help creating correct SHACL (or SPARQL) through a (graphical) user interface. While such tools are certainly practically relevant, another approach could be to start from one or multiple existing RDF datasets to derive the required graph patterns and formalize them in correct SHACL shapes.

Specifically in context of the built environment, we focus on checking the presence or absence of objects in a building, on the granularity level of rooms. This may relate to regulations as well as to client requirements. Information needed may include (but is not limited to) the room type and the requirements to be checked, e.g. is there a minimal amount of fire extinguishers in a room, or is the maximum amount of seats for a given area not exceeded?

## Challenger research questions
- Can you build an application interface that helps people to kickstart the creation of the SHACL shapes starting from example data? Would it help to also have example datasets used by the tool that includes some “wrong” graph patterns?
- As an example scenario related to building data, you may base upon the above-mentioned allocation of objects in spaces: can we formalise regulations or client requirements regarding which rooms contain which objects, and which objects are in which rooms? Would topological statements be sufficient, or is a more spatial approach necessary (e.g. including cartesian coordinates of an object)?
- Finally, can you critically reflect on how the outcome (i.e., shapes, datasets or interfaces) demonstrates one (or more) of the above-mentioned philosophical theories about (non-)knowledge and uncertainty?

## Datasets
- Building datasets in TTL: duplex, schependomlaan, …
- Generate your own dataset

## Supplementary Resources

1. The approach to generate SHACL shapes can be similar to several tools that help users to create a JSON schema starting from a piece of available JSON (example) data:

    - [extendsclass.com/json-schema-validator.html](https://extendsclass.com/json-schema-validator.html) 
    - [github.com/krg7880/json-schema-generator](https://github.com/krg7880/json-schema-generator) 
    - [github.com/simplymequeeny/json-string-schema-generator](https://github.com/simplymequeeny/json-string-schema-generator)

2. A first step of formalizing knowledge is the compaction of information into qualified rules, which can be done using the RASE framework. RASE says knowledge is a hierarchy of objectives containing objectives and metrics classified as Requirement/Register/Record, Application, Selection, or Exception. Each of these is a predicate-relationship with a target. A Semantic Data subject is an Applicability it is own right.

- [www.aec3.eu/require1/Help_en-GB/index.html](http://www.aec3.eu/require1/Help_en-GB/index.html)
- HJELSETH, Eilif; NISBET, Nick. Capturing normative constraints by use of the semantic mark-up RASE methodology. In: Proceedings of CIB W78-W102 Conference. 2011. p. 1-10.
- NISBET, Nicholas, et al. Presentations of rase knowledge mark-up. In: EC3 Conference 2022. University of Turin, 2022. p. 0-0.

## Tools Needed

    - Code editor
    - SHACL validation engine
    - Semantic platform (triple store / LDP / …)
