---
title: 'The Plant Breeding Ontology (PBO): towards an ontology for the plant breeding community'
title_short: 'The Plant Breeding Ontology (PBO)'
tags:
  - Linked Data
  - Plant Breeding
  - Bio-Ontology
authors:
  - name: Erick Antezana
    orcid: 0000-0002-2497-8236
    affiliation: 1
  - name: Hiromi Kajiya-Kanegae
    orcid: 0000-0002-5719-7559
    affiliation: 2
  - name: Maria Gomez
    orcid: 0000-0003-2549-5807
    affiliation: 3
  - name: Shuichi Kawashima
    orcid: 0000-0001-7883-3756
    affiliation: 4
affiliations:
  - name: UN - International Computing Center (UNICC)
    index: 1
  - name: Research Center for Agricultural Information Technology (NARO)
    index: 2
  - name: Computational Bioscience Research Center (CBRC), King Abdullah University of Science and Technology (KAUST)
    index: 3
  - name: Database Center for Life Science, Joint Support-Center for Data Science Research, Research Organization of Information and Systems
    index: 4
date: 30 June 2023
cito-bibliography: paper.bib
event: BH23JP
biohackathon_name: "BioHackathon Japan 2023"
biohackathon_url:   "https://2023.biohackathon.org/"
biohackathon_location: "Kagawa, Japan, 2023"
group: R3
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackathon-jp/bh23-report-template
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: First Author \emph{et al.}
---

# Abstract

The need of standardizing the language used within a community has been recognized as one of the major components to enable a better integration of data as well as their further analysis. The plant breeding community makes use of a very specialized language, which has been evolving according to the new technologies and needs of their final users (e.g. farmers). That community is disparate all over the world. Therefore, a translation of the most common used terms has always been a key asset to accomplish their objectives as well as the ones of their collaborators. Here, we present PBO (Plant Breeding Ontology), an ontology for the plant breeding community which captures core 80 terms in 4 different languages: English (main language), Spanish, French, Dutch, German and Japanese, as well as their definitions, synonyms, derived terms and samples of their usage. PBO has been built partially manually and semiautomatically.

# Introduction

The exercise of standardizing the specialized vocabulary of a certain community is nowadays considered as an important component in any project, discussion, documentation, and so forth [Bos1995]. Several initiatives, from the academic and industrial sectors, have proposed standards for exchanging data, sharing documentation, or to simply provide a common framework to ensure a better communication [Shrestha2012]. The creation of specialized ontologies paves the way towards a uniform, standard language within a specialized community. The plant breeding community, as any other specialized community, has its own language in which the terminology is not only used by the plant breeders themselves but an entire chain of people: growers, researchers, regulatory affairs officers, and so on [Bruskiewich2008]. 

In spite of the existence of several glossaries, dictionaries, and in general terminological resources for the plant breeding community [Schlegel2009, Nagur, Jain2006, Choudhary2012], there are only a few resources which are first of all up-to-date, and that cover their terminology systematically, categorically and in various languages. Such a limitation prevents the common exchange channels to work in a more efficient manner. In this work, around 2500 terms were collected that are relevant for the plant breeding domain. Out of those 2500 terms, we have chosen 80 core entries for which a definition (plus its source), synonyms (plus their source) and their equivalents in other 5 languages: Spanish, French, Dutch, German, and Japanese are provided for each entry. In this work, English has been taken as the driver language for its importance in technical and specialized situations: R&D communications, business communications, data exchange between academic/industry partners, and computational systems support.

Another important motivation for improving PBO came from the BioHackathon 2023 to support the data harmonization and standardization efforts through controlled vocabularies, taxonomies and ontologies in the Life Sciences and within the academic research community in that domain. The resulting ontology is expected to be a key component for the next steps towards such a standardization.

This document is organized as follows: an introductory section (this section), which spells out the motivation and reasons on embarking on improving PBO; a methods section, which details how the ontology was built; an outcomes section, which summarizes the product features; and finally, the future work section delineates the next steps for the follow up of the ontology.

# Methods

a) Motivation and prospective users

