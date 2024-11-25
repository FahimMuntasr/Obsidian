---
Syllabus: "[[CSE_173_content.pdf]]"
Relations:
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

# Sets, Functions

## Sets
#### Describing a Set
A set is an unordered collection of distinct non-repeating elements.
Ways to describe a set:
- **Roster Method :** Listing out all the elements of the set$$A=\{1,2,3,4,5,6,7,8\}$$
- **Set Builder Notation :** Instead of listing out all the elements the characteristics $$A = \{x|x\;\text{is an odd positive integer less than 10}\}$$
#### Cardinality
The **cardinality** of a set is the number of elements in that set.
Sets with a **cardinality** of 0 are called **Null** sets$$\varnothing=\{\}\;;\;|\varnothing| = 0$$
Sets with a **cardinality** of 1 are called **singleton** sets
#### Subsets
If set $A$ is a *subset* of set $B$, then set $B$ is a superset of set $A$. Where every element in set $A$ is an element of set $B$.
$$A \subseteq B$$
#### Power Sets
For a set $A$, the *power set* of $A$ is the set of all subsets of the set $S$. Denoted by $\mathcal{P}(A)$
$A = \{ 0,1,2\}$
$\mathcal{P}(A) = \{ \emptyset , \{0\},\{1\},\{2\},\{0,1\},\{0,2\},\{1,2\},\{0,1,2\}\}$
$|\mathcal{P}(A)| = 2^{|A|}$
#### Cartesian Product
The cartesian product of sets $A$ and $B$ is the set of all ordered pairs $(a,b)$.
$A = \{1,2,3\}$
$B = \{a,b,c\}$
$A\times B = \{(1,a),(1,b),(1,c),(2,a),(2,b),(2,c),(3,a),(3,b),(3,c)\}$
## Set Operations
#### Union
Let;
	$A = \{x|x\in A\}$
	$B=\{x|x\in B\}$
The union of sets $A$ and $B$ is denoted by;
	$A\cup B\equiv\{x|x\in A\lor x\in B\}$
#### Intersection
Let;$$A=\{x|x\in A\}$$$$B=\{x|x\in B\}$$The intersection of sets $A$ and $B$ is denoted by;$$A\cap B\equiv \{x|x\in A\land x\in B\}$$
#### Complement 
The complement of set $A$ is the set of all elements that is not in $A$ 
$\overline{A} = \{x|x\notin A\}$
#### Disjoint sets
When the intersection of multiple sets result in a null set, the sets are said to be disjoint$$A\cap B=\varnothing$$
#### Difference 
The difference of set $A$ and $B$ is the set of elements that are in $A$ but not in $B$ 
$A-B = \{x|x\in A\cap x\notin B\}$
	   $=\{x|x\in A\cap x\in\overline{B}\}$
	   $=\{x|x\in A\cap\overline{B}\}$
$A-B = A\cap\overline{B}$

#### Set Identities

| Identity                                                                                            | Name                 |
| --------------------------------------------------------------------------------------------------- | -------------------- |
| $$A\cap U=A$$$$A\cup\emptyset=A$$                                                                   | Identity laws        |
| $$A\cup U=U$$$$A\cap\emptyset=\emptyset$$                                                           | Domination laws      |
| $$A\cup A=A$$$$A\cap A=A$$                                                                          | Idempotent laws      |
| $$\overline{(\overline A)}=A$$                                                                      | Complementation laws |
| $$A\cup B=B\cup A$$$$A\cap B=B\cap A$$                                                              | Commutative laws     |
| $$A\cup(B\cup C)=(A\cup B)\cup C$$$$A\cap(B\cap C)=(A\cap B)\cap C$$                                | Associative laws     |
| $$A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$$$$A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$$                  | Distributive laws    |
| $$\overline{ A\cap B}=\overline A\cup\overline B$$$$\overline{A\cup B}=\overline A\cap\overline B$$ | De Morgan's laws     |
| $$A\cup(A\cap B)=A$$$$A\cap(A\cup B)=A$$                                                            | Absorption laws      |
| $$A\cup\overline A=U$$$$A\cap\overline A=\emptyset$$                                                | Complement laws      |
## Functions
A function maps each element from a non-empty set $A$ to exactly one element from a non-empty set $B$.
#### Types of functions
- Injective (One-to-One)
	`A function f is one-to-one if and only if f(a) = f(b) implies a=b for all values of $a$ and $b$ within the domain of f.`
	`For a function f(x) = x, all distinct values of x within the domain must have a distinct corresponding value of f(x)`
	For the function $f:A\to B$ , if it is injective
	$|A|\le |B|$
