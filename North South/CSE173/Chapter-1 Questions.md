# Sample Quiz 1

### Question 1
Identify the propositions, and show their relations:
	(a) If you are happy and watch movies then your friend becomes unhappy.
		$p$ : You are happy
		$q$ : You watch movies
		$r$ : Your friend is happy
		$(p\land q)\to \neg r$
	(b) You are a Bangladeshi or if you are not a Bangladeshi then your friend is European.
		$p$ : You are Bangladeshi
		$q$ : Your friend is European
		$p\lor(\neg p\to q)$
### Question 2
Use a series of logical equivalences to identify if the compound proposition $(p\land(p\to q))\to q$ is a tautology/contradiction/contingency.
	$(p\land(p\to q))\to q$
	$\equiv(p\land(\neg p\lor q))\to q$              \[Definition of Implication]
	$\equiv\neg(p\land(\neg p\lor q))\lor q$             \[Definition of Implication]
	$\equiv(\neg p\lor\neg(\neg p\lor q))\lor q$            \[De Morgan's Law]
	$\equiv(\neg p\lor(p\land\neg q))\lor q$               \[De Morgan's Law]
	$\equiv ((\neg p\lor p)\land(\neg p\lor\neg q))\lor q$    \[Distributive Law]
	$\equiv (T\land(\neg p\lor\neg q))\lor q$               \[Negation Law]
	$\equiv(\neg p\lor\neg q)\lor q$                        \[Identity Law]
	$\equiv\neg p\lor(\neg q\lor q)$                        \[Commutative Law]
	$\equiv\neg p\lor T$                                  \[Negation Law]
	$\equiv T$                                          \[Domination Law]
	$\therefore$ Tautology
### Question 3
Construct the Truth Table for the compound proposition defined as $(\neg q)\to(p\lor\neg r)$

| $p$ | $q$ | $r$ | $\neg q$ | $\neg r$ | $p\lor\neg r$ | $(\neg q)\to(p\lor\neg r$) |
| --- | --- | --- | -------- | -------- | ------------- | -------------------------- |
| $T$ | $T$ | $T$ | $F$      | $F$      | $T$           | $T$                        |
| $T$ | $T$ | $F$ | $F$      | $T$      | $T$           | $T$                        |
| $T$ | $F$ | $T$ | $T$      | $F$      | $T$           | $T$                        |
| $T$ | $F$ | $F$ | $T$      | $T$      | $T$           | $T$                        |
| $F$ | $T$ | $T$ | $F$      | $F$      | $F$           | $T$                        |
| $F$ | $T$ | $F$ | $F$      | $T$      | $T$           | $T$                        |
| $F$ | $F$ | $T$ | $T$      | $F$      | $F$           | $F$                        |
| $F$ | $F$ | $F$ | $T$      | $T$      | $T$           | $T$                        |
### Question 4
Apply a series of logical equivalences to show that: $((\neg p)\to(r\lor q))\equiv ((\neg r)\to((\neg p)\to q))$ are logically equivalent

$((\neg p)\to(r\lor q))\equiv ((\neg r)\to((\neg p)\to q))$
$(\neg(\neg p)\lor(r\lor q))\equiv(\neg(\neg r)\lor(\neg(\neg p)\lor q)$
$(p\lor(r\lor q))\equiv(r\lor(p\lor q)$
$p\lor q\lor r\equiv p\lor q\lor r$
$\therefore$ Logically equivalent

### Question 5
Determine if the below statements are True or False. Justify your answers with example or counter example.
	(a) $\exists x(P(x):x^5=-1),x\in\mathbb{z}$
		When, $x = -1$ ; $x^5 = -1$
		as $P(-1)$ is True, $\exists x(P(x))$ is True
	(b) $\exists x(P(x):x^6<x^2),x\in\mathbb{R}$
		When, $x=\frac{1}{2}$ ; $x^2 =\frac{1}{2}$, $x^6=\frac{1}{64}$ , $x^2>x^6$
		as $P(\frac{1}{2})$ is True, $\exists x(P(x))$ is True
	(c) $\forall x(P(x):1000x>x),x\in\mathbb{R}$
		$1000x>x$ (Divide both sides by $x$)
		Statement becomes : $1000>1$ which is always true no matter what the value of $x$ is.
		As $P(x)$ is True for all values of $x$, $\forall x(P(x))$ is True
	(d) $\forall x(P(x):(-x)^4=x^4),x\in\mathbb{R}$
		$(-1)^4(x)^4=x^4$
		$x^4=x^4$ 
		Both sides are equal, the statement will be true no matter what the value of $x$ is.
		As $P(x)$ is True for all values of $x$, $\forall(P(x))$ is True
# Section 1.1

### Question 9
 Suppose that during the most recent fiscal year, the annual revenue of Acme Computer was 138 billion dollars and its net profit was 8 billion dollars, the annual revenue of Nadir Software was 87 billion dollars and its net profit was 5 billion dollars, and the annual revenue of Quixote Media was 111 billion dollars and its net profit was 13 billion dollars. Determine the truth value of each of these propositions for the most recent fiscal year.
	 (a) Quixote Media had the largest annual revenue. $$F$$(b) Nadir Software had the lowest net profit and Acme Computer had the largest annual revenue. $$T\land T\equiv T$$(c) Acme Computer had the largest net profit or Quixote Media had the largest net profit. $$F\lor T\equiv T$$(d) If Quixote Media had the smallest net profit, then Acme Computer had the largest annual revenue. $$F\to T\equiv T$$(e) Nadir Software had the smallest net profit if and only if Acme Computer had the largest annual revenue.$$T\leftrightarrow T\equiv T$$
### Question 12
Let $p$ and $q$ be the propositions “The election is decided” and “The votes have been counted,” respectively. Express each of these compound propositions as an English sentence.
	(a) $\neg p$ : The election is not decided
	(b) $p\lor q$ : The election is decided or the votes have been counted
	(c) $\neg p\land q$ : The election is not decided and the votes have been counted
	(d) $q\to p$ : If the votes have been counted, then the election is decided
	(e) $\neg q\to\neg p$ : If the votes have not been counted, then the election is not decided
	(f) $\neg p\to\neg q$ : If the election is not decided, then the votes have not been counted
	(g) $p\leftrightarrow q$ : The election is decided if and only if the votes have been counted
	(h) $\neg q\lor(\neg p\land q)$ : Either the votes have not been counted, or the election is not decided and the votes have been counted.
### Question 14
Let $p$, $q$ and $r$ be the propositions
	$p$ : You have the flu
	$q$ :  You miss the final examination
	$r$ : You pass the course.
Express each of these propositions as an English sentence.
	(a) $p\to q$
		If you have the flu, then you miss the final examination
	(b)$\neg q\leftrightarrow r$
		You pass the course if and only if you do not miss the final examination
	(c) $q\to\neg r$
		if you miss the final examination you will not pass the course
	(d)$p\lor q\lor r$
		You have the flu or you miss the final examination or you pass the course
	(e)$(p\to\neg r)\lor(q\to\neg r)$
		If you have the flu then you will not pass the course, or if you miss the final examination you will not pass the course.
	(f)$(p\land q)\lor(\neg q\land r)$
		You have the flu and you miss the final examination, or you don't have the flue and you pass the course
### Question 15
Let $p$ and $q$ be the propositions
	$p$ : You drive over 65 miles per hour.
	$q$ : You get a speeding ticket.
Write these propositions using $p$ and $q$ and logical connectives(including negations).
	(a) You do not drive over 65 miles per hour.
		$\neg p$
	(b) You drive over 65 miles per hour, but you do not get a speeding ticket.
		$p\land \neg q$
	(c) You will get a speeding ticket if you drive over 65 miles per hour.
		$p\to q$
	(d) If you do not drive over 65 miles per hour, then you will not get a speeding ticket.
		$\neg p\to\neg q$
	(e) Driving over 65 miles per hour is sufficient for getting a speeding ticket.
		$p\to q$
	(f) You get a speeding ticket, but you do not drive over 65 miles per hour.
		$q\land\neg p$
	(g) Whenever you get a speeding ticket, you are driving over 65 miles per hour.
		$q\leftrightarrow p$
### Question 19
Determine whether each of these conditional statements is true or false.
	(a) If 1+1 = 3, then 2 + 2 = 5
		$p : 1 + 1 = 3\equiv F$ 
		$q : 2 + 2 = 5\equiv F$
		$\therefore p\to q \equiv T$
	(b) If 1+1 = 3, then dogs can fly
		$p : 1 + 1 = 3\equiv F$
		$q$ : dogs can fly $\equiv F$
		$\therefore p\to q\equiv T$ 
	(c) If 1+1 = 2, then dogs can fly
		$p: 1+ 1 = 2\equiv T$
		$q :$ Dogs can fly $\equiv F$
		$\therefore p\to q\equiv F$
	(d) If 2 + 2 = 4, then 1 + 2 = 3
		$p : 2 + 2 = 4\equiv T$
		$q:1 + 2 = 3\equiv T$
		$p\to q\equiv T$
### Question 26
Write each of these statements in the form “if p, then q” in English. 
	(a) I will remember to send you the address only if you send me an e-mail message. 
		If you send me an e-mail message ,then I will remember to send you the address.
	(b) To be a citizen of this country, it is sufficient that you were born in the United States.
		If you were born in the United States ,then you are a citizen of this country.
	(c) If you keep your textbook, it will be a useful reference in your future courses.
		If you keep your textbook ,then it will be a useful reference in your future courses.
	(d) The Red Wings will win the Stanley Cup if their goalie plays well. 
		If their goalie plays well, then the Red Wings will win the Stanley Cup
	(e) That you get the job implies that you had the best credentials. 
		If you get the job, then you get the job
	(f) The beach erodes whenever there is a storm. 
		If there is a storm, then the beach erodes
	(g) It is necessary to have a valid password to log on to the server. 
		If you have a valid password, then you can log on to the server
	(h) You will reach the summit unless you begin your climb too late. 
		If you do not climb too late, then you will reach the summit
	(i) You will get a free ice cream cone, provided that you are among the first 100 customers tomorrow.
		If you are among the first 100 customers tomorrow, then you will get a free ice cream cone
### Question 27
Write each of these propositions in the form “$p$ if and only if $q$” in English.
	(a) If it is hot outside you buy an ice cream cone, and if you buy an ice cream cone it is hot outside.
		You buy an ice cream cone if and only if it is hot outside.
	(b) For you to win the contest it is necessary and sufficient that you have the only winning ticket.
		You win the contest if and only if you have the only winning ticket.
	(c) You get promoted only if you have connections, and you have connections only if you get promoted.
		You get promoted if and only if you have connections.
	(d) If you watch television your mind will decay, and conversely.
		Your mind will decay if and only if you watch television.
	(e) The trains run late on exactly those days when I take it.
		The trains run late if and only if I take it.
# Section 1.2
### Question 7
Express these system specifications using the propositions p: “The message is scanned for viruses” and q: “The message was sent from an unknown system” together with logical connectives (including negations).
	(a)“The message is scanned for viruses whenever the message was sent from an unknown system.”
		$q\to p$
	(b) “The message was sent from an unknown system but it was not scanned for viruses.” 
		$q\land\neg p$
	(c) “It is necessary to scan the message for viruses whenever it was sent from an unknown system.” 
		$q\to p$
	(d) “When a message is not sent from an unknown system it is not scanned for viruses.”
		$\neg q\to\neg p$
### Question 9
Are these system specifications consistent? “The system is in multiuser state if and only if it is operating normally. If the system is operating normally, the kernel is
functioning. The kernel is not functioning or the system is in interrupt mode. If the system is not in multiuser state, then it is in interrupt mode. The system is not in interrupt mode.”
	$p$ : System is in multiuser state
	$q$ : System is operating normally
	$r$ : Kernel is functioning 
	$q$ : System is in interrupt mode
	Specifications:
	$p\leftrightarrow q$ 
	$q\to r$
	$\neg r\lor q$
	$\neg p\to q$
	$\neg q$

| p   | q   | r   | $\neg q$ | $p\leftrightarrow q$ | $q\to r$ | $\neg r\lor q$ | $\neg p\to q$ |
| --- | --- | --- | -------- | -------------------- | -------- | -------------- | ------------- |
| T   | T   | T   | F        | T                    | T        | T              | T             |
| T   | T   | F   | F        | T                    | T        | T              | T             |
| T   | F   | T   | T        | F                    | T        | F              | T             |
| T   | F   | F   | T        | F                    | T        | T              | T             |
| F   | T   | T   | F        | F                    | F        | T              | T             |
| F   | T   | F   | F        | F                    | F        | T              | T             |
| F   | F   | T   | T        | T                    | T        | F              | F             |
| F   | F   | F   | T        | T                    | T        | T              | F             |
There is no scenario where $p\leftrightarrow q$, $q\to r$, $\neg r\lor q$, $\neg p\to q$ and $\neg q$ are true at the same time, $\therefore$ Not consistent
### Question 10
Are these system specifications consistent? “Whenever the system software is being upgraded, users cannot access the file system. If users can access the file system, then they can save new files. If users cannot save new files, then the system software is not being upgraded.”
	$p$ : system software is being upgraded
	$q$ : users can access the file system
	$r$ : users can save new files
	Specifications:
	$p\to\neg q$
	$\neg q\lor r$
	$r\lor\neg p$

| p   | q   | r   | $p\to\neg q$ | $\neg q\lor r$ | $r\lor\neg p$ |
| --- | --- | --- | ------------ | -------------- | ------------- |
| T   | T   | T   | F            | T              | T             |
| T   | T   | F   | F            | F              | F             |
| T   | F   | T   | T            | T              | T             |
| T   | F   | F   | T            | T              | F             |
| F   | T   | T   | T            | T              | T             |
| F   | T   | F   | T            | F              | T             |
| F   | F   | T   | T            | T              | T             |
| F   | F   | F   | T            | T              | T             |
There exists a scenario where $p\to\neg q$,$\neg q\lor r$ and $r\lor\neg p$ are true at the same time
$\therefore$ Consistent
### Question 12
Are these system specifications consistent? “If the file system is not locked, then new messages will be queued. If the file system is not locked, then the system is functioning normally, and conversely. If new messages are not queued, then they will be sent to the message buffer. If the file system is not locked, then new messages will be sent to the message buffer. New messages will not be sent to the message buffer.”
	$p$ : The file system is locked
	$q$ : New messages will be queued
	$r$ : System is functioning normally
	$s$ : Messages will be sent to the message buffer
	Specifications
	$\neg p\to q$
	$\neg p\leftrightarrow r$
	$\neg q\to s$
	$\neg p\to s$
	$\neg s$

| p   | q   | r   | s   | $\neg s$ | $\neg p\to q$ | $\neg p\leftrightarrow r$ | $\neg q\to s$ | $\neg p\to s$ |
| --- | --- | --- | --- | -------- | ------------- | ------------------------- | ------------- | ------------- |
| T   | T   | T   | T   | F        | T             | F                         | T             | T             |
| T   | T   | T   | F   | T        | T             | F                         | T             | T             |
| T   | T   | F   | T   | F        | T             | T                         | T             | T             |
| T   | T   | F   | F   | T        | T             | T                         | T             | T             |
| T   | F   | T   | T   | F        | T             | F                         | T             | T             |
| T   | F   | T   | F   | T        | T             | F                         | F             | T             |
| T   | F   | F   | T   | F        | T             | T                         | T             | T             |
| T   | F   | F   | F   | T        | T             | T                         | F             | T             |
| F   | T   | T   | T   | F        | T             | T                         | T             | T             |
| F   | T   | T   | F   | T        | T             | T                         | T             | F             |
| F   | T   | F   | T   | F        | T             | F                         | T             | T             |
| F   | T   | F   | F   | T        | T             | F                         | T             | F             |
| F   | F   | T   | T   | F        | F             | T                         | T             | T             |
| F   | F   | T   | F   | T        | F             | T                         | F             | T             |
| F   | F   | F   | T   | F        | F             | F                         | T             | F             |
| F   | F   | F   | F   | T        | F             | F                         | F             | F             |
$\therefore$ There exists a scenario where $\neg p\to q$,$\neg p\leftrightarrow r$,$\neg q\to s$,$\neg p\to s$ and $\neg s$ are True
# Section 1.3
### Question 10
Show that each of these conditional statements is a tautology by using truth tables. 
	a) $[\neg p\land(p\lor q)]\to q$

| $p$ | $q$ | $(p\lor q)$ | $\neg p\land(p\lor q)$ | $[\neg p\land(p\lor q)]\to q$ |
| --- | --- | ----------- | ---------------------- | ----------------------------- |
| T   | T   | T           | F                      | T                             |
| T   | F   | T           | F                      | T                             |
| F   | T   | T           | T                      | T                             |
| F   | F   | F           | F                      | T                             |
	b) $[(p → q) ∧ (q → r)] → (p → r)$ 
	
| $p$ | $q$ | $r$ | (p → q) | (q → r) | (p → r) | (p → q) ∧ (q → r) | $[(p → q) ∧ (q → r)] → (p → r)$ |
| --- | --- | --- | ------- | ------- | ------- | ----------------- | ------------------------------- |
| T   | T   | T   | T       | T       | T       | T                 | T                               |
| T   | T   | F   | T       | F       | F       | F                 | T                               |
| T   | F   | T   | F       | T       | T       | F                 | T                               |
| T   | F   | F   | F       | T       | F       | F                 | T                               |
| F   | T   | T   | T       | T       | T       | T                 | T                               |
| F   | T   | F   | T       | F       | T       | F                 | T                               |
| F   | F   | T   | T       | T       | T       | T                 | T                               |
| F   | F   | F   | T       | T       | T       | T                 | T                               |
	c) $[p ∧ (p → q)] → q$

| $p$ | $q$ | $(p → q)$ | $p ∧ (p → q)$ | $[p ∧ (p → q)] → q$ |
| --- | --- | --------- | ------------- | ------------------- |
| T   | T   | T         | T             | T                   |
| T   | F   | F         | F             | T                   |
| F   | T   | T         | F             | T                   |
| F   | F   | T         | F             | T                   |
	d) $[(p ∨ q) ∧ (p → r) ∧ (q → r)] → r$

