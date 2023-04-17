---
tags:
  - probability
---

# Probability Theory

(content:Set_Theory)=
## Set Theory

**_Sample space_**: The set, $S$, of all possible outcomes of a particular experiment is called the sample space for the experiment.

**_Event_**: An event is any collection of possible outcomes of an experiment, that is, any subset of S (including S itself).

**_Containment_**:
$
    A \subset B \Leftrightarrow x \in A \rightarrow x \in B
$

**_Equality_**:
$
    A = B \Leftrightarrow A \subset B~\text{and}~B \subset A
$

**_Union_**:
$
A \cup B = \{x: x \in A~\text{or}~x \in B\}
$

**_Intersection_**:
$
    A \cap B = \{x: x \in A~\text{and} ~x \in B\}
$

**_Complementation_**:
$
    A^c = \{x: x \notin A\}
$

**Theorem**: For any three events, $A, B, C$, defined on a sample space $S$,

a. Commutativity:

$$
    A \cup B = B \cup A \\
    A \cap B = B \cap A
$$

b. Associativity:

$$
    A \cup (B \cup C) = (A \cup B) \cup C \\
    A \cap (B \cap C) = (A \cap B) \cap C
$$

c. Distributive Laws:

$$
    A \cap (B \cup C) = (A \cap B) \cup (A \cap C) \\
    A \cup (B \cap C) = (A \cup B) \cap (A \cup C) \\
$$

d. DeMorgan's Laws:

$$
    (A \cup B)^c =  A^c \cap B^c \\
    (A \cap B)^c =  A^c \cup B^c \\
$$

**_Disjoint (or Mutually exclusive)_**: Two events $A$ and $B$ are disjoint (or mutually exclusive) if $A \cap B = \emptyset$. The events $A_1, A_2, \dots$ are pairwise disjoint (or mutually exclusive) if $A_i \cap A_j = \emptyset$ for all $i = j$.

````{margin}
```{note}
Partitions allows us to divide the sample space into small, nonoverlapping pieces.
```
````

**_Partition_**: If $A_1, A_2, \dots$ are pairwise disjoint and $\cup_{i=1}^\infty A_i = S$, then the
collection $A_1, A_2, \dots$ forms a partition of $S$.

(content:Basics_of_Probability_Theory)=
## Basics of Probability Theory

When an experiment is performed, _the realization of the experiment_ is an outcome in the sample space.

For each event $A$ in the sample space $S$ we want to associate with $A$ a number between zero and one that will be called the probability of $A$, denoted by $P(A)$.

(content:Axiomatic_Foundations)=
### Axiomatic Foundations

**_Definition 1.2.1_**: A collection of subsets of $S$ is called a sigma algebra (or Borel field), denoted by $\mathcal{B}$, if it satisfies the following three properties:

- $\emptyset \in \mathcal{B}$ (the empty set is an element of $\mathcal{B}$)
- If $\mathcal{A} \in \mathcal{B}$, then $\mathcal{A}^c \in \mathcal{B}$ ($\mathcal{B}$ is closed under complementation).
- If $A_1, A_2, \dots \in \mathcal{B}$, then $\cup_{i=1}^\infty A_i \in \mathcal{B}$ ($\mathcal{B}$ is closed under countable unions)

````{margin}
```{note}
- The three properties given abvoe are usually referred to as *the Axioms of Probability* (or the Kolmogorov Axioms, after A. Kolmogorov, one of the fathers of probability theory)
- Any function $P$ that satisfies the Axioms of Probability is called a probability function.
```
````

**_Definition 1.2.4_**: Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a probability function is a function $P$ with domain $\mathcal{B}$ that satisfies

1. $P(A) \geq 0$ for all $A \in \mathcal{B}.$
2. $P(S) = 1$
3. If $A_1, A_2, \dots \in  \mathcal{B}$ are pairwise disjoint, then $P(\cup_{i=1}^\infty A_i) = \sum_{i=1}^\infty P(A_i)$

**Theorem 1.2.6**: Let $S = \{s_1, \dots, s_n\}$ be a finite set. Let $\mathcal{B}$ be any sigma algebra of subsets of $S$. Let $p_1, \dots, p_n$ be nonnegative numbers that sum to 1. For any $A \in \mathcal{B}$, define $P(A)$ by

$$
    P(A) = \sum_{\{i: s_i \in A\}} p_i
$$

(The sum over an empty set is defined to be 0.) Then $P$ is a probability function on $\mathcal{B}$. This remains true if $S = \{s_1, s_2, \dots\}$ is a countable set.

**Axiom of Finite Additivity**: If $A \in \mathcal{B}$ and $B \in \mathcal{B}$ are disjoint, then

```{math}
:label: eq-Axiom of Finite Additivity
P(A \cup B) = P(A) + P(B)
```

(content:The_Calculus_of_Probabilities)=
### The Calculus of Probabilities

**Theorem**: If $P$ is a probability function and $A$ is any set in $\mathcal{B}$, then

1. $P(\emptyset) = 0$, where $\emptyset$ is the empty set;
2. $P(A) \leq 1$;
3. $P(A^c) = 1 − P(A)$.

**Theorem**: If $P$ is a probability function and $A$ and $B$ are any sets in $\mathcal{B}$, then

1. $P(B \cap A^c) = P(B) − P(A \cap B)$;
2. $P(A \cup B) = P(A) + P(B) − P(A \cup B)$;
3. If $A \subset B$, then $P(A) \leq P(B)$.

**Theorem 1.2.11** If $P$ is a probability function, then

