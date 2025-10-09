## Intro
+ Hello everyone, my name is Jingang Zhang, and I'm the one of the TAs for this exercise.
+ Today's exercise will be split up into two parts. 
+ I will cover the first part from Task x.x through Task x.x.
+ XXX will handle the remaining tasks.
+ Ok, Alright, if there are no questions so far, let's get started.

 ## Task 1.1

1. **NAND Gate**:
   * Symbol:...
   * Boolean expression: $\text{Out} = \overline{A \land B}$

2. **XOR Gate**:
   * Output is 1 only if the two inputs are different
   * Truth table:...
   * **DNF: Disjunctive Normal Form**:
     $$\text{Out} = \overline{A}\land B \lor A \land \overline{B}$$
   * Consists of AND gates, OR gates, and NOT gates.
   * Build AND, OR, and NOT gates using NAND gates.

3. **NOT gate using only NAND gates**:
   * Idempotent law: $A = A \land A$
   * Expression: $\text{Out} = \overline{A \land A}$

4. **AND gate using only NAND gates**:
   * Double negation law: $A = \overline{\overline{A}}$
   * $A \land B = \overline{\overline{A \land B}}$
   * Using idempotent law ($A \land A = A$), we get:
     $$A \land B = \overline{\overline{A \land B}} = \overline{\overline{A \land B} \land \overline{A \land B}}$$

5. **OR gate using only NAND gates**:
   * De Morgan’s law: $\overline{A \lor B} = \overline{A} \land \overline{B}$
   * $$A \lor B = \overline{\overline{A \lor B}} = \overline{\overline{A} \land \overline{B}} = \overline{\overline{A \land A} \land \overline{B \land B}}$$

6. **XOR gate using only NAND gates**:
   * $$\text{Out} = \overline{A}\land B \lor A \land \overline{B} \\ = \overline{\overline{\overline{A} \land B \lor A \land \overline{B}}} \\ = \overline{\overline{\overline{A} \land B} \land \overline{A \land \overline{B}}} \\ = \overline{\overline{\overline{A \land A} \land B} \land \overline{A \land \overline{B \land B}}}$$
   * Logic circuit: ...
  
7. **XNOR gate using only NAND gates**:
   * $\text{XNOR} = \overline{\text{XOR}} = \overline{\text{XOR} \land \text{XOR}}$
   * Logic circuit: ...

8. **2-input MUX using only NAND gates**:
   * $\text{Out} = A \land \overline{S} \lor B \land S$
   * Rewritten using NAND gates:
     $$\text{Out} = A \land \overline{S} \lor B \land S \\ = \overline{\overline{A \land \overline{S} \lor B \land S}} \\ = \overline{\overline{A \land \overline{S}} \land \overline{B \land S}} \\ = \overline{\overline{A \land \overline{S \land S}} \land \overline{B \land S}}$$
   * Logic circuit: ...

9. **Boolean Algebra**:
   * **Commutative law**:
     $A \land B = B \land A$, $A \lor B = B \lor A$
   * **Associative law**:
     $A \land (B \land C) = (A \land B) \land C$, $A \lor (B \lor C) = (A \lor B) \lor C$
   * **Distributive law**:
     $A \land (B \lor C) = (A \land B) \lor (A \land C)$, $A \lor (B \land C) = (A \lor B) \land (A \lor C)$
   * **Identity law**:
     $A \lor 0 = A$, $A \land 1 = A$
   * **Idempotent law**:
     $A \lor A = A$, $A \land A = A$
   * **Complement law**:
     $A \lor \bar{A} = 1$, $A \land \bar{A} = 0$
   * **Double negation law**:
     $\overline{\overline{A}} = A$
   * **De Morgan’s law**:
     $\overline{A\land B} = \overline{A} \lor \overline{B}$, $\overline{A \lor B} = \overline{A} \land \overline{B}$
   * **Absorption law**:
     $A \lor (A \land B) = A$, $A \land (A \lor B) = A$

10. **Extension**: Try to design XOR, XNOR, and a 2-to-1 Multiplexer **using only NOR gates**.

## Task 1.2
1. **Rewrite expression**: 
    $$F_1 = AC \lor BC \\ = \overline{\overline{A\land C \lor B\land C}} \\ = \overline{\overline{A \land C} \land \overline{B \land C}} $$
2. **CNF to NDF**: 
    * Distributive law: $$F_2 = (A \lor B)\land(\overline{C} \lor B) \\ = (A \land \overline{C}) \lor B \\ = \overline{\overline{(A \land \overline{C}) \lor B}} \\ = \overline{\overline{A \land \overline{C}} \land \overline{B}} \\ = \overline{\overline{A \land \overline{C \land C}} \land \overline{B \land B}}$$