| $p$ | $q$ | $r$ | $(p ∨ q)$ | $(p → r)$ | $(q → r)$ | $[(p ∨ q) ∧ (p → r) ∧ (q → r)]$ | $[(p ∨ q) ∧ (p → r) ∧ (q → r)] → r$ |
| --- | --- | --- | --------- | --------- | --------- | ------------------------------- | ----------------------------------- |
| T   | T   | T   | T         | T         | T         | T                               | T                                   |
| T   | T   | F   | T         | F         | F         | F                               | T                                   |
| T   | F   | T   | T         | T         | T         | T                               | T                                   |
| T   | F   | F   | T         | F         | T         | F                               | T                                   |
| F   | T   | T   | T         | T         | T         | T                               | T                                   |
| F   | T   | F   | T         | T         | F         | F                               | T                                   |
| F   | F   | T   | F         | T         | T         | F                               | T                                   |
| F   | F   | F   | F         | T         | T         | F                               | T                                   |
### Question 14
Determine whether $(¬p ∧ (p → q)) → ¬q$ is a tautology.

| $p$ | $q$ | $(p → q)$ | $(¬p ∧ (p → q))$ | $(¬p ∧ (p → q)) → ¬q$ |
| --- | --- | --------- | ---------------- | --------------------- |
| T   | T   | T         | F                | T                     |
| T   | F   | F         | F                | T                     |
| F   | T   | T         | T                | F                     |
| F   | F   | T         | T                | T                     |
$\therefore$Not a tautology
### Question 25
Show that $(p → r) ∨ (q → r)$ and $(p ∧ q) → r$ are logically equivalent

