---
title: "Small Molecule in Water"
description: "Doks is a Hugo theme for building secure, fast, and SEO-ready documentation websites, which you can easily update and customize."
lead: "Doks is a Hugo theme for building secure, fast, and SEO-ready documentation websites, which you can easily update and customize."
date: 2021-10-06T08:48:57+00:00
lastmod: 2021-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "first-step"
weight: 110
toc: true
---

<h1>
# Small Molecule in Water
</h1>

<div class="callout callout-info">
Example, a homogenous aqueous system
</div>

<br>

[SAMPL0](http://www.samplchallenges.org/) molecules have been chosen for a benchmark set to challenge and test how accurately our model predicts several properties of small molecules regarding the drug discovery.

One of the small molcules in the SAMPL0 set will be tested here to get started with DFT-CES.

<h2>
Get Started
</h2>
A system consists of one benzyl bromide molecule and 1000 water molecules. The benzyl bromide will be treated at quantum mechanics (QM) level, while the water molecules will be treated at the molecular mechanics (MM) level, described by the [TIP4P](https://doi.org/10.1063/1.1683075) model.

{{< alert icon="👉" text="Check out the details of TIP4P water model." />}}

<h3>
Construction of Systems
</h3>

{{< alert icon="💡" text="The information for QM/MM coupling is mediated by the real-space grid." />}}

It is important to note that in our real-space grid-based approach, the exchange of inforamtion about interactions across the systems occurs through the grid. Therefore, it is necessary to first construct the grid.

The grid will cover the whole QM/MM system, and its grid size is determined based on the QM system, taking into account the desired level of accuracy. Considering the memory allocation requirements, it is generally recommended to have a grid size of around 0.15 angstrom along x-, y-, and z-coordinate. When performing DFT calculations, the default number of grid points (nr1, nr2, nr3) is typically sufficient, based on the [ecutrho](https://www.quantum-espresso.org/Doc/INPUT_PW.html#idm313/) criterion.

In a homogeneous system, it is important to consider the potential overlap between the QM and MM regions and the possibility of change in the density afterwards. Taking these factors into account, you can utilize the OPLS force field to predict the density and adjust the grid size accordingly.

To proceed with the QM/MM system construction, you can follow these steps:

1. Define the QM and MM regions: Identify the specific atoms or molecular fragments that will be treated quantum mechanically (QM) and those that will be treated using the OPLS force field (MM). It is crucial to ensure that there is no overlap between the QM and MM regions.

2. Predict the density using the OPLS force field: Apply the OPLS force field to the MM region to obtain a density. This density prediction will serve as a basis for subsequent QM calculations.

3. Adjust the grid size: Since the QM calculations will be performed on a real-space grid, the grid size should be adjusted accordingly. Consider the level of accuracy required and ensure that the grid is fine enough to capture the relevant electronic properties of the QM region.

4. Deform the system box: On a given condition, `deform` the box to obtain a cell with the structure which is presumably acceptable.

5. Perform QM calculations: Use an appropriate quantum mechanical method (e.g., DFT) to perform calculations on the QM region. The QM/MM interface will allow for the exchange of information between the QM and MM regions.

By following these steps, you can construct a QM/MM system for a homogeneous system, taking into account the potential overlap between regions and adjusting the grid size based on the density prediction obtained from the OPLS force field.

{{< alert icon="💡" text="Here, the OPLS force field is used to predict the density at a glance. You can use some other force fields and then modify later on according to the result of QM/MM." />}}

{{< details "How to partition the system?" >}}
In DFT-CES, each region of the QM/MM system is not spatially partitioned. Instead, when it is necessary to analyze the electronic structure or when bond interactions are of primary importance, specific atoms are designated for QM calculations, while the remaining atoms are treated under the molecular mechanics (MM) representation.
{{< /details >}}

<h2>
## Go Further
</h2>
### Generation of Cube Files

Extract the information for coupling the QM/MM systems. First of all, obtain the cube file of electrostatic potential with 6 float numbers in a row.

The `plot_num = 11` will give you the bare potential and hartree potential as described in [pp.x](https://www.quantum-espresso.org/Doc/INPUT_PP.html) of Quantum ESPRESSO. And, plot another cube with `plot_num = 0` for the valence charge density. These cube files encompassing the QM system store the information for QM/MM simulations in DFT-CES (DFT-CES2 with charge density).

### Preparation for the Pauli Repulsion (DFT-CES2 only)

A gaussian convoluted density will be used to interpret the Pauli repulsion interaction across the interface between QM and MM subsystems where the non-bond interaction is dominant. We placed commands for the gaussian blurring after checking some requirements during the QM/MM iteration, you need to make sure that the libraries are installed properly to call the convolution function.

### Preparation for the Run

When you have all systems, and cube files intensionally modified, generally you can run the DFT-CES with the provided executable bash script, but you can do manually.

An executable for the same job but works with only one handy input will be soon released.
<h2>
## Run
</h2>

```bash
./qmmm.sh -c or --configuration
./qmmm.sh 
```

<h2>
## Analysis
</h2>

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
