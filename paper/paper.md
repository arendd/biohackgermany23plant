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
    role: Writing – original draft
    
  - name: Patrick König
    orcid: 0000-0002-8948-6793
    affiliation: 3        
    role: Writing – original draft
    
  - name: Cyril Pommier
    orcid: 0000-0002-9040-8733
    affiliation: 2,11
    role: Writing – original draft
    
  - name: Carissa Bleker
    orcid: 0000-0003-1617-7145
    affiliation: 4
    role: Writing – original draft
    
  - name: Pedro M. Barros
    orcid: 0000-0001-5626-0619
    affiliation: 5
    role: Writing – original draft
    
  - name: Filippo Bergeretti
    orcid: 0000-0002-6863-5577
    affiliation: 5
    role: Writing – original draft
    
  - name: Ana Usié
    orcid: 0000-0002-3364-9434
    affiliation: 6,7
    role: Writing – original draft
    
  - name: Daniel Arend
    affiliation: 3
    orcid: 0000-0002-2455-5938
    role: Writing – original draft
    
  - name: Sebastian Beier
    affiliation: 12
    orcid: 0000-0002-2177-8781
    role: Writing - original draft
    
  - name: Marco Brandizi
    orcid: 0000-0002-5427-2496
    affiliation: 8
    role: Writing – original draft
    
  - name: Dominik Brilhaus
    affiliation: 13
    orcid: 0000-0001-9021-3197
    role: Writing - original draft
    
  - name: Manuel Feser
    affiliation: 3
    orcid: 0000-0001-6546-1818
    role: Writing – original draft
    
  - name: Jonas Grieb
    orcid: 0000-0002-8876-1722
    affiliation: 10
    role: Writing – original draft
    
  - name: Daniel Martini
    orcid: 0000-0002-6953-4524
    affiliaton: 9
    role: Writing – original draft
    
  - name: Cristina Martins Rodrigues
    affiliation: 15
    orcid: 0000-0002-4849-1537
    role: Writing - original draft
    
  - name: Dennis Psaroudakis
    orcid: 0000-0002-7521-798X
    affiliation: 3
    role: Writing – original draft
    
  - name: Nils Reinosch
    affiliation: 9
    role: Writing – original draft
    
  - name: Jascha Jung
    affiliation: 9
    role: Writing – original draft
    
  - name: Heinrich Lukas Weil
    affiliation: 14
    orcid: 0000-0003-1945-6342
    role: Writing - original draft
  
affiliations:
  - name: ZB MED - Information Centre for Life Sciences
    index: 1
    ror:
    
  - name: Université Paris-Saclay, INRAE, URGI, Versailles, France
    index: 2
    ror:
        
  - name: Leibniz Institute for Plant Genetics and Crop Plant Research (IPK) Gatersleben, Germany
    index: 3
    ror: 
    
  - name: Department of Biotechnology and Systems Biology, National Institute of Biology, Ljubljana, Slovenia #Večna pot 121, 1000 
    index: 4
    ror: 
    
  - name: Instituto de Tecnologia Química e Biológica António Xavier, Universidade Nova de Lisboa  (ITQB NOVA), Oeiras, Portugal
    index: 5
    ror: 
    
  - name: Centro de Biotecnologia Agrícola e Agro-alimentar do Alentejo (CEBAL), Beja, Portugal
    index: 6
    ror: 
    
  - name: MED–Instituto Mediterrâneo para a Agricultura, Ambiente e Desenvolvimento & CHANGE–Global Change and Sustainability Institute, Évora, Portugal
    index: 7
    ror: 
    
  - name: Rothamstead Research
    index: 8
    ror: 
    
  - name: Kuratorium für Technik und Bauwesen in der Landwirtschaft e.V. (KTBL)
    index: 9
    ror: 
    
  - name: Senckenberg Society for Nature Research
    index: 10
    ror: 
    
  - name: Université Paris-Saclay, INRAE, BioinfOmics, Plant Bioinformatics Facility, Versailles, France
    index: 11
    ror: 
    
  - name: Forschungszentrum Jülich GmbH
    index: 12
    ror: 
    
  - name: Cluster of Excellence on Plant Sciences (CEPLAS), Faculty of Mathematics and Natural Science, Heinrich Heine University, Düsseldorf, Germany
    index: 13
    ror: 
    
  - name: RPTU Kaiserslautern-Landau, Rheinland-Pfälzische Technische Universität Kaiserslautern-Landau, Technische Universität Kaiserslautern
    index: 14
    ror: 
    
  - name: Albert-Ludwigs-Universität Freiburg
    index: 15
    ror: 
    
