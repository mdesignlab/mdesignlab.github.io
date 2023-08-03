---
title: "Introduction"
description: ""
lead: "Doks is a Hugo theme for building secure, fast, and SEO-ready documentation websites, which you can easily update and customize."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "first-step"
weight: 100
toc: true
---

<h1> DFT-CES Tutorials </h1>

<div class="callout callout-info">
A mean-field QM/MM method, DFT-CES which stands for the <strong> density functional theory in classical explicit solvents.</strong>
</div> 

## What is DFT-CES for?
Describing solvation effects on electronic structures of condensed-phase systems and catalytic systems have been recently studied by a variety of methods such as density functional theory (DFT) calculations coupled with implicit solvation models. However, the specific configuration or stabilization of reactant in solvated system has been reported, and this can be a kinetically significant influence.

Then, how can explicit solvents be considered without much increase in computational cost? What can you see from the result?

We are dealing with this using a mean-field QM/MM method, DFT-CES. You can check the details at [DFT-CES](https://doi.org/10.1021/acs.jctc.6b00469); J. Chem. Theory Comput. 12, 10 (2016), [DFT-CES2](https://ththjang.github.io); J. Chem. Theory Comput. XXX

Our new generation of QM/MM method has been released in public.

This site has introductory materials which will let you know how to perform DFT-CES simulation, and ways to go further to apply to your own system of interest.

## First Steps

Starting from the installation of open-source programs and relevant libraries, if you are already set to perform calculations in real-space grid with DFT-CES. You can skip here.

[Install]({{< relref "installation" >}}) --- How to install and couple two different methods for DFT-CES.


## How to use for various systems

[Small Molecule in Water]({{< relref "homogeneous" >}}) --- How to construct a homogeneous system for DFT-CES.
[Heterogeneous Catalyst]({{< relref "heterogeneous" >}}) --- Move onto a heterogeneous system.

## Recent Publications using DFT-CES

[Anion Salt-in-Water](https://pubs.acs.org/doi/full/10.1021/jacsau.3c00061) --- Oh et al., JACS Au 3, 5 (2023).
<br>
[Solvation Shell on Zinc](https://onlinelibrary.wiley.com/doi/10.1002/anie.202211589) --- Kim et al., Angew. Chem. 134, e202211589 (2022)
<br>
[C1 and C2 on Electrocatalyst](https://www.nature.com/articles/s41467-022-33199-8) --- Shin et al., Nat. Commun. 13, 5482 (2022)
<br>
[π–π Interaction](https://www.mdpi.com/1422-0067/23/17/9811) --- Paik & Lee et al., Int. J. Mol. Sci. 23, 17 (2022)
<br>
[Review of DFT-CES](https://onlinelibrary.wiley.com/doi/10.1002/bkcs.12485) --- Jang & Paik et al., Bull. Korean Chem. Soc. 43, 476 (2022)
<br>
[Electric Double Layer](https://www.nature.com/articles/s41467-021-27909-x) --- Shin et al., Nat. Commun. 13, 174 (2022)

<!-- ## Get started

There are two main ways to get started with Doks:

### Tutorial

{{< alert icon="👉" text="The Tutorial is intended for novice to intermediate users." />}}

Step-by-step instructions on how to start a new Doks project. [Tutorial →](https://getdoks.org/tutorial/introduction/)

### Quick Start

{{< alert icon="👉" text="The Quick Start is intended for intermediate to advanced users." />}}

One page summary of how to start a new Doks project. [Quick Start →]({{< relref "quick-start" >}})

## Go further

Recipes, Reference Guides, Extensions, and Showcase.

### Recipes

Get instructions on how to accomplish common tasks with Doks. [Recipes →](https://getdoks.org/docs/recipes/project-configuration/)

### Reference Guides

Learn how to customize Doks to fully make it your own. [Reference Guides →](https://getdoks.org/docs/reference-guides/security/)

### Extensions

Get instructions on how to add even more to Doks. [Extensions →](https://getdoks.org/docs/extensions/breadcrumb-navigation/)

### Showcase

See what others have build with Doks. [Showcase →](https://getdoks.org/showcase/electric-blocks/)

## Contributing

Find out how to contribute to Doks. [Contributing →](https://getdoks.org/docs/contributing/how-to-contribute/)

## Help

Get help on Doks. [Help →]({{< relref "how-to-update" >}}) -->
