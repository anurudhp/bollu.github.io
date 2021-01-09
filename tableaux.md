- Schur polynomials: \sum_[T in SSYT(N, m/n)] x^[content[T]]
- semistandard tableaux (increases in col, does not decrease in row, contains entires from {1..N}) 
- standard: contain each number in 1..n exactly once
- standard tableaux (increases in col, increases in row, contains entires from {1..N}) 

- power sums: p[k] = sum[i] x_i^k
- elementary symmetric polynomials: e[k](x1,...xn) = sum over all k-tuples of [x_1...xn] WITHOUT repetition
  eg: e[2](x1, ... x5) = x1x2 + x2x3+  ... + x4x5. So this something like `Sn(x^{subset of K})`
  or `Sn(x^(2^K))`
- complete symmetric polynomials: h[k](x1, ... xn) = sum over all k-tuples of [x1..xn] WITH repetition
  eg: e[2](x1...x5) = x1^2 + x2^2 + ... x5^2 + 
- monomial symmetric polynomial `m_ρ = Sn (x^ρ)`

Examples for degree 2 in 3 variables:

- elementary: $XY + YZ + XZ$ (variables of power 0/1, of degree 2.) (Alternatively, all subsets of size $2$ of $\{X, Y, Z\})$
- complete: $X^2 + XY + YZ + XZ + Y^2 + Z^2$ (all possible ways to get to degree 2). (Alternatively, all jjj
- monomial from $X^2$: X^2 + Y^2 + Z^2$ (act with $S_3$ on the _variables_, generated by $X^2$).
  monomial from $XY$: $XY + YZ + XZ$ (act with $S_3$ on the _variables_, generated by $XY$).



- we're saying: take ALL possible ways with repetition.
- of course this will include all possibele ways to take "permuted".

- We are picking {1...N} with repetition $k$ times
- (a1, a2, .. an) | a1 + a2 + ... + an = k
- a[σ1], a[σ2]... a[σn] | aσ1 + aσ2 + ... + an = k [σ is a permutation]


- N = 8
- mu: 5 >= 2 >= 1


- x1^5 x2^2 x3 + x2^5 x3^2 x4 + ... + x8^1 x7^5 x6^2

- mu = mu[1] >= mu[2] >= ... >= mu[n].
- monominal symmetric polynomial indexed by mu: Informally whose ex-ponent vector can be rearranged to give μ.
- monomial symmetric polynomial: best way to make the monomial `x^mu` symmetric.


let i = σ-1[j]

- f[1] = 5; f[2] = 3; f[3] = 1;
x[1]^f[1] x[2]^f[2] x[3]^f[3] = x1^5 x2^3 x3

σ 1 <-> 2

x[σ[1]]^f[1] + x[σ[2]]^f[2] + x[σ[3]]^f[3]

x[1]^f[σ-1[1]] + x[2]^f[σ-1[2]] + x[3]^f[σ-1[3]]

g[1] = f[σ-1[1]] 
g[2] = f[σ-1[2]] 
g[3] = f[σ-1[3]] 


x[1]^g[1] x[2]^g[2] x[3]^g[3]

sort(f) = sort(g) = [5, 3, 1]
- Λn = all symmetric polynomials x1...xn


- The symmetric polynomials eα hα pα: let α be a sequence of [psotive integers (α1, ... αn)
  eα = prod_i eαi


x1, x1^2, x2, x2^2, ... x_k -> basis
schur polynomials -> basis


- homogenous stuff.
- homogenous poly: all terms of the same degree. x1^2 + x2^2: homo. x1 + x2^2 NOT
- homogenous poly of degree k: form a vector space: (intuition: adding and scaling don't change degree)
- some symmetric polynomial:
- `p(x) = x1x2^2 + x2x1^2 + x1x2 + x2x1 + x1 + x2`
- `p_1(x) = x1 + x2  ∈ Λ_2[1]`
- `p_2(x) = x1x2 + x2x1  ∈ Λ_2[2]`
- `p_3(x) = x1x2^3 + x2^2x1  ∈ Λ_2[3]`
- `p = p1 + p2 + p3`

- What is a good example of a ring that is not a vector space over some field?

# Basis for degree k with N variables:

- for each partition μ of k, we will have ONE basis element coresponding to μ, call it B(μ, k)
- Pick μ a partition of k
- `B(μ, k) = \sum_{α: sort(α) = μ} x^α`
- `x^α = x1^α1 . x2^α2 . xN^αN`

#### Example when k = 3, N = 4


- `(a) 3 = 3 -> (3) -> (3, 0, 0, 0)`
- `(b) 3 = 2 + 1 -> (2, 1) -> (2, 1, 0, 0)`
- `(c) 3 = 1 + 1 + 1 -> (1, 1, 1) -> (1, 1, 1, 0)`

- Consider all `α` such that `sort(α) = (3, 0, 0, 0)`
- `(3, 0, 0, 0)`: X^3
- `(0, 3, 0, 0)`: Y^3
- `(0, 0, 3, 0)`: Z^3
- `(0, 0, 0, 3)`: W^3
- `B(μ, k, N) = \sum_{α: sort(α) = μ} x^α`
- `B((3, 0, 0, 0), 3, 4) = X^3 + Y^3 + Z^3 + W^3`
- `B((2, 1, 0, 0), 3, 4) = X^2Y + ...`
- `B((1, 1, 1, 0), 3, 4) = XYZ + YZW + ZWX + WXY`

#### Partitions of a number $Par_N(k)$ and $Par(k)$

- $Par(k)$ are numbers $a_1 \geq a_2 \geq \dots$ such that $\sum_i a_i = k$
- $Par_N(k)$ are numbers $a_1 \geq a_2 \geq \dots a_N$ such that $\sum_i a_i = k$.
    That is, partitions of $k$ into exactly $N$ parts.

#### Symmetry of Schur polynomials

#### Kostka numbers

For each `m/n` shape and `α` sequence, define `K(m/n, α)` as the coefficient of `x^α`
in `s(m/n, x1, ..., xN)`.

Equivalenetly, `K(m/n, α)` is the number of semistandard tableaux of shape
`m/n` and content `α`.


- for all skew shapes `m/n` and all alpha `a, b` such that `sort(a) = sort(b)` we have 
  `K(m/n, a) = K(m/n, b)`.


#### 10.41: Theorem: Lexicographic vs. Dominance Ordering.

Find better explanation (picture proof?)

If you have two non-decrasing functions μ and ν such that (integral_0^i μ < integral_0^i ν) for all i,
then there exists a point $p$ such that μ(x < p) = ν(x < p) and μ(p) < ν(p)

#### Definition of Raising Operation:

Restrict $R$ such that it only works for adjacent elements. May make life easier.
Currently, we can move index $i$ to $j$ for $j < i$. 