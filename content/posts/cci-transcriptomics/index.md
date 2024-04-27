---
title: "Why Use Transcriptomics to Analyse Cell-Cell Interactions?"
date: 2024-04-27T11:49:09+08:00
draft: false
tags: ["bioinformatics"]
---

## What are Cell-Cell Interactions?
Cell-cell interactions (CCI) refer to the various ways in which cells within an organism communicate and interact with each other. These interactions are essential for coordinating cellular activities necessary for growth, development, function and survival of an organism. For example, neurons connecting at synapses to transmit nerve impulses is an example of a direct contact CCI. Another example is endocrine signalling, where, cells in specialised glands release hormones into the blood stream that are carried to distant parts of the body.

There are various types of cell-cell interactions. Here are a few that involve cells communicating with each other using chemical signals.
    - In **autocrine signalling**, a cell produces and releases a chemical messenger (like a hormone or growth factor) that binds to receptors on the same cell, leading to changes within the cells themselves. This kind of signalling in cancer cells leads to uncontrolled cell growth and survival.
    - **Paracrine signalling** refers to a cell releasing a signal to target nearby cells. These signals does not travel very far, affecting only cells in the immediate vicinity of the originating cell. A classic example is release of neurotransmitters by neurons.
    - When the signalling involves direct contact between the signalling cell and the target cell, often mediated by cell-membrane proteins or other molecules that interact directly, it is called **juxtacrine signalling**.
    - **Endocrine signalling** occurs when the glands or cells release hormones into the bloodstream, which then travel to distant targets like organs and tissues. For example, insulin secreted by pancreatic cells, travels throughout the body and regulates glucose uptake and metabolism.

The target cells have specific proteins on their surface or inside them, to which the signalling molecules bind. Once the receptor is activated, it starts a chain reaction inside the cell. These reactions usually involve multiple steps and various molecules in the cell, and usually reaches the cell's nucleus and causes a change in gene expression. Such changes in gene expression in a cell will affect how that cell behaves in it's microenvironment (think immediate neighbourhood), which in turn influences the behaviour of nearby cells. To understand the role of each cell within it's local community, one must identify protein messages passed between cells. Measuring expressed messenger molecules and associated pathways is necessary to understand the directionality, magnitude and relevance of CCIs.

## Transcriptomics

Directly measuring the proteins involved in the CCI is difficult since it requires specialised equipment and extensive domain knowledge. Moreover, these proteins cannot be always studied within their native microenvironment. However, specialised equipment like biochemical assays have been used to identify interactions between proteins that are secreted or displayed outside the cell to mediate CCI.

Proteomics and transcriptomics can be used to reinforce such studies. Proteomics is the field that studies the set of proteins that are expressed in a cell, tissue or an organism at a given time. Proteomics is useful for identifying and quantifying proteins that are secreted or displayed cell surfaces. Transcriptomics is the study of complete RNA transcripts that are produced by the genome. Using techniques like RNA sequencing (RNA-seq), transcriptomics helps in understanding which genes are being actively expressed in cells, providing *indirect evidence* for the presence of proteins. Evidence of expression from proteomics and transcriptomics can further reinforce the presence of proteins identified using biochemical assays.


## Why use transcriptomics to analyse CCI?
While proteomics is preferable since they directly measure protein abundances, RNA-seq datasets are plentiful and easier to access and analyse. Since RNA sequencing can be performed on bulk samples, micro-dissected specimens or single cell suspensions (single cell proteomic technologies are still under development), it can also enable CCI studies at different resolutions. Results from transcriptomics should be carefully considered and validated to avoid misleading hypothesis. However, the ubiquity and ease of analysis have enabled many recent studies to infer CCI from gene expression. In particular, coordinated gene expression of ligands and receptors can be used to infer intercellular communication.

In this post, we looked at what are cell-cell interactions and why transcriptomics can be used for detecting these interactions. In a future post, we can look at specific transcriptomics methods that is helpful for these analysis.

## Acknoledgement
This blog post contains by notes from reading the introduction section of the following paper:
> E. Armingol, A. Officer, O. Harismendy, and N. E. Lewis, “Deciphering cell–cell interactions and communication from gene expression,” Nat Rev Genet, vol. 22, no. 2, pp. 71–88, Feb. 2021, doi: 10.1038/s41576-020-00292-x.
