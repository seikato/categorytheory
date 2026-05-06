# Algebraic Topology

Algebraic topology studies **topological spaces** by associating algebraic structures (groups, rings, modules) to them, turning geometric problems into algebraic ones.

---

## Core Idea

The fundamental philosophy is:

> Assign algebraic invariants to topological spaces so that **homeomorphic spaces yield isomorphic algebras**.

This lets us distinguish spaces that *look* different by computing algebra — no need for explicit geometric arguments.

---

## Key Constructions

### 1. Homotopy & Fundamental Group

Two continuous maps $f, g : X \to Y$ are **homotopic** if one can be continuously deformed into the other.

The **fundamental group** $\pi_1(X, x_0)$ captures loops based at $x_0$:

$$\pi_1(X, x_0) = \{\text{loops at } x_0\} / \text{homotopy}$$

| Space | $\pi_1$ |
|-------|---------|
| $\mathbb{R}^n$, disk | $0$ (trivial) |
| Circle $S^1$ | $\mathbb{Z}$ |
| Torus $T^2$ | $\mathbb{Z} \times \mathbb{Z}$ |

More generally, **higher homotopy groups** $\pi_n(X)$ detect higher-dimensional "holes".

---

### 2. Singular Homology

Using the machinery of homological algebra, one builds:

$$H_n(X) = \ker(d_n) / \operatorname{im}(d_{n+1})$$

by forming a chain complex from **singular simplices** (continuous maps $\Delta^n \to X$).

Intuitively:

| Group | Detects |
|-------|---------|
| $H_0(X)$ | Connected components |
| $H_1(X)$ | 1-dimensional loops (abelianization of $\pi_1$) |
| $H_2(X)$ | Enclosed 2D voids |
| $H_n(X)$ | $n$-dimensional holes |

---

### 3. Cohomology

**Cohomology** $H^n(X)$ is the dual theory, obtained by applying $\operatorname{Hom}(-, R)$ to the chain complex:

$$\cdots \to C^{n-1} \xrightarrow{d^*} C^n \xrightarrow{d^*} C^{n+1} \to \cdots$$

Cohomology carries extra structure — the **cup product** — making $H^*(X) = \bigoplus_n H^n(X)$ a **graded ring**, which is a strictly finer invariant than homology alone.

---

### 4. CW Complexes

A practical way to build spaces: start from points, attach **cells** $e^n \cong D^n$ inductively by dimension.

$$X = X^0 \subset X^1 \subset X^2 \subset \cdots$$

CW complexes are general enough to model most spaces of interest, yet structured enough to make computation tractable via **cellular homology**.

---

## Major Theorems

| Theorem | Statement (informal) |
|---------|----------------------|
| **Brouwer Fixed Point** | Every continuous map $D^n \to D^n$ has a fixed point |
| **Invariance of Domain** | A continuous injective map $\mathbb{R}^n \to \mathbb{R}^n$ is open |
| **Mayer–Vietoris** | Homology of $X = A \cup B$ fits into a long exact sequence from $A$, $B$, $A \cap B$ |
| **Hurewicz** | Under connectivity conditions, $\pi_n(X) \cong H_n(X)$ |
| **Poincaré Duality** | For a closed orientable $n$-manifold: $H^k(M) \cong H_{n-k}(M)$ |

---

## Relationship to Homological Algebra

Algebraic topology is one of the **primary motivations** for homological algebra:

```
Topological Space X
        │
                ▼
                  Chain Complex C•(X)
                          │
                                  ▼
                                    Homology Groups Hₙ(X)   ←── algebraic invariants
                                    ```

Derived functors (`Ext`, `Tor`), spectral sequences, and sheaf cohomology all grew out of efforts to generalize and compute topological invariants.

---

## Why It Matters

- **Geometry**: classifying surfaces, manifolds, knots
- **Physics**: topological phases of matter, string theory
- **Data science**: *Topological Data Analysis (TDA)* uses persistent homology to detect shape in data
- **Algebra**: motivates derived categories and modern homological methods