| p   | q   | r   | $(p ∧ q) → r$ | $(p → r) ∨ (q → r)$ |
| --- | --- | --- | ------------- | ------------------- |
| T   | T   | T   | T             | T                   |
| T   | T   | F   | F             | F                   |
| T   | F   | T   | T             | T                   |
| T   | F   | F   | T             | T                   |
| F   | T   | T   | T             | T                   |
| F   | T   | F   | T             | T                   |
| F   | F   | T   | T             | T                   |
| F   | F   | F   | T             | T                   |
# Section 1.4
### Question 6
Let N(x) be the statement “x has visited North Dakota,” where the domain consists of the students in your school. Express each of these quantifications in English. 
	a) $∃xN(x)$ 
		There exists a student in my school who has visited North Dakota
	b) $∀xN(x)$
		Every student in my school has visited North Dakota
	c) $¬∃xN(x)$ 
		There does not exist a student in my school who has visited North Dakota
	d) $∃x¬N(x)$ 
		There exists a student in my school who has not visited North Dakota
	e) $¬∀xN(x)$ 
		It is not the case that every student in my school has visited North Dakota
	f ) $∀x¬N(x)$
		Every student in my school has not visited North Dakota
### Question 10
Let C(x) be the statement “x has a cat,” let D(x) be the statement “x has a dog,” and let F (x) be the statement “x has a ferret.” Express each of these statements in terms of C(x), D(x), F (x), quantifiers, and logical connectives. Let the domain consist of all students in your class. 
	a) A student in your class has a cat, a dog, and a ferret.
		$\exists x(C(x)\land D(x)\land F(x))$ 
	b) All students in your class have a cat, a dog, or a ferret. 
		$\forall x(C(x)\lor D(x)\lor F(x))$
	c) Some student in your class has a cat and a ferret, but not a dog. 
		$\exists x(C(x)\land F(x)\land\neg D(x))$
	d) No student in your class has a cat, a dog, and a ferret. 
		$\neg\exists x(C(x)\land D(x)\land F(x))$
	e) For each of the three animals, cats, dogs, and ferrets, there is a student in your class who has this animal as a pet.
		$(\exists xC(x))\lor (\exists xD(x))\lor(\exists xF(x))$