date: 18 december 2023
cito-bibliography: paper.bib
event: BH23DE
biohackathon_name: "2th BioHackathon Germany"
biohackathon_url: "https://www.denbi.de/de-nbi-events/1547-biohackathon-germany-2"
biohackathon_location: "Bielefeld, Germany"
group: Project 9
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackrxiv/publication-template
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Gabriel Schneider \emph{et al.}
---

# Introduction

As part of the de.NBI BioHackathon 2023, we here report about our progress on increasing FAIR-compliance in agrosystem sciences and plant phenomics. Through the collaborative efforts of the agrosystem and plant sciences communities, research data are available through various data repositories and infrastructures. To foster these developments and increase the value for the communities, enabling FAIR-compliance for scientific datasets is one top priority strategic aim. Due to the heterogeneity of the sub-domains and their requirements, we addressed three challenges with direct relation to specific FAIR principles: Increasing findability of digital agrosystem resources by extending Schema.org, Enabling easy creation of MIAPPE-compliant ISA metadata for Plant Phenotyping Experiments, and Increasing Plant Data Accessibility and Collaboration with FAIDARE. 

## Increasing findability of digital agrosystem resources by extending Schema.org

### Introduction

Research Data Infrastructures (RDIs) in the agrosystem domain established services and published research data of their communities for years. Each infrastructure is tailored to its users' needs, also concerning its metadata, leading to a very heterogeneous landscape. To increase the findability of their content via search engines, RDIs can expose the metadata of resources as markup via Schema.org. 
In the context of [FAIRagro](https://fairagro.net/), the German National Research Data Infrastructure for the agrosystem domain, several RDIs already do so: For each landing page of a dataset, a [JSON-LD](https://json-ld.org/) based resource is created, that contains part of the metadata information, using Schema.org types and properties. This annotation is then consumed by search engines to present enriched search results to users. As Schema.org follows a generic approach, its core schema doesn't suffice in describing all entities relevant for agrosystem researchers with the required level of detail.
Therefore this hackathon subproject evaluated Schema.org, its extension [Bioschemas](https://bioschemas.org/) and the [Agri-schemas](https://github.com/Rothamsted/agri-schemas) project in regards to modeling metadata of datasets relevant to [FAIRagro](https://fairagro.net/) use cases. 

Following the [FAIR principles](https://www.go-fair.org/fair-principles/) and its ideas on reusability, the approach was to identifiy which kinds of entities relevant to the agrosystems domain, could also be modelled with already available types and properties and where gaps are, that could be closed in the future with an extension of mentioned schemas.

### Tasks

During the hackathon the project group analysed different published datasets, relevant to a crop modeling use-case in FAIRagro. For each dataset the group identified the entities described in the metadata, directly provided via the RDI that published the datasets, as well as the contents of the datafiles themselves. 
As the provision of Schema.org markup in our projects context is about increasing the findability of digital resources, we focussed on entities, that agrosystem scientists will most likely search for. Soil, crop, fertilizers and management actions were identified as central entities for searches, based on feedback by hackathon participants and discussions of the project group.

For crop and soil, the project group used types and properties of Schema.org / Bioschemas / Agri-schemas to model the metadata information of the example datasets and their included entities explicitly. For technical representation of modelling the information the project group used either [Turtle](https://www.w3.org/TR/turtle/) as an RDF serialization or [JSON-LD](https://json-ld.org/), one of the formats Schema.org uses.

As Schema.org builds the foundation for metadata description in [RO-Crates](https://www.researchobject.org/ro-crate/), we converted one of the analysed datasets to an RO-Crate, to demonstrate how RDIs could enrich their datasets to achieve increased interoperability towards [FAIR Digital Objects](https://fairdo.org/1316-2/). 
In parallel to the modelling we analysed how RDIs currently use Schema.org and how they could improve their usage. To demonstrate the benefits of such an optimisation, we outlined new search queries that users would be able to execute after implementation.

### Results

A central result of the hackathon work is the realisation that many of the requirements of the analysed use-case can be satisfied by contributing to already existing communities, such as Bioschemas. By following its community based approach of extension, the agrosystem domain can work on establishing the concepts it needs, while embedding them in a broader context, increasing interoperability. 
During the modelling of example dataset metadata with already available types and properties of Schema.org / Bioschemas / Agri-schemas, we identified multiple approaches, that are feasible, depending on requirements of specific use cases.

Crop is one of the central entities, found in a majority of the analysed datasets. It describes a type of plant, that is in some way related to a dataset. It can be expressed using the type "FieldTrialMaterialSource" from Agri-schemas, which is a proposition of a subclass of Bioschemas ["BioChemEntity"](https://bioschemas.org/BioChemEntity).  The crop is described with a ["taxonomicRange"](https://schema.org/taxonomicRange), which is a property of "BioChemEntity". Furthermore it relies on the Schema.org core properties ["name"](https://schema.org/name) and ["subjectOf"](https://schema.org/subjectOf) to link it to a ["Study"](https://bioschemas.org/Study). Implementing this approach would mean the development of a new subclass. Using the term "FieldTrialMaterialSource", which has its source in the [MIAPPE](https://www.miappe.org/) standard, would increase the understanding of researchers familiar with MIAPPE terminology.
An example study on wheat (*Triticum aestivum*) could be modelled the follwing way:

    @prefix bioschemas: <https://bioschemas.org/> . 
	@prefix agri: <https://github.com/Rothamsted/agri-schemas/> . 
	@prefix schema: <https://schema.org/> . 

	<example_study> a bioschemas:Study .
	<example_crop_source> a agri:FieldTrialMaterialSource,
        schema:BioChemEntity;
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
		dct:conformsTo 
        <https://bioschemas.org/profiles/example_Crop/0.1-TO-BE-CREATED> ;
		bioschemas:taxonomicRange 
        <http://aims.fao.org/aos/agrovoc/c_890> ;
        schema:name "Beta vulgaris"
		] .

The decision between a subclass vs. a profile based approach depends on the necessity of new properties. Both presented options leverage existing Bioschemas resources, but differ in their extension requirements. A profile "Crop" for [BioChemEntity](https://bioschemas.org/BioChemEntity) would be sufficient, if relevant search queries can be satisfied with the use of BioChemEntity properties, e.g. by employing values from domain specific ontologies and by defining marginalities.

Defining a subclass instead, that inherits all properties of its superclass(es) additionally to its own specific properties, would open new possibilities for describing agrosystem datasets and therefore enable new search queries them. With the example of crop as "FieldTrialMaterialSource" a new property "variety" might be relevant, to enable searches for specific varieties.
    
    @prefix bioschemas: <https://bioschemas.org/> . 
	@prefix agri: <https://github.com/Rothamsted/agri-schemas/> . 
	@prefix schema: <https://schema.org/> . 

	<example_study> a bioschemas:Study .
	<example_crop_source> a agri:FieldTrialMaterialSource, 
    schema:BioChemEntity;
		bioschemas:taxonomicRange <http://aims.fao.org/aos/agrovoc/c_7951>;
		schema:name "Triticum aestivum";
        bioschemas:exampleProperty_variety
        <https://fsp.ucdavis.edu/seed-catalog/wheat-varieties/Yecora-Rojo> ;
		schema:subjectOf <example_study>;
		schema:identifier <example_identifier> .  

To evaluate on which entities are most relevant and how best to model them, a result of the hackathon is the founding of a agricultural Bioschemas working group. The results of the hackathon will be used as a foundation to discuss required entities and how to model them in detail. The ideas will then be discussed with a broader community via Bioschemas established processes. The working group will be open to everyone interested in working on increasing the findability of agriculture related digital resources.

Further results and material can be found in the subprojects Github repository, created during the hackathon: https://github.com/fairagro/biohackathon2023.

## MIAPPE Wizard - Enabling easy creation of MIAPPE-compliant ISA metadata for Plant Phenotyping Experiments

### Introduction

The MIAPPE Wizard is a tool that should make MIAPPE-compliant metadata annotation of plant phenotyping experiments as easy as possible. It should hide the complexity of the ISA framework, ontology selection and annotation and mapping of attributes of the MIAPPE checklist to ISA entities for non-expert users.
The development of the MIAPPE Wizard began with the first Biohackathon Germany in 2022 [@citesAsAuthority:denbi_biohack_2022].

### Results

The focus at this year's de.NBI BioHackathon was to enhance and extend the features available in the MIAPPE Wizard. Previously, the Wizard was only capable of creating ISA JSON and ISA Tab formatted archives, with a significant amount of MIAPPE specific metadata missing. This year, the group focused on implementing a) the MIAPPE checklist b) the management of protocols and c) the upload of material and sample sheets. 

In addition to supporting ISA Tab and ISA JSON, the MIAPPE Wizard was also enhanced to create "Annotated Research Contexts" (ARC) by using the [ARCtrl Javascript library](https://github.com/nfdi4plants/ARCtrl) provided by the NFDI DataPLANT consortium. The ARC can be downloaded as a zip archive and transferred from the local machine to PLANTdataHUB through `git` [@citesAsAuthority:plantdatahub]. The direct transfer of ARC archives to a PLANTdataHUB instance is still in development.

The graphical user interface was improved by adding a progress bar and updating the color scheme and logo.

### Discussion

The integration of ontology terms, which is a challenging task, is still missing and a task for future activities.

## FAIDARE: Increasing Plant Data Accessibility and Collaboration through Integration, Usability and Community Engagement

### Introduction

FAIDARE (https://urgi.versailles.inra.fr/faidare) is a comprehensive search portal harvesting diverse plant-centric data resources and providing a central access point for the plant research community. It addresses the findability aspect of the FAIR principles and is hosted and maintained by ELIXIR France and established as the European Search Portal for plant related datasets, in collaboration with EMPHASIS. For increasing the usability for the data users the aim of this subproject was connecting additional established resources used by the plant research community, specifically e!DAL-PGP (de.NBI/ELIXIR Germany)[@citesAsAuthority:Arend2020], CorkOakDB (ELIXIR Portugal)[@citesAsAuthority:Arias-Baldrich2020] and the Stress Knowledge Map (ELIXIR Slovenia)[@citesAsAuthority:Bleker2024] were the main targets of the project. 
<!-- 
To achieve this goal, we will use the common schema.org/BioSchemas markup to harvest and index these resources. In addition to these two major infrastructures, we will highly motivate additional resource providers to join us, and assess how this integration can be implemented to add their own system to the federated search portal of FAIDARE. To lower the barrier for connecting new data repositories, we also plan on generating training materials and ‘how-to’ guides to facilitate the future integration of additional data repositories. This will help to encourage the growth and expansion of FAIDARE as a comprehensive search portal for plant data and support capacity building for further resource providers. Therefore we are also looking for people who can support us in creating these materials and have knowledge on how to share and present it in a user appealing and helpful manner. This will enable researchers to access a wider range of plant data in a more efficient way and lead to greater collaboration and innovation within the field. Our vision is to create a comprehensive and user-friendly platform that serves as a one-stop-shop for all plant data needs.
-->

### Implementation

#### CorkOakDB
[CorkOakDB](https://corkoakdb.org/) is a web-based resource to access the draft genome sequence of cork oak (*Quercus suber*). It provides public access to a set of standard tools for data visualization and retrieval, including gene sequences, structural and functional annotation, as well as gene expression based on available datasets. 

In this project we have developed a method to access CorkOakDB through the existing web service and retrieve functional information of all cork oak gene entries, together with corresponding links. All this information was compiled in a structured JSON file, with the required metadata, following [FAIDARE](https://urgi.versailles.inra.fr/faidare/join) specifications. The scripts prepared for this purpose and additional documentation were deposited on [github](https://github.com/anausie/FAIDARECorkOakDB). The JSON file was then uploaded to [FAIRDOM SEEK](https://seek4science.org/), for efficient access by FAIDARE. 

#### Stress Knowledge Map
Stress Knowledge Map ([SKM](https://skm.nib.si)) is a publicly available resource containing two knowledge graphs describing current knowledge of biochemical, signalling, and regulatory molecular interactions in plants: a highly curated model of plant stress signalling (PSS, 1,425 entities and 543 reactions) and a large comprehensive knowledge network (CKN, 26,234 entities and 488,390 interactions). Both were constructed by domain experts through systematic curation of diverse literature and database resources. The main features include content exploration and visualisation, access to various export formats, and the ability to contribute novel biological knowledge. 

Prior to the hackathon, only PSS was indexed in FAIDARE (a total of 686 genes). During the project, indexing of PSS was improved, updating the number of genes to 750 and providing more contextual information. CKN was newly indexed, also on the gene level. This resulted in SKM providing a total of 14,045 entries in FAIDARE. To provide more compelling gene entry pages in SKM, PSS entries in FAIDARE are now directed to the interactive [PSS Explorer](https://skm.nib.si/biomine/). To make the same possible for CKN, SKM was extended during the project by adding a gene identifier URL parameter to the interactive [CKN Explorer](https://skm.nib.si/ckn/). To further aid FAIDARE users in searching for genes of interest, both also contain [GoMapMan](https://gomapman.nib.si) annotations and definitions per gene, that can be used to filter the results in FAIDARE. 

As a result of this project, SKM now provides two endpoints for harvest by FAIDARE (one for each knowledge graph, https://skm.nib.si/downloads/pss/public/faidare and https://skm.nib.si/downloads/ckn/faidare). Each provides gene level metadata in JSON format, reproduced at every knowledge graph update. 

#### e!DAL-PGP
The e!DAL-PGP (Plant Genomics and Phenomics Research Data Repository) is an infrastructure to comprehensively publish plant research data [@citesAsAuthority:Arend2020]. This covers in particular cross-domain datasets that are not being published in central repositories because of its volume or unsupported data scope, like image collections from plant phenotyping and microscopy, unfinished genomes, genotyping data, visualizations of morphological plant models, data from mass spectrometry as well as software and documents. All published datasets are accessible via a DOI linking to a dedicated content page, which embeds a schema.org and BioSchema markup in the HTML code.

In frame of this project the existing web server of e!DAL-PGP was extended to provide an additional endpoint which delivers dynamically a JSON dump of published datasets in a compatible format. This allows FAIdare to harvest all datasets on demand and add them to the internal search index. The endpoint is accessible at https://doi.ipk-gatersleben.de/faidare.json.

## Acknowledgements

This work was performed during the de.NBI BioHackathon Germany 2023 organized by ELIXIR Germany in December 2023. This work was funded by ELIXIR, the research infrastructure for life-science data; by the Federal Government of Germany and the county of North Rhine-Westphalia (de.NBI - the German Network for Bioinformatics Infrastructure); by the DFG in frame of the FAIRagro (https://www.fairagro.net, project number 501899475), NFDI4BioDiversity (https://www.nfdi4biodiversity.org, project number 442032008) and DataPLANT (https://www.nfdi4plants.de/, project number 442077441); consortia of the NFDI; by the Slovenian Research and Innovation Agency (https://projects.nib.si/translate/, project number Z4-50146); and by Fundação para a Ciência e a Tecnologia (Portugal) through the R&D Unit "GREEN-IT - Bioresources for Sustainability" (DOI: 10.54499/UIDB/04551/2020 and DOI: 10.54499/UIDP/04551/2020) and LS4FUTURE Associated Laboratory (DOI: 10.54499/LA/P/0087/2020). 

## References
