.BONSAI Hackathon Spring 2020: Realizing the promise

At our hackathon in 2019, we established an ontology for BONSAI data, and developed prototypes for a set of software libraries to take in raw data and output consolidated life cycle inventories. Details on this hackathon can be found at https://github.com/BONSAMURAIS/hackathon-2019.

In the Spring 2020 hackathon, we are shifting our emphasis from ontologies and semantic web databases to get a complete toolchain that can produce a truly open, consistent, and comprehensive database for use in life cycle assessment and material flow analysis. We will build on the produced ontologies (link), correspondence tables (link), and database schema (link), and add the following:

A. Introduction of new data sources

---

B. Harmonization and System Models

This theme will consist of a series of Python software libraries that will each work on a specific step in data processing. Data IO will come via CSV with Data Package metadata.

i. Raw data input

Software repository: https://github.com/BONSAMURAIS/vacuum_pump/

Scripts to input raw data (in whatever form provided) into database. Needs to indicate common metadata (license, source, nomenclature system).

See the first list of data sources to process: (https://github.com/BONSAMURAIS/vacuum_pump/issues?q=is%3Aissue+is%3Aopen+label%3Adata-source)


Preparation

As in previous hackathons, the core members of the BONSAI project will prepare the necessary data, infrastructure, and documentation before the hackthon starts such that everyone can work productively from day one. Weekly coordination calls will be held, and open to everyone.


Harmonization:

- Mapping of native nomenclature system to common base naming system
    - e.g. HS tariff product codes, ISIC industry code, ISO country/region codes
    - Mapping allows for incomplete matching
- Allocation where necessary (if allocation is used)

Choice of scale:

- Space (assumption is countries/regions)
- Time (assumption is intervals consisting of years)
- Technology (activities and products)

- Should be based on objective/scientific quantitative methods (reduction of uncertainty)

Linking suppliers and consumers

- Need policy on "rest of" fields
    - e.g. EXIOBASE versus technology-specific

Applying system models

- Allocation of multi-output or waste flows (if allocation is used)
- Construction of markets (if markets are used)

Validation

- Basic measures like mass or energetic balances
- Some data is set aside as validation data (e.g. atmospheric measurements)
- Boot-strapping
- Statistics on unmet demand or supply

Time: May 2020

Location: Berlin

Expected participation (approximate):

BONSAI core team: 3 people
BONSAI previous participants: 2 people
Open energy modelling forum: 2 people
TRASE (https://trase.earth/): 2 people
HESTIA project (open database of food/agriculture LCA data): 2 people
New/other participants: 4 people

Remote BONSAI/other participation: up to 15 people

About BONSAI

The BONSAI project is a volunteer interdisciplinary community of scientists, practitioners, and other interested individuals trying to make sustainability assessment better and more open; it currently has more than 25 active members across Europe and North America. BONSAI is completely open in its efforts and its management; all software repositories can be found at https://github.com/BONSAMURAIS/, and all major decisions at https://github.com/BONSAMURAIS/enhancements. In particular, BEP 0002 (https://github.com/BONSAMURAIS/enhancements/blob/master/beps/0002-bonsai-project-community-governance-structure.md) provides a community governance standard.

The non-profit association BONSAI coordinates and organizes the BONSAI project. It is headquartered in Denmark; details on its statues and governing board can be found at https://bonsai.uno/organisation/.
