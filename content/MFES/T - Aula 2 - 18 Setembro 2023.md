# Conteúdo
1. [[T - Aula 2 - 18 Setembro 2023#1. Intro|Intro]]
	1. [[T - Aula 2 - 18 Setembro 2023#1.1 SAT|SAT]]
	2. [[T - Aula 2 - 18 Setembro 2023#1.2 Proposicional Logic (PL)|Lógica Proposicional]]
3. [[T - Aula 2 - 18 Setembro 2023#SAT Solvers|SAT Solvers]]

# 1. Intro
*Formal modeling* - formally represent the system and its properties in the syntactic conventions that the tool understands and can process. 

Formal Logic = logical language (logical symbols + non-logical symbols) + semantics +proof system

### 1.1 SAT
<iframe title="Boolean Satisfiability Problem - Intro to Theoretical Computer Science" src="https://www.youtube.com/embed/uAdVzz1hKYY?feature=oembed" height="113" width="200" allowfullscreen="" allow="fullscreen" style="aspect-ratio: 1.76991 / 1; width: 100%; height: 100%;"></iframe>

The Boolean satisfiability (SAT) problem:

Find an assignment to the propositional variables of the formula such that the formula evaluates to TRUE, or prove that no such assignment exists.

  
- SAT is an NP-complete decision problem.
	- SAT was the first problem to be shown NP-complete.
	- There are no known polynomial time algorithms for SAT.


Usually SAT solvers deal with formulas in conjunctive normal form (CNF)
- **literal**: propositional variable or its negation A, ¬A, B, ¬B, C, ¬C
- **clause**: disjuntion of literals. (A _ ¬B _ C)
- **conjunctive normal form**: conjuction of clauses. (A _ ¬B _ C) ^ (B _ ¬A) ^ ¬C

> [!info]+ Cook's theorem(1971)
> SAT is NP-complete


## 1.2 Proposicional Logic (PL)

>[!note] Nota
>Esta secção basicamente só contém revisão de conceitos. Aconselha-se a ver a coisa rapidamente, porque é só a formalidade de lógica escrita por extenso.

Let $A$ be an assignment and let $F$ be a formula. If $A(F) = 1$, then we say **$F$ holds under assignment**, or **$A$ models $F$.**
We write A $\models F$ iff $A(F)=1$, and $A \not \models F$ iff $A(F) = 0$.


An assignment is a function $A$ : $V_{prop} \implies {0,1}$  , that assigns to every
propositional variable a truth value. An assignment $A$ naturally extends to all formulas, $A$ : **Form** $\implies {0,1}$. The truth value of a formula is computed using **truth tables**:

| F         | $A$ | $B$ | $\neg A$ | $A \land B$ | $A \lor B$ | $A \implies B$ | $A \iff B$ | $\bot$ | $\top$ |
| --------- | --- | --- | -------- | ----------- | ---------- | -------------- | ---------- | ------ | ------ |
| $A_1 (F)$ | 0   | 1   | 1   |      0      |     1       |       1         |    0        |  0      |   1     |
| $A_2 (F)$ | 0   | 0   | 1   |      0      |     0       |       1         |    1        |  0      |   1     |
| $A_3 (F)$ | 1   | 1   | 0   |      1      |     1       |       1         |    1        |  0      |   1     |
| $A_4 (F)$ | 1   | 0   | 0   |      0      |     1       |       0         |    0        |  0      |   1     |



A formula $F$ is:
1. **valid**  iff it holds under every assignment. We write $\models F$. A valid formula is called a *tautology*.
2. **satisfiable** iff it folds (true) under some assignment.
3. **unsatisfiable** iff it holds under no assignment. An unsatisfiable formula is called a *contradiction*.
4. **refutable** iff it is not valid.

   > [!tip]+ Proposition
   >  $F$ is **valid** iff $\neg F$ is **unsatisfiable**.
   

- $F \models G$ iff for every assignment $A$, if $A \models F$ then $A \models G$. We say $G$ is a **consequence** of $F$.
- $F \equiv G$ iff $F \models G$ and $G \models F$. We say $F$ and $G$ are **equivalent**.
- Let $\Gamma = { F_1, F_2, F_3,... }$ be a set of formulas.
	- $A \models \Gamma$ iff $A \models F_i$ for each formula $F_i$ in $\Gamma$. We say $A$ models $\Gamma$.
	- $\Gamma \models G$ iff $A \models \Gamma$ implies $A \models G$ for every assignment $A$. We say $G$ is a **consequence** of $\Gamma$.

   > [!tip]+ Proposition
   >  - $F \models G$ iff $\models F \implies G$.
   >  - $\Gamma \models G$ and $\Gamma$ finite iff $\models \land \Gamma \implies G$.
   >  

	 - $\Gamma$ is *consistent* or *satisfiable* iff there is an assignment that models $\Gamma$.
	 - We say that $\Gamma$ is inconsistent or unsatisfiable iff there is not consistent and denote this by $\Gamma \models \bot$.

   > [!tip]+ Proposition
   >  - {$F, \neg F$} $\models \bot$
   >  - If $\Gamma \models \bot$ and $\Gamma \subseteq \Gamma '$, then $\Gamma ' \models \bot$
   >  - $\Gamma \models F$ iff $\Gamma, \neg F \models \bot$

- Formula $G$ is a subformula of formula F if it occurs syntactically within F
- Formula G is a strict subformula of F if G is a subformula of $F$ and $G \neg = F$


**Basic Equivalences:**
1. $\neg \neg A \equiv A$
2. $A \lor A \equiv A$
3. $A \land A \equiv A$
4. $A \land \neg A \equiv \bot$
5. $A \lor \neg A \equiv \top$
6. $A \lor B \equiv B \lor A$
7. $A \land B \equiv B \land A$
8. $A \land \top \equiv A$
9. $A \lor \top \equiv \top$
10. $A \land \bot \equiv \bot$
11. $A \lor \bot \equiv A$
12. $A \land (B \lor A) \equiv A$
13. $A \land (B \lor C) \equiv (A \land B) \lor (A \land C)$
14. $A \lor (B \land C) \equiv (A \lor B) \land (A \lor C)$
15. $\neg (A \lor B) \equiv \neg A \land \neg B$
16. $\neg (A \land B) \equiv \neg A \lor \neg B$
17. $A \implies B \equiv \neg A \lor B$
18. $A \iff B \equiv (A \implies B) \land (B \implies A)$




# 2. SAT Solvers
- There are several techniques and algorithms for SAT solving.
- Usually SAT solvers receive as input a formula in a specific syntatical format.
- SAT solvers deal with formulas in **conjunctive normal form (CNF)**.

- Most current state-of-the-art SAT solvers are based on the **Davis-Putnam-Logemann-Loveland (DPLL) framework**.

## 2.1 DPLL Framework
The idea is to **incrementally construct an assignment compatible with a CNF**, propagating the implications of the decisions made that are easy to detect and simplifying the clauses.

A CNF is satisfied by an assignment if all its clauses are satisfied. And a clause is satisfied if at least one of its literals is satisfied.
