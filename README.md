# README

We computed the capacity of a hedgehog spanned by two distinct complex numbers. Our 
computation builds on the Riemann parameterization of headgehogs computed by [Harry 
Schmidt](https://livewarwickac-my.sharepoint.com/personal/u2272428_live_warwick_ac_uk/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fu2272428%5Flive%5Fwarwick%5Fac%5Fuk%2FDocuments%2FHedgehogs%2FRiemann%5Fand%5Fhedegehogs%2Epdf&parent=%2Fpersonal%2Fu2272428%5Flive%5Fwarwick%5Fac%5Fuk%2FDocuments%2FHedgehogs&ga=1). The theory is contained in the file **notes.pdf**, while the Wolfram Language 
notebook **Animation** contains a visualization of the Riemann parameterization.


## TwoHedgehogs

**TwoHedgehogs** is a Wolfram Language package for visualizing the boundary values of a Riemann map associated with a two-hedgehog domain. It provides functions for computing the modulus of the uniformization map on the unit circle, locating distinguished branch points, and producing an interactive graphics illustrating the construction.

### Features

The package includes functions to

* compute the modulus of the uniformization map on the unit circle,
* visualize the parameterization of the unit circle,
* visualize the corresponding two-hedgehog domain,
* plot the boundary modulus as a function of the parameter, and
* interactively explore the construction through a `Manipulate` interface.

### Repository Contents

```text
TwoHedgehogs.wl      Wolfram Language package
Animation.nb         Notebook demonstrating the package
README.md            This file
main.pdf             pdf notes on the topic
```

### Requirements

* Wolfram Language / Mathematica Version 14.3 or later.

### Installation

Clone or download this repository.

Run the package `TwoHedgehogs.wl`. If `TwoHedgehogs.wl` is in the same directory as your notebook, load it with

```wl
Get[FileNameJoin[{NotebookDirectory[], "TwoHedgehogs.wl"}]]
```

Alternatively, if the package has been placed on Mathematica's `$Path`, load it with

```wl
Needs["TwoHedgehogs`"]
```

### Quick Start

After loading the package, the interactive demonstration is launched with

```wl
hedgehogAnimation[]
```

Individual functions can also be used directly. For example,

```wl
uniformizationValue[Pi/3, Pi, 2/3]

realQuillParameter[Pi, 2/3]

complexQuillParameter[Pi, 2/3]

domainGraphic[Pi, 2/3, Pi/4]

hedgehogGraphic[Pi, 2/3, Pi/4]

profileGraphic[Pi, 2/3, Pi/4]
```

### Exported Functions

In the following functions, `s` denotes the parameter associated with the given hedgehog while `p` is $\theta / \pi$,
where $\theta$ denotes the oriented anlge between the quills.

| Function                     | Description                                                       |
| ---------------------------- | ----------------------------------------------------------------- |
| `uniformizationValue[t,s,p]` | Computes the modulus of the Riemann map on the unit circle.       |
| `auxiliaryAngle[s,p]`        | Computes the auxiliary angle used in the branch-point formulas.   |
| `realQuillParameter[s,p]`    | Computes the parameter corresponding to the real endopoint.       |
| `complexQuillParameter[s,p]` | Computes the parameter corresponding to the complex endpoint.     |
| `domainGraphic[s,p,a]`       | Draws the parameterization of the unit circle.                    |
| `hedgehogGraphic[s,p,a]`     | Draws the corresponding two-hedgehog.                             |
| `profileGraphic[s,p,a]`      | Plots the boundary modulus as a function of the parameter.        |
| `hedgehogAnimation[]`        | Opens an interactive visualization.                               |

### Dynamic Content

The example notebook uses Mathematica's `Manipulate`, which relies on dynamic evaluation. Consequently, Mathematica may display the message

> *"This file contains potentially unsafe dynamic content."*

when the notebook is opened. This is expected behavior. If you trust the source of the notebook, choose **Enable Dynamic Content** to use the interactive visualization.

### Mathematical Background

The package accompanies the study of conformal mappings onto two-hedgehog domains. It visualizes the boundary parameterization of the associated Riemann map and highlights the distinguished branch points arising in the construction.

For the mathematical details, please refer to the accompanying notes.

### Author

Alessio Cangini

### License
?
