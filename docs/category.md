# Category Theory

Category theory is a branch of mathematics that studies **abstract structures and relationships between them**. Often called the "mathematics of mathematics," it provides a universal language unifying nearly all areas of math.

---

## Core Definitions

### Category

A **category** $\mathcal{C}$ consists of:

- A collection of **objects**: $A, B, C, \ldots$
- A collection of **morphisms** (arrows): $f : A \to B$ between objects
- A **composition law**: $g \circ f : A \to C$ for $f: A \to B$, $g: B \to C$
- An **identity morphism**: $\text{id}_A : A \to A$ for each object $A$

satisfying two axioms:

| Axiom | Condition |
|-------|-----------|
| **Associativity** | $h \circ (g \circ f) = (h \circ g) \circ f$ |
| **Identity** | $f \circ \text{id}_A = f = \text{id}_B \circ f$ |

---

### Examples of Categories

| Category | Objects | Morphisms |
|----------|---------|-----------|
| **Set** | Sets | Functions |
| **Grp** | Groups | Group homomorphisms |
| **Top** | Topological spaces | Continuous maps |
| **Vect**$_k$ | $k$-vector spaces | Linear maps |
| **Ring** | Rings | Ring homomorphisms |
| Any poset $(P, \leq)$ | Elements of $P$ | $a \to b$ iff $a \leq b$ |

> The power of category theory is that results proven for **any** category apply to **all** these examples simultaneously.

---

## Key Concepts

### Functor

A **functor** $F : \mathcal{C} \to \mathcal{D}$ maps between categories, preserving structure:

$$F(g \circ f) = F(g) \circ F(f), \qquad F(\text{id}_A) = \text{id}_{F(A)}$$

- **Covariant**: preserves direction of morphisms
- **Contravariant**: reverses direction of morphisms

**Examples:**
- Fundamental group: $\pi_1 : \mathbf{Top}_* \to \mathbf{Grp}$
- Homology: $H_n : \mathbf{Top} \to \mathbf{Ab}$
- Forgetful functor: $\mathbf{Grp} \to \mathbf{Set}$ (forgets group structure)

---

### Natural Transformation

A **natural transformation** $\eta : F \Rightarrow G$ between functors $F, G : \mathcal{C} \to \mathcal{D}$ is a family of morphisms:

$$\eta_A : F(A) \to G(A) \quad \text{for each object } A \in \mathcal{C}$$

such that for every morphism $f : A \to B$, the following **naturality square** commutes:

$$\begin{array}{ccc} F(A) & \xrightarrow{\eta_A} & G(A) \\ F(f)\downarrow & & \downarrow G(f) \\ F(B) & \xrightarrow{\eta_B} & G(B) \end{array}$$

> Natural transformations are morphisms *between* functors — category theory applies its own abstraction to itself.

---

### Universal Properties

Many constructions are best defined by what they do rather than what they are, via a **universal property**.

| Construction | Universal Property |
|---|---|
| **Product** $A \times B$ | Terminal object among cones over $A, B$ |
| **Coproduct** $A \sqcup B$ | Initial object among cocones |
| **Kernel** | Equalizer of $f$ and $0$ |
| **Tensor product** $A \otimes B$ | Represents bilinear maps |

If an object satisfies a universal property, it is **unique up to unique isomorphism** — the canonical categorical notion of "sameness."

---

### Adjoint Functors

Functors $F : \mathcal{C} \rightleftharpoons \mathcal{D} : G$ are **adjoint** ($F \dashv G$) if there is a natural bijection:

$$\operatorname{Hom}_{\mathcal{D}}(F(A),\ B) \;\cong\; \operatorname{Hom}_{\mathcal{C}}(A,\ G(B))$$

$F$ is the **left adjoint**, $G$ is the **right adjoint**.

**Examples:**

| Left Adjoint $F$ | Right Adjoint $G$ |
|---|---|
| Free group functor | Forgetful functor $\mathbf{Grp} \to \mathbf{Set}$ |
| $- \otimes B$ | $\operatorname{Hom}(B, -)$ |
| Suspension $\Sigma$ | Loop space $\Omega$ |
| Discrete topology | Forgetful functor $\mathbf{Top} \to \mathbf{Set}$ |

> **"Adjoint functors arise everywhere."** — Saunders Mac Lane

---

### Limits and Colimits

**Limits** (e.g., products, pullbacks, equalizers) and **colimits** (e.g., coproducts, pushouts, coequalizers) generalize constructions across all categories.

A **limit** of a diagram $D : \mathcal{J} \to \mathcal{C}$ is a terminal cone over $D$; a **colimit** is an initial cocone.

```
        Limit                   Colimit

          L                    A   B
                   / \                    \ /
                           /   \         vs         C
                                  A     B                (pushout)
                                      (pullback)
                                      ```

---

## The Yoneda Lemma

Perhaps the most fundamental result in category theory:

$$\operatorname{Nat}(\operatorname{Hom}(A, -),\ F) \;\cong\; F(A)$$

for any functor $F : \mathcal{C} \to \mathbf{Set}$ and object $A \in \mathcal{C}$.

**Corollary (Yoneda embedding):** Every category $\mathcal{C}$ embeds fully faithfully into $[\mathcal{C}^{op}, \mathbf{Set}]$.

> An object is **completely determined** by how other objects map into it — identity through relationships.

---

## Hierarchy of Abstraction

```
   Objects & Morphisms       ←── Category
             │
                       ▼
                          Maps between categories   ←── Functor
                                    │
                                              ▼
                                                 Maps between functors     ←── Natural Transformation
                                                           │
                                                                     ▼
                                                                        Categories of categories  ←── 2-Category, ∞-Category
                                                                        ```

---

## Connections to Other Fields

| Field | Category Theory Role |
|-------|----------------------|
| **Algebraic topology** | Homology/homotopy as functors; derived categories |
| **Homological algebra** | Abelian categories, derived functors |
| **Logic & CS** | Curry–Howard–Lambek correspondence; type theory |
| **Algebraic geometry** | Topos theory, étale cohomology, schemes |
| **Physics** | Topological QFT, monoidal categories in quantum groups |

---

## Why It Matters

Category theory forces you to think in terms of **structure and relationships** rather than elements and sets. Its power lies not in solving problems directly, but in:

1. **Unifying** constructions across different areas of math
2. **Clarifying** what theorems really depend on
3. **Transporting** results from one field to another via functors
4. **Revealing** deep analogies invisible at the set-theoretic level