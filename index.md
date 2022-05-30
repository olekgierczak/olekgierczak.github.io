---
title: Olek Gierczak
---

# About

Hi! My name is [Olek](mailto:gierczak.o@northeastern.edu) and I'm a third year PhD student studying under [Amal Ahmed](https://www.ccs.neu.edu/home/amal/) at the [Secure Interoperability, Languages, and Compilers](https://silc.ccs.neu.edu/) group, which is part of the [Programming Research Laboratory](https://prl.ccs.neu.edu/) at Northeastern University. Before coming to Northeastern, I worked under [Steve Zdancewic](https://www.cis.upenn.edu/~stevez/) and [Benjamin C. Pierce](https://www.cis.upenn.edu/~bcpierce/) at the University of Pennsylvania.

# Research Interests

I'm broadly interested in creating formal models and properties that help researchers understand, compare, and expand programming languages.

I've been working on [Oxide](https://arxiv.org/abs/1903.00982), a type safe formalized semantics for surface level safe Rust which includes features like non lexical lifetimes, reborrowing, and closures. The crucial realizations are that lifetimes can be modelled by information from a form of points to analysis, and that this information can be used to give a formal model of the borrowchecker. Using this realization we were able to prove Progress and Preservation style soundness, and demonstrated our type system worked for the portion of the Rust test suite we supported. 

I've also been working on semantically modelling a property of gradual typing called Complete Monitoring. You can view a value in a gradually typed programming language as travelling through various boundaries which have type specifications on the possibly untyped value. But in many gradually typed semantics, these type specifications can have little to no enforcement, and so can be misleading for the programmer. [Existing work](https://cs.brown.edu/people/bgreenma/publications/apples-to-apples/gfd-oopsla-2019.pdf) specifies Complete Monitoring as a labelled reduction semantics that transforms, propogates, and removes labels according to a set of laws. This approach lacks both intuition for the property as well as generality. My work comes in the form of a unary Logical Relation that instead keeps the complexity in the model, and allows a wide range of languages with minimal changes. 

I've started working on a type preserving compilation of Oxide down to a lower level intermediate language based on [Paul Levy](https://www.cs.bham.ac.uk/~pbl/)'s Call By Push Value. With such a type preserving compilation in hand, we could model safe interoperation at the low level language, and apply this to contexts where we have a core safety sensitive component interacting with unsafe code. The goal is to preserve Oxide types by mapping them to a range of capabilities already well understood in the field that are sufficient to model the interactions between the features in Oxide. 

# Publications

[Oxide: The Essence of Rust](https://arxiv.org/abs/1903.00982)
Aaron Weiss, Olek Gierczak, Daniel Patterson, Amal Ahmed.
On arXiv, October 2021.