1. $P(A) = \sum_{i=1}^\infty P(A \cap C_i)$ for any partition $C_1, C_2, \dots$
2. $P(\cup_{i=1}^\infty A_i) \leq \sum_{i=1}^\infty P(A_i)$ for any sets $A_1, A_2, \dots$ (Bool's Inequality)

(content:Counting)=
### Counting

````{margin}
```{note}
**Theorem 1.2.14 is the Fundamental Theorem of Counting**
```
````

**Theorem 1.2.14** If a job consists of $k$ separate tasks, the $i$th of which can be done in $n_i$ ways, $i = 1, \dots, k$, then the entire job can be done in $n_1 \times n_2 \times \dots \times n_k$ ways.

Number of possible arrangements of size $r$ from $n$ objects

|           | Without replacement |   With replacement    |
| :-------: | :-----------------: | :-------------------: |
|  Ordered  | $\frac{n!}{(n-r)!}$ |         $n^r$         |
| Unordered |   $\binom{n}{r}$    | $\binom{n + r -1}{r}$ |

(content:Conditional_Probability_and_Independence)=
## Conditional Probability and Independence

**_Definition 1.3.2_**: If $A$ and $B$ are events in $S$, and $P(B) > 0$, then the conditional probability of $A$ given $B$, written $P(A|B)$, is

```{math}
:label: eq-conditional probability
P(A|B) = \frac{P(A \cap B)}{P(B)}
```

**Theorem 1.3.5** (Bayes’ Rule) Let $A_1, A_2, \dots$ be a partition of the sample space, and let $B$ be any set. Then, for each $i = 1, 2, \dots$,

```{math}
:label: eq-Baye's Rule
P(A_i|B) = \frac{P(B|A_i)P(A_i)}{\sum_{j=1}^\infty P(B|A_j)P(A_j)}
```

**_Definition 1.3.7_** Two events, $A$ and $B$, are statistically independent if

```{math}
:label: eq-statistically independent
P(A \cap B) = P(A)P(B)
```

**Theorem 1.3.9** If $A$ and $B$ are independent events, then the following pairs are
also independent:

1. $A$ and $B^c$,
2. $A^c$ and $B$,
3. $A^c$ and $B^c$

**_Definition 1.3.12_** A collection of events $A_1, \dots, A_n$ are mutually independent if for any subcollection $A_{i_1}, \dots, A_{i_k}$, we have

```{math}
:label: eq-mutually independent
P\left(\cap_{j=1}^k A_{i_j}\right) = \prod_{j=1}^k P(A_{i_j})
```

(content:Random_Variables)=
## Random Variables

**_Definition 1.4.1_** A random variable is a function from a sample space $S$ into the real numbers.

<center>Examples of random variables</center>

| Experiment                                           | Random Variables                   |
| :--------------------------------------------------- | :--------------------------------- |
| Toss two dice                                        | $X =$ sum of the numbers           |
| Toss a coin 25 times                                 | $X =$ number of heads in 25 tosses |
| Apply different amounts of fertilizer to corn plants | $X =$ yield/acre                   |

(content:Distribution_Functions)=
## Distribution Functions

**_Definition 1.5.1_** The cumulative distribution function or cdf of a random variable $X$, denoted by $F_X(x)$, is defined by

```{math}
:label: eq-cdf
F_X(x) = P_X(X \leq x), \text{for all} x.
```

**Theorem 1.5.3** The function $F(x)$ is a cdf if and only if the following three conditions hold:

1. $\lim_{x \rightarrow -\infty}F(x) = 0$ and $\lim_{x \rightarrow \infty}F(x) = 1$.
2. $F(x)$ is a nondecreasing function of $x$.
3. $F(x)$ is right-continuous; that is, for every number $x_0$, $\lim_{x \downarrow x_0} F(x) = F(x_0)$

**_Definition 1.5.7_** A random variable $X$ is continuous if $F_X(x)$ is a continuous function of $x$. A random variable $X$ is discrete if $F_X(x)$ is a step function of $x$.

````{margin}
```{note}
Note that two random variables that are identically distributed are not necessarily equal. That is, Definition 1.5.8 does not say that $X = Y$ .
```
````

**_Definition 1.5.8_** The random variables $X$ and $Y$ are identically distributed if, for every set $A \in \mathcal{B^1}, P(X \in A) = P(Y \in A)$.

**Theorem 1.5.10** The following two statements are equivalent:

1. The random variables $X$ and $Y$ are identically distributed.
2. $F_X(x) = F_Y (x)$ for every $x$.

(content:Density_and_Mass_Functions)=
## Density and Mass Functions

***Definition 1.6.1*** The probability mass function (pmf) of a discrete random variable $X$ is given by

```{math}
:label: eq-pmf
f_X(x) = P(X = x), \text{for all} ~x.
```

````{margin}
```{note}
The expression “$X$ has a distribution given by $F_X(x)$” is abbreviated symbolically by “$X \thicksim F_X(x)$,” where we read the symbol “$\thicksim$” as “is distributed as.” We can similarly write $X \thicksim f_X(x)$ or, if $X$ and $Y$ have the same distribution, $X \thicksim Y$ .
```
````

***Definition 1.6.3*** The probability density function or pdf , $f_X(x)$, of a continuous random variable $X$ is the function that satisfies

```{math}
:label: eq-pdf
F_X(x) = \int_{- \infty}^x f_X(t) dt, \text{for all} ~x.
```

**Theorem 1.6.5** A function $f_X(x)$ is a pdf (or pmf) of a random variable $X$ if and only if

1. $f_X(x) \geq 0$ for all $x$,
2. $\sum_x f_X(x) = 1$ (pmf) or $\int_{- \infty}^\infty f_X(x) dx = 1$ (pdf)