### Question 16
Determine the truth value of each of these statements if the domain of each variable consists of all real numbers. 
	a) $∃x(x^2 = 2)$ 
		True
	b) $∃x(x^2 = −1)$
		False 
	c) $∀x(x^2 + 2 ≥ 1)$ 
		False
	d) $∀x(x^2 = x)$
		False
### Question 20
Suppose that the domain of the propositional function P (x) consists of −5, −3, −1, 1, 3, and 5. Express these statements without using quantifiers, instead using only negations, disjunctions, and conjunctions. 
	a) $∃xP (x)$ 
		$P(-5)\lor P(-3)\lor P(-1)\lor P(1)\lor P(3)\lor P(3)\lor P(5)$
	b) $∀xP (x)$
		$P(-5)\land P(-3)\land P(-1)\land P(1)\land P(3)\land P(3)\land P(5)$
	c) $∀x((x \neq 1) → P (x))$ 
		$P(-5)\land P(-3)\land P(-1)\land P(3)\land P(5)$
	d) $∃x((x ≥ 0) ∧ P (x))$ 
		$P(1)\lor P(3)\lor P(5)$
	e) $∃x(¬P (x)) ∧ ∀x((x < 0) → P (x))$
		$(\neg P(-5)\lor \neg P(-3)\lor \neg P(-1)\lor\neg P(1)\lor\neg P(3)\lor\neg P(5))\land(P(-5)\land P(-3)\land P(-1))$
