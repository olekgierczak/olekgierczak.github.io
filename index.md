---
title: Olek Gierczak
---

# About

Hi! My name is [Olek](mailto:gierczak.o@northeastern.edu) and I'm a third year PhD student studying under [Amal Ahmed](https://www.ccs.neu.edu/home/amal/) at the [Secure Interoperability, Languages, and Compilers](https://silc.ccs.neu.edu/) group, which is part of the [Programming Research Laboratory](https://prl.ccs.neu.edu/) at Northeastern University. Before coming to Northeastern, I worked under [Steve Zdancewic](https://www.cis.upenn.edu/~stevez/) and [Benjamin C. Pierce](https://www.cis.upenn.edu/~bcpierce/) at the University of Pennsylvania.

# Research Interests

I'm interested in creating formal models and properties that help
researchers understand, compare, and expand programming languages. In
particular, I've been interested in gradually typed languages, and the
distinctions between type soundness and other correctness properties,
as well as Rust and more generally alias management type systems.

# Projects


I've also developed a semantic property of gradually typed languages
called Type Vigilance that determines when a language's type system
matches its semantics, meaning that the static reasoning provided by
types and the dynamic type based reasoning programmers can perform
based on those types correspond. I proved that as expected the Natural
semantics is Vigilant with the standard type system. But I also
examined what type systems the Transient semantics is Vigilant for,
and developed a type system, dubbed Truer Transient Typing, that
provides stronger types than the first order tags seen in previous
work. I proved that Transient is vigilant with Truer Transient Typing,
showing that these types are a match with the semantics. I also found
that with these types came type based optimizations, which means that
type systems like Truer Transient Typing could provide more efficient
gradual typing with semantically honest types. In the future, I plan
to explore this by extending, implementing, and evaluating Truer
Transient Typing.

I've also been working on [Oxide](https://arxiv.org/abs/1903.00982), a
type safe formalized semantics for surface level safe Rust which
includes features like non lexical lifetimes, reborrowing, and
closures. The crucial realizations are that lifetimes can be modelled
by information from a form of points to analysis, and that this
information can be used to give a formal model of the borrowchecker.
Using this realization we were able to prove Progress and Preservation
style soundness, and demonstrated our type system worked for the
portion of the Rust test suite we supported. 

I've additionally been working on a type preserving compilation of
Oxide down to a lower level intermediate language based on [Paul
Levy](https://www.cs.bham.ac.uk/~pbl/)'s Call By Push Value. With such
a type preserving compilation in hand, we could model safe
interoperation at the low level language, and apply this to contexts
where we have a core safety sensitive component interacting with
unsafe code. The goal is to preserve Oxide types by mapping them to a
range of capabilities, some already well understood in the field, and
some new but fundamental, that are sufficient to model the
interactions between the features in Oxide. 

# Publications

[Type Vigilance And The Truth About Transient Gradual Typing,](http://olekg.pl/papers/vigilance.pdf) Olek Gierczak, Lucy
Menon, Christos Dimoulas, Amal Ahmed. In Submission ICFP 2023,
March 2023. [Technical Appendix](http://olekg.pl/papers/vigilance-techreport.pdf)

[Oxide: The Essence of Rust,](https://arxiv.org/abs/1903.00982)
Aaron Weiss, Olek Gierczak, Daniel Patterson, Amal Ahmed.
On arXiv, October 2021.
