# Probability Theory

## Set Theory

***Sample space***: The set, $S$, of all possible outcomes of a particular experiment is called the sample space for the experiment.

***Event***: An event is any collection of possible outcomes of an experiment, that is, any subset of S (including S itself).

**Containment**:
$
    A \subset B \Leftrightarrow x \in A \rightarrow x \in B
$

**Equality**
$
    A = B \Leftrightarrow A \subset B~\text{and}~B \subset A
$

**Union**:
$
A \cup B = {x: x \in A~\text{or}~x \in B}
$

**Intersection**:
$
    A \cap B = {x: x \in A~\text{and} ~x \in B}
$

**Complementation**: 
$
    A^c = {x: x \notin A}
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

### Axiomatic Foundations

### The Calculus of Probabilities

### Counting

### Enumerating Outcomes

## Conditional Probability and Independence

## Random Variables

## Distribution Functions

## Density and Mass Functions