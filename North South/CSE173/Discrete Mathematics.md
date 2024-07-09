# Reference
Syllabus : [[CSE_173_content.pdf]]
Related to : [[Computer Science]],[[AI and Data Science]],[[Probability & Combinatrics]]
Lectures : [[CSE173 INTRODUCTION.pdf]],[[PROPOSITIONAL LOGIC.pdf]],[[PREDICATE QUANTIFIER.pdf]],[[RULE OF INFERENCE.pdf]],[[PROOF TECHNIQUES.pdf]],[[SET FUNCTIONS.pdf]],[[SET FUNCTIONS II.pdf]],[[SUM SEQUENCE.pdf]],[[RELATION.pdf]],[[RELATION II.pdf]],[[RECURSION COUNTING.pdf]],[[GRAPHS.pdf]],[[NUMBER II.pdf]]
Sample Questions : [[CSE 173 0.pdf]],[[CSE 173 1.pdf]],[[CSE 173 2.pdf]],[[CSE 173 4.pdf]],[[CSE 173 3.pdf]],[[CSE 173 5.pdf]]
Books : [[Kenneth Rosen - Discrete Mathematics and Its Applications.pdf]]

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

If $P\leftrightarrow Q$ denotes the proposition "A polygon is called a triangle only if it has three sides" where,
$P\to$ "A polygon is a triangle"
$Q\to$ "The polygon has three sides"
Possible scenarios : 

| $P$ | $Q$ | $P\leftrightarrow Q$ |
| --- | --- | -------------------- |
| $T$ | $T$ | $T$                  |
| $T$ | $F$ | $F$                  |
| $F$ | $T$ | $F$                  |
| $F$ | $F$ | $T$                  |
