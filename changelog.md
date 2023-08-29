# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.1] - 2023-01-16

##### *Author: Tiago Oliveira*
### Added

- This CHANGELOG file is created.
- Entity **Patent** created.

## [0.0.2] - 2023-02-22

##### *Author: Vivian Silva*
### Structural changes to group related attributes as subfields of a common complex field

- Entity **Person**
    1. Fields _givenName_ and _familyName_ grouped under _fullName_
    2. Fields _birthCity_, _birthState_ and _birthCountry_ grouped under _birthLocation_

- Entity **OrgUnit**
    1. Fields _coordinate.latitude_ and _coordinate.longitude_ renamed to _latitude_ and _longitude_, and grouped under _coordinates_
    2. Fields _address.description_, _address.cep_, _address.city_, _address.neighborhood_, _address.state_ and _address.country_ renamed to _description_, _cep_, _city_, _neighborhood_, _state_ and _country_, and grouped under _address_

- Entity **Journal**
    1. Fields _apcAmount_ and _apcCurrency_ grouped under _apcCost_
    2. Fields _submissionAmount_ and _submissionCurrency_ grouped under _submissionCost_

- Entity **Project**
    1. Fields _modalityCode_ and _modalityName_ grouped under _modality_
    2. Fields _callAbbreviation_ and _callName_ grouped under _call_

## [0.0.3] - 2023-04-27

##### *Author: Raulivan Rodrigo*
### Updated

- Entity **Journal**
    - Included fields
        - urlOpenalex
        - publisher
        - worksCount
        - citedByCount
        - isOa
        - isInDoaj
        - homepageUrl
        - countryCode
        - type
        - worksApiUrl
        - countByYear
- Entity **Patent**
    - Included fields
        - urlEspacenet

## [0.0.4] - 2023-04-28

##### *Author: Vivian Silva*
### Updated

- Entity **OrgUnit**
    - Included fields
        - identifier.ci
        - identifier.scopus

## [0.0.5] - 2023-05-09

##### *Author: Raulivan Rodrigo*
### Added

- Entity **Software** created.
## [0.0.6] - 2023-05-09

##### *Author: Tiago Oliveira*
### Created

- Entity **ResearchGroup**
  - Included fields
    - identifier.brcris
    - identifier.dgp
    - name
    - description
    - status
    - creationYear
    - URL
    - researchLine
    - keywork
    - knowledgeArea
    - applicationSector
    - equipament
    - software

- Relationship **MemberResearchGroup**
  - Relationship between **ResearchGroup** - **Person**
  - Included fields
    - scholarshipHolder

- Relationship **LeaderResearchGroup**
  - Relationship from **ResearchGroup** and **Person**

- Relationship **LeaderResearchGroupOrgUnit**
  - Relationship from **ResearchGroup** and **OrgUnit**

- Relationship **PartnerResearchGroupOrgUnit**
  - Relationship from **ResearchGroup** and **OrgUnit**
  
## [0.0.5] - 2023-07-10

##### *Author: Raulivan Rodrigo*
### Updated

- Entity **Journal**
    - Included fields
        - identifier.issn_l
		- identifier.mag
		- identifier.openalex
		- identifier.wikidata
		- identifier.fatcat

## [0.0.6] - 2023-08-29

##### *Author: Vivian Silva*
### Entity **Journal** cleaned and refactored to cover only the information currently being collected from OpenAlex

- Fields maintained:
	- identifier.issn
	- identifier.issn_l
	- identifier.openalex
	- identifier.brcris
	- title
	- publisher
	- websiteURL
	- isOa
	- isInDoaj
	- apcCost (including subfields _apcAmount_ and _apcCurrency_)
	- countryCode
	- type
	- assessmentArea
	- qualis
	- keywords
	- 2yr_mean_citedness
	- h_index
	- i10_index
	- googleH5