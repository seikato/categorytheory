#Algebra

##Set Theory and Topology
---
### Topological Spaces

!!! note "Definition"
    A **topological space** is a pair $(X, \mathcal{T})$ where $\mathcal{T} \subseteq \mathcal{P}(X)$ satisfies:

    1. $\emptyset, X \in \mathcal{T}$
    2. Arbitrary unions of elements of $\mathcal{T}$ are in $\mathcal{T}$
    3. Finite intersections of elements of $\mathcal{T}$ are in $\mathcal{T}$

---

### Open and Closed Sets

- Open set: $U \in \mathcal{T}$
- Interior:
  $$
  \operatorname{int}(A)
  $$
- Closure:
  $$
  \overline{A}
  $$
- Boundary:
  $$
  \partial A = \overline{A} \setminus \operatorname{int}(A)
  $$

---

### Basis of a Topology

!!! note "Definition"
    A **basis** $\mathcal{B}$ of a topology $\mathcal{T}$ is a collection such that every open set is a union of elements of $\mathcal{B}$.

---

### Separation Axioms

#### $T_1$ Space

A space where all singleton sets are closed.

#### Hausdorff Space

!!! note "Definition"
    A space is **Hausdorff** if for any $x \neq y$, there exist disjoint open sets $U, V$ such that:
    $$
    x \in U, \quad y \in V
    $$

---

### Compactness

!!! note "Definition"
    A space is **compact** if every open cover has a finite subcover.

---

### Connectedness

A space is connected if it cannot be written as a disjoint union of two non-empty open sets.

---

## Group Theory

### Magma

!!! note "Definition"
    A **magma** is a set $M$ with a binary operation:
    $$
    M \times M \to M
    $$

---

### Semigroup

A magma with associativity:
$$
(a b)c = a(b c)
$$

---

### Monoid

A semigroup with identity element $e$:
$$
a e = e a = a
$$

---

### Group

!!! note "Definition"
    A **group** is a monoid where every element has an inverse:
    $$
    \forall a \in G, \exists a^{-1} \in G
    $$

---

### Abelian Group

A group satisfying:
$$
a b = b a
$$

---

## Ring Theory

### Ring

!!! note "Definition"
    A **ring** is a set $R$ with two operations $(+, \cdot)$ such that:

    - $(R, +)$ is an abelian group
    - Multiplication is associative

---

### Polynomial Rings

A ring of the form:
$$
R[x]
$$

---

### Ideals

!!! note "Definition"
    An **ideal** $I \subseteq R$ satisfies:
    $$
    rI \subseteq I
    $$

---

### Noetherian Rings

A ring satisfying the ascending chain condition on ideals.

---

## Field Theory

### Field

!!! note "Definition"
    A **field** is a commutative ring where every nonzero element is invertible.

---

### Field Extensions

A field extension:
$$
K \subseteq L
$$

---

### Galois Theory

Studies the correspondence:
$$
\text{Field Extensions} \leftrightarrow \text{Groups}
$$

---

### Cohomology

Used to study algebraic structures via derived functors.


##集合論基礎
###位相空間
###開集合、開核、閉包、内点、触点、外点、境界点、集積点、孤立点、近傍
###位相の基準底
###可分位相空間
###連結性
###コンパクト性とハウスドルフ空間
###分離公理
#### $T_1$空間
#### Hausorff空間
#### 正則空間
#### 正規空間
#### ウリゾーンの補題、拡張定理

##群論基礎
###マグマ
####擬群
####Loop
####半群
####モノイド
####群
####可換群
###環
####多項式環
####イデアル、素イデアル、拡大イデアル
####非可換環と表現論
####加群
####ネーター環、アルティン環
###体
####体の拡大
####ガロア理論
####群のコホモロジー

## Category Theory
- [Category](category.md)