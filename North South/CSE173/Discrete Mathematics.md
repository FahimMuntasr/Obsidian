---
Syllabus: "[[CSE_173_content.pdf]]"
Relations:
  - "[[Computer Science]]"
  - "[[AI and Data Science]]"
  - "[[Probability & Combinatrics]]"
  - "[[Calculus and Analytic Geometry]]"
  - "[[Introduction to Linear Algebra]]"
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
`Fahim Muntasir` 
 # Foundational Logic and Proofs
## Propositional Logic

Syllogism : A logical argument which relies on two or more propositions to come to a conclusion.
Proposition : A declarative sentence that can be definitively proved to be true or false.

#### Boolean Algebra

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

| $P$ | $Q$ | $P\lor Q$ |     |
| --- | --- | --------- | --- |
| $T$ | $T$ | $T$       |     |
| $T$ | $F$ | $T$       |     |
| $F$ | $T$ | $T$       |     |
| $F$ | $F$ | $F$       |     |

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

| $P$ | $Q$ | $P\to Q$ | $\neg P \lor Q$ |
| --- | --- | -------- | --------------- |
| $T$ | $T$ | $T$      | $T$             |
| $T$ | $F$ | $F$      | $F$             |
| $F$ | $T$ | $T$      | $T$             |
| $F$ | $F$ | $T$      | $T$             |

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

A tautology is always true.
$(p\land q)\to(p\lor q) \equiv \neg(p\land q)\lor (p\lor q)$
$\neg(p\land q)\lor (p\lor q)\equiv\neg p \lor \neg q \lor(p\lor q)$
$\neg p \lor \neg q \lor(p\lor q)\equiv (\neg p\lor p)\lor(\neg q\lor q)$
$(\neg p\lor p)\lor(\neg q\lor q)\equiv T \lor T$
$T \lor T\equiv T$
Some important logical equivalencies:

| Equivalence                                                                                                                                                                                                                                                                                                         | Name                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------- |
| $$P\land T\equiv P$$$$P\lor F\equiv P$$                                                                                                                                                                                                                                                                             | Identity laws               |
| $$P\land F\equiv F$$$$P\lor T\equiv T\;$$                                                                                                                                                                                                                                                                           | Domination laws             |
| $$P\land P\equiv P $$$$P\lor P\equiv P$$                                                                                                                                                                                                                                                                            | Idempotent laws             |
| $$\neg(\neg P)\equiv P$$                                                                                                                                                                                                                                                                                            | Double negation law         |
| $$P\lor Q\equiv Q\lor P$$$$P\land Q\equiv Q\land P$$                                                                                                                                                                                                                                                                | Commutative laws            |
| $$(P\lor Q)\lor R\equiv P \lor (Q\lor R)$$<br>$$(P\land Q)\land R\equiv P \land (Q\land R)$$                                                                                                                                                                                                                        | Associative laws            |
| $$P\lor(Q\land R)\equiv(P\lor Q)\land (P\lor R)$$<br>$$P\land(Q\lor R)\equiv(P\land Q)\lor (P\land R)$$                                                                                                                                                                                                             | Distributive laws           |
| $$\neg(P\lor Q) \equiv \neg P\land \neg Q$$<br>$$\neg(P\land Q) \equiv \neg P\lor \neg Q$$<br>$$\neg(P_1\lor P_2\lor P_3 ... \lor P_n) \equiv \neg P_1\land \neg P_2\land \neg P_3 ... \land \neg P_n$$<br>$$\neg(P_1\land P_2\land P_3 ... \lor P_n) \equiv \neg P_1\lor \neg P_2\lor \neg P_3 ... \lor \neg P_n$$ | De Morgan's laws            |
| $$(P\to Q) \equiv (\neg P \lor Q)$$                                                                                                                                                                                                                                                                                 | Definition of Implication   |
| $$P\lor(P\land Q)\equiv P$$$$P\land(P\lor Q)\equiv P$$                                                                                                                                                                                                                                                              | Absorption laws             |
| $$P\lor\neg P\equiv T$$$$P\land\neg P\equiv F$$                                                                                                                                                                                                                                                                     | Negation laws               |
| $$P\leftrightarrow Q\equiv (P\to Q)\land(Q\to P)$$                                                                                                                                                                                                                                                                  | Definition of biconditional |

## Predicate Quantifiers

