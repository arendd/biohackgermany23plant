---
title: 'Increasing FAIRness in agrosystem sciences and plant phenomics'
title_short: 'Increasing FAIRness in agrosystem sciences and plant phenomics'
tags:
  - FAIR
  - plant science
  - agronomy
authors:
  - name: Gabriel Schneider
    orcid: 0000-0001-6573-3115
    affiliation: 1
  - name: Patrick
    affiliation: 3
  - name: Cyril
    affiliation: 2
  - name: Carissa BLeker
    orcid: 0000-0003-1617-7145
    affiliation: 4    
  - name: Pedro M Barros
    orcid: 0000-0001-5626-0619
    affiliation: 5 
  - name: Filippo Bergeretti
    orcid: 0000-0002-6863-5577
    affiliation: 5 
  - name: Ana Usié
    orcid: 0000-0002-3364-9434
    affiliation: 6
  - name: Further Author (PLEASE INSERT YOURSELF)
    orcid: 0000-0000-0000-0000
    affiliation: 
  - name: Daniel Arend
    affiliation: 3
    orcid: 0000-0002-2455-5938
  - name: Marco Brandizi
    orcid: 0000-0002-5427-2496
    affiliation: 7
  - name: Daniel Martini
    orcid: 0000-0002-6953-4524
    affiliaton: 8
  - name: Jonas Grieb
    orcid: 0000-0002-8876-1722
    affiliaton: 9
  - name: Nils Reinosch
    affiliaton: 8
  - name: Jascha Jung
    affiliation: 8
    
    

affiliations:
  - name: ZB MED - Information Centre for Life Sciences
    index: 1
  - name: Second Affiliation
    index: 2
  - name: Leibniz Institute for Plant Genetics and Crop Plant Research (IPK) Gatersleben, Germany
    index: 3
  - name: National Institute of Biology, Večna pot 121, 1000 Ljubljana, Slovenia
    index: 4    
  - name: Instituto de Tecnologia Química e Biológica António Xavier, Universidade Nova de Lisboa  (ITQB NOVA), Oeiras, Portugal
    index: 5
  - name: Centro de Biotecnologia Agrícola e Agro-alimentar do Alentejo (CEBAL), Beja, Portugal
    index: 6
  - name: Rothamstead Research
    index: 7
  - name: Kuratorium für Technik und Bauwesen in der Landwirtschaft e.V. (KTBL)
    index: 8
  - name: Senckenberg Society for Nature Research
    index: 9
date: 18 december 2023
cito-bibliography: paper.bib
event: BH23DE
biohackathon_name: "BioHackathon Germany 2023"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Bielefeld, Germany, 2023"
group: Project 9
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackrxiv/publication-template
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: First Author \emph{et al.}
---


# Introduction

As part of the de.NBI BioHackathon 2023, we here report about our progress on increasing FAIR-compliance in agrosystem sciences and plant phenomics.


