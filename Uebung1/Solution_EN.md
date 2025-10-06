## Task 1.1

1. First, let’s understand what a **NAND Gate** is:

   * Its symbol is ...
   * Its Boolean equation is $\text{Out} = \overline{A \cdot B}$ or $\text{Out} = \overline{A \land B}$

2. Next, the **XOR Gate**:

   * In the XOR gate, the output is 1 only if the two inputs are different.
   * From this, we can construct its truth table.
   * Its logical expression (in **DNF: Disjunctive Normal Form**) is:
     $\text{Out} = \overline{A}\cdot B + A \cdot \overline{B}$ or $\text{Out} = \overline{A}\land B \lor A \land \overline{B}$
   * This shows that the XOR gate consists of AND gates, OR gates, and NOT gates.
   * But since we can only use **NAND gate** to build it, we must build AND, OR, and NOT gates using NAND gates.

3. **NOT gate using only NAND gates**:

   * Connect the two inputs of a NAND gate together (Idempotent law).
   * Expression: $\text{Out} = \overline{A \cdot A}$ or $\text{Out} = \overline{A \land A}$

4. **AND gate using only NAND gates** (via double negation law, $A = \overline{\overline{A}}$):

   * $A \land B = \overline{\overline{A \land B}}$
   * Using idempotent law ($A \land A = A$), we get:
     $$A \land B = \overline{\overline{A \land B}} = \overline{\overline{A \land B} \land \overline{A \land B}}$$

5. **OR gate using only NAND gates** (via De Morgan’s law, $\overline{A \lor B} = \overline{A} \land \overline{B}$):

   * $$A \lor B = \overline{\overline{A \lor B}} = \overline{\overline{A} \land \overline{B}} = \overline{\overline{A \land A} \land \overline{B \land B}}$$

6. Thus, for the **XOR gate**, we rewrite its logical expression using only NAND gates:
   $$\text{Out} = \overline{A}\land B \lor A \land \overline{B} \\ = \overline{\overline{\overline{A} \land B \lor A \land \overline{B}}} \\ = \overline{\overline{\overline{A} \land B} \land \overline{A \land \overline{B}}} \\ = \overline{\overline{\overline{A \land A} \land B} \land \overline{A \land \overline{B \land B}}}$$

   The corresponding logic circuit can then be drawn from this expression.

7. For the **XNOR gate**, we can simply add a NOT gate after the XOR gate:

   * $\text{XNOR} = \overline{\text{XOR}} = \overline{\text{XOR} \land \text{XOR}}$

8. For the **2-input Multiplexer (MUX)**:

   * Its DNF is $\text{Out} = A \land \overline{S} \lor B \land S$
   * Rewritten using NAND gates:
     $$\text{Out} = A \land \overline{S} \lor B \land S \\ = \overline{\overline{A \land \overline{S} \lor B \land S}} \\ = \overline{\overline{A \land \overline{S}} \land \overline{B \land S}} \\ = \overline{\overline{A \land \overline{S \land S}} \land \overline{B \land S}}$$

   From this rewritten expression, we can also draw its corresponding circuit.

9. **Key solving technique**: use and understand the Boolean Algebra, including:
   * **Commutative law**:
     $A + B = B + A$, $A \cdot B = B \cdot A$
   * **Associative law**:
     $A + (B + C) = (A + B) + C$, $A \cdot (B \cdot C) = (A \cdot B) \cdot C$
   * **Distributive law**:
     $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$, $A + (B \cdot C) = (A + B) \cdot (A + C)$
   * **Identity law**:
     $A + 0 = A$, $A \cdot 1 = A$
   * **Idempotent law**:
     $A + A = A$, $A \cdot A = A$
   * **Complement law**:
     $A + \bar{A} = 1$, $A \cdot \bar{A} = 0$
   * **Double negation law**:
     $\overline{\overline{A}} = A$
   * **De Morgan’s law**:
     $\overline{A\cdot B} = \overline{A} + \overline{B}$, $\overline{A + B} = \overline{A} \cdot \overline{B}$
   * **Absorption law**:
     $A + (A \cdot B) = A$, $A \cdot (A + B) = A$

10. **Extension**: Try to design XOR, XNOR, and a 2-to-1 Multiplexer **using only NOR gates**.

