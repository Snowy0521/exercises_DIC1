## Task 1.1
1. 首先我们需要知道什么是NAND Gate：
    + 他的Symbol是...
    + 他的Boolean equations是 $\text{Out} = \overline{A \cdot B}$ 或者 $\text{Out} = \overline{A \land B}$
2. 现在我们要知道什么是XOR Gate：
    + In the XOR gate, the output is 1 only if the two inputs are different
    + 因此我们可以得到他的真值表...
    + 然后从中得到他的逻辑表达式（DNF: Disjunctive Normal Form）是: $\text{Out} = \overline{A}\cdot B + A \cdot \overline{B}$ or $\text{Out} = \overline{A}\land B \lor A \land \overline{B}$
    + 从这个DNF我们知道XOR gate由AND gates， OR gates 和 NOT gates 组成
    + 但是我们只有NAND Gate，所以我们需要用NAND gates 分别组成 AND Gate， OR Gate 和 NOT Gate

3. 只用NAND gate 组成 NOT gate的方法是将两个inputs连接到一起(Idempotent law)：
    + 他的逻辑表达式是 $\text{Out} = \overline{A \cdot A}$ or $\text{Out} = \overline{A \land A}$

4. 只用NAND gate 组成 AND gate的方法是要用到double negation law ($A = \overline{\overline{A}}$):
    + 所以 $A \land B = \overline{\overline{A \land B}}$
    + 又因为 Idempotent law ($A \land A = A$), 所以:
    $$A \land B = \overline{\overline{A \land B}} = \overline{\overline{A \land B} \land \overline{A \land B}}$$

5. 只用NAND gate 组成 OR gate 是要用到De Morgan's law ($\overline{A \lor B} = \overline{A} \land \overline{B}$)
    + 所以 $$A \lor B = \overline{\overline{A \lor B}} = \overline{\overline{A} \land \overline{B}} = \overline{\overline{A \land A} \land \overline{B \land B}}$$

6. 因此对于XOR gate, 我们只使用NAND gate 重写他的逻辑表达式：
    + $$\text{Out} = \overline{A}\land B \lor A \land \overline{B} \\ = \overline{\overline{\overline{A} \land B \lor A \land \overline{B}}} \\ = \overline{\overline{\overline{A} \land B} \land \overline{A \land \overline{B}}} \\ = \overline{\overline{\overline{A \land A} \land B} \land \overline{A \land \overline{B \land B}}}$$
    + 然后可以根据重新后的逻辑表达式画出对应的逻辑电路图

7. 对于XNOR gate 就是基于XOR gate的基础上再加一个NOT gate：
    + $\text{XNOR} = \overline{\text{XOR}} = \overline{\text{XOR} \land \text{XOR}}$

8. 对于2-Input Multiplexer (MUX):
    + 他的DNF是 $\text{Out} = A \land \overline{S} \lor B \land S$
    + 只使用NAND gate 重写得到：$$\text{Out} = A \land \overline{S} \lor B \land S \\ = \overline{\overline{A \land \overline{S} \lor B \land S}} \\ =  \overline{\overline{A \land \overline{S}} \land \overline{B \land S}} \\ = \overline{\overline{A \land \overline{S \land S}} \land \overline{B \land S}}$$
    + 根据重新后的逻辑表达式画出对应的逻辑电路图

9. 解题技巧是理解并熟练掌握 Boolean Algebra：
    + Commutative law: 
        + $A + B = B + A$ 
        + $A \cdot B = B \cdot A$
    + Associative law: 
        + $A + (B + C) = (A + B) + C$ 
        + $A \cdot (B \cdot C) = (A \cdot B) \cdot C$
    + Distributive law: 
        + $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$ 
        + $A + (B \cdot C) = (A + B) \cdot (A + C)$
    + Indentity law: 
        + $A + 0 = A$
        + $A\cdot 1 = A$
    + Idempotent law: 
        + $A + A = A$ 
        + $A \cdot A = A$
    + Complement law:
        + $A + \bar{A} = 1$
        + $A \cdot \bar{A} = 0$    
    + Double negation law: 
        + $\overline{\overline{A}} = A$
    + De Morgan's law: 
        + $\overline{A\cdot B} = \overline{A} + \overline{B}$ 
        + $\overline{A + B} = \overline{A} \cdot \overline{B}$
    + Absorption law:
        + $A + (A \cdot B) = A$
        + $A \cdot (A + B) = A$