## Subproject 1:<br>Increasing findability of digital agrosystem resources by extending Schema.org
### Introduction
Research Data Infrastructures (RDIs) in the agrosystem domain established services and published research data of their communities for years. Each infrastructure is tailored to its users needs, also concerning its metadata, leading to a very heterogeneous landscape. To increase the findability of their content via search engines, RDIs can expose the metadata of resources as markup via Schema.org. 
In the context of [FAIRagro](https://fairagro.net/), the German National Research Data Infrastructure for the agrosystem domain, several RDIs already do so: For each landing page of a dataset, a [JSON-LD](https://json-ld.org/) based resource is created, that contains part of the metadata information, using Schema.org types and properties. This annotation is then consumed by search engines to present enriched search results to users. As Schema.org follows a generic approach, its core schema doesn't suffice in describing all entities relevant for agrosystem researchers with the required level of detail.
Therefore this hackathon subproject evaluated Schema.org, its extension [Bioschemas](https://bioschemas.org/) and the [Agri-schemas](https://github.com/Rothamsted/agri-schemas) project in regards to modeling metadata of datasets relevant to [FAIRagro](https://fairagro.net/) use cases. 


Following the [FAIR principles](https://www.go-fair.org/fair-principles/) and its ideas on reusability, the approach was to identifiy which kinds of entities relevant to the agrosystems domain, could also be modelled with already available types and properties and where gaps are, that could be closed in the future with an extension of mentioned schemas.

### Tasks
During the hackathon the project group analysed different published datasets, relevant to a crop modeling use case in FAIRagro. For each dataset the group identified the entities described in the metadata, directly provided via the RDI that published the datasets, as well as the contents of the datafiles themselves. 
As the provision of Schema.org markup in our projects context is about increasing the findability of digital resources, we focussed on entities, that agrosystem scientists will most likely search for. Soil, crop, fertilizers and management actions were identified as central entities for searches, based on feedback by hackathon participants and discussions of the project group.

For crop and soil, the project group used types and properties of Schema.org / Bioschemas / Agri-schemas to model the metadata information of the example datasets and their  included entities explicitly. For technical representation of modelling the information the project group used either [Turtle](https://www.w3.org/TR/turtle/) as a RDF serialization or [JSON-LD](https://json-ld.org/), one of the formats Schema.org uses.

As Schema.org builds the foundation for metadata description in [RO-Crates](https://www.researchobject.org/ro-crate/), we converted one of the analysed datasets to a RO-Crate, to demonstrate how RDIs could enrich their datasets to achieve increased interoperability towards [FAIR Digital Objects](https://fairdo.org/1316-2/). 
In parallel to the modelling we analysed how RDIs currently use Schema.org and how they could improve their usage. To demonstrate the benefits of such an optimisation, we outlined new search queries that users would be able to execute after implementation.

### Results
A central result of the hackathon work is the realisation that many of the requirements of the analysed use case can be satisfied by contributing to already existing communities, such as Bioschemas. By following its community based approach of extension, the agrosystem domain can work on establishing the concepts it needs, while embedding them in a broader context, increasing interoperability. 
During the modelling of example dataset metadata with already available types and properties of Schema.org / Bioschemas / Agri-schemas, we identified multiple approaches, that are feasible, depending on requirements of specific use cases.

Crop is one of the central entities, found in a majority of the analysed datasets. It describes a type of plant, that is in some way related to a dataset. It can be expressed using the type "FieldTrialMaterialSource" from Agri-schemas, which is a proposition of a subclass of Bioschemas ["BioChemEntity"](https://bioschemas.org/BioChemEntity).  The crop is described with a ["taxonomicRange"](https://schema.org/taxonomicRange), which is a property of "BioChemEntity". Furthermore it relies on the Schema.org core properties ["name"](https://schema.org/name) and ["subjectOf"](https://schema.org/subjectOf) to link it to a ["Study"](https://bioschemas.org/Study). Implementing this approach would mean the development of a new subclass. Using the term "FieldTrialMaterialSource", which has its source in the [MIAPPE](https://www.miappe.org/) standard, would increase the understanding of researchers familiar with MIAPPE terminology.
An example study on wheat could be modelled the follwing way:

    @prefix bioschemas: <https://bioschemas.org/> . 
	@prefix agri: <https://github.com/Rothamsted/agri-schemas/> . 
	@prefix schema: <https://schema.org/> . 

	<example_study> a bioschemas:Study .
	<example_crop_source> a agri:FieldTrialMaterialSource, schema:BioChemEntity;
		bioschemas:taxonomicRange <http://aims.fao.org/aos/agrovoc/c_7951>;
		schema:name "Triticum aestivum";
		schema:subjectOf <example_study>;
		schema:identifier <example_identifier> . 
        

A different approach originates from a ["Dataset"](https://schema.org/Dataset), links it to a crop entity via ["about"](https://schema.org/about) and models crop as a regular ["BioChemEntity"](https://bioschemas.org/BioChemEntity) with a ["taxonomicRange"](https://schema.org/taxonomicRange). Instead of defining a new subclass this approach relies on [Bioschemas profile mechanism]("https://bioschemas.org/profiles/") and requires Bioschemas to support multiple profiles per type.

    @prefix bioschemas: <https://bioschemas.org/> . 
	@prefix schema: <https://schema.org/> . 

	<example_dataset> a schema:Dataset ;
	schema:about [
		a bioschemas:BioChemEntity ;
		dct:conformsTo <https://bioschemas.org/profiles/example_Crop/0.1-TO-BE-CREATED> ;
		bioschemas:taxonomicRange <http://aims.fao.org/aos/agrovoc/c_890> ;
        schema:name "Beta vulgaris"
		] .

The decision between a subclass vs. a profile based approach depends on the necessity of new properties. Both presented options leverage existing Bioschemas resources, but differ in their extension requirements. A profile "Crop" for [BioChemEntity](https://bioschemas.org/BioChemEntity) would be sufficient, if relevant search queries can be satisfied with the use of BioChemEntity properties, e.g. by employing values from domain specific ontologies and by defining marginalities.

Defining a subclass instead, that inherits all properties of its superclass(es) additionally to its own specific properties, would open new possibilities for describing agrosystem datasets and therefore enable new search queries them. With the example of crop as "FieldTrialMaterialSource" a new property "variety" might be relevant, to enable searches for specific varieties.

    
    @prefix bioschemas: <https://bioschemas.org/> . 
	@prefix agri: <https://github.com/Rothamsted/agri-schemas/> . 
	@prefix schema: <https://schema.org/> . 

	<example_study> a bioschemas:Study .
	<example_crop_source> a agri:FieldTrialMaterialSource, schema:BioChemEntity;
		bioschemas:taxonomicRange <http://aims.fao.org/aos/agrovoc/c_7951>;
		schema:name "Triticum aestivum";
        bioschemas:exampleProperty_variety <https://fsp.ucdavis.edu/seed-catalog/wheat-varieties/Yecora-Rojo> ;
		schema:subjectOf <example_study>;
		schema:identifier <example_identifier> .
    

To evaluate on which entities are most relevant and how best to model them, a result of the hackathon is the founding of a agricultural Bioschemas working group. The results of the hackathon will be used as a foundation to discuss required entities and how to model them in detail. The ideas will then be discussed with a broader community via Bioschemas established processes. The working group will be open to everyone interested in working on increasing the findability of agriculture related digital resources.

Further results and material can be found in the subprojects Github repository, created during the hackathon: https://github.com/fairagro/biohackathon2023.

## Subproject 2:<br>MIAPPE Wizard - Enabling easy creation of MIAPPE-compliant ISA metadata for Plant Phenotyping Experiments

Section with description about and aims of the MIAPPE-Wizard.

### Introduction

Development of the MIAPPE Wizard began with the first Biohackathon Germany in 2022 [@citeAsRelated:https://doi.org/10.37044/osf.io/ekhdw]. 

### Results

The focus of this year's hackathon was to enhance and extend the features available in the MIAPPE Wizard. Previously, the Wizard was only capable of creating ISA JSON and ISA Tab formatted archives, with a significant amount of MIAPPE specific metadata missing. This year, the group focused on implementing the MIAPPE checklist and data model, as well as protocol and material/sample management. 

In addition to supporting ISA Tab and ISA JSON, the MIAPPE Wizard was also enhanced to create ARCs. The ARC can be downloaded as a zip archive and transferred from the local machine to the DataHUB through `git`. Currently, direct transfer of the ARC into a DataHUB instance is still in development.

To guide the development, an example dataset was taken, formatted in ISA Tab, and transformed into the ARC structure. The dataset has a similar structure to datasets in the BreedFides project, where the MIAPPE Wizard will be used as part of the dataset registration process. 

The MIAPPE Wizard user interface was improved by adding a progress bar and updating the color scheme and logo.

### Discussion


## Subproject 3:<br>FAIDARE: Increasing Plant Data Accessibility and Collaboration through Integration, Usability and Community Engagement

FAIDARE (https://urgi.versailles.inra.fr/faidare) is a comprehensive search portal harvesting diverse plant-centric data resources and providing a central access point for the plant research community. It addresses the findability aspect of the FAIR principles and is hosted and maintained by ELIXIR France and established as the European Search Portal for plant related datasets, in collaboration with EMPHASIS. For increasing the usability for the data users the aim of this subproject was connecting additional established resources used by the plant research community, specifically e!DAL-PGP (de.NBI/ELIXIR Germany)[@citesAsAuthority:Arend2020], CorkoakDB (ELIXIR Portugal)[@citesAsAuthority:Arias-Baldrich2020] and the Stress Knowledge Map (ELIXIR Slovenia)[@citesAsAuthority:Bleker2023] were the main targets of the project. 
<!-- 
To achieve this goal, we will use the common schema.org/BioSchemas markup to harvest and index these resources. In addition to these two major infrastructures, we will highly motivate additional resource providers to join us, and assess how this integration can be implemented to add their own system to the federated search portal of FAIDARE. To lower the barrier for connecting new data repositories, we also plan on generating training materials and ‘how-to’ guides to facilitate the future integration of additional data repositories. This will help to encourage the growth and expansion of FAIDARE as a comprehensive search portal for plant data and support capacity building for further resource providers. Therefore we are also looking for people who can support us in creating these materials and have knowledge on how to share and present it in a user appealing and helpful manner. This will enable researchers to access a wider range of plant data in a more efficient way and lead to greater collaboration and innovation within the field. Our vision is to create a comprehensive and user-friendly platform that serves as a one-stop-shop for all plant data needs.
-->

### CorkOakDB
[CorkOakDB](https://corkoakdb.org/) is a web-based resource to access the draft genome sequence of cork oak (*Quercus suber*). It provides public access to a set of standard tools for data visualization and retrieval, including gene sequences, structural and functional annotation, as well as gene expression based on available datasets. 

In this project we have developed a method to access CorkOakDB through the existing web service and retrieve functional information of all cork oak gene entries, together with corresponding links. All this information was compiled in a structured JSON file, with the required metadata, following [FAIDARE](https://urgi.versailles.inra.fr/faidare/join) specifications. The scripts prepared for this purpose and additional documentation were deposited on [github](https://github.com/anausie/FAIDARECorkOakDB). The JSON file was then uploaded to [FAIRDOM SEEK](https://seek4science.org/), for efficient access by FAIDARE. 

### Stress Knowledge Map
Stress Knowledge Map ([SKM](https://skm.nib.si)) is a publicly available resource containing two knowledge graphs describing current knowledge of biochemical, signalling, and regulatory molecular interactions in plants: a highly curated model of plant stress signalling (PSS, 1,425 entities and 543 reactions) and a large comprehensive knowledge network (CKN, 26,234 entities and 488,390 interactions). Both were constructed by domain experts through systematic curation of diverse literature and database resources. The main features include content exploration and visualisation, access to various export formats, and the ability to contribute improvements based on novel biological knowledge. 

Prior to the hackathon, only PSS was indexed in FAIDARE (a total of 686 genes). During the project, indexing of PSS was improved, updating the number of genes to 750 and providing more contextual information. CKN was newly indexed, also on the gene level. This resulted in SKM providing a total of 14,045 entries in FAIDARE. To provide more compelling gene entry pages in SKM, PSS entries in FAIDARE are now directed to the interactive [PSS Explorer](https://skm.nib.si/biomine/), and to make the same possible for CKN, SKM was extended during the project by adding a gene identifier URL parameter to the interactive [CKN Explorer](https://skm.nib.si/ckn/). 

As a result of this project, SKM now provides two endpoints (one for each knowledge graph) providing gene level metadata in JSON format, reproduced at every knowledge graph update, for harvest by FAIDARE. To further aid FAIDARE users in searching for genes of interest, both JSON files also contain [GoMapMan](https://gomapman.nib.si) annotations and definitions per gene, that can be used to filter the results in FAIDARE. 

### e!DAL-PGP
The e!DAL-PGP (Plant Genomics and Phenomics Research Data Repository) is an infrastructure to comprehensively publish plant research data. This covers in particular cross-domain datasets that are not being published in central repositories because of its volume or unsupported data scope, like image collections from plant phenotyping and microscopy, unfinished genomes, genotyping data, visualizations of morphological plant models, data from mass spectrometry as well as software and documents. All published datasets are accessible via a DOI linking to a dedicated content page, which embeds a schema.org and BioSchema markup in the HTML code.

In frame of this project the existing web server of e!DAL-PGP was extended to provide an additional endpoint which delivers dynamically a JSON dump of published datasets in a compatible format. This allows FAIdare to harvest all datasets on demand and add them to the internal search index. The endpoint is accessible at https://doi.ipk-gatersleben.de/faidare.json.


### Results


# JUST CODE EXAMPLES -->remove later


## Tables and figures

Tables can be added in the following way, though alternatives are possible:

Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |

A figure is added with:

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

# Other main section on your manuscript level 1

Lists can be added with:

1. Item 1
2. Item 2

# Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation


# Results


# Discussion

...

## Acknowledgements

This work was performed during the de.NBI BioHackathon Germany 2023 organized by ELIXIR Germany in December 2023. This work was funded by ELIXIR, the research infrastructure for life-science data; by the Federal Government of Germany and the county of North Rhine-Westphalia (de.NBI - the German Network for Bioinformatics Infrastructure); and the DFG in frame of the FAIRagro (www.fairagro.net, project number 501899475), NFDI4BioDiversity (www.nfdi4biodiversity.org, project number 442032008) and DataPLANT (https://www.nfdi4plants.de/, project number 442077441) consortia of the NFDI;  the Slovenian Research and Innovation Agency, project number Z4-50146

## References