#### Predicates
Predicates: Statements that, due to lack of information, are neither true or false.
`x>3 is a predicate as without knowing the value of x we cannot definitively say if it is true or false.`
Predicates are denoted as a propositional function;
$$P(x)=x>3$$
When we assign a value to x and **quantify** it, the propositional function becomes a proposition that is either TRUE or FALSE.
#### Quantifiers
Types of quantifications:
- Universal quantification: Where a predicate is true for every element in a set. Denoted by $$\forall xP(x)$$
- Existential quantification: Where a predicate is true for at least one element in a set. Denoted by $$\exists xP(x)$$
$\forall$ and $\exists$ quantifiers have a higher precedence than all other logical operators
$$\forall x(P(x)\land Q(x))\equiv\forall xP(x)\land\forall xQ(x)$$
#### Negating quantified expressions
Let $P(x)$ denote 'It has rained today'
Thus, $\forall xP(x)$ denotes 'It has rained everyday'
Negating this function would give $\neg\forall xP(x)$ 'It is not the  case that it has rained everyday'
This statement is the same as 'There is at least one day where it has not rained' which is denoted by $\exists x\neg P(x)$
$$\therefore\neg\forall xP(x)\equiv\exists x\neg P(x)$$
$$\therefore\neg\exists xP(x)\equiv\forall x\neg P(x)$$
#### Uniqueness quantifier

When it is stated that 'There exists a unique singular value of $x$ such that $P(x)$ is true", it is denoted as $\exists !xP(x)$ 

#### Nested Quantifiers
When one quantifier is within the scope of another quantifier it is called a nested quantifier.

| Statement                                            | When True                                                | When False                                                |
| ---------------------------------------------------- | -------------------------------------------------------- | --------------------------------------------------------- |
| $\forall x\forall yP(x,y)$$\forall y\forall xP(x,y)$ | $P(x,y)$ is true for every pair $x,y$                    | There is a pair $x,y$ for which $P(x,y)$ is false         |
| $\forall x\exists yP(x,y)$                           | For every $x$ there is a $y$ for which $P(x,y)$ is true  | There is an $x$ such that $P(x,y)$ is false for every $y$ |
| $\exists x\forall yP(x,y)$                           | There is an $x$ for which $P(x,y)$ is true for every $y$ | For every $x$ there is a $y$ for which $P(x,y)$ is false  |
| $\exists x\exists yP(x,y)$$\exists y\exists xP(x,y)$ | There is a pair $x,y$ for which $P(x,y)$ is true         | $P(x,y)$ is false for every pair $x,y$.                   |

## Rules of Inference

Inference : The process of reaching a conclusion using premises

You must have a **valid** **argument** to prove anything in mathematics. 

An argument is a sequence of statements that end with a conclusion, it is only valid when the conclusion follows the truth of the preceding premises/statements.

Fallacies : Invalid arguments that are based on incorrect reasoning. 

Example: If an argument is denoted by $p\to q$, it has 3 truth values ($p$,$q$,$p\to q$). If we have only 2 out of these 3 values we can *infer* the value of the third proposition.

When $p\to q$ and $p$ are both true, the only possible value of $q$ is true . Hence we can *infer* $q$ is true.

### Inference Laws
#### Modus Ponens
 `Mode that affirms`
$$(p\land(p\to q))\to q$$
If $p$ is *true*, and $p$ implies $q$, $\therefore$ we can infer that $q$ is also *true* 
	$p$
	$p\to q$
	$\therefore$ $q$
#### Modus Tollens
`Mode that denies`
$$(\neg q\land(p\to q))\to\neg p$$
If $q$ is false, and $p$ implies $q$ is true, $\therefore$ we can infer that p is also *false*
	$\neg q$
	$p\to q$
	$\therefore\neg p$
#### Hypothetical syllogism
`Syllogistic reasoning using two different hypothesis`
$$((p\to q)\land(q\to r))\to(p\to r)$$
If  $p$ implies $q$, and $q$ implies $r$, $\therefore$ we can infer that $p$ implies $r$
	$p\to q$
	$q\to r$
	$\therefore p\to r$
#### Disjunctive syllogism 
`Syllogistic reasoning using disjunction`
$$((p\lor q)\land\neg p)\to q$$
If $p$ OR $q$ is *true*, and $p$ is *false*, $\therefore$ we can infer that $q$ is *true* 
	$p\lor q$
	$\neg p$
	$\therefore q$
#### Addition
$$p\to(p\lor q)$$
If $p$ is *true*, $\therefore$ disjunction of $p$ and $q$ must be *true*
	$p$
	$\therefore p\lor q$
