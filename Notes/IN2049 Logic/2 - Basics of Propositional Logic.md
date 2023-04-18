----
slides 1-24

----

## Syntax of Propositional Logic

##### Formulas
**atomic fomulas** or **atoms**: $A_i,\> i=1,2,3,\dots$
inductive definition of other formulas:
- $\bot$ and $\top$ are formulas
- atomic formulas are formulas
- for all formulas $F$, $\neg F$ is a formula
- for all fomulas $F, G$, $(F \circ G)$ is a formula where $\circ \in \{\land, \lor, \rightarrow, \leftrightarrow\}$

##### Operators
| operator          | name           |
| ----------------- | -------------- |
| $\neg$            | negation       |
| $\land$           | conjugation    |
| $\lor$            | disjunction    |
| $\rightarrow$     | implication    |
| $\leftrightarrow$ | bi-implication |

##### Operator Precedence
in decreasing order:
> $\neg \quad \land \quad \lor \quad \rightarrow \quad \leftrightarrow$

example: instead of $(A \rightarrow (B \land C))$ we can write $A \rightarrow B \land C$

##### Syntax Tree
helps us get subformulas: subformulas correspond to subtrees of the syntax tree

##### Induction on formulas
- base cases
	- prove $\mathcal{P}(\bot)$, $\mathcal{P}(\top)$, $\mathcal{P}(A_i)$
- induction step for $\neg$ 
	- from IH $\mathcal{P}(F)$ prove $\mathcal{P}(\neg F)$
- induction step for all $\circ \in \{\land, \lor, \rightarrow, \leftrightarrow\}$
	- from IHs $\mathcal{P}(F)$ and $\mathcal{P}(G)$ prove $\mathcal{P}(F \circ G)$


## Semantics of Propositional Logic
find the truth values of atoms and formulas

##### Truth values
- elements of $\{0, 1\}$
- **assignment** function $\mathcal{A}: \text{Atoms} \to \{0,1\}$
- $\mathcal{A}$ can be extended to $\hat{\mathcal{A}}: \text{Formulas} \to \{0, 1\}$