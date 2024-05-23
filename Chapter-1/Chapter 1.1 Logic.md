---
id: "1.1"
tags:
  - Book
---

# Logic

- [Propositions](#propositions)
- [Bit Operations](#bit-operations)
- [Logical Equivalence](#logical-equivalence)

- [Exercise with Working](#exercise-1.1.1-answers)

## Propositions

Propositions
: A statement that is either true or false, but not both.

- $1+1=2$ (true)
- $2+2=4$ (false)

### NOT

> Let $p$ be a proposition. The statement "It is not the case
> that $p$" is another proposition, called **negation** of $p$.
> The negation of $p$ is denoted by $\lnot p$ (not $p$).
> If $p$ is true, then $\lnot p$ is false, vice versa

| $p$ | $\lnot p$ |
| --- | --------- |
| T   | F         |
| F   | T         |

### AND

> Let $p$ and $q$ be propositions
> Where "$p$ and $q$" is denoted by $p \land q$ is true if both $p$ and $q$ is true.
>
> $p\land q$ is the conjunction of two proposition

| $p$ | $q$ | $p\land q$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | F          |
| F   | F   | F          |

### OR

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\lor q$ is true if both $p$ and $q$ is false.
>
> $p\lor q$ is the disconjunction of two propositions

| $p$ | $q$ | $p\lor q$ |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | T         |
| F   | T   | T         |
| F   | F   | F         |

### XOR

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\oplus q$ is true if either $p$
> and $q$ is true.
>
> $p\oplus q$ is the exclusive of two propositions

| $p$ | $q$ | $p\oplus q$ |
| --- | --- | ----------- |
| T   | T   | F           |
| T   | F   | T           |
| F   | T   | T           |
| F   | F   | F           |

### Conditional

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\implies q$ is
> true if $p$ is true and $q$ is false.
>
> $p\implies q$ is the implication of two propositions

| $p$ | $q$ | $p\implies q$ |
| --- | --- | ------------- |
| T   | T   | T             |
| T   | F   | F             |
| F   | T   | T             |
| F   | F   | F             |

### Biconditional

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\iff q$ is true if
> both $p$ and $q$ have the same truth values.
>
> $p\iff q$ is the biconditional of two propositions

| $p$ | $q$ | $p\iff q$ |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | F         |
| F   | T   | F         |
| F   | F   | T         |

## Bit-Operations

$\land$ (AND) $\lor$ (OR) $\oplus$ (XOR)

| $\land$ | 0   | 1   |
| ------- | --- | --- |
| 0       | 0   | 1   |
| 1       | 1   | 1   |

| $\lor$ | 0   | 1   |
| ------ | --- | --- |
| 0      | 0   | 0   |
| 1      | 0   | 1   |

| $\oplus$ | 0   | 1   |
| -------- | --- | --- |
| 0        | 0   | 1   |
| 1        | 1   | 0   |

> Comparing 2 bit to find the final bitwise using the tables.

|          | 0   | 1   | 1   | 0   | 1   |     | 1   | 0   | 1   | 1   | 0   |
| -------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|          | 1   | 1   | 0   | 0   | 0   |     | 1   | 1   | 1   | 0   | 1   |
| $\lor$   | 1   | 1   | 1   | 0   | 1   |     | 1   | 1   | 1   | 1   | 1   |
| $\land$  | 0   | 1   | 0   | 0   | 0   |     | 1   | 0   | 1   | 0   | 0   |
| $\oplus$ | 1   | 0   | 1   | 0   | 1   |     | 0   | 1   | 0   | 1   | 1   |

### Examples

> 1. Construct the truth table for the statement form $(p\lor q)\land(p\land q)$, also known as $p\oplus q$.

| $p$ | $q$ | $p\lor q$ | $p\land q$ | $\lnot(p\land q)$ | $(p\lor q)\land \lnot(p\land q)$ |
| --- | --- | --------- | ---------- | ----------------- | -------------------------------- |
| T   | T   | T         | T          | F                 | F                                |
| T   | F   | T         | F          | T                 | T                                |
| F   | T   | T         | F          | T                 | T                                |
| F   | F   | F         | F          | T                 | F                                |

> 2. Construct the truth table for $(p\land q) \lor \lnot r$.

| $p$ | $q$ | $r$ | $p\land q$ | $\lnot r$ | $(p\land q)\lor \lnot r$ |
| --- | --- | --- | ---------- | --------- | ------------------------ |
| T   | T   | T   | T          | F         | T                        |
| T   | T   | F   | T          | T         | T                        |
| T   | F   | T   | F          | F         | F                        |
| T   | F   | F   | F          | T         | T                        |
| F   | T   | T   | F          | F         | F                        |
| F   | T   | F   | F          | T         | T                        |
| F   | F   | T   | F          | F         | F                        |
| F   | F   | F   | F          | T         | T                        |

---

## Logical Equivalence

- The statements below statements are two different way of saying the same thing and they both have the same logical form. In this case we call this **logically equivalent**.
  - 6 is greater than 2
  - 2 is less than 6

Definition
: Two statements forms are called logically equivalent if, and only if, they have identical truth values for rach possible substitution statements for their statement variables. The local equivalent of $P$ and $Q$ is $P\equiv Q$.

| $p$ | $q$ | $p\land q$ | $q \land p$ | $p\equiv q$ |
| --- | --- | ---------- | ----------- | ----------- |
| T   | T   | T          | T           | T           |
| T   | F   | F          | F           | T           |
| F   | T   | F          | F           | T           |
| F   | F   | F          | F           | T           |

> Testing $P\equiv Q$
>
> > 1. Construct truth table to P and Q
> > 2. Check each combination of truth value to see whether they are the same.
> >    - If the truth value of both are the same in each combination, they are logically equivalent.

### Showing Non-equivalence

1. Show that the statement forms $\lnot (p \land q)$ and $\lnot p \land \lnot q$ is not logically equivalent.

| $p$ | $q$ | $\lnot p$ | $\lnot q$ | $p\land q$ | $\lnot (p\land q)$ | $\lnot p \land \lnot q$ |
| --- | --- | --------- | --------- | ---------- | ------------------ | ----------------------- |
| T   | T   | F         | F         | T          | F                  | F                       |
| T   | F   | F         | T         | F          | T                  | F                       |
| F   | T   | T         | F         | F          | T                  | F                       |
| F   | F   | T         | T         | F          | T                  | T                       |

> $\lnot(p\land q)$ and $\lnot p \land\lnot q$ have different truth values in row 2 and 3, so they are not logically equivalent.

### De-Morgans-Law

Definition
: The negation of an _AND_ statement is logically equivalent to the _OR_ statement in which each component is negated.
The negation of an _OR_ statement is logically equivalent to the _and_ statement in which each component is negated.

| $p$ | $q$ | $\lnot p$ | $\lnot q$ | $p\land q$ | $\lnot(p\land q)$ | $\lnot p \lor \lnot q$ |
| --- | --- | --------- | --------- | ---------- | ----------------- | ---------------------- |
| T   | T   | F         | F         | T          | F                 | T                      |
| T   | F   | F         | T         | F          | T                 | T                      |
| F   | T   | T         | F         | F          | T                 | T                      |
| F   | F   | T         | T         | F          | T                 | T                      |

$\lnot(p \land q)$ and $\lnot p \lor \lnot q$ always have
the same truth value, so they are logically equivalent.

$\therefore \lnot (p\land q) \equiv \lnot p \land \lnot q$

---

### Tautology-&-Contradiction

Tautology $t$
: Tautology is a statement that is always true.

Contradiction $c$
: Contradictions are statements is is always false.

| $p$   | $\lnot p$   | $p\lor \lnot p$ | $p\land\lnot p$ |
| ----- | ----------- | --------------- | --------------- |
| T     | F           | T               | F               |
| F     | T           | T               | F               |
| ----- | ----------- | Always True     | Always False    |

---

#### Theorem-1.1.1

- Let propositions be $p,q,r$ and let tautology be $t$ and contradictions be $c$.

1. Commutative Laws

   - $p\land q\equiv q\land p$
   - $p\lor q\equiv q\lor p$

| $p$ | $q$ | $p\land q$ | $q\land p$ |
| --- | --- | ---------- | ---------- |
| T   | T   | T          | T          |
| T   | F   | F          | F          |
| F   | T   | F          | F          |
| F   | F   | F          | F          |

$\therefore p\land q\equiv q\land p$

2. Associative Laws

   - $(p\land q)\land r\equiv p\land (q\land r)$
   - $(p\lor q)\lor r \equiv p\lor (q\lor r)$

| $p\land q$ | $r$ | $q\land r$ | $(p\land q)\land r$ | $p\land (q\land r)$ |
| ---------- | --- | ---------- | ------------------- | ------------------- |
| T          | T   | T          | T                   | T                   |
| T          | F   | F          | F                   | F                   |
| F          | T   | F          | F                   | F                   |
| F          | T   | T          | F                   | F                   |
| F          | F   | F          | F                   | F                   |
| F          | F   | F          | F                   | F                   |
| F          | T   | F          | F                   | F                   |
| F          | F   | F          | F                   | F                   |

$\therefore (p\land q)\land r \equiv p\land (q\land r)$

3. Distributive Laws

   - $p\land(q\lor r)\equiv (p\land q) \lor (p\land r)$
   - $p\lor(q\land r)\equiv (p\lor q)\land (p\lor r)$

| $p\land r$ | $p\land(q\lor r)$ | $(p\land q)\lor (p\land r)$ |
| ---------- | ----------------- | --------------------------- |
| T          | T                 | T                           |
| F          | T                 | T                           |
| T          | T                 | T                           |
| F          | F                 | F                           |
| F          | F                 | F                           |
| F          | F                 | F                           |
| F          | F                 | F                           |
| F          | F                 | F                           |

$\therefore p\land(q\lor r)\equiv (p\land q)\lor (p\land r)$

4. Identity Laws

   - $p\land t\equiv p$
   - $p\lor c \equiv p$

| $p$ | $t$ | $p\land t$ |
| --- | --- | ---------- |
| T   | T   | T          |
| F   | T   | F          |

$\therefore p\land t\equiv p$

| $p$ | $c$ | $p\lor c$ |
| --- | --- | --------- |
| T   | F   | T         |
| F   | F   | F         |

$\therefore p\lor c\equiv p$

5. Negation Laws
   - $p\lor \lnot p \equiv t$
   - $p\land \lnot p \equiv c$

| $p$ | $\lnot p$ | $t$ | $p\lor\lnot p$ |
| --- | --------- | --- | -------------- |
| T   | F         | T   | T              |
| F   | T         | T   | T              |

$\therefore p\lor\lnot p\equiv t$

| $p$ | $\lnot p$ | $c$ | $p\land\lnot p$ |
| --- | --------- | --- | --------------- |
| T   | F         | F   | F               |
| F   | T         | F   | F               |

$\therefore p\land\lnot p\equiv c$

> Using these 5 laws we can then deduce the rest. The first 5 laws is also called the _Axioms for a mathematical structure_ AKA **_Boolean Algebra_**

6. Double Negative Law
   - $\lnot(\lnot p)\equiv p$
7. Idempotent Laws
   - $p\land p \equiv p$
   - $p\lor p \equiv p$
8. Universal bound Laws
   - $p\lor t \equiv t$
   - $p\land c \equiv c$
9. [De Morgan's laws](#de-morgans-law)
   - $\lnot(p\land q)\equiv \lnot p \lor \lnot q$
   - $\lnot(p\lor q)\equiv\lnot p\land \lnot q$
10. Absorption Laws:
    - $p\lor(p\land q)\equiv p$
    - $p\land(p\lor q)\equiv p$
11. Negation of $t$ and $c$:
    - $\lnot t \equiv c$
    - $\lnot c \equiv t$

---

## [Exercise 1.1.1](#Exercise-1.1.1-Answers)

1. Use [Theorem 1.1.1](#theorem-1.1.1) to verify the logical equivalence in the following questions. Supply a reason for each step.

   1. $(p \land \lnot q) \lor p \equiv p$
   2. $p \land (\lnot q \lor p ) \equiv p$
   3. $\lnot (p \lor \lnot q) \lor (\lnot p \land \lnot q) \equiv \lnot p$
   4. $\lnot ((\lnot p \land q) \lor (\lnot p \land \lnot q)) \lor (p \land q) \equiv p$
   5. $(p \land (\lnot (\lnot p \lor q))) \lor (p \land q) \equiv p$

2. Since $p \oplus q \equiv (p \lor q) \land \lnot (p \land q)$.

   1. Find simpler statement forms that are logically equivalent to $p \oplus p$ and $(p \oplus p ) \oplus p$.
   2. Is $(p \oplus q) \oplus r \equiv p \oplus (q \oplus r)$? Justify your answer.
   3. Is $(p \oplus q) \land r \equiv (p \land r) \oplus (q \land r)$? Justify your answer.

<<<<<<< HEAD
---

## Exercise Answers

### Exercise-1.1.1-Answers

1. Use Theorem 1.1.1 to verify the logical equivalence in the following questions. Supply a reason for each step.
   1. $(p \land \lnot q) \lor p \equiv p$
      $$
      \begin{align*}
      Commutative\;Law&\equiv p \lor (p \land \lnot q) \\
      Distributive\;Law &\equiv (p \lor p)\land (p\lor \lnot q)
      \\ Idempotent\;Law &\equiv p \land (p\lor \lnot q)
      \\ Absorption\;Law &\equiv p
      \\ \therefore (p \land \lnot q) \lor p &\equiv p
      \end{align*}
      $$
   2. $p \land (\lnot q \lor p ) \equiv p$
      $$
      \begin{align*}
      Commutative\;Law&\equiv p \land (p \lor \lnot q)
      \\Distributive\;Law&\equiv (p \land p) \lor (p \land \lnot q)
      \\Idempotent\;Law&\equiv p \lor (p \land \lnot q)
      \\ Absorption\;Law&\equiv p
      \\ \therefore p \land (\lnot q \lor p ) &\equiv p
      \end{align*}
      $$
   3. $\lnot (p \lor \lnot q) \lor (\lnot p \land \lnot q) \equiv \lnot p$
      $$
      \begin{align*}
      De\;Morgan's\;Law &\equiv (\lnot p \land \lnot(\lnot q)) \lor (\lnot p \land \lnot q)
      \\Double\;Neative\;Law &\equiv (\lnot p \land q) \lor (\lnot p \land \lnot q)
      \\Distributive\;Law&\equiv \lnot p \land (q \lor \lnot q)
      \\Negation\;Law&\equiv \lnot p \land t
      \\Identity\;Law&\equiv \lnot p
      \\ \therefore \lnot (p \lor \lnot q) \lor (\lnot p \land \lnot q) &\equiv \lnot p
      \end{align*}
      $$
   4. $\lnot ((\lnot p \land q) \lor (\lnot p \land \lnot q)) \lor (p \land q) \equiv p$
      $$
      \begin{align*}
      Distributive\;Law&\equiv \lnot(\lnot p \land (q \lor \lnot q)) \lor (p \land q)
      \\Negation\;law&\equiv \lnot(\lnot p \land t) \lor (p\land q)
      \\Identity\;Law&\equiv \lnot(\lnot p) \lor (p \land q)
      \\Double\;Negative\;Law&\equiv p \lor (p \land q)
      \\Absorption\;Law&\equiv p
      \\ \therefore \lnot ((\lnot p \land q) \lor (\lnot p \land \lnot q)) \lor (p \land q) &\equiv p
      \end{align*}
      $$
   5. $(p \land (\lnot (\lnot p \lor q))) \lor (p \land q) \equiv p$
      $$
      \begin{align*}
      De\;Morgan's\;Law&\equiv (p\land \lnot(\lnot(\lnot p)\land\lnot q))) \lor (p \land q)
      \\Double\;Negative\;Law&\equiv (p \land (\lnot p\land \lnot q)) \lor (p \land q)
      \\Associative\;Law&\equiv ((p \land \lnot p ) \land \lnot q) \lor (p \land q)
      \\Negation\;Law&\equiv (c \land \lnot q) \lor (p \land q)
      \\Universal\;Bound\;Law&\equiv c \lor (p \land q)
      \\????
      \end{align*}
      $$
=======
[Answers](Chapter-1/Answers.md)
>>>>>>> e06bf0d0c8e9dd8024b3ebb9e06edbd709a2db50