10. 拓展题目：试试只使用NOR gate 实现 XOR gate，XNOR gate 和 2 in 1 Multiplexer


## Task 1.2
1. 这道题和前面一道题是一样的，需要用NAND gates重写逻辑表达式然后再根据逻辑表达式画出电路图。
2. 因此由于时间原因，我这里不在解释，请自行作答并比较参考答案，如有任何问题，请写邮件给我或者我的同事。

## Task 1.3
1. 这道题需要我们熟悉掌握Boolean Algebra。
2. 对于问题a来说：
    + 由于 $F = \overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}$
    + 所以他的complement：
        $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}}$$
    + 如果考试时的题目没有说明逻辑表达式需要化简成DNF，到这里就可以结束

3. 如果$\overline{F}$ in DNF:
    + Using demorgen's law ($\overline{A \land B} = \overline{A} \ \lor \overline{B}$): 
        $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}} \\ = \overline{\overline{A} \ \overline{B} \ C} \land \overline{\overline{A} \ B \ \overline{C}} \land \overline{A \ B \ \overline{C}} \\ = (\overline{\overline{A}} \lor \overline{\overline{B}} \lor \overline{C}) \ \land (\overline{\overline{A}} \lor \overline{B} \lor \overline{\overline{C}}) \ \land (\overline{A} \lor \overline{B} \lor \overline{\overline{C}})$$
    
    + Using double negation law ($\overline{\overline{A}} = A$):
        $$\overline{F} = (A \lor B \lor \overline{C}) \ \land (A \lor \overline{B} \lor C) \ \land (\overline{A} \lor \overline{B} \lor C)$$

    + Using distributive law ($A \lor (B \land C) = (A \lor B) \land (A \lor C)$), Complement law ($A \land \overline{A} = 0$) and identity law ($A \lor 0 = A$):
        $$(A \lor \overline{B} \lor C) \ \land (\overline{A} \lor \overline{B} \lor C) \\ = ((\overline{B} \lor C) \ \lor A) \ \land ((\overline{B} \lor C) \ \lor \overline{A}) \\ = (\overline{B} \lor C) \lor (A \land \overline{A}) \\ = (\overline{B} \lor C)$$
    
    + So, $$\overline{F} = (A \lor B \lor \overline{C}) \ \land (\overline{B} \lor C)$$

4. 对于问题b和c请自行练习并比较参考答案，如有任何问题，请写邮件给我或者我的同事。

## Task 1.4
1. RS latch 是一个2 state memory，output Q = 0 or 1. 从他的struture可知：
    + 当Set（S=1）和 Reset （R=0）时， Q = 1
    + 当Set (S=0) 和 Reset （R=1）时，Q = 0
    + 当Set (S=0) 和 Reset （R=0）时, Q keeps its state
    + 当Set (S=0) 和 Reset （R=0）时, Q and $\overline{Q} = 0$, 这是个亚稳态，don't care.
2. logic automaton graph 就是列出所有输出组合状态，并列举出所有状态组合转换的条件，也就是所需要的输入组合。

3. 这个RS latch有四种输出组合状态（$00 = \overline{Q_1} \ \overline{Q_0}, 01 = \overline{Q_1} \ Q_0, 10 = Q_1 \ \overline{Q_0}, 11 = Q_1 \ Q_0$）

4. 我们先假设起始输出组合状态 $00 = \overline{Q_1} \ \overline{Q_0}$:
    + 如果要使得这个输出组合状态保持不变，$\text{SR}=11$
    + 如果要跳变到输出组合状态$11 = Q_1 \ Q_0$, 那么$\text{SR}=00$, 也就是 $\overline{S}\overline{R}$
    + 如果要跳变到输出组合状态$10 = Q_1 \ \overline{Q_0}$, 那么$\text{SR}=10$, 也就是 $S\overline{R}$
    + 如果要跳变到输出组合状态$01 = \overline{Q_1} \ Q_0$, 那么$\text{SR}=01$, 也就是 $\overline{S}R$

5. 对于其他的输出组合状态转换，请参考答案自己练习。

6. 有一点需要注意的是这里的条件1表示无所谓输入组合SR是多少，状态$Q_1Q_0$ 总是要跳变到$\overline{Q_1}\ \overline{Q_0}$

7. 他的reduced switching table就是RS latch的truth table

8. 这里的$^n{Q}$ 代表着new Q state, $^a{Q}$ 代表着 old Q state