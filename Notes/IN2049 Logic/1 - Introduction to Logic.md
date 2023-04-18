----

## Basic Terms and Background

> **Logic**: subject of identifying true statements in a language of which you only know a few words

- necessary words: if, and, or.... what words do we need to define math?
- application: description logic

> **Logic**: ==science of inferences== → which inferences are correct?

> **Inference**: statements of form 'if A is true, then B is true', where A is *hypothesis*, B is *conclusion*

example of a correct inference:
```
if 
	all men are mortal and Socrates is a man 
then 
	Socrates is mortal
```

NOTE:  ``if A then B``  being correct does not imply  ``A``  being correct. we only know that if the inference is correct **and** A is true, then B is true
(colloquially, if A then B can also mean you believe A to be true apparently)

example of an incorrect inference:
```
if
	some women are tall and all mothers are women
then
	some mothers are tall
```
%%naturalistischer Fehlschluss?%%

inferences might require additional knowledge:
```
if
	Anne has a gradchild
then
	Anne is a mother
```


#### Definition: Logical Inferences

non-standard definition:
> **Logical inference**: inference with variables

key point: logical inference is correct if all its instances are correct
> meaning the inference is **valid** or a **tautology**

examples of valid tautologies:
- $((A \land B) \land (B \rightarrow C)) \rightarrow A \land C$ 

NOTE: correct != valid


#### Logic Facts

- basis of mathematical proof
	- people used to do it very hand-wave-ily but then needed a more solid framework for math

**Different kinds of logic**:
- different language fragments
- **propositional**: and, or, not, if..then
	- if X and Y then Y 
	- variables are statements
- **syllogistic**: all, some, none
	- if all A are B and no B is a C then no A is a C
	- variables are objects
- **temporal**: propositional + today, tomorrow, sometime, never

Bertrand Russell: "...the subject in which we never know what we are talking about, nor whether what we are saying is true"

also: ChatGPT can be tricked into logical fallacies


## History of Logic

[Wikipedia article](https://en.wikipedia.org/wiki/Mathematical_logic#History)

#### Aristotle and Syllogisms

**Aristotle**: the founder of logic → systematic study of syllogisms
(books are student's notes, not actual books - here is an [excerpt](https://www.csus.edu/indiv/e/eppersonm/hist104a/documents/aristotle%20-%20selections_prioranalytics.pdf))

> Syllogisms: discourse in which, certain things being stated...

3 valid syllogisms:
- all P are M and all M are S → all P are S
- no P is M and all M are S → no P is S
- all M are ...

##### Limitations
- many valid deductions are not syllogisms
- no calculus for long chains of deductions

#### Boole and Propositional Logic
(2000 year jump lmao)

- atomic propositions: can be TRUE or FALSE
- operators are used to link propositions: $\land, \lor, \neg, \dots$
- no quantification

given 2 propositions, there are 4 possible situations/worlds
- in that context, **B is a consequence of A** means B is true in all worlds in which A is true
- tautologies are true in all worlds

#### Predicate Logic
Frege, Peano, Russell

- proofs were still being conducted using natural language
- logic was needed as a formal tool for avoiding contradictions

use of predicate logic:
- relations between entities
- formulate **existential** and **universal** statements


## Logic in Computer Science

- **Shannon** proposed using propositional logic to describe and optimize electromechanical circuits
- **Newell, SImon, Robinson** developed first systems for mechanization of logcial deduction

##### Applications
- circuit design
- models and specifications
- verification
- databases
- AI
- logic programming

Dijkstra: "informatics = Very Large Scale Application of Logics"

Gottlob: "Computer science is the continuation of logic by other means"
- Klausewitz: prussian war theoretician: "War is the continuation of diplomacy by other means"
