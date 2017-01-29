# Rationale
first draft - Georg Vogeler, 22.12.2016

## Use cases
### biographical lexicon
I'm working on a biographical lexicon. I would be so happy to have all source reference to a person aggregated with one click, which I could easily put as references into my descriptive text of the biography.

### Carreers
I'm studying carreers of a group of persons. I would be so happy to get a data matrix in which for each person the steps of their carreer would listed according to a well crafted and well documented taxonomy with the dates of these steps. (Yes, I know these dates can be time ranges, single dates for transitions from one 'grade' to the other, termini a quo and ante quem etc. etc.

### Source editing
I'm working with primary sources in which a person is mentioned or for which a person has an important role (author, sender of a letter etc.). I want to offer the information provided in the source for others to be reused in their prosopographical research (and would be happy to create automatically an index of persons named in my soure integrating the information from other sources.) I am willing to refer to a well crafted and well documented taxonomy for the events and/or activities mentioned in my source text and the role of the person in this event/activity.

### Fact checking
I find a statement about a person made by a colleague/a source text. I have my doubts on the reliability of the statement and want to check if it is consistent to all other statements made about the person. (or vice versa: I don't trust all the others statements, which could mean I can revolutionize history.)

### New interpretation
I want to establish a statement about a person, well founded by a primary source. Unfortunately my source is interpreted by others not in my way. I want to make my modification of the interpretation of the source available to the Giant Global Graph (aka the semantic web) and by this to the scholarly community being able to use the prosopographical API

### Publish database
I have created a prosopographical database and would be happy if somebody else would use it as well. So I want to publish it in a way that it is easy to use (and to cite). Btw my "database" are just lots of spreadsheets.

### Other databses
I have created a database which - by chance - contains lots of information about people (e.g. bibliographies). I am curious if this data can be used for prosopographical studies as well.

### Analysis
I'm a wizard in visualisation, a nerd in network analysis, a sage of statistics, a genius of GIS fallen in deep love with the people from the past. I want to grab easily all available data about a group of them and create fancy visualisations, tight networks, explorative maps, and brain blowing calculations.

### Tool user
I am a non technical humanist creating prosopographical data ("a person database"). I would be happy to use the database server from somebody else (e.g. a common repository) and the easiest to use data capture tool (with fancy autosuggestion, automatic check of existing data etc. etc.).

## Basic considerations for paths
The data can be accessed via the four major components (objects) of the factoid model:

* the **person**, which only has to be identified abstractly, i.e. by an id or IRI. There can be alternative IRIs which describe the same person, so they are owl:sameAs
* a **statement** about this person, formalized in RDF assertions or just plain text
* a **source** attesting this statement
* the **factoid** tying all the three together, created by somebody at some time

The paths therefore have to be able to
* *create*, *update* and *delete* these four objects - well protected by authentication and user roles.
* *query* these four objects (incl. pointing directly to one single object - preferably via the IRI for it)
* give information about the *context* for the four objects (e.g. the schema of for the formal representation of the statements, relationship between them incl. versioning, number of objects available, etc.)