### Question 24
Translate in two ways each of these statements into logical expressions using predicates, quantifiers, and logical connectives. First, let the domain consist of the students in your class and second, let it consist of all people. 
	a) Everyone in your class has a cellular phone. 
		$C(x): x$ has a cellular phone
		$\forall xC(x$) 
	b) Somebody in your class has seen a foreign movie. 
		$F(x) : x$ has seen a foreign movie
		$\exists xF(x)$ 
	c) There is a person in your class who cannot swim. 
		$S(x):x$ can swim
		$\exists x\neg S(x)$
	d) All students in your class can solve quadratic equations. 
		$Q(x):x$ can solve quadratic equations
		$\forall xQ(x)$
	e) Some student in your class does not want to be rich
		$R(x):x$ wants to be rich
		$\exists x\neg R(x)$
### Question 28
Translate each of these statements into logical expressions using predicates, quantifiers, and logical connectives. 
	$Q(x) : x$ is in excellent condition
	$P(x):x$ is in the correct place
	a) Something is not in the correct place. 
		$\exists xP(x)$
	b) All tools are in the correct place and are in excellent condition. 
		$\forall x(P(x)\land Q(x))$
	c) Everything is in the correct place and in excellent condition. 
		$\forall x(P(x)\land Q(x))$
	d) Nothing is in the correct place and is in excellent condition. 
		$\neg\forall x(P(x)\land Q(x))$
	e) One of your tools is not in the correct place, but it is in excellent condition
		$\exists x(\neg P(x)\land Q(x))$
