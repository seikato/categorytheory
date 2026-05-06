# Homological Algebra

Homological algebra is a branch of mathematics that studies algebraic structures using *chain complexes* and their *homology groups*.

---

## Core Definitions

### Chain Complex

A **chain complex** $(C_\bullet, d)$ is a sequence of abelian groups (or modules) connected by homomorphisms:

$$\cdots \xrightarrow{d_{n+1}} C_n \xrightarrow{d_n} C_{n-1} \xrightarrow{d_{n-1}} \cdots$$

satisfying the key condition:

$$d_n \circ d_{n+1} = 0 \quad \text{(i.e., } \text{im}(d_{n+1}) \subseteq \ker(d_n)\text{)}$$

The maps $d_n$ are called **boundary operators** (or differentials).

---

### Cycles, Boundaries, and Homology

| Term | Definition |
|------|-----------|
| **Cycles** $Z_n$ | $\ker(d_n)$ — elements mapped to zero |
| **Boundaries** $B_n$ | $\text{im}(d_{n+1})$ — elements coming from the next group |
| **Homology group** $H_n$ | $Z_n / B_n = \ker(d_n) / \text{im}(d_{n+1})$ |

Since $B_n \subseteq Z_n$, the quotient is well-defined. Intuitively, $H_n$ **measures the "holes"** that are not filled by boundaries.

---

### Exact Sequence

A sequence is **exact at $C_n$** if $\text{im}(d_{n+1}) = \ker(d_n)$, i.e., $H_n = 0$.

A **short exact sequence** takes the form:

$$0 \to A \xrightarrow{f} B \xrightarrow{g} C \to 0$$

---

## Key Tools

- **Functors** `Hom` and `⊗`: used to construct new chain complexes from existing ones.
- **Derived functors**: `Ext` and `Tor` capture how far a module is from being projective/injective/flat.
- **Long exact sequence**: a short exact sequence of complexes induces a long exact sequence in homology, connecting the $H_n$ groups.

---

## Why It Matters

Homological algebra provides a unified language for:
- **Algebraic topology** (singular homology, cohomology)
- **Algebraic geometry** (sheaf cohomology, derived categories)
- **Group theory** (group cohomology)
- **Commutative algebra** (projective resolutions, depth)