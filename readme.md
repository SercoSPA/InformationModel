# Information Model Management System
An Information Model defines an high-level and domain-agnostic vocabulary of the Copernicus Data Space as per an ontology.<br>
This is an open-source project for the Configuration Management of the Information Model Management System (**IMMS**) hosting all the relevant documentation produced on development.

## Table of Contents
1. [Repository Contents](#repository-contents)
2. [License](#license)
3. [Project Notes](#project-notes)
## Repository Structure
The repository is presented as follows:
* The folder `Documentation` contains all the related contents of the documentation package as required by the [Widoco](https://github.com/dgarijo/Widoco) an open-source project for documenting ontologies.
* The following files:
    * `Abstract.txt` being the fixed preamble added to the documentation content, explaining the context and main ontology structure
    * `CDS_V1.0.owl` the master ontology file generated with [Protégé](https://protege.stanford.edu/), containing the information model structure as published via Widoco
    * `config.properties` collecting all configurations applied to generate the Documentation
## License
The content of this project itself is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

## Project Notes
The Information Model is given the following representations:
* *Declarative representation* to generate and publish the Copernicus Data Space Information Model, starting from the input definition (1st draft released in March 2022). A prototype is available at <https://imms.copernicus-dataspace.eu> with credentials `imms` / `cds.gu3st`.
* *Programmatic representation* to put in place an API system able to retrieve all the metadata defined within the Copernicus Data Space ontology:
    * Specifications are given as per declarative representation, so the user can retrieve all the data properties defined by the ontology
    * The prototypal endpoint `/db` (under development) allows to access the ontology contents registered in a database. Classes are queriable individually by name.
    
    Examples: 

    <https://test-imms.copernicus-dataspace.eu/db/Participant>
    
    <https://test-imms.copernicus-dataspace.eu/db/Participant?Role=eq.Service%20Consumer>

An API prototype is available [here](https://test-imms.copernicus-dataspace.eu/db) accessible also via UI [here](https://test-imms.copernicus-dataspace.eu/DB/Home.html) - credentials `imms` / `cds.gu3st`.