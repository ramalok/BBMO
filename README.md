# BBMO Krabberød et al.

This repository contains data  from the Blanes Bay Microbial Observatory (BBMO) (http://bbmo.icm.csic.es)from the year 2004 until 2013 used in the manuscript of Krabberød et al. (https://doi.org/10.1101/2021.03.18.435965)


## Environmental data

Sample_metadata.v2.tsv : contains enviromental variables. See description in https://doi.org/10.1101/2021.03.18.435965

## Full OTU (ASV) data

ASV_full_table.tsv: contains OTUs (ASVs). See description in https://doi.org/10.1101/2021.03.18.435965

Table containing 2960 ASVs and 120 samples

```R
bbmo.asv.tab<-read.table(file="ASV_full_table.tsv", header=T, sep="\t")

dim(bbmo.asv.tab) # 2960  120

```

## Resident OTU table

ASV_residents.tsv: contains resident OTUs. See description in https://doi.org/10.1101/2021.03.18.435965

Table containing 709 ASVs and 120 samples

```R
resident.otu.table<-read.table(file="ASV_residents.tsv", header=T, sep="\t")

dim(resident.otu.table) # 709 120

```



## Core network

core.network.graphml: includes the full network containing 262 nodes and 1411 edges.
It can be easily loaded into igraph using:

``` R
library(igraph)

core.nw<-read_graph("core.network.graphml", format = c("graphml"))
```