The motivation for building an ontology about plant breeding is outlined in the introduction section; briefly, the need arises from better supporting the work of plant breeding actors:

  - seed growers,
  - plant breeders,
  - field testers,
  - wet-lab scientist,
  - dry-lab scientists (e.g. computational life scientists).

Although PBO is targeted to mainly support the activities of those prospective users, it could also be employed by other users or groups of people, for instance:

  - agronomists,
  - students (e.g. biology, biochemistry, terminology, computer sciences)
  - lawyers dealing with plant variety protection aspect,
  - regulatory affairs officers,
  - intellectual property counselors.

Given that the ontology is specialized, it might not be useful or informative for other groups of people (e.g. pilot, pediatrician). Nevertheless, it might be still hold terms that to some extend are found in the intersection of some domains. For instance, a pediatrician who works on particular genetic diseases might find terms relevant to his/her domain (e.g. mutant). The vast majority of users of PBO is expected to belong to: 

  1. the group of specialists in the domain who are formalizing their knowledge, refreshing it, or simply catching up with not-know terms
  2. the people who is relatively new to the plant breeding domain who have to learn the language of their colleagues, collaborators, or others.

b) Terms compilation and selection

The terminology of a specialized domain, such as plant breeing, is typically found in specialized literature (e.g., scientific articles) or specialized resources (e.g. databases). All terms considered in this work were collected from scientific publications within the plant breeding domain (see Table 1). The identification of candidate terms for the ontology was mainly driven by the author's experience and exposure to the plant-breeding domain. The  candidate terms cover diverse sub-domains within the plant-breeding field (e.g. breeding methods, genetics). Currently, PBO currently captures 80 core entries, which were picked up based on the following criteria (in order or importance):

  - The term serves as a “hub concept”, i.e. connects several other related concepts.
  - The term is found in most introductory and advanced literature about plant breeding.
  - The term is relevant for our current activities.

The “dumping out” of terms has been manually done: going through selected sections of the available material, then highlighting the nouns, adjectives and adverbs relevant to the field and according to the criteria stated above, then adding them into a graph of concepts (see map of concepts).

The compilation of the candidate terms produced several terms that were repeated (identical lexemes) and terms that were synonyms of other terms that had been already captured. In those cases, the terms were unified and only one representative was kept. During the compilation, several acronyms appeared often in the literature (e.g. SNP). The most frequent were considered in this work.

The selection of the 80 key terms ensures a balanced coverage of the various sub-domains represented in the resulting compilation. Some terms are very specialized to the domain (e.g., cultivar), while others are more generic (e.g., gene).

c) Network of concepts (NoC)

During the “dumping out” process, each candidate term was systematically added to a network of concepts. That network not only captured the terms themselves but also the relationships amongst them. Therefore, related terms were connected through a relationships which could either be hierarchical (sub-type) or simply connectional (i.e. there is a relation between the two terms, which is not hierarchical). Figure 1 shows a part of the network of concepts (NoC).

![Fig. 1](./biohackrxiv.png)

The plant-breeding network of concepts should be read from the top to the down for having a better overview of each entry and its conceptual neighborhood. Concepts that are at the same level of importance or that are somehow comparable are shown at the same horizontal level. On the one hand, the dotted lines between two nodes denote that there is a non-hierarchical relation between them (e.g. is involved in). On the other hand, the arrows connection two nodes denote a subtyping (hierarchical) relation. For the sake of readability, some nodes (shown in red) were duplicated. The length of each relationship has no meaning at all. However, the closer two entries that are connected to the same 3rd entry, the more related they are. 

The NoC was designed so that there are no isolated entries, that is, all of them are somehow connected. Such a connectivity strategy enables to “hop” from one entry to another one through related concepts.

Some nodes have more than 1 relationship connecting it to other terms; however, there are no nodes with more than one hierarchical link to a second generic node.

All the encircled nodes (80 in total) in the NoC are currently part of PBO. The rest (around 170) provide not only a context for the encircled nodes but also complementary information. Figure 2 depicts the entire network (due to its complexity and size, it is recommended to instead check the supplementary material to view the details thereof).

![Fug. 2](./biohackrxiv.png)

