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
1. $P(A) \gep 0$ for all $A \in \mathcal{B}.$
2. $P(S) = 1$
3. If $A_1, A_2, \dots \in  \mathcal{B}$ are pairwise disjoint, then $P(\cap_{i=1}^\infty A_i = \sum_{i=1}^\infty P(A_i)$

````{margin}
```{note}
- The three properties given abvoe are usually referred to as *the Axioms of Probability* (or the Kolmogorov Axioms, after A. Kolmogorov, one of the fathers of probability theory)
- Any function $P$ that satisfies the Axioms of Probability is called
a probability function.
```
````

### Axiomatic Foundations

### The Calculus of Probabilities

### Counting

### Enumerating Outcomes

## Conditional Probability and Independence

## Random Variables

## Distribution Functions

## Density and Mass Functions