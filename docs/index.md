# Category Theory Notes

> Personal notes by [seikato](https://github.com/seikato/categorytheory)

---

## What Is This Site?

This site is a self-contained set of notes designed to help **general science and engineering students** — not specialist mathematicians — build an intuitive picture of modern mathematical structures as quickly as possible.

The goal is to climb from **sets** all the way up to **topological spaces**, **measurable spaces**, and eventually **category theory**, without getting lost in the weeds.

---

## The Problem This Site Addresses

Many students encounter abstract algebra for the first time through a textbook like Ichiro Satake's *Linear Algebra*, which opens with definitions like:

> *"Let $K$ be a set equipped with two operations called addition and multiplication satisfying the following axioms; $K$ is then called a field."*

This kind of definition — precise, but stripped of all context — can be disorienting. A student who tries to understand what a **field** is will be led to **groups, rings, and fields**, then to **sets and topology**, and may spend an entire semester on prerequisites before ever returning to linear algebra itself.

The same challenge arises with measure theory: concepts like $\sigma$-algebras and Borel sets are notoriously hard to visualize, even though in practice "almost every set you will ever encounter is a Borel set."

---

## The Approach

Rather than building every concept from scratch in full generality, this site takes a **fast, example-driven approach**. Each mathematical structure is illustrated with just four recurring examples:

| # | Example |
|---|---------|
| 1 | A set with exactly **two elements** |
| 2 | The familiar number systems: $\mathbb{N}, \mathbb{Z}, \mathbb{Q}, \mathbb{R}, \mathbb{C}$ |
| 3 | The set of all **$n \times n$ square matrices** |
| 4 | The set of all **real-valued functions** on the interval $[0, 1]$ |

By returning to these four examples repeatedly, the reader can build concrete intuition for each abstract structure before moving on.

---

## Recommended Reading Order

The notes are designed to be read in the following order:

1. **[Introduction](intro/)** — Motivation and overview
2. **[Homological Algebra](algebra/)** — Chain complexes, homology groups, exact sequences
3. **[Algebraic Topology](topology/)** — Fundamental groups, singular homology, cohomology
4. **[Category Theory](category/)** — Categories, functors, natural transformations, adjoints

Each chapter builds on the previous one. Category theory, rather than being the starting point, emerges as the **natural language** that unifies everything covered before it.

---

## Who Is This For?

- Undergraduate students in **science or engineering** who want a panoramic view of modern mathematics
- Anyone who has felt lost when encountering abstract algebraic definitions for the first time
- Readers who want to understand the *why* behind structures like groups, modules, and chain complexes before diving into the details

No prior exposure to abstract algebra or topology is assumed — only mathematical maturity at the level of introductory calculus and linear algebra.<