Organizing the concepts in a graph was essential to fulfill one of the aims of this work: categorize the entries in the ontology. 

d) Finding a definition for each concept

Several resources (see Table 2) were used to gather the definitions corresponding to the entries in PBO. Most of the ontology term definitions were collected from online resources, with the exception of a few hard-copy resources.

All the 80 key terms have a definition and a reference, which links the entry to the source of the definition itself. None of the definitions was adapted (i.e. changed).

e) Synonyms and derived terms

Systematic searches in dictionaries and online resources were manually performed in order to look up for synonyms as well as derived terms for each one of the 80 selected key entries. PBO has synonyms for more than 30 entries and derivatives for 12 entries.

f) A sample context

A sentence showing the usage of each term has been collected. The source of those examples is listed in Table 1. Each sentence has been carefully reviewed so that it belongs to the main domain: plant breeding. 

g) A manual compilation empowered by automatic retrieval 

All terms, their definitions, their synonyms an derived terms were manually collected. The network of concepts has also been manually built (terms plus relationships). During the entire process, various validations steps were included to ensure a high quality of the resulting product. Most of those validation steps were automatically done (computationally developed) to deal with aspects such a term duplication, consistency of identifiers, generation of reports based on the master data file, uniformity, ordering, formatting, etc.

Automatic tools (not yet publically available) were developed to support the compilation of the context samples and collocations. Also, those tools supported the automatic retrieval (from sources such as PubMed, WordNet, IATE, dict.org) of terms as well as the quality checks (e.g. consistency).

Another motivation for automatizing some parts of the process came from the fact that this ontology is expected to continue growing. Therefore, even thought it has taken a lot of time to develop such automatized solutions, future improvements will be facilitated. On the one hand, a more advanced natural language processing could improve the glossary building process.

Relying on automatic tools could be risky; thus, a manual curation component as part of the process should be envisaged.

# Results

1. The 80 core records capture the entries currently held in PBO. All entries have an ID of the form: PBO:nnnnnnn, where nnnnnnn corresponds to a unique number. It is important to note that even though almost all entries are nouns, most of them can also be employed as adjectives with no modification (e.g. inbreeding, mutant). Moreover, some entries may also be used as verbs (e.g. to plant, to phenotype). A separate property captures the term translations in five languages (Spanish, French, Dutch, German, and Japanese) for each record. Each one of the 80 core records has a definition as well as a reference, which corresponds to the source from where the definition was taken (see Table 2). Some entries include synonyms as well as acronyms (which for the sake of simplicity are captured within the same group). Finally, each entry provides a sample context text, where the term (or an inflection thereof) is employed (see excel file).

2. An ontology, named PBO, holding 80 core entries has been produced. This ontology aims at filling a gap in the plant breeding community in a way that the terminology could be findable, accessible, interoperable, and reusable (F.A.I.R). PBO is not intended to compete with ontologies from authoritative bodies or similar resources (e.g., Food and Agriculture Organization [AGROVOC], IATE [IATE], Crop Ontology Shrestha2012CO); on the contrary, it aims at complementing them by providing specially a categorical view of the terminology, which could be used in various languages and enable a better communication among the actors within the plant breeding community. PBO is currently available in OBO and RDF formats - an excel dump is as well available (see supplementary material) so that it could be easily reused, extended and shared. Building this ontology with the aid of specialized computational tools not only fostered the development of the terminological resources but also contributed to their quality and future enrichement.

# Future work

The resulting network of concepts amounts to almost 2500 entries (see the NoC in the supplementary data). We expect to cover, in the near future, the entries that were not taken into account in this improvement phase and to come up with a sounder ontology. PBO will be made available in a public ontology repository (e.g., BioPortal), so that it could get improved by experts in the field. The automatic tools that were implemented will be improved and ideally published as a complementary material to the ontology. 

## Acknowledgements

We would like to thank the fellow participants at BioHackathon 2023 for their collaboration and constructive advice, which greatly influenced our project. We are grateful to the organizers for providing this platform and the opportunity to collaborate.

## References

1. Bos1995
2. Shrestha2012