- Surjective (Onto)
	`A function f is onto if and only if every element in the codomain of the function can be mapped from an element of the domain.`
	For the function $f:A\to B$, if it is surjective
	$|A|\ge |B|$
- Bijective (One-to-One correspondence)
	`A function f is bijective if both it is both one-to-one and onto`
	For the function $f:A\to B$ if it is bijective,
	$|A|=|B|$
#### Increasing and Decreasing functions
For a function $f(x)$, 
- **INCREASING** when $x_2>x_1$ and $f(x_2)\ge f(x_1)$
- **STRICTLY INCREASING** when $x_2>x_1$ and $f(x_2)> f(x_1)$
- **DECREASING** when $x_2>x_1$ and $f(x_2)\le f(x_1)$
- **STRICTLY DECREASING** when $x_2>x_1$ and $f(x_2)< f(x_1)$

A function reaches a stationary point when $\frac{d}{dx}=0$
A function reaches a minima when $\frac{d^2}{dx^2}>0$
A function reaches a maxima when $\frac{d^2}{dx^2}<0$
#### Inverse Functions
For a function $f:A\to B$ which is bijective, the inverse of $f$ assigns codomain elements to a unique domain element such $f(a)=b$ when $f^{-1}(b) = a$ 
**ONLY BIJECTIVE FUNCTIONS CAN BE INVERSED**
#### Floor and Ceiling Functions
Floor functions
- The floor of a variable $x$ is denoted by $\lfloor x\rfloor$, it is defined as the largest integer that is smaller than $x$.
Ceiling functions
- The ceiling of a variable $x$ is denoted by $\lceil x\rceil$, it is defined as the smallest integer that is larger than $x$.
## Cardinality of Sets
#### Countable Sets
If a set is finite then it is said to be countable.
If a set is infinite then it can also be said to be countable, with a condition that the cardinality of the set must be equal to the cardinality of positive integers ($\mathbb{N}:\{1,2,3,4,5,....\}$)
## Recursion
A function/relation that repeats or uses its own previous term to calculate subsequent terms 
The factorial function is a basic example of a recursive function;
$f(x)=x!$ 
$f(5) = 5! = 5 \times 4\times 3\times 2\times 1$
$f(5) = 5\times 4!$
$f(5) = 5\times f(4)$
$\therefore f(x) = x\times f(x-1)$ , where $f(0) = 1$ 

## Sequences & Summation
A sequence is a function which maps elements from a subset of integers to a set $S$.  
It is a discrete structure used to represent an ordered list
#### Types of sequences
- Geometric
	A common ratio $r$ exists between two subsequent terms.$$n^{th}\;term = ar^{n-1},\;where\;n=1 \;for\;the \;first\;term$$
	Summation ;$$\sum_{i=0}^{n}ar^i=\frac{ar^{n+1}-a}{r-1}\;,r\ne1$$
- Arithmetic
	A common difference $d$ exists between two subsequent terms.$$n^{th}\;term=a+(n-1)d,\;where\;n=1\;for\;the\;first \;term$$
	Summation;$$\sum_{i=0}^{n-1}a+id=\frac{n}{2}[2a+(n-1)d]$$
#### Useful summation formulae

| Sum                                     | Closed Form/Equivalent Form          |
| --------------------------------------- | ------------------------------------ |
| $$\sum^{n}_{k=0}ar^k\;(r\neq 0)$$       | $$\frac{ar^{n+1}-a}{r-1},\;r\neq 1$$ |
| $$\sum^n_{k=1}k$$                       | $$\frac{n(n+1)}{2}$$                 |
| $$\sum^n_{k=1}k^2$$                     | $$\frac{n(n+1)(2n+1)}{6}$$           |
| $$\sum^n_{k=1}k^3$$                     | $$\frac{n^2(n+1)^2}{4}$$             |
| $$\sum^n_{k=1}c$$                       | $$nc$$                               |
| $$\sum^{\infty}_{k=0}x^k,\|x\|<1$$      | $$\frac{1}{1-x}$$                    |
| $$\sum^{\infty}_{k=1}kx^{k-1},\|x\|<1$$ | $$\frac{1}{(1-x)^2}$$                |
| $$\sum^a_bf(x)$$                        | $$\sum^a_1f(x)-\sum^{b-1}_1f(x)$$    |
| $$\sum^a_b kf(x)$$                      | $$k\sum^a_bf(x)$$                    |
| $$\sum^a_b[f(x)+k]$$                    | $$\sum^a_bf(x)+\sum^a_bk$$           |
# Relations

