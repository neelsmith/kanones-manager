---
layout: page
title: "Kanones manager"
nav_order: 0
---


# Kanones manager

`kanones-manager.jl` is a Pluto notebook that includes a parser for standard literary Greek built with the `Kanones` system.


## What it's for

With `kanones-manager`, you can:

- morphologically parse texts in standard literary Greek orthography using millions of precomputed analyses of vocabulary automatically extracted from LSJ
- add your own morphological stems for vocabulary not in the precomputed data set (e.g., personal names not in LSJ), and merge them with the precomputed data.


## What you need: software

- the [Julia](https://julialang.org) language, with [the Pluto package](https://github.com/fonsp/Pluto.jl) installed. 

## What you need: data

1. A downloaded copy of this set of [precomputed morphological analyses](https://www.homermultitext.org/morphology/morphology-current.csv) in `csv` format.
2. A copy or clone of the [`Kanones.jl`](https://github.com/neelsmith/Kanones.jl) repository.
3. A directory of delimited-text files with your additional morphological data, organized in subdirectories following Kanones' schema for data sets.  (For details about how to organize these delimited-text files, see the Kanones "[Guide to editing lexica](https://neelsmith.github.io/Kanones-vocab-guide/)."
4. A copy of the `kanones-manger.jl` Pluto notebook

You can keep these four items anywhere you like in your local file system if you adjust the settings in the Pluto notebook appropriately, but the simplest way to get started is to follow the default directory setup, either by copying this repository, or creating your own directory system like this:

```
.
├── Kanones.jl (a copy or clone of the Kanones.jl repository)
└── kanones-manager (or your own directory)
    ├── morphology
    │   ├── datatables (a standard Kanones dataset of delimited-text files)
    │   │   └── stems-tables
    │   │       ├── adjectives
    │   │       ├── nouns
    │   │       ├── verbs-compound
    │   │       └── verbs-simplex
    │   └── morphology-current.csv (the file of precomputed analyses)
    └── pluto
        └── kanones-manager.jl (the pluto notebook)
``` 


## How to use it

- start a Pluto notebook server, and open `kanones-manager.jl`
