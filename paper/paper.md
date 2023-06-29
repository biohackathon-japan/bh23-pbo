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

# Background

The need of standardizing the language used within a community has been recognized as one of the major components to enable a better integration of data as well as their further analysis. The plant breeding community makes use of a very specialized language, which has been evolving according to the new technologies and needs of their final users (e.g. farmers). That community is disparate all over the world. Therefore, a translation of the most common used terms has always been a key asset to accomplish their objectives as well as the ones of their collaborators. Here, we present PBO (Plant Breeding Ontology), an ontology for the plant breeding community which captures core 80 terms in 4 different languages: English (main language), Spanish, French, Dutch, German and Japanese, as well as their definitions, synonyms, derived terms and samples of their usage. PBO has been built partially manually and semiautomatically.

# Introduction

The exercise of standardizing the specialized vocabulary of a certain community is nowadays considered as an important component in any project, discussion, documentation, and so forth [Bos1995]. Several initiatives, from the academic and industrial sectors, have proposed standards for exchanging data, sharing documentation, or to simply provide a common framework to ensure a better communication [Shrestha2012]. The creation of specialized ontologies paves the way towards a uniform, standard language within a specialized community. The plant breeding community, as any other specialized community, has its own language in which the terminology is not only used by the plant breeders themselves but an entire chain of people: growers, researchers, regulatory affairs officers, and so on [ref]. 

In spite of the existence of several glossaries, dictionaries, and in general terminological resources for the plant breeding community [4-7], there are only a few resources which are first of all up-to-date, and that cover their terminology systematically, categorically and in various languages. Such a limitation prevents the common exchange channels to work in a more efficient manner. In this work, around 2500 terms were collected that are relevant for the plant breeding domain. Out of those 2500 terms, we have chosen 80 core entries for which a definition (plus its source), synonyms (plus their source) and their equivalents in other 5 languages: Spanish, French, Dutch, German, and Japanese are provided for each entry. In this work, English has been taken as the driver language for its importance in technical and specialized situations: R&D communications, business communications, data exchange between academic/industry partners, and computational systems support.

Another important motivation for improving PBO came from the BioHackathon 2023 to support the data harmonization and standardization efforts through controlled vocabularies, taxonomies and ontologies in the Life Sciences and within the academic research community in that domain. The resulting ontology is expected to be a key component for the next steps towards such a standardization.

This document is organized as follows: an introductory section (this section), which spells out the motivation and reasons on embarking on improving PBO; a methods section, which details how the ontology was built; an outcomes section, which summarizes the product features; and finally, the future work section delineates the next steps for the follow up of the ontology.

# Outcomes

1. The 80 core records capture the entries currently held in PB. All entries have an ID of the form: PBO:nnnnnnn, where nnnnnnn corresponds to a unique number. It is important to note that even though almost all entries are nouns, most of them can also be employed as adjectives with no modification (e.g. inbreeding, mutant). Moreover, some entries may also be used as verbs (e.g. to plant, to phenotype). A separate property captures the term translations in five languages (Spanish, French, Dutch, German, and Japanese) for each record. Each one of the 80 core records has a definition as well as a reference, which corresponds to the source from where the definition was taken (see Table 2). Some entries include synonyms as well as acronyms (which for the sake of simplicity are captured within the same group). Finally, each entry provides a sample context text, where the term (or an inflection thereof) is employed (see excel file).

2. An ontology, named PBO, holding 80 core entries has been produced. This ontology aims at filling a gap in the plant breeding community in a way that the terminology could be findable, accessible and reusable. PBO is not intended to compete with ontologies from authoritative bodies or similar resources (e.g. Food and Agriculture Organization [ref], IATE [ref]); on the contrary, it aims at complementing them by providing specially a categorical view of the terminology, which could be used in various languages and enable a better communication among the actors within the plant breeding community. PBO is currently available in OBO and RDF formats - an excel dump is as well available (see supplementary material) so that it could be easily reused, extended and shared. Building this ontology with the aid of specialized computational tools not only fostered the development of the terminological resources but also contributed to their quality and future enrichement.

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

# Future work

The resulting network of concepts amounts to almost 2500 entries (see the NoC in the supplementary data). We expect to cover, in the near future, the entries that were not taken into account in this improvement phase and to come up with a sounder ontology. PBO will be made available in a public ontology repository (e.g. EBI RDF platform), so that it could get improved by experts in the field. The automatic tools that were implemented will be improved and ideally published as a complementary material to the ontology. 

## Acknowledgements

We would like to thank the fellow participants at BioHackathon 2023 for their collaboration and constructive advice, which greatly influenced our project. We are grateful to the organizers for providing this platform and the developers of open source language models. Special thanks to our mentors, advisors, and colleagues for their guidance and support. Without their contributions, our project in linked data standardization with LLMs in bioinformatics would not have been possible.

## References

1.
