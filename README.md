# BBMO Krabberød et al.

This repository contains data  from the Blanes Bay Microbial Observatory (BBMO) (http://bbmo.icm.csic.es) from the year 2004 until 2013 used in the manuscript of Krabberød et al. (https://doi.org/10.1101/2021.03.18.435965). See further descriptions in this manuscript file.


## Raw data (fastq files)


DNA sequences are publicly available at the European Nucleotide Archive (http://www.ebi.ac.uk/ena; accession numbers PRJEB23788 for 18S rRNA genes & PRJEB38773 for 16S rRNA genes)



## Environmental data

Sample_metadata.v2.tsv : contains enviromental variables. 

```R
env.data<-read.table("Sample_metadata.v2.tsv", header=T, sep="\t")

dim(env.data) # 19 120
```


## Full OTU (ASV) table

ASV_full_table.tsv: contains OTUs (ASVs).

Table containing 2960 ASVs and 120 samples

```R
bbmo.asv.tab<-read.table(file="ASV_full_table.tsv", header=T, sep="\t")

dim(bbmo.asv.tab) # 2960  120

```

## Resident OTU (ASV) table

ASV_residents.tsv: contains resident OTUs. 

Table containing 709 ASVs and 120 samples

```R
resident.otu.table<-read.table(file="ASV_residents.tsv", header=T, sep="\t")

dim(resident.otu.table) # 709 120

```

## Core OTU (ASV) table

ASV_core.tsv: contains core OTUs. 

Table containing 259 ASVs and 120 samples

```R

core.asv<-read.table("ASV_core.tsv", header=T, sep="\t")

dim(core.asv) # 259 120

```

## Core network

core.network.graphml: includes the core network containing 262 nodes and 1411 edges.
It can be easily loaded into igraph using:

``` R
library(igraph)

core.nw<-read_graph("core.network.graphml", format = c("graphml"))
```








