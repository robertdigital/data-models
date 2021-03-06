# Smart Data Models

Umbrella Repository for Data Models

**Note: This Repository does not accept Pull Requests concerning Data Models.
Pull Requests concerning Data Models shall be made against the corresponding
Data Model Repository**

[![Status badge](https://img.shields.io/badge/status-draft-red.svg)](RELEASE_NOTES)
[![Build badge](https://img.shields.io/travis/smart-data-models/data-models.svg "Travis build status")](https://travis-ci.org/smart-data-models/data-models/)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

:dart: [Roadmap](roadmap.md)

The availability of widely adopted (de-facto standard) information models is key
for creating a global digital single market of interoperable and replicable
(portable) IoT-enabled smart solutions in multiple domains (smart cities, smart
agrifood, smart utilities, smart industry, …). Such models provide an essential
element in the common technical ground needed for standards-based open
innovation and procurement.

Data Models play a crucial role because they define the **harmonised
representation formats and semantics** that will be used by applications both to
consume and to publish data.

The **FIWARE Foundation** and **TM Forum** are leading a joint collaboration
program to support the adoption of a reference architecture and compatible
common data models that underpin a digital market of interoperable and
replicable smart solutions in multiple sectors, starting with smart cities.

The Reference Architecture and Data Models use the FIWARE NGSI API and TM Forum
Open APIs for interoperability and scalability of smart solutions. The FIWARE
Context Broker technology, implementing the FIWARE NGSI APIs (**NGSI v2 and
NGSI-LD**), provides the basis for breaking information silos in organizations
aiming at becoming smart. Actually, it enables a real-time (or close to real
time, i.e., right-time) view and foundation for the development of governance
systems at global organization level. Examples of such organizations include
cities, factories, hospitals, airports, farms, etc.

Combined with TM Forum Open APIs, data publication platforms can support
organizations to realise the potential of real-time (or right-time) open data,
easing development of innovative solutions by third parties. In addition,
organizations can evolve their current data sharing policies towards a vision
which, shared with other organizations, brings support to a Data Economy. This
way, the proposed Reference Architecture is ready to solve the needs of
organizations today while future-proofing for tomorrow’s requirements.

This GitHub organization structure contains **JSON Schemas and documentation**
on harmonized Data Models for different Smart Domains, **starting with Smart
Cities**. The following repositories are available:

-   data-models repository which is an umbrella repository that contains all the
    Data Models from different verticals (e.g., Parking, Street lighting, etc.).
    _This Repository does not admit Pull Requests._

-   For each Vertical there is a Repository containing the Data Models related
    to that vertical. _These repositories do admit pull requests_.

## General Principles

-   **Driven-by-implementation approach**: Specifications will be considered
    stable as soon as enough end user organizations (e.g., cities) have
    validated them in practice. Stable specifications may become TM Forum formal
    deliverables by following TM Forum’s defined processes.

-   **Open-closed**. Breaking changes to already approved specs are not allowed.
    Instead, new versions shall deprecate attributes, add new attributes, extend
    enumerations, etc.

-   **Public and royalty-free** nature of specifications. Data Model Licensing
    mode. [Creative Commons by Attribution 4.0](https://creativecommons.org/licenses/by/4.0/)

-   **Open contribution**. Contributions open to anybody (not only members),
    while final decision making corresponds to TM Forum and FIWARE Foundation
    members

## Lifecycle

Specifications evolve over time through versions generated after _RFC (Request for
Comments)_ periods, of a typical duration of 6 months, in between.

![Data Model Lifecycle](docs/lifecycle.png)

The way to handle new Data Models is administrated by the different topics and domains:

- FIWARE foundation and TMForum will check for th consitency and updating of the different
data models in this group of repositories

- It is possible to request a [new data model](https://docs.google.com/forms/d/e/1FAIpQLSfoiKoVNkDC2eXLgJh3-6Wlu-DS4LJfizFKsinpNwGIeIox4g/viewform) through the link. 

## How to contribute

Contributions should come in the form of **pull requests** made against the
corresponding Vertical Data Model repository.

A Data Model specification shall contain the following artefacts:

-   `spec.md` Markdown specification in accordance with this
    [template](templates/data-model-template.md).

-   `schema.json` JSON Schema associated to the specification. Such JSON Schema
    should be based on Base Schemas, see for instance
    [schema.json](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/schema.json)
    of
    [WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/doc/spec.md)

-   examples encoded in FIWARE NGSI v2 and NGSI-LD, see for instance
    [example.json](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/example.json),
    [example-normalized.json](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/example-normalized.json)
    and
    [example-normalized-ld.jsonld](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/example-normalized-ld.jsonld)
    of `WeatherObserved`.

The artefacts referred below should be under a folder structured as follows:

-   `specs/`
    -   `NewModel/`
        -   `doc/`
            -   `spec.md`: A data model description based on the
                [data model template](https://github.com/smart-data-models/data-models/blob/master/templates/data-model-template.md),
                e.g.
                [spec.md of WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/doc/spec.md).
        -   `README.md`: A summary file (as an extract from the spec file), e.g.
            [README.md of WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/blob/master/README.md)
        -   `schema.json`: The JSON Schema definition, e.g.
            [schema.json of WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/schema.json)
        -   `example.json`: One or more JSON example file, e.g.
            [example.json of WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/example.json)
        -   `example-normalized.json`: One or more JSON example file in NGSI v2
            normalized format, e.g.
            [example-normalized.json of WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/example-normalized.json)
        -   `example-normalized-ld.jsonld`: One or more JSON example file in
            **NGSI-LD** normalized format, e.g.
            [example-normalized-ld.jsonld of WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/blob/master/WeatherObserved/example-normalized-ld.jsonld)

To facilitate contributions and their validation, we developed a
[tool](https://github.com/smart-data-models/tools/tree/master/validator) that is
also used for the Continuous Integration.

To achieve a better performance, we need to break down silo’s of data, 
ensuring that artificial intelligence can be applied across aggregated datasets 
and to ensure that individual citizen experience can be optimized across 
different services.

To achieve this, TM Forum and FIWARE launched this initiative, which seeks to 
harmonize data models across Smart applications and with the Data Models of 
TM Forum which have been deployed globally.

By agreeing across different communities, the common definition of smart
data models, this will empower innovators and companies to develop solutions
that adhere to this common definition and ultimately help enable
interoperability of services.

By way of example, the data models that have been harmonized to date can be
found in the submodules in the [specs](https://github.com/smart-data-models/data-models/tree/master/specs) directory. 

there are new data models in progress for the following areas:

-   Tourism
-   Water Management
-   Energy
-   Robotics 