## Task 1.3

1. Given $F = \overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}$
   * Its complement is:
     $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}}$$

3. If $\overline{F}$ needs to be simplified:

   * Using **De Morgan's law** ($\overline{A \land B} = \overline{A} \lor \overline{B}$):
     $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}} \\ = \overline{\overline{A} \ \overline{B} \ C} \land \overline{\overline{A} \ B \ \overline{C}} \land \overline{A \ B \ \overline{C}} \\ = (\overline{\overline{A}} \lor \overline{\overline{B}} \lor \overline{C}) \land (\overline{\overline{A}} \lor \overline{B} \lor \overline{\overline{C}}) \land (\overline{A} \lor \overline{B} \lor \overline{\overline{C}})$$
   * Using **double negation** ($\overline{\overline{A}} = A$):
     $$\overline{F} = (A \lor B \lor \overline{C}) \land (A \lor \overline{B} \lor C) \land (\overline{A} \lor \overline{B} \lor C)$$
   * Using **distributive law** ($A \lor (B \land C) = (A \lor B) \land (A \lor C)$), **complement law** ($A \land \overline{A} = 0$), and **identity law** ($A \lor 0 = A$):
     $$(A \lor \overline{B} \lor C) \land (\overline{A} \lor \overline{B} \lor C) \\ = ((\overline{B} \lor C) \lor A) \land ((\overline{B} \lor C) \lor \overline{A}) \\ = (\overline{B} \lor C) \lor (A \land \overline{A}) \\ = (\overline{B} \lor C)$$
   * Therefore:
     $$\overline{F} = (A \lor B \lor \overline{C}) \land (\overline{B} \lor C)$$

4. tasks (b) and (c)...

## Task 1.4

1. **RS latch**:
   * Set ($S=1$) and Reset ($R=0$), $Q = 1$
   * Set ($S=0$) and Reset ($R=1$), $Q = 0$
   * Set ($S=0$) and Reset ($R=0$), $Q$ keeps its state
   * Set ($S=1$) and Reset ($R=1$), $Q$ and $\overline{Q} = 0$, metastable state (“don’t care”)

2. **logic automaton graph**: 
  + lists all output states and all possible state transitions, along with the input conditions required for each transition.
  * Four output state combinations:
    $$00 = \overline{Q_1} \ \overline{Q_0}, \quad 01 = \overline{Q_1} \ Q_0, \quad 10 = Q_1 \ \overline{Q_0}, \quad 11 = Q_1 \ Q_0$$

  + Assuming the initial output combination is $00 = \overline{Q_1} \ \overline{Q_0}$:
    * To keep this state unchanged: $\text{SR} = 11$
    * To transition to $11 = Q_1 \ Q_0$: $\text{SR} = 00$ (i.e., $\overline{S} \ \overline{R}$)
    * To transition to $10 = Q_1 \ \overline{Q_0}$: $\text{SR} = 10$ (i.e., $S\overline{R}$)
    * To transition to $01 = \overline{Q_1} \ Q_0$: $\text{SR} = 01$ (i.e., $\overline{S}R$)

  + Others and “condition 1”

3. **reduced switching table**
  + RS latch truth table.
  + $^n{Q}$: **new Q state**, $^a{Q}$ : **old Q state**.


## Task 1.5
1. JK-FF:
  + two 3-input NAND gates and one RS latch.
  + **clk = 0**, **R = 1** and **S = 1**, $^n{Q} =\ ^a{Q}$.
  + **clk** transitions from 0 to 1 (rising edge), the output $^n{Q}$ is determined by the input signals **J** and **K**.
  + In this switching table (excluding **clk**),
    + four input signals: $\overline{^a{Q}},\ ^a{Q},\ J,\ K$
    + two intermediate signals: **R**, **S**
    + two output signals: $^n{Q},\ \overline{^n{Q}}$.
  + The four input signals correspond to 8 possible signal combinations.
  + Each signal combination corresponds to a specific **R-S** combination.
  + Finally, based on **R**, **S**, $\overline{^a{Q}}$, and $^a{Q}$, we can get the outputs $^n{Q}$ and $\overline{^n{Q}}$.

2. The reduced switching table:
   * **JK = 00**, $^n{Q} = ^a{Q}$
   * **JK = 01**, $^n{Q} = 0$
   * **JK = 10**, $^n{Q} = 1$
   * **JK = 11**, $^n{Q} = \overline{^a{Q}}$