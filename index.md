---
title: Olek Gierczak
---

# About

Hi! My name is [Olek](mailto:gierczak.o@northeastern.edu) and I'm a third year PhD student studying under [Amal Ahmed](https://www.ccs.neu.edu/home/amal/) at the [Secure Interoperability, Languages, and Compilers](https://silc.ccs.neu.edu/) group, which is part of the [Programming Research Laboratory](https://prl.ccs.neu.edu/) at Northeastern University. Before coming to Northeastern, I worked under [Steve Zdancewic](https://www.cis.upenn.edu/~stevez/) and [Benjamin C. Pierce](https://www.cis.upenn.edu/~bcpierce/) at the University of Pennsylvania.

# Research Interests

I'm interested in creating formal models and properties that help researchers understand, compare,
and expand programming languages. In particular, I've been interested in the semantics of safe Rust
and more generally lifetimes and borrowing, as well as gradually typed languages and the
distinctions between type soundness and other correctness properties for them.

# Projects

I developed a semantic property of gradually typed languages called Type Vigilance that
determines when a language's type system matches its semantics. In other words, the static reasoning
provided by types and the dynamic type based reasoning programmers can perform based on those types
correspond. In gradual typing, values that flow through a program accumulate type assertions each
time they cross a "typed/untyped" boundary. Vigilance says that every value _semantically_ satisfies
every one of these type assertions.

In the past I've worked on [Oxide](https://arxiv.org/abs/1903.00982), a type safe syntactic
formalized semantics for surface level safe Rust which includes features like non lexical lifetimes,
reborrowing, and closures. The crucial realizations are that lifetimes can be modelled by
information from a form of points to analysis, and that this information can be used to give a
formal model of the borrowchecker. Using this realization we were able to prove Progress and
Preservation style soundness, and demonstrated our type system worked for the portion of the Rust
test suite we supported.

I'm currently working on a semantic model and type system for surface level safe Rust called Aecia.
Compared to Oxide, Aecia's type system will build on the work (incorporating lessons learned along
the way), but the semantic model and operational semantics are novel. Our operational semantics gets
stuck not only when memory safety is violated, but also when the principles of the borrowing
discipline are violated. It is based on [Stacked Borrows](), but specialized for safe surface Rust,
meaning a much stricter meaning of borrow is enforced. We will use the semantic model to show that
the type system indeed enforces this meaning of a borrow, and as a side effect produce a program
logic with primitives that behave like separation logic, enabling source based verification of Rust.

# Publications

[Type Vigilance And The Truth About Transient Gradual Typing,](http://olekg.pl/papers/vigilance.pdf) Olek Gierczak, Lucy
Menon, Christos Dimoulas, Amal Ahmed. Accepted in OOPSLA 2024 Round 1,
March 2024. [Technical Appendix](http://olekg.pl/papers/vigilance-techreport.pdf)

[Oxide: The Essence of Rust,](https://arxiv.org/abs/1903.00982)
Aaron Weiss, Olek Gierczak, Daniel Patterson, Amal Ahmed.
On arXiv, October 2021.
