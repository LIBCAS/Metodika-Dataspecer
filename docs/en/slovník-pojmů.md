# Glossary

The glossary contains an overview of basic terms used in data modeling in the [Dataspecer tool](dataspecer.md).

## Application Profile
In metadata modeling, an application profile is a specialized set of rules and specifications that modifies the use of existing metadata schemas or standards for a specific purpose, domain, or organization. It is not a new metadata standard, but a combination and modification of existing elements to meet specific needs.

## Attribute
In data modeling, an attribute represents a specific property of a class (entity) that describes a certain detail or aspect of its instance. Each attribute has a designated name, data type, and may have additional rules such as mandatory completion or repeatability. For example, in the `Address` class, there may be attributes such as `full address`, `post code`, `post name`, `locator designator` (numerical designation, e.g., house number), or `locator name` (street name). The attributes `latitude` and `longitude` belong to the `Geometry` class and serve for spatial determination of the address. Each of these attributes captures specific information about the address and together they form a structured description of data that can be unambiguously interpreted and machine-processed. For example, a specific address may have:

```text
post code = "110 00"
locator name = "Národní"
latitude = "50.087"
```
Each of these data is a value assigned to its attribute.

## International Resource Identifier (IRI)
A unique identifier used to designate resources on the web, which, unlike `URI` (Uniform Resource Identifier), allows the use of characters from the full Unicode character set – including letters with diacritics, Cyrillic, Chinese characters, etc.
IRI is used especially in the semantic web environment, RDF, ontologies, and metadata models, where it ensures globally unique and readable identification of concepts, classes, or instances.

Example:
```text
https://data.město.cz/osoby/Jiří_Černý
```

## Cross-Origin Resource Sharing (CORS)
**Cross-Origin Resource Sharing (CORS)** is a security mechanism using HTTP headers that allows web applications to access resources (e.g., APIs or datasets) on different domains than those on which they were loaded. By default, browsers restrict such cross-border requests to protect user data, but through CORS, a server can explicitly allow access from other trusted domains. This mechanism is important especially when making open data available to end users or frontend applications.

CORS behavior is described in the [Fetch Standard (WHATWG) specification](https://fetch.spec.whatwg.org/#http-cors-protocol) and practical explanations and examples can be found on [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS).

## Cardinality
Cardinality in data modeling determines how many times a certain relationship or property between two classes can or must be used. In other words, it describes the number of occurrences that are allowed or required between objects.

For example, if a dataset (`Dataset`) has a `title` property, cardinality `1..1` means it must have exactly one title. If the cardinality were `0..*`, it could have zero, one, or more titles.

Cardinality is often written in the format:

```text
0..1 – at most one occurrence (optional)
1..1 – exactly one occurrence (mandatory)
0..* – any number of occurrences (including zero)
1..* – at least one occurrence
```

## RDF
(Resource Description Framework) is a standard for data representation that serves to describe information using triples in the form subject–predicate–object. Each triple expresses one statement about some resource, where all elements can be uniquely identified using URI. RDF is often used to link data from different sources and forms the basis of the semantic web.

Example triple:
```text
<http://example.org/JanNovak> <http://schema.org/jobTitle> "analyst"
```
says that Jan Novák has the job title analyst.

RDF is often written in TTL (Turtle) format. For example, the notation:
```turtle
ex:JanNovak schema:jobTitle "analyst"
```
says that Jan Novák has the job title "analyst".

## Semantic Data Specifications
A semantic data specification is a formal description of a data structure that, in addition to the technical definition of data (e.g., types, attributes, relationships), also includes the meaning of this data in a specific domain context. The goal is to ensure unambiguous interpretation and correct understanding of data across different systems, organizations, and users. Such a specification often uses standards such as ontologies, data vocabularies, or models like `RDF`/`OWL`, which enable linking data with their semantics and thus support interoperability, validation, and automated processing.

## Specialization

## Vocabulary
A vocabulary is a collection of formally defined concepts (e.g., classes, attributes, and relationships) that serve to describe data structures and metadata. The vocabulary contains specific semantic elements that can be reused across different data models. In the vocabulary, concepts are uniquely identified (e.g., URI) and often derive from existing standards (e.g., `DCAT`, `Dublin Core`, `DataCite`, `FOAF`).

## Class
A class in data modeling designates a type of objects that share the same properties and meaning. It is used to describe data categories such as `persons`, `addresses`, `documents`, or `distribution files`. Each specific object in the data is an instance of some class. Classes can be hierarchically arranged (e.g., subclasses) and can have assigned attributes and relationships.

## Relationship
Describes relationships between two classes of the application profile.

Example:
```text
Dataset has funding reference
```