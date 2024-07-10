---
Syllabus: "[[CSE_173_content.pdf]]"
Relations:
  - "[[Computer Science]]"
  - "[[AI and Data Science]]"
  - "[[Probability & Combinatrics]]"
Reference:
  - "[[CSE173 INTRODUCTION.pdf]]"
  - "[[PROPOSITIONAL LOGIC.pdf]]"
  - "[[PREDICATE QUANTIFIER.pdf]]"
  - "[[RULE OF INFERENCE.pdf]]"
  - "[[PROOF TECHNIQUES.pdf]]"
  - "[[SET FUNCTIONS.pdf]]"
  - "[[SET FUNCTIONS II.pdf]]"
  - "[[SUM SEQUENCE.pdf]]"
  - "[[RELATION.pdf]]"
  - "[[RELATION II.pdf]]"
  - "[[RECURSION COUNTING.pdf]]"
  - "[[GRAPHS.pdf]]"
  - "[[NUMBER II.pdf]]"
Practice:
  - "[[CSE 173 0.pdf]]"
  - "[[CSE 173 1.pdf]]"
  - "[[CSE 173 2.pdf]]"
  - "[[CSE 173 3.pdf]]"
  - "[[CSE 173 4.pdf]]"
  - "[[CSE 173 5.pdf]]"
Books:
  - "[[Kenneth Rosen - Discrete Mathematics and Its Applications.pdf]]"
---

# Propositional Logic

Syllogism : A logical argument which relies on two or more propositions to come to a conclusion.
Proposition : A declarative sentence that can be definitively proved to be true or false.

### Boolean Algebra

Compound propositions were first discussed by English Mathematician George Boole.
`Boolean Algebra is named after him`

**Negation** : If $P$ is a proposition, the negation of $P$ is $\neg P$. 
$\neg P$ is true when $P$ is false and vice versa.
`Same as a NOT gate`

| $P$ | $\neg P$ |
| --- | -------- |
| $T$ | $F$      |
| $F$ | $T$      |

**Conjunction** : If $P$ and $Q$ are propositions, the conjunction of $P$ and $Q$ is $P\land Q$.
$P\land Q$ is true when BOTH $P$ and $Q$ is true.
`Same as an AND gate`

| $P$ | $Q$ | $P\land Q$ |
| --- | --- | ---------- |
| $T$ | $T$ | $T$        |
| $T$ | $F$ | $F$        |
| $F$ | $T$ | $F$        |
| $F$ | $F$ | $F$        |

**Disjunction** : If $P$ and $Q$ are propositions, the disjunction of $P$ and $Q$ is $P\lor Q$.
$P\lor Q$ is true when either $P$ and/or $Q$ is true.
`Same as an OR gate`

| $P$ | $Q$ | $P\lor Q$ |
| --- | --- | --------- |
| $T$ | $T$ | $T$       |
| $T$ | $F$ | $T$       |
| $F$ | $T$ | $T$       |
| $F$ | $F$ | $F$       |

**Exclusive or** : If $P$ and $Q$ are propositions, the *exclusive or* of $P$ and $Q$ is $P\oplus Q$.
$P\oplus Q$ is true exclusively when either $P$ or $Q$ is true, but false when both have the same value.
`Same as XOR gate`

| $P$ | $Q$ | $P\oplus Q$ |
| --- | --- | ----------- |
| $T$ | $T$ | $F$         |
| $T$ | $F$ | $T$         |
| $F$ | $T$ | $T$         |
| $F$ | $F$ | $F$         |

**Conditional Statements** : Denoted by $P\to Q$ , false only when $P$ is true and $Q$ is false, and is true otherwise.

This might be confusing, giving an example will help:
If a proposition is "If it rains today, the ground will get wet", it is denoted by $P\to Q$ where, 
$P\to$ "It's raining today"
$Q\to$ "The ground got wet"
Possible scenarios :

