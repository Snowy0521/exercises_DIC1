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

## Task 1.5

1. For **Task (a)** (as shown in the diagram), the JK flip-flop can be constructed using two 3-input NAND gates and one RS latch.
2. When **clk = 0**, both **R** and **S** are set to 1, and $^n{Q} =\ ^a{Q}$.
3. When **clk** transitions from 0 to 1 (rising edge), the output $^n{Q}$ is determined by the input signals **J** and **K**.
4. The specific state transitions can be seen from its **switching table**.
5. In this switching table (excluding **clk**), there are four input signals: $\overline{^a{Q}},\ ^a{Q},\ J,\ K$; two intermediate signals: **R**, **S**; and two output signals: $^n{Q},\ \overline{^n{Q}}$.
6. The four input signals correspond to 8 possible signal combinations.
7. Each signal combination corresponds to a specific **R-S** combination.
8. Finally, based on **R**, **S**, $\overline{^a{Q}}$, and $^a{Q}$, we can get the outputs $^n{Q}$ and $\overline{^n{Q}}$.
9. For **Task (b)**, according to the switching table:

   * When **JK = 00**, $^n{Q} = ^a{Q}$
   * When **JK = 01**, $^n{Q} = 0$
   * When **JK = 10**, $^n{Q} = 1$
   * When **JK = 11**, $^n{Q} = \overline{^a{Q}}$


## Task 1.6

1. According to the capacitor equations for charge and current:
   $$Q = C V \quad \text{and} \quad I = \frac{dQ}{dt}$$
   Therefore:
   $$I = \frac{dQ}{dt} = C \frac{dV}{dt} = C \frac{\Delta V}{\Delta t} = \dots$$


## Task 1.7
1. We consider the voltage across the capaitor as $V_{out}$
2. According to Kirchoff's Voltage LAW and the the capacitor current equation $I = CdV/dt$
    + $$V_{in} = IR + V_{out} \\ = RCdV_{out}/dt + V_{out}$$
    + $$\frac{V_{in}-V_{out}}{R} = C \frac{dV_{out}}{dt}$$
    + $$dt = RC \frac{dV_{out}}{V_{in}-V_{out}}$$
    + Integrating both sides give: $$\int_{0}^{t} dt = RC \int_{0}^{V_{out}}\frac{dV_{out}}{V_{in}-V_{out}}$$
    + $$t = RC \ln(V_{in}-V_{out})\big|_0^{V_{out}}$$
    + $$t = -RC \ln\frac{V_{in}-V_{out}}{V_{in}}$$

## Task 1.8

1. For task (a) we take $V_{in}=V_{DD}$. Let $V_{out}$ be the voltage across the capacitor $C_L$.

2. This is the same RC charging circuit as in Task 1.7, so apply the formula:
   $$
   t = -RC\ln\frac{V_{in}-V_{out}}{V_{in}}
   $$
   Replacing $V_{in}=V_{DD}$ and the target $V_{out}=V_{DD}/2$:
   $$
   t = -R_1 C_L \ln\frac{V_{DD}-V_{DD}/2}{V_{DD}} = -R_1 C_L \ln\frac{1}{2} = R_1 C_L \ln 2.
   $$

3. For task (b) consider the capacitor initially charged to $V_{DD}$. Let $V_{out}$ be the voltage across resistor $R_2$ while the capacitor discharges through $R_2$.

4. Using the capacitor discharge current $I = -CdV_{out}/dt$ and KCL:
  $$
  -C_L \frac{dV_{out}}{dt} = \frac{V_{out}}{R_2}
  \quad\Longrightarrow\quad
  dt = -R_2 C_L \frac{dV_{out}}{V_{out}}.
  $$

5. Integrate both sides from $t=0$ with $V_{out}(0)=V_{DD}$ to time (t) with voltage $V_{out}$:
   $$
   \int_0^t dt = -R_2 C_L \int_{V_{DD}}^{V_{out}} \frac{dV_{out}}{V_{out}}
   \quad\Longrightarrow\quad
   t = -R_2 C_L \ln\frac{V_{out}}{V_{DD}}.
   $$

6. For the target $V_{out}=V_{DD}/2$ we get
   $$
   t = -R_2 C_L \ln\frac{1/2}{1} = R_2 C_L \ln 2.
   $$

7. The ratio of the two delays (a) over (b) is therefore
   $$
   \frac{R_1 C_L \ln 2}{R_2 C_L \ln 2} = \frac{R_1}{R_2}.
   $$

## Task 1.9 & 1.10

1. These two tasks are simple mathematical problems. Please try to understand them on your own and refer to the official reference solutions. If you have any questions, please email me or my colleagues.