#### Simplification
$$(p\land q)\to p$$
If both $p$ AND $q$ are *true*, $\therefore$ $p$ must also be *true*
	$p\land q$
	$\therefore p$
#### Conjunction
$$((p)\land(q))\to(p\land q)$$
If $p$ is *true*, and $q$ is also *true*, $\therefore$ Conjunction between $p$ and $q$ must also be *true* 
	$p$
	$q$
	$\therefore p\land q$
#### Resolution
$$((p\lor q)\land(\neg p\lor r))\to(q\lor r)$$
If $p$ OR $q$ is true, and negation of $p$ or $r$ is also true, $\therefore$ Disjunction between $q$ and $r$ must be *true*
	$p\lor q$
	$\neg p\lor r$
	$\therefore q\lor r$

### Validity of an argument
If an argument consists of $n$ number of $p$ premises and a conclusion $q$, the argument is only valid when $(p_1\land p_2\land p_3\land ...\land p_n)\to q$ is a tautology
## Proof Techniques
**Theorem**: A statement that can be shown to be true

**Axioms**: Statements that we assume to be true

**Lemma**: A less important theorem that is helpful in the proof of other results

**Corrolary**: It is a theorem that can be established directly from a proven theorem

**Conjecture**: A statement that is proposed as true statement, usually on the basis of some partial evidence.

### Types of proof

**Direct proof** : Use of standard rules of inference to draw a conclusion without changing the problem statement.
	Example: Prove that if $m$ is even and $n$ is odd, their sum is always odd
	$n = 2k+1\;,\;k\in\mathbb{Z}$
	$m = 2j\;,\;j\in\mathbb{Z}$
	$\therefore m+n = 2j+2k+1 = 2(j+k) + 1$ 
	As both $j$ and $k$ are integers ($\mathbb{Z}$), $j+k$ must also be an integer. Therefore $m+n$ is odd by definition.

**Indirect proof** : Changing the problem statement and proving the new statement

Types of Indirect Proof
- Contrapositive : if we cant directly prove $p\to q$, we can prove the contrapositive of the statement which is $\neg q\to\neg p$   
	Example: Given $n\in\mathbb{Z}$ and $3n+2$ is odd, show that $n$ is odd.
	$p$ : $3n+2$ is odd
	$q$ : $n$ is odd
	Problem statement in propositional terms ; $p\to q$
	The contrapositive of this statement is $\neg q\to\neg p$
	Which translates to : If $n$ is even, $3n+2$ is even (Proving this will prove the original statement).
	$n = 2k\;,\;k\in\mathbb{Z}$
	$\therefore 3n+2=3(2k)+2 = 2(3k+1)$ (Even number definition).
	As $\neg q\to\neg p$ has been proven, this indirectly proves $p\to q$
- Proof by cases : Given $x$ is an integer, prove  that $x^2 +x$ is even
	Here there are two cases where $x$ can either be even or odd, if both of these individual cases can be proven then the problem statement can be proven to be true.
	Case 1
		$p:x = 2n$ (even)
		$x^2+x=(2n)^2+2n=4n^2+2n=2(2n^2+n)$ (even)
	Case 2
		$q:x=2n+1$ (odd)
		$x^2+x=(2n+1)^2+2n+1= (4n^2+6n+2) = 2(2n^2+3n+1)$ (even)
	As both cases are true, the problem statement is also proved.
- Proof by contradiction : Instead of proving the statement, we can prove the negation of the statement to be false.
	Example: Prove that $\sqrt 2$ is irrational.
	$P : \sqrt 2 \in\mathbb{I}$
	$\neg P:\sqrt 2\in\mathbb{Q}$
	All rational numbers can be expressed in the form $\frac{P}{Q}$ where it is in its lowest terms.
	$\sqrt 2 = \frac{P}{Q}$
	$2 = \frac{P^2}{Q^2}$
	$P^2=2Q^2$ ($P^2$ is in even form , $\therefore P$ is also even)
	$(2k)^2 = 2Q^2 \equiv 2k^2 = Q^2$($\therefore Q$ is also even)  
	As both $P$ and $Q$ are even, both of them have a common factor of $2$ , which contradicts with the fact that $\frac{P}{Q}$ has to be in its lowest terms.
	As we proved the negation of $P$ to be false, this proves $P$ to be true $[\neg(\neg P)\equiv P\equiv T]$  