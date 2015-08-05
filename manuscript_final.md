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

Numerous advances in nucleic acid manipulation methods have come from the field of synthetic biology. Seamless cloning methods, such as the Gibson and CPEC (#abbr) assembly methods (#cite), enable molecular biologists to assembly plasmids of arbitrary sequences without needing to be concerned with restriction enzyme cut sites. Through reverse genetics methods, the influenza research community has had the capability to clone influenza viral segments from synthesized cDNA (#abbr)(#cite). However, the rapid mutation rate of IAV (#abbr)(#cite) may inadvertently introduce restriction enzyme sites into the influenza genome, hence complicating the process of genome cloning. Restriction cloning methods are the dominant technique in the influenza community, and hence there is an opportunity to disseminate seamless cloning protocols to improve the efficiency and rate of successful cloning for downstream applications. 

Here, we present, FluGibson, a software tool that can be used to automatically design primers for seamless cloning of influenza viral genomes. 

# Implementation

The software tool is implemented in the Python programming language. We implemented a graph-based algorithm for primer design, based on the design principles for the Gibson assembly method (#cite). We assume that each DNA part of the circular viral segment plasmid that need to be assembled together are ordered in a FASTA file in clockwise order.

Each DNA part represented as a node in a NetworkX (#cite) directed graph, where the directed edges indicate the 5' to 3' directionality of one strand. Primers are designed with 25 n.t. annealing to the DNA part, and 15 n.t. overhang with the upstream and downstream parts for a total length of 40 n.t., and are stored as node attributes. The primer total length can be specified (#TODO), though 40 n.t. is selected as a default as cost-effective primer ordering options exist for this primer length (#cite: Invitorgen website).

A command-line interface (CLI) is provided. Users provide a FASTA formatted file that contains the DNA parts that they wish to amplify and stitch together. The DNA parts, listed top to bottom, are assumed to be ordered clockwise, corresponding to a single strand. The CLI provides the ability for researchers proficient in scripting to automate the production of multiple primer sets. A simple web interface is also provided for point-and-click ease of use, and is located at (#web interface address)(#TODO).

# Results and Discussion

To validate our primer design software, we performed the CPEC assembly method on a set of viral polymerase segments that had previously resisted successful restriction enzyme cloning, into a polymerase expression backbone, for viral assays. The four segments required were the PB2, PB1, PA and NP segments. The PCR reactions protocols were standardized across the reactions. Briefly, (#add PCR protocol + DpnI). Though non-specific banding patterns were observed (#figure), size selection of the correct band through gel purification followed by the CPEC protocol (#add protocol) resulted in successful clones, which were verified by restriction enzyme digest and sequencing (#figure, #table - from Islam). Functional assays also showed expression of the viral polymerase (#figure - from Islam).

We also cloned an H3N8 virus from cDNA into reverse genetics plasmids with standardized UTR sequences. Successful cloning was verified by sequencing, and TCID50 assays showed successful replication (#figure - from Chris) at titers similar to frozen viral stocks (#figure - from Chris). Finally, we assembled a panel of HA and NA viral-like particles (VLPs), and successfully validated their presence in viral cells (#figure - from Wendy, get protocol as well), and their antigenicity values.

Beyond the immediate applications of automated primer design as described here, we believe that the issue of protocol and data standards needs to be raised. Viral characterization is an integral part of molecular surveillance efforts. In our software development and experimental efforts here, we recognize that having standardized plasmid backbones would greatly facilitate our ability to rapidly clone viral segments for characterization and comparison of data. As such, we would like to propose the plasmid backbone sequences used here as standard viral expression backbones. Going forth, much discussion will be needed by the influenza research community on data reporting standards for particular assays, especially in academic publications. 

# Conclusions

FluGibson is a software tool that has the potential to enhance the influenza research community's capability to clone viruses for downstream applications. As the seamless cloning methods are agnostic to application, FluGibson also has applications beyond the influenza research community.

# Availability

FluGibson is available at:

1. PyPI: (#url) (#todo)
2. Github: (http://www.github.com/ericmjl/flu-gibson)

Documentation, along with examples, is available at (#url) (#todo).

# Abbreviations


# Competing Interests


# Authors' Contributions

- E.J.M. wrote the software and the paper.
- I.H. tested the primers in constructing plasmids for the polymerase assay.
- C.B. tested the primers in constructing plasmids for viral rescue.
- W.P. tested the primers in constructing plasmids for VLP production.
- J.A.R. wrote the paper.

# Authors' Information


# Acknowledgments

The authors would like to acknowledge funding from the NIH/NIAID CEIRS Program (Contract no.: HHSN272014000008C).

# Endnotes


# References

