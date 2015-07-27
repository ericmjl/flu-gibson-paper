# Title Page

## Title

## Authors and Emails

|Author Name|Initials |Email|
|-----------|---------|-----|
|Eric J. Ma |(E.J.M.) |ericmjl@mit.edu|
|Islam T.M. Hussein|(I.H.)|ihus@mit.edu|
|Christopher Bandoro|(C.B.)|cbandoro@mit.edu|
|Wendy Puryear|(W.P.)|wpuryear@mit.edu|
|Jonathan A. Runstadler|(J.A.R.)|jrun@mit.edu|

## Author Affiliations

- Department of Biological Engineering: E.J.M., I.H., W.P., J.A.R.
- Microbiology Program: C.B.
- Division of Comparative Medicine: J.A.R.

## Corresponding Author

J.A.R.

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

A command-line interface (CLI) is provided. Users provide a FASTA formatted file that contains the DNA parts that they wish to amplify and stitch together. The DNA parts, listed top to bottom, are assumed to be ordered clockwise, corresponding to a single strand. The CLI provides the ability for researchers proficient in scripting to automate the production of multiple primer sets. A simple web interface is also provided for point-and-click ease of use, and is located at (#web interface address).

# Results and Discussion

To validate our primer design software, we performed the CPEC assembly method on a set of viral polymerase segments that had previously resisted successful restriction enzyme cloning, into a polymerase expression backbone, for viral assays. The four segments required were the PB2, PB1, PA and NP segments. The PCR reactions protocols were standardized across the reactions. Briefly, (#add PCR protocol + DpnI). Though non-specific banding patterns were observed (#figure), size selection of the correct band through gel purification followed by the CPEC protocol (#add protocol) resulted in successful clones, which were verified by restriction enzyme digest and sequencing (#figure, #table). Functional assays also showed expression of the viral polymerase (#figure).

To demonstrate the use of our software tool in the rescue of whole viruses, we cloned an H3N8 virus from cDNA into reverse genetics plasmids, using a similar protocol. Successful cloning was verified by sequencing, and TCID50 assays showed successful replication (#figure).

# Conclusions


# Availability


# Abbreviations


# Competing Interests


# Authors' Contributions


# Authors' Information


# Acknowledgments


# Endnotes


# References