## Task 1.2
1. This task is the same as the previous one. you need to rewrite the logical expression using NAND gates and then draw the corresponding circuit.

2. Therefore, because of time constraints, I will not provide detailed explanations here. 

3. Please complete the task on your own and compare it with the reference answer. If you have any questions, please email me or my colleagues.

## Task 1.3

1. To solve this task, we need to understand and use Boolean Algebra.

2. For task (a):

   * Given $F = \overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}$
   * Its complement is:
     $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}}$$
   * If the exam question does not require the logical expression to be simplified into DNF, you may stop here.

3. If $\overline{F}$ needs to be in DNF:

   * Using **De Morgan's law** ($\overline{A \land B} = \overline{A} \lor \overline{B}$):
     $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}} \\ = \overline{\overline{A} \ \overline{B} \ C} \land \overline{\overline{A} \ B \ \overline{C}} \land \overline{A \ B \ \overline{C}} \\ = (\overline{\overline{A}} \lor \overline{\overline{B}} \lor \overline{C}) \land (\overline{\overline{A}} \lor \overline{B} \lor \overline{\overline{C}}) \land (\overline{A} \lor \overline{B} \lor \overline{\overline{C}})$$
   * Using **double negation** ($\overline{\overline{A}} = A$):
     $$\overline{F} = (A \lor B \lor \overline{C}) \land (A \lor \overline{B} \lor C) \land (\overline{A} \lor \overline{B} \lor C)$$
   * Using **distributive law** ($A \lor (B \land C) = (A \lor B) \land (A \lor C)$), **complement law** ($A \land \overline{A} = 0$), and **identity law** ($A \lor 0 = A$):
     $$(A \lor \overline{B} \lor C) \land (\overline{A} \lor \overline{B} \lor C) \\ = ((\overline{B} \lor C) \lor A) \land ((\overline{B} \lor C) \lor \overline{A}) \\ = (\overline{B} \lor C) \lor (A \land \overline{A}) \\ = (\overline{B} \lor C)$$
   * Therefore:
     $$\overline{F} = (A \lor B \lor \overline{C}) \land (\overline{B} \lor C)$$

4. For tasks (b) and (c), please practice on your own and compare with the reference answers. If you have any questions, email me or my colleagues.

## Task 1.4

1. The **RS latch** is a 2-state memory with output $Q = 0$ or $1$. From its structure:

   * When Set ($S=1$) and Reset ($R=0$), $Q = 1$
   * When Set ($S=0$) and Reset ($R=1$), $Q = 0$
   * When Set ($S=0$) and Reset ($R=0$), $Q$ keeps its state
   * When Set ($S=1$) and Reset ($R=1$), $Q$ and $\overline{Q} = 0$, which is a metastable state (“don’t care”)

2. The **logic automaton graph** lists all output states and all possible state transitions, along with the input conditions required for each transition.

3. This RS latch has four output combinations:
   $$00 = \overline{Q_1} \ \overline{Q_0}, \quad 01 = \overline{Q_1} \ Q_0, \quad 10 = Q_1 \ \overline{Q_0}, \quad 11 = Q_1 \ Q_0$$

4. Assuming the initial output combination is $00 = \overline{Q_1} \ \overline{Q_0}$:

   * To keep this state unchanged: $\text{SR} = 11$
   * To transition to $11 = Q_1 \ Q_0$: $\text{SR} = 00$ (i.e., $\overline{S} \ \overline{R}$)
   * To transition to $10 = Q_1 \ \overline{Q_0}$: $\text{SR} = 10$ (i.e., $S\overline{R}$)
   * To transition to $01 = \overline{Q_1} \ Q_0$: $\text{SR} = 01$ (i.e., $\overline{S}R$)

5. For transitions from other output combinations, refer to the solution and practice on your own.

6. Note: Here, “condition 1” means the input combination $SR$ does not matter; the state $Q_1 Q_0$ always transitions to $\overline{Q_1} \ \overline{Q_0}$.

7. The **reduced switching table** corresponds to the RS latch truth table.

8. Notation: $^n{Q}$ denotes the **new Q state**, while $^a{Q}$ denotes the **old Q state**.