### Question 32
 Express each of these statements using quantifiers. Then form the negation of the statement so that no negation is to the left of a quantifier. Next, express the negation in simple English. (Do not simply use the phrase “It is not the case that.”) 
	 a) All dogs have fleas. 
		 $D(x):x$ is a dog
		 $F(x):x$ has fleas.
		 $\neg\forall x(D(x)\to F(x)\equiv\exists x(D(x)\land\neg F(x))$
		 `There exists a horse which does not have fleas`
	 b) There is a horse that can add.
		 $H(x) : x$ is a horse
		 $A(x):x$ can add. 
		 $\neg\exists x(H(x)\land A(x))\equiv\forall x(H(x)\to\neg A(x))$
		 `All horses are incapable of adding`
	 c) Every koala can climb. 
		 $K(x): x$ is a Koala
		 $C(x):x$ can climb
		 $\neg\forall x(K(x)\to C(x)))\equiv\exists x(K(x)\land\neg C(x))$
		 `There exists a koala who cannot climb`
	 d) No monkey can speak French. 
		 $M(x):x$ is a monkey
		 $F(x):x$ can speak french
		 $\neg(\neg\forall x(M(x)\to F(x)))\equiv\forall x(M(x)\to F(x))$
		 `All monkeys can speak French`
	 e) There exists a pig that can swim and catch fish
		 $P(x):x$ is a pig
		 $S(x):x$ can swim
		 $F(x):x$ can catch fish
		 $\neg\exists x(P(x)\land S(x)\land F(x)\equiv\forall x(P(x)\to(\neg S(x)\lor \neg F(x))$
		 `All pigs cannot swim or catch fish`
# Section 1.5
### Question 3
Let Q(x, y) be the statement “x has sent an e-mail message to y,” where the domain for both x and y consists of all students in your class. Express each of these quantifications in English. 
	a) $∃x∃yQ(x, y)$
		There exists a student in your class who has sent an email to another student in your class
	b) $∃x∀yQ(x, y)$
		There exists a student in your class who has sent an email to every student in your class
	c) $∀x∃yQ(x, y)$ 
		Every student in your class has sent an email to another student in your class
	d) $∃y∀xQ(x, y)$ 
		There exists a student in your class who has received an email from all students in your class
	e) $∀y∃xQ(x, y)$
		All students in your class have received an email from a student in your class 
	f ) $∀x∀yQ(x, y)$
		All students in your class have sent to email to every student in your class
