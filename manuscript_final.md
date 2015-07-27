# Title


# Abstract

## Introduction

Reverse genetics methods enable influenza research community to clone viruses for genetic manipulation and biochemical characterization. The influenza research community uses traditional restriction cloning to assemble the necessary plasmids. However, with modern synthetic biology methods, it is possible to rapidly assemble the reverse genetics plasmids necessary from viral cDNA. 

## Results

Here, we present a software implementation of seamless cloning primer design tools tailored for use with the influenza research community, enabling rapid and cost-effective cloning of influenza viruses into reverse genetics and protein expression plasmids. The tool, (#currently unnamed), is available as a Python package on PyPI and Anaconda, and as a web app. Using the primers designed by (#currently unnamed software tool), we were able to rapidly clone a set of viral polymerases for a polymerase assay, which previously resisted cloning attempts. (#note: any other experimental results needed?) 

## Conclusions

Our (#software name) will enable the influenza research community to assemble the necessary reverse genetics plasmids for functional viral assays at a faster pace and lower cost. The software is freely available under the MIT License, and the source code is available on Github.

# Keywords

<!-- Note: There can be up to 10 keywords. -->
influenza, cloning, primer design, gibson assembly, CPEC assembly, reverse genetics, 


# Background

Numerous technical progresses in the past decade have enabled the influenza research community to rapidly clone viral gene segments for genetic manipulation and biochemical characterization. The advent 

# Implementation

The software tool is implemented in the Python programming language. We implemented a graph-based algorithm for primer design, based on the design principles for the Gibson assembly method (#cite). We assume that each DNA part of the circular viral segment plasmid that need to be assembled together are ordered in a FASTA file in clockwise order.

Each DNA part represented as a node in a NetworkX (#cite) directed graph, where the directed edges indicate the 5' to 3' directionality of one strand. Primers are designed with 25 n.t. annealing to the DNA part, and 15 n.t. overhang with the upstream and downstream parts for a total length of 40 n.t., and are stored as node attributes. (# The primer total length can be specified.)

# Results and Discussion


# Conclusions


# Availability


# Abbreviations


# Competing Interests


# Authors' Contributions


# Authors' Information


# Acknowledgments


# Endnotes


# References

