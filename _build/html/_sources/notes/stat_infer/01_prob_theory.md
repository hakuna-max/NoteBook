# Probability Theory

## Set Theory

***Sample space***: The set, $S$, of all possible outcomes of a particular experiment is called the sample space for the experiment.

***Event***: An event is any collection of possible outcomes of an experiment, that is, any subset of S (including S itself).

***Containment***:
$
    A \subset B \Leftrightarrow x \in A \rightarrow x \in B
$

***Equality***:
$
    A = B \Leftrightarrow A \subset B~\text{and}~B \subset A
$

***Union***:
$
A \cup B = \{x: x \in A~\text{or}~x \in B\}
$

***Intersection***:
$
    A \cap B = \{x: x \in A~\text{and} ~x \in B\}
$

***Complementation***: 
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

***Disjoint (or Mutually exclusive)***: Two events $A$ and $B$ are disjoint (or mutually exclusive) if $A \cap B = \emptyset$. The events $A_1, A_2, \dots$ are pairwise disjoint (or mutually exclusive) if $A_i \cap A_j = \emptyset$ for all $i = j$.

***Partition***: If $A_1, A_2, \dots$ are pairwise disjoint and $\cup_{i=1}^\infty A_i = S$, then the
collection $A_1, A_2, \dots$ forms a partition of $S$.

````{margin}
```{note}
Partitions allows us to divide the sample space into small, nonoverlapping pieces.
```
````

## Basics of Probability Theory

When an experiment is performed, *the realization of the experiment* is an outcome in the sample space.

For each event $A$ in the sample space $S$ we want to associate with $A$ a number between zero and one that will be called the probability of $A$, denoted by $P(A)$.

***sigma algebra (or Borel field)***: A collection of subsets of $S$ is called a sigma algebra (or Borel field), denoted by $\mathcal{B}$, if it satisfies the following three properties:
- $\emptyset \in \mathcal{B}$ (the empty set is an element of $\mathcal{B}$)
- If $\mathcal{A} \in \mathcal{B}$, then  $\mathcal{A}^c \in \mathcal{B}$ ($\mathcal{B}$ is closed under complementation).
- If $A_1, A_2, \dots \in \mathcal{B}$, then $\cup_{i=1}^\infty A_i \in \mathcal{B}$ ($\mathcal{B}$ is closed under countable unions)

***Probability function***: Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a probability function is a function $P$ with domain $\mathcal{B}$ that satisfies
1. $P(A) \geq 0$ for all $A \in \mathcal{B}.$
2. $P(S) = 1$
3. If $A_1, A_2, \dots \in  \mathcal{B}$ are pairwise disjoint, then $P(\cup_{i=1}^\infty A_i) = \sum_{i=1}^\infty P(A_i)$

````{margin}
```{note}
- The three properties given abvoe are usually referred to as *the Axioms of Probability* (or the Kolmogorov Axioms, after A. Kolmogorov, one of the fathers of probability theory)
- Any function $P$ that satisfies the Axioms of Probability is called a probability function.
```
````

**Theorem**: Let $S = \{s_1, \dots, s_n\}$ be a finite set. Let $\mathcal{B}$ be any sigma algebra of subsets of $S$. Let $p_1, \dots, p_n$ be nonnegative numbers that sum to 1. For any $A \in \mathcal{B}$, define $P(A)$ by

$$
    P(A) = \sum_{\{i: s_i \in A\}} p_i
$$

(The sum over an empty set is defined to be 0.) Then $P$ is a probability function on $\mathcal{B}$. This remains true if $S = \{s_1, s_2, \dots\}$ is a countable set.

**Theorem**: If $P$ is a probability function and $A$ is any set in $\mathcal{B}$, then
1. $P(\emptyset) = 0$, where $\emptyset$ is the empty set;
2. $P(A) \leq 1$;
3. $P(A^c) = 1 − P(A)$.

**Theorem**: If $P$ is a probability function and $A$ and $B$ are any sets in $B$, then
1. $P(B \cap A^c) = P(B) − P(A \cap B)$;
2. $P(A \cup B) = P(A) + P(B) − P(A \cup B)$;
3. If $A \subset B$, then $P(A) \leq P(B)$.
   
### Axiomatic Foundations

### The Calculus of Probabilities

### Counting

### Enumerating Outcomes

## Conditional Probability and Independence

## Random Variables

## Distribution Functions

## Density and Mass Functions