### Question 4
Let P (x, y) be the statement “Student x has taken class y,” where the domain for x consists of all students in your class and for y consists of all computer science courses at your school. Express each of these quantifications in English. 
	a) $∃x∃yP (x, y)$ 
		There exists a student in your class who has taken a computer science course at your school
	b) $∃x∀yP (x, y)$ 
		There exists a student in your class who has taken every computer science course at your school
	c) $∀x∃yP (x, y)$ 
		Every student in your class has taken a computer science course at your school
	d) $∃y∀xP (x, y)$ 
		There exists a computer science course at your school which has been taken by every student in your class
	e) $∀y∃xP (x, y)$ 
		All computer science courses at your school has been taken by a student in your class
	f) $∀x∀yP (x, y)$
		All computer science courses at your school has been taken by every student in your class
### Question 6
Let C(x, y) mean that student x is enrolled in class y, where the domain for x consists of all students in your school and the domain for y consists of all classes being given at your school. Express each of these statements by a simple English sentence. 
	a) $C(Randy Goldberg, CS 252)$ 
		Randy Goldberg is enrolled in CS 252
	b) $∃xC(x, Math 695)$ 
		There exists a student in your school who is enrolled in Math695
	c) $∃yC(Carol Sitea, y)$
		Carol Sitea is enrolled in a course at your school 
	d) $∃x(C(x, Math 222) ∧ C(x, CS 252))$ 
		There is a student who is enrolled at Math 222 and CS 252
	e) $∃x∃y∀z((x \neq y) ∧ (C(x, z) → C(y, z)))$
		 There are atleast two seperate students such that if one of them has enrolled in classes then the other one is also enrolled in all classes
	f) $∃x∃y∀z((x \neq y) ∧ (C(x, z) ↔ C(y, z)))$
		There exists atleast two seperate students such that if and only if one of them is enrolled in all the classes , the other student is also enrolled in all the classes
### Question 16
A discrete mathematics class contains 1 mathematics major who is a freshman, 12 mathematics majors who are sophomores, 15 computer science majors who are sophomores, 2 mathematics majors who are juniors, 2 computer science majors who are juniors, and 1 computer science major who is a senior. Express each of these statements in terms of quantifiers and then determine its truth value. 
	$P(x,y,m) : x$ is a student in $y$ year with a major in $m$ 
	 a) There is a student in the class who is a junior. 
		 $\exists x\exists mP(x,junior,m)\equiv T$  
	 b) Every student in the class is a computer science major. 
		 $\forall x\exists yP(x,y,Computer\;Science)\equiv F$
	 c) There is a student in the class who is neither a mathematics major nor a junior. 
		 $\exists x\exists y\exists m (P(x,y,m)\land (y\neq junior)\land(m\neq mathematics))\equiv T$
	 d) Every student in the class is either a sophomore or a computer science major. 
		 $\forall x(\exists mP(x,sophomore,m)\lor\exists cP(x,c,computer\;science))\equiv$ F
	 e) There is a major such that there is a student in the class in every year of study with that major
		 $\exists m\forall y\exists xP(x,y,m)\equiv F$