1. It rained today ($P$ is true), and the ground got wet ($Q$ is true). As this supports the original proposition, $P\to Q$ is true in this case.
2. It rained today ($P$ is true), but the ground didn't get wet ($Q$ is false). As this **contradicts** the original proposition, $P\to Q$ is false in this situation.
3. It did not rain today ($P$ is false), but the ground still got wet because of some other reason ($Q$ is true). This statement does not **contradict** the original proposition, $P\to Q$ is still true in this situation.
4. It did not rain today ($P$ is false), and the ground did not get wet ($Q$ is false). This supports the original proposition so $P\to Q$ is true in this situation.

| $P$ | $Q$ | $P\to Q$ |
| --- | --- | -------- |
| $T$ | $T$ | $T$      |
| $T$ | $F$ | $F$      |
| $F$ | $T$ | $T$      |
| $F$ | $F$ | $T$      |

**Biconditional statement** : Denoted by $P\leftrightarrow Q$, true only when both $P$ and $Q$ have same values and false otherwise.

If $P\leftrightarrow Q$ denotes the proposition "A shape is called a triangle only if it has three sides" where,
$P\to$ "A shape is a triangle"
$Q\to$ "The shape has three sides"
Possible scenarios : 

1. The shape is called a triangle ($P$ is true), and it has three sides ($Q$ is true). As this supports the original proposition, $P\leftrightarrow Q$ is true here.
2. The shape is called a triangle ($P$ is true), but it does not have three sides ($Q$ is false). This contradicts the proposition which means $P\leftrightarrow Q$ is false.
3. The shape is not called a triangle ($P$ is false), but it has three sides ($Q$ is true). This also contradicts the proposition which means $P\leftrightarrow Q$ is false.
4. The shape is not called a triangle ($P$ is false), and it does not have three sides($Q$ is false). This supports the original proposition which means $P\leftrightarrow Q$ is true.

| $P$ | $Q$ | $P\leftrightarrow Q$ |
| --- | --- | -------------------- |
| $T$ | $T$ | $T$                  |
| $T$ | $F$ | $F$                  |
| $F$ | $T$ | $F$                  |
| $F$ | $F$ | $T$                  |

**Converse, Contrapositive and Inverse** : 

If $P\to Q$ is a proposition;
- Converse : $Q\to P$
- Contrapositive : $\neg Q\to \neg P$ 
- Inverse : $\neg P\to \neg Q$ 
The contrapositive of a proposition is effectively the same thing as the original proposition.

Example : 

Original proposition : $P\to Q$ ; "If it is raining, the ground will get wet"
Contrapositive proposition : $\neg Q\to \neg P$ ; "If the ground is not wet, it is not raining"
Converse proposition : $Q\to P$ ; "If the ground is wet, it is raining"
Inverse proposition : $\neg P\to \neg Q$ ; "If it is not raining, the ground will not get wet"

**Truth tables**

| $P$ | $Q$ | $\neg P$ | $\neg Q$ | $P\land Q$ | $P\lor Q$ | $P\oplus Q$ | $P\to Q$ | $P\leftrightarrow Q$ |
| --- | --- | -------- | -------- | ---------- | --------- | ----------- | -------- | -------------------- |
| $T$ | $T$ | $F$      | $F$      | $T$        | $T$       | $F$         | $T$      | $T$                  |
| $T$ | $F$ | $F$      | $T$      | $F$        | $T$       | $T$         | $F$      | $F$                  |
| $F$ | $T$ | $T$      | $F$      | $F$        | $T$       | $T$         | $T$      | $F$                  |
| $F$ | $F$ | $T$      | $T$      | $F$        | $F$       | $F$         | $T$      | $T$                  |

Practice: Find the truth table for $(P\lor \neg Q)\to (P\land Q)$

