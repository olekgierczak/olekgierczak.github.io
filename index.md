---
title: Olek Gierczak
---

# About

Hi! My name is [Olek](mailto:gierczak.o@northeastern.edu) and I'm a sixth year
PhD student studying under [Amal Ahmed](https://www.ccs.neu.edu/home/amal/) at
the [Secure Interoperability, Languages, and
Compilers](https://silc.ccs.neu.edu/) group, which is part of the [Programming
Research Laboratory](https://prl.ccs.neu.edu/) at Northeastern University.
Before coming to Northeastern, I worked under [Steve
Zdancewic](https://www.cis.upenn.edu/~stevez/) and [Benjamin C.
Pierce](https://www.cis.upenn.edu/~bcpierce/) at the University of
Pennsylvania.

# Research Interests

I'm interested in creating formal models and properties that help researchers
understand, compare, and expand programming languages. In particular, I've been
interested in the semantics of Rust-style borrowing, as well as gradually typed
languages, and I'm currently exploring a gradual presentation of borrowing.

# Projects

I developed a semantic property of gradually typed languages called Vigilance
that determines when a language's type system matches its semantics. In other
words, the static reasoning provided by types and the dynamic type based
reasoning programmers can perform based on those types correspond. In gradual
typing, values that flow through a program accumulate type assertions each time
they cross a "typed/untyped" boundary. Vigilance says that every value
_semantically_ satisfies every one of these type assertions.

In the past I've worked on [Oxide](https://arxiv.org/abs/1903.00982), a type
safe syntactic formalized semantics for surface level safe Rust which includes
features like non lexical lifetimes, reborrowing, and closures. The crucial
realizations are that lifetimes can be modelled by information from a form of
points to analysis, and that this information can be used to give a formal
model of the borrowchecker. Using this realization we were able to prove
Progress and Preservation style soundness, and demonstrated our type system
worked for the portion of the Rust test suite we supported.

I'm currently working on a more fundamental calculus for Rust style borrowing,
with a rich program logic built from the ground up. We restrict to lexical
lifetimes, but as a result get a much simpler type system and logic. We hope PL
research that seeks to examine borrowing in contexts further from Rust can
utilize the simpler formalism to expand and prototype easier and faster.

Alongside this borrow calculus, I'm currently working on a gradual version of
the borrow calculus, where the "unknown" type is an unrestricted pointer, and
casts move between borrows managed by the type system and pointers with
(potentially) some dynamic enforcement. I hope to implement multiple dynamic
borrow enforcement strategies and analyze them with the lens of Vigilance.

# Publications

[Gradually Typed Languages Should Be
Vigilant!,](http://olekg.pl/papers/vigilance.pdf) Olek Gierczak, Lucy Menon,
Christos Dimoulas, Amal Ahmed. OOPSLA 2024, March 2024.
[Technical Appendix](http://olekg.pl/papers/vigilance-techreport.pdf)

[Oxide: The Essence of Rust,](https://arxiv.org/abs/1903.00982)
Aaron Weiss, Olek Gierczak, Daniel Patterson, Amal Ahmed.
On arXiv, October 2021.
