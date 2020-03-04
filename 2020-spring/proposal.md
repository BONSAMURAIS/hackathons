# BONSAI Hackathon Spring 2020: Realizing the promise

At our [hackathon in 2019](https://github.com/BONSAMURAIS/hackathon-2019), we established an ontology for BONSAI data, and developed prototypes for a set of software libraries to take in raw data and output consolidated life cycle inventories.

In the Spring 2020 hackathon, we are shifting our emphasis from ontologies and semantic web databases to get a complete tool chain that can produce a truly open, consistent, and comprehensive database for use in life cycle assessment and material flow analysis. We will build on the produced [ontologies](https://github.com/BONSAMURAIS/BONSAI-ontology-RDF-framework), [correspondence tables](https://github.com/BONSAMURAIS/correspondence_tables), and [database schema](https://github.com/BONSAMURAIS/schema), and add the following themes:

## A. Introduction of new data sources

One of the key advances in the BONSAI approach is the use of many different kinds of data to both generate and validate our system. For example, we can use techniques and data from material flow analysis to understand major or critical mass flows missing or out of balance in our life cycle inventories. Remote sensing data can serve as independent validation data, giving us rough estimates on how far our models depart from observations. We can also automatically combine data sources to give a complete picture of the inputs and outputs of specific technologies. As a first step, BONSAI will make these many data sources available with a common nomenclature and ontology, so that individual researchers can test different approaches to building consistent, complete, and comprehensive datasets. The hackathon will build on [existing work](https://github.com/BONSAMURAIS/vacuum_pump/) to import a number of [new data sources](https://github.com/BONSAMURAIS/vacuum_pump/issues?q=is%3Aissue+is%3Aopen+label%3Adata-source). We will use these intial data sources to test and adapt our system concepts & nomenclature lists.

## B. Data harmonization and system models

This theme will consist of a series of Python software libraries that will each work on a specific step in data processing. A common data format, CSV with [Data Package](https://frictionlessdata.io/data-packages/) metadata, will be used for both inputs and outputs, allowing each library to be developed independently (ETL workflow).

### Data harmonization

Data harmonization is the construction and application of correspondence mappings, so that data provided with different naming and modelling approaches can be combined. Correspondence mappings can be one-to-one, one-to-many, or many-to-many, and are stored as open metadata. To handle many different naming systems, BONSAI is using a single common base based on international standards (e.g. [HS tariff product codes](https://en.wikipedia.org/wiki/Harmonized_System), [ISIC industry code](https://en.wikipedia.org/wiki/International_Standard_Industrial_Classification), [ISO country/region codes](https://www.iso.org/iso-3166-country-codes.html), though our software allows for exceptions in specific cases.

Data harmonization could sometimes require allocation. For example, if widget production is only available for the EU, additional data sources would be used to disaggregate production to each EU member state. Such data could be specific to the product or industrial activity, or could be proxy data such as GDP or population. Both data and disaggregation algorithms should be open and transparent.

### Choice of scale

Should be based on objective/scientific quantitative methods (reduction of uncertainty)

* Space (assumption is countries/regions)
* Time (assumption is intervals consisting of years)
* Technology (activities and products)

### Applying system models

System models are a systematic formulation of practitioner choices in cases where there is no "correct" alternative. This library will build off the substantial research and code produced in the [Ocelot project](https://ocelot.space/), and produce algorithmic options for:

* Allocation of multiple output products/recyclable waste flows (if allocation is used)
* Construction of markets (if markets are used): Should the average mix or marginal producer be chosen? Should markets always/sometimes/never be used as modelling constructs, or should suppliers link directly to consumers.

Includes linking suppliers and consumers.

At first, build off well known system constructs from Input-Output modelling which have [software implementations](https://github.com/stefanpauliuk/pySUT).

### Validation

* Basic measures like mass or energetic balances
* Some data is set aside as validation data (e.g. atmospheric measurements)
* Boot-strapping
* Statistics on unmet demand or supply

Outputs from validation can feed into earlier libraries in an iterative fashion.

## Preparation

As in previous hackathons, the core members of the BONSAI project will prepare the necessary data, infrastructure, and documentation before the hackthon starts such that everyone can work productively from day one. Weekly coordination calls will be held, and open to everyone.

## Time & Location

May 2020, Berlin

## Expected participation (very approximate)

* BONSAI core team: 3 people
* BONSAI previous participants: 2 people
* [Open energy modelling initiative](https://openmod-initiative.org/): 2 people
* [TRASE](https://trase.earth/): 2 people
* HESTIA project (open database of food/agriculture LCA data): 2 people
* New/other participants: 4 people
* Remote BONSAI/other participation: up to 15 people

## About BONSAI

The BONSAI project is a volunteer interdisciplinary community of scientists, practitioners, and other interested individuals trying to make sustainability assessment better and more open; it currently has more than 25 active members across Europe and North America. BONSAI is completely open in its efforts and its management; all software repositories can be found at https://github.com/BONSAMURAIS/, and all major decisions at https://github.com/BONSAMURAIS/enhancements. In particular, [BEP 0002](https://github.com/BONSAMURAIS/enhancements/blob/master/beps/0002-bonsai-project-community-governance-structure.md) provides a community governance standard.

The non-profit association BONSAI coordinates and organizes the BONSAI project. It is headquartered in Denmark; details on its statues and governing board can be found at [online](https://bonsai.uno/organisation/).