| $P$ | $Q$ | $\neg Q$ | $P\lor \neg Q$ | $P\land Q$ | $(P\lor \neg Q)\to (P\land Q)$ |
| --- | --- | -------- | -------------- | ---------- | ------------------------------ |
| $T$ | $T$ | $F$      | $T$            | $T$        | $T$                            |
| $T$ | $F$ | $T$      | $T$            | $F$        | $F$                            |
| $F$ | $T$ | $F$      | $F$            | $F$        | $T$                            |
| $F$ | $F$ | $T$      | $T$            | $F$        | $F$                            |

**Operator precedence**

| Operator          | Precedence |
| ----------------- | ---------- |
| $\neg$            | 1          |
| $\land$           | 2          |
| $\lor$            | 3          |
| $\to$             | 4          |
| $\leftrightarrow$ | 5          |

**Propositional Equivalence**

Tautology : A compound proposition that is always true and independent of the truth values of its constituent propositions
Contradictions : A compound proposition that is always false and independent of the truth values of its constituent propositions
Contingency : A compound proposition that is neither a tautology nor a contradiction.

**Logical Equivalence**

When two compound propositions have the same truth values for all  possible cases, they are logically equivalent. This is denoted by $P\equiv Q$ .
If $P\leftrightarrow Q$ is a tautology then $P\equiv Q$.
example:

| $P$ | $Q$ | $\neg P$ | $P\to Q$ | $\neg P\lor Q$ |
| --- | --- | -------- | -------- | -------------- |
| $T$ | $T$ | $F$      | $T$      | $T$            |
| $T$ | $F$ | $F$      | $F$      | $F$            |
| $F$ | $T$ | $T$      | $T$      | $T$            |
| $F$ | $F$ | $T$      | $T$      | $T$            |

$(P\to Q) \equiv (\neg P \lor Q)$

**De Morgan's Law** is used to convert conjunctions to disjunctions and vice versa.
1. $\neg(P\lor Q) \equiv \neg P\land \neg Q$
2. $\neg(P\land Q) \equiv \neg P\lor \neg Q$
Similarly, for $n$ propositional variables;
1. $\neg(P_1\lor P_2\lor P_3 ... \lor P_n) \equiv \neg P_1\land \neg P_2\land \neg P_3 ... \land \neg P_n$
2. $\neg(P_1\land P_2\land P_3 ... \lor P_n) \equiv \neg P_1\lor \neg P_2\lor \neg P_3 ... \lor \neg P_n$

Practice : 
Prove $(p\land q)\to(p\lor q)$ is a tautology.

A tautology is a always true.
$(p\land q)\to(p\lor q)\equiv \neg (p\land q)\lor (p\lor q)$
$\equiv (\neg p \lor \neg q) \lor (p \lor q)$
$\equiv (\neg p \lor p) \lor (\neg q\lor q)$ 
$\equiv T \lor T$
$\equiv T$

Some important logical equivalencies:
$$\neg(P\lor Q) \equiv \neg P\land \neg Q$$
$$\neg(P\land Q) \equiv \neg P\lor \neg Q$$
$$\neg(P_1\lor P_2\lor P_3 ... \lor P_n) \equiv \neg P_1\land \neg P_2\land \neg P_3 ... \land \neg P_n$$
$$\neg(P_1\land P_2\land P_3 ... \lor P_n) \equiv \neg P_1\lor \neg P_2\lor \neg P_3 ... \lor \neg P_n$$
$$(P\to Q) \equiv (\neg P \lor Q)$$
$$P\land T\equiv P$$
$$P\land F\equiv F$$
$$P\lor F\equiv P$$
$$P\lor T\equiv T$$
$$(P\lor Q)\lor R\equiv P \lor (Q\lor R)$$
$$(P\land Q)\land R\equiv P \land (Q\land R)$$
$$P\lor Q\equiv Q\lor P$$
$$P\land Q\equiv Q\land P$$
$$P\lor(Q\land R)\equiv(P\lor Q)\land (P\lor R)$$
$$P\land(Q\lor R)\equiv(P\land Q)\lor (P\land R)$$
# Predicate Quantifiers
