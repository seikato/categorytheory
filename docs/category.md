# Category Theory

---

## ホモロジーと圏論

エミー・ネーターは、ベッチ数と捩れ係数を商群として整理し、ベッチ群の概念を導入した。

---

## 随伴の例

### 自由関手と忘却関手
$k$ を体とする。忘却関手 \( U \)、自由関手 \( F \) と書くと、

$$
\mathbf{Vect}_k \;\leftrightarrows\; \mathbf{Set}
$$

これは典型的な随伴の例である。

---

### 随伴の本質

随伴とは自然同型

$$
\mathrm{Hom}_{\mathbf{Vect}_k}(F(X), V)
\cong
\mathrm{Hom}_{\mathbf{Set}}(X, U(V))
$$

によって特徴付けられる。

---
\subsection{自由$R$加群の構成}
集合$E$と環$R$が与えられたとき，$E$を基底とする自由$R$加群を以下のように加群の直和により構成できる．
\begin{equation}
    R^{(E)} = \bigoplus_{e\in E} R.
\end{equation}
このとき，任意の$R^{(E)}$の要素は一意に
\begin{equation}
    \sum_{e\in E} c_e e
\end{equation}
と書ける．


## 関連ノート

- [Algebra](algebra.md)