# Section 1.6
15, 23, 24, 31
### Question 3
What rule of inference is used in each of these arguments? 
	a) Alice is a mathematics major. Therefore, Alice is either a mathematics major or a computer science major. 
		Addition
	b) Jerry is a mathematics major and a computer science major. Therefore, Jerry is a mathematics major.
		Simplification 
	c) If it is rainy, then the pool will be closed. It is rainy. Therefore, the pool is closed. 
		Modus ponens
	d) If it snows today, the university will close. The university is not closed today. Therefore, it did not snow today. 
		Modus tollens
	e) If I go swimming, then I will stay in the sun too long. If I stay in the sun too long, then I will sunburn. Therefore, if I go swimming, then I will sunburn
		Hypothetical syllogism
### Question 4
 What rule of inference is used in each of these arguments? 
	 a) Kangaroos live in Australia and are marsupials. Therefore, kangaroos are marsupials. 
		Simplification
	 b) It is either hotter than 100 degrees today or the pollution is dangerous. It is less than 100 degrees outside today. Therefore, the pollution is dangerous.
		Disjunctive syllogism
	 c) Linda is an excellent swimmer. If Linda is an excellent swimmer, then she can work as a lifeguard. Therefore, Linda can work as a lifeguard. 
		 Modus ponens
	 d) Steve will work at a computer company this summer. Therefore, this summer Steve will work at a computer company or he will be a beach bum
		Conjunction
### Question 5
 Use rules of inference to show that the hypotheses “Randy works hard,” “If Randy works hard, then he is a dull boy,” and “If Randy is a dull boy, then he will not get the job” imply the conclusion “Randy will not get the job.”
	$p:$ Randy works hard
	$q:$ Randy is a dull boy
	$r:$ Randy will get the job
	1.$p$
	2.$p\to q$
	3.$q\to\neg r$
	4.$q$ \[Modus ponens between 1,2]
	5.$\neg r$ \[Modus ponens between 3,4]
### Question 6
 Use rules of inference to show that the hypotheses “If it does not rain or if it is not foggy, then the sailing race will be held and the lifesaving demonstration will go on,” “If the sailing race is held, then the trophy will be awarded,” and “The trophy was not awarded” imply the conclusion “It rained
	 $p:$ It rained
	 $q:$ It is foggy
	 $r:$ The sailing race will be held
	 $s:$ The life saving demonstration will go on
	 $t:$ The trophy will be awarded
	 1. $(\neg p\lor\neg q)\to (r\land s)$ \[Premise]
	 2. $r\to t$ \[Premise]
	 3. $\neg t$  \[Premise]
	 4. $\neg r$ \[Modus tollens 2,3]
	 5. $\neg r\lor\neg s$ \[Addition of 4]
	 6. $\neg(r\land s)$ \[Logical equivalence of 5 using De Morgans Law]
	 7. $\neg(\neg p\lor\neg q)$ \[Modus tollens 1,6]
	 8. $(p\land q)$ \[Logical equivalence of 7 using De Morgans Law]
	 9. $\therefore p$ \[Simplification of 8]
	 Conclusion : It rained
### Question 9
 For each of these collections of premises, what relevant conclusion or conclusions can be drawn? Explain the rules of inference used to obtain each conclusion from the premises. 
	 b) “If I eat spicy foods, then I have strange dreams.” “I have strange dreams if there is thunder while I sleep.” “I did not have strange dreams.” 
		 $p:$ I eat spicy foods
		 $q:$ I have strange dreams
		 $r:$ There is thunder while i sleep
		 1. $p\to q$
		 2. $r\to q$
		 3. $\neg q$
		 4. $\neg r$ \[Modus tollens between 2,3]
		 5. $\neg p$ \[Modus tollens between 1,3]
		 $\therefore \neg r\land\neg p$ \[Conjunction of 4,5]
		 `I did not eat spicy foods and there was no thunder while i slept`
	 c) “I am either clever or lucky.” “I am not lucky.” “If I am lucky, then I will win the lottery.” 
		 $p:$ I am clever
		 $q:$ I am lucky
		 $r:$ I will win the lottery
		 1. $p\lor q$
		 2. $\neg q$
		 3. $q\to r$
		 4. $p$ \[Dysjunctive syllogism 1,2]
		 `I am clever`
	 d) “Every computer science major has a personal computer.” “Ralph does not have a personal computer.” “Ann has a personal computer.” 
		 
	 e) “What is good for corporations is good for the United States.” “What is good for the United States is good for you.” “What is good for corporations is for you to buy lots of stuff.” 
	 f ) “All rodents gnaw their food.” “Mice are rodents.” “Rabbits do not gnaw their food.” “Bats are not rodents.”
### Question 16
### Question 23
### Question 24
### Question 30