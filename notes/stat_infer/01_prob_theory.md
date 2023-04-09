---
tags: 
    - probability
---

# Probability Theory

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

## Basics of Probability Theory

When an experiment is performed, _the realization of the experiment_ is an outcome in the sample space.

For each event $A$ in the sample space $S$ we want to associate with $A$ a number between zero and one that will be called the probability of $A$, denoted by $P(A)$.

**_sigma algebra (or Borel field)_**: A collection of subsets of $S$ is called a sigma algebra (or Borel field), denoted by $\mathcal{B}$, if it satisfies the following three properties:

- $\emptyset \in \mathcal{B}$ (the empty set is an element of $\mathcal{B}$)
- If $\mathcal{A} \in \mathcal{B}$, then $\mathcal{A}^c \in \mathcal{B}$ ($\mathcal{B}$ is closed under complementation).
- If $A_1, A_2, \dots \in \mathcal{B}$, then $\cup_{i=1}^\infty A_i \in \mathcal{B}$ ($\mathcal{B}$ is closed under countable unions)

````{margin}
```{note}
- The three properties given abvoe are usually referred to as *the Axioms of Probability* (or the Kolmogorov Axioms, after A. Kolmogorov, one of the fathers of probability theory)
- Any function $P$ that satisfies the Axioms of Probability is called a probability function.
```
````

**_Probability function_**: Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a probability function is a function $P$ with domain $\mathcal{B}$ that satisfies

1. $P(A) \geq 0$ for all $A \in \mathcal{B}.$
2. $P(S) = 1$
3. If $A_1, A_2, \dots \in  \mathcal{B}$ are pairwise disjoint, then $P(\cup_{i=1}^\infty A_i) = \sum_{i=1}^\infty P(A_i)$

**Theorem**: Let $S = \{s_1, \dots, s_n\}$ be a finite set. Let $\mathcal{B}$ be any sigma algebra of subsets of $S$. Let $p_1, \dots, p_n$ be nonnegative numbers that sum to 1. For any $A \in \mathcal{B}$, define $P(A)$ by

$$
    P(A) = \sum_{\{i: s_i \in A\}} p_i
$$

(The sum over an empty set is defined to be 0.) Then $P$ is a probability function on $\mathcal{B}$. This remains true if $S = \{s_1, s_2, \dots\}$ is a countable set.

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

````{margin}
```{note}
**Theorem 1.2.14 is the Fundamental Theorem of Counting**
```
````

**Theorem 1.2.14** If a job consists of $k$ separate tasks, the $i$th of which can be done in $n_i$ ways, $i = 1, \dots, k$, then the entire job can be done in $n_1 \times n_2 \times \dots \times n_k$ ways.

<center>Table 1.2.1 Number of possible arrangements of size r from n objects</center>

|           | Without replacement |   With replacement    |
| :-------: | :-----------------: | :-------------------: |
|  Ordered  | $\frac{n!}{(n-r)!}$ |         $n^r$         |
| Unordered |   $\binom{n}{r}$    | $\binom{n + r -1}{r}$ |

**_Definition 1.3.2_**: If $A$ and $B$ are events in $S$, and $P(B) > 0$, then the conditional probability of $A$ given $B$, written $P(A|B)$, is

```{math}
:label: eq-conditional probability
P(A|B) = \frac{P(A \cap B)}{P(B)}
```

**Theorem 1.3.5** (Bayes’ Rule) Let $A1_, A_2, \dots$ be a partition of the sample space, and let $B$ be any set. Then, for each $i = 1, 2, \dots$,

```{math}
:label: eq-Baye's Rule
P(A_i|B) = \frac{P(B|A_i)P(A_i)}{\sum_{j=1}^\infty P(B|A_j)P(A_j)}
```

### Axiomatic Foundations

### The Calculus of Probabilities

### Counting

### Enumerating Outcomes

## Conditional Probability and Independence

## Random Variables

## Distribution Functions

## Density and Mass Functions