#### Relation between two sets
A relation $R$ from two sets $A$ to $B$ is a subset of $A\times B$ $$R\subseteq A\times B$$
#### Relation on a set
A relation $R$ on a set $A$ is a subset of $A\times A$$$R\subseteq A\times A$$
#### Relational Matrix
A relational Matrix $M_r$ representing a relation $R$ on a set $A$ looks like this:
if set $A$ is defined as; $$A=\{0,1,2\}$$
And relation $R$ is defined as;$$R = \{(1,0),(0,1),(1,1),(1,2),(2,2)\}$$
The relational matrix $M_r$ is defined as; $$M_r=\begin{bmatrix}0&1&0\\1&1&0\\0&1&1\end{bmatrix}$$
#### Types of relations
##### Reflexive
A relation $R$ on a set $A$ is called *reflexive* if $(a,a)\in R$ for every element $a\in A$ 

The trace of $M_r$ will be equal to the cardinality of $A$ , as the main diagonal will all be 1s.$$tr(M_r) = |A|$$
##### Symmetric
A relation $R$ on a set $A$ is called symmetric if $(b, a) ∈ R$ whenever $(a, b) ∈ R$, for all $a, b ∈ A$

The trace of $M_r$ will be equal to cardinality of $A$ , as the main diagonal will all be 1s.$$tr(M_r)=|A|$$
The matrix formed be transposing $M_r$ will be identical to $M_r$
$$(M_r)^T\equiv M_r$$
##### Antisymmetric
A relation $R$ on a set $A$ such that for all $a, b ∈ A$, if $(a, b) ∈ R$ and $(b, a) ∈ R$, then $a = b$ is called antisymmetric.

The trace of $M_r$ will be equal to cardinality of $A$ , as the main diagonal will all be 1s.$$tr(M_r)=|A|$$
The matrix formed be transposing $M_r$ can NOT be identical to $M_r$\[Unless $M_r$ is an identity matrix\]$$(M_r)^T\not\equiv M_r\;, M_r\not\equiv I$$
##### Transitive 
A relation $R$ on a set $A$ is called transitive if whenever $(a, b) ∈ R$ and $(b, c) ∈ R$, then $(a, c) ∈ R$, for all $a, b, c ∈ A$
`No notable property can be observed from a transitive matrix , unlike the other types`
##### Composite relations 
$$\text{if , }R=\{(a,b)\in R|a\in A, b\in B\}$$$$\text{and , }S=\{(b,c)\in S|b\in B, c\in C\}$$$$\text{then , }R\circ S=\{(a,c)\in R\circ S|a\in A, c\in C\}$$
##### Powers of a relation
If $R$ is a relation on set $A$, then the $n^{th}$ power of $R$ , is defined recursively as ;$$R^n = R^{n-1}\circ R\;,n=1,2,3,...$$
**SIDE NOTE**
	The relation $R$ on set $A$ is transitive if and only if $R^n\subseteq R$ for $n=1,2,3,...$ 
##### Transitive closure
The **transitive closure** of a relation $R$ on a set $A$ is the smallest transitive relation $T$ on $A$ such that $R⊆T$ . 

If $M_R$ is an $n\times n$ matrix, the transitive closure denoted by $M_{R*}$ is defined as;$$M_{R*}=M_R\lor M^{[2]}_R\lor M^{[3]}_R\lor...\lor M^{[n]}_R$$where, $$M^{[k]}_R = M^{[k-1]}_R\odot M_R$$
##### Equivalence relations
A relation on set $A$ is called an *equivalence relation* if it is reflexive, symmetric, and transitive.

# Counting

#### Product rule 
If a task can be split into a sequence of two tasks, where there are $n_1$  ways to do the first task and for each of these ways of doing the first task, there are $n_2$ ways to do the second task, then there are $n_1n_2$ ways to do the task.

#### Sum rule
If a task can be done either in one of $n_1$ ways or in one of $n_2$ ways, where none of the set of $n_1$ ways is the same as any of the set of $n_2$ ways, then there are $n_1 + n_2$ ways to do the task.

#### Subtraction rule (Inclusion-Exclusion Principle)
If a task can be done in either $n_1$ ways or $n_2$ ways, then the number of ways to do the task is $n_1 + n_2$ minus the number of ways to do the task that are common to the two different ways$$|A_1\cup A_2|=|A_1|+|A_2|-|A_1\cap A_2|$$