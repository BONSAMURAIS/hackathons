# Hackathon preliminary agenda

This agenda is **preliminary**, feel free to suggest or make changes!

## Before the Hackathon

The key to the hackathon being an effective use of our time is proper preparation. There are some tasks that everyone needs to do, to be ready to start on the first day. Other individual tasks are also listed below - please volunteer yourself for suitable tasks!

I think that we will need an online meeting before the hackathon, about one week before the workshop.

### Tasks for everyone

* Schema finalized
* Do basic tutorials using RDFLib
* Background reading TBD
* Review of EXIOBASE data and metadata
* Choose new data source
* Choice of inventory module
* Read basic overview of relevant resources

### Individual tasks

| Task | Responsible |
| --- | --- |
| Design/find basic tutorials using RDFLib | ? |
| Choose background reading | All (individual contributions) |
| Extract or create lists of JSON-LD UUIDs for common data (units, etc.) | ? |
| Map (or borrow existing mappings of) EXIOBASE elementary flows to ecoinvent | ? |
| Pre-calculate example results for EXIOBASE in Brightway | Chris |
| Generate basic overview of existing BONSAI or other relevant outside resources | Chris |

## Monday (All times are local to Barcelona: CET time UTC+0100)

### Morning: Basic foundation

9:00-10:00 Zoom meeting: 

* Review of our data schema
* RDF parsing/construction (Matteo?)
* DB access and querying
* EXIOBASE structure and metadata

10:00-13:00 Work in groups

13:00-15:00 Lunch break (Note that we have long lunch breaks in order to enjoy that you are in sunny Barcelona and that we will enjoy splendid food - sorry for the rest of you J)

### Afternoon: Getting EXIOBASE into database

15:00-15:30 Zoom status meeting

15:30-18:30 Work in groups

* Mapping EXIOBASE categories to our standards (industry and product codes, locations, etc.)
* Write parsers for EXIOBASE format to RDF
* Entering data into Jena DB (possible evening or overnight)
* Keep running list of schema or other potential future changes

18:30-19:00 Zoom status meeting

20:00-21:30 Dinner

## Tuesday: Retrieving data from Jena as usable LCI datasets


9:00-9:30 Zoom meeting

9:30-13:00 Work in groups:

* Review JSON-LD format
* Write queries to join relevant data to create datasets as JSON-LD
* Test LCA results against existing implementation in Brightway

13:00-15:00 Lunch break

15:00-15:30 Zoom status meeting

15:30-18:30 Work in groups

18:30-19:00 Zoom status meeting

20:00-21:30 Dinner

## Wednesday

### Morning: Addition of new data sources (TBD)

9:00-9:30 Zoom meeting

9:30-13:00 Work in groups:

* Map metadata to our standards
* Write parsers to RDF
* Enter data into Jena DB

### Afternoon
Social event

## Thursday

9:00-9:30 Zoom meeting

9:30-13:00 Work in groups:

### Group A: Data reconciliation

* Data reconciliation algorithms: Theory and practice (possible link to pre-workshop reading)
* Data reconciliation of new data source and EXIOBASE
* How to store reconciled data: Best practices and implementation in our database

**Goal**: Implementation of a small test algorithm

### Group B: Inventory modules
By inventory modules, we mean a basic model of a process or industrial sector that can be easily updated, manually or (preferably) automatically, as well as applied to multiple world regions.

* Programming standards and common APIs (or meta-APIs)
* Best practices for testing and documentation
* Implementation of a pre-selected inventory module in Python

**Goal**: Implementation of a small test model

13:00-15:00 Lunch break

15:00-15:30 Zoom status meeting: Sharing approaches, challenges, and potential solutions between groups

15:30-18:30 Work in groups

18:30-19:00 Zoom status meeting

20:00-21:30 Dinner

## Friday

### First part

9:00-9:30 Zoom meeting

9:30-10:30 Groups document and publish their work

10:30-12:30 Each group reviews and tests out the work of the other group

12:30-13:30: Finishing up any outstanding tasks

13:30-14:00 Zoom closing meeting:

* Organization of workshop report paper
* Planning for & assignment of next steps

14:00-16:00 Farewell meal and celebration 
