# BONSAI Hackathon Spring 2020: Realizing the promise

At our hackathon in 2019, we established an ontology for BONSAI data, and developed prototypes for a set of software libraries to take in raw data and output consolidated life cycle inventories. Details on this hackathon can be found at https://github.com/BONSAMURAIS/hackathon-2019.

In the Spring 2020 hackathon, we are shifting our emphasis from ontologies and semantic web databases to get a complete toolchain that can produce a truly open, consistent, and comprehensive database for use in life cycle assessment and material flow analysis. We will build on the produced ontologies (link), correspondence tables (link), and database schema (link), and add the following:

## A. Introduction of new data sources

One of the key advances in the BONSAI approach is the use of many different kinds of data to both generate and validate our system. For example, we can use techniques and data from material flow analysis to understand major or critical mass flows missing or out of balance in our life cycle inventories. Similarly, remote sensing data can serve as independent validation data, giving us rough estimates on how far our models depart from observations. We can also combine data sources automatically to generate specific models. In the first priority, BONSAI will make these many data sources available with a common nomenclature and ontological, so that individual researchers can test different approaches in each system modelling step. The hackathon theme will build on an [existing repository](https://github.com/BONSAMURAIS/vacuum_pump/) to import a number of [new data sources](https://github.com/BONSAMURAIS/vacuum_pump/issues?q=is%3Aissue+is%3Aopen+label%3Adata-source), and adapt our system concepts & nomenclature lists based on this experience.

## B. Harmonization and System Models

This theme will consist of a series of Python software libraries that will each work on a specific step in data processing. Data IO will come via CSV with Data Package metadata.

### Harmonization

* Mapping of native nomenclature system to common base naming system
    * e.g. HS tariff product codes, ISIC industry code, ISO country/region codes
    * Mapping allows for incomplete matching
* Allocation where necessary (if allocation is used)

### Choice of scale

Should be based on objective/scientific quantitative methods (reduction of uncertainty)

* Space (assumption is countries/regions)
* Time (assumption is intervals consisting of years)
* Technology (activities and products)

### Linking suppliers and consumers

Need policy on "rest of" fields, e.g. EXIOBASE versus technology-specific data: should we subtract the technology-specific data from the aggregated totals?

### Applying system models

* Allocation of multi-output or waste flows (if allocation is used)
* Construction of markets (if markets are used)

### Validation

* Basic measures like mass or energetic balances
* Some data is set aside as validation data (e.g. atmospheric measurements)
* Boot-strapping
* Statistics on unmet demand or supply

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
