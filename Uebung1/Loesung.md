## Aufgabe 1.1

1. Zuerst betrachten wir, was ein **NAND-Gatter** ist:

   * Sein Symbol ist …
   * Seine Boolesche Gleichung ist $\text{Out} = \overline{A \cdot B}$ oder $\text{Out} = \overline{A \land B}$

2. Nächstes betrachten wir das **XOR-Gatter**:

   * Beim XOR-Gatter ist der Ausgang 1, wenn die beiden Eingänge unterschiedlich sind.
   * Daraus können wir seine Truth Table aufstellen.
   * Sein logischer Ausdruck (in **DNF: Disjunktive Normalform**) ist:
     $\text{Out} = \overline{A}\cdot B + A \cdot \overline{B}$ oder $\text{Out} = \overline{A}\land B \lor A \land \overline{B}$
   * Dies zeigt, dass das XOR-Gatter aus AND-, OR- und NOT-Gattern zusammengesetzt ist.
   * Da wir können **nur NAND-Gatter** verwenden dürfen, müssen wir AND, OR und NOT mit NAND-Gattern aufbauen.

3. **NOT-Gatter mit NAND-Gattern**:
   * Wir verbinden die beiden Eingänge des NAND-Gatters miteinander laut Idempotenzgesetz.
   * Ausdruck: $\text{Out} = \overline{A \cdot A}$ oder $\text{Out} = \overline{A \land A}$

4. **AND-Gatter mit NAND-Gattern** (mittels Doppelnegationsgesetz, $A = \overline{\overline{A}}$):

   * $A \land B = \overline{\overline{A \land B}}$
   * Mit dem Idempotenzgesetz ($A \land A = A$) ergibt sich:
     $$A \land B = \overline{\overline{A \land B}} = \overline{\overline{A \land B} \land \overline{A \land B}}$$

5. **OR-Gatter mit NAND-Gattern** (mittels De Morgan, $\overline{A \lor B} = \overline{A} \land \overline{B}$):

   * $$A \lor B = \overline{\overline{A \lor B}} = \overline{\overline{A} \land \overline{B}} = \overline{\overline{A \land A} \land \overline{B \land B}}$$

6. Damit können wir den Ausdruck für das **XOR-Gatter** mit NAND-Gattern umschreiben:
   $$\text{Out} = \overline{A}\land B \lor A \land \overline{B} \\ = \overline{\overline{\overline{A} \land B \lor A \land \overline{B}}} \\ = \overline{\overline{\overline{A} \land B} \land \overline{A \land \overline{B}}} \\ = \overline{\overline{\overline{A \land A} \land B} \land \overline{A \land \overline{B \land B}}}$$

   Daraus kann man das entsprechende Schaltbild zeichnen.

7. Für das **XNOR-Gatter** kann man einfach ein NOT-Gatter hinter das XOR-Gatter setzen:

   * $\text{XNOR} = \overline{\text{XOR}} = \overline{\text{XOR} \land \text{XOR}}$

8. Für den **2-Eingang-Multiplexer (MUX)**:

   * Seine DNF lautet $\text{Out} = A \land \overline{S} \lor B \land S$
   * Mit NAND-Gattern umgeschrieben:
     $$\text{Out} = A \land \overline{S} \lor B \land S \\ = \overline{\overline{A \land \overline{S} \lor B \land S}} \\ = \overline{\overline{A \land \overline{S}} \land \overline{B \land S}} \\ = \overline{\overline{A \land \overline{S \land S}} \land \overline{B \land S}}$$

   Aus diesem Ausdruck kann man ebenso seines Schaltbild abbilden.

9. **Wichtige Rechengesetze der Booleschen Algebra**:

   * **Kommutativgesetz**:
     $A + B = B + A$, $A \cdot B = B \cdot A$
   * **Assoziativgesetz**:
     $A + (B + C) = (A + B) + C$, $A \cdot (B \cdot C) = (A \cdot B) \cdot C$
   * **Distributivgesetz**:
     $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$, $A + (B \cdot C) = (A + B) \cdot (A + C)$
   * **Identitätsgesetz**:
     $A + 0 = A$, $A \cdot 1 = A$
   * **Idempotenzgesetz**:
     $A + A = A$, $A \cdot A = A$
   * **Komplementgesetz**:
     $A + \bar{A} = 1$, $A \cdot \bar{A} = 0$
   * **Doppelnegation**:
     $\overline{\overline{A}} = A$
   * **De Morgan**:
     $\overline{A\cdot B} = \overline{A} + \overline{B}$, $\overline{A + B} = \overline{A} \cdot \overline{B}$
   * **Absorptionsgesetz**:
     $A + (A \cdot B) = A$, $A \cdot (A + B) = A$

10. **Erweiterung**: Versuchen Sie, XOR, XNOR und einen 2-zu-1-Multiplexer **nur mit NOR-Gattern** zu realisieren.

## Aufgabe 1.2
1. Diese Aufgabe ist dieselbe wie die vorne Aufgabe 1.1: Man muss nur den logischen Ausdruck mit NAND-Gattern umschreiben und anschließend das entsprechende Schaltbild zeichnen.
2. Aus Zeitdruck gebe ich hier keine weiteren Erklärungen. Bitte machen Sie die Aufgabe selber und vergleichen Sie ihre Ergebnisse mit der Musterlösungen. Falls Sie Fragen haben, schreiben Sie mir oder meinem Kollegen eine E-Mail.

## Aufgabe 1.3

1. Diese Aufgabe erfordert uns, die Booleschen Algebra gut verstehen und benutzen.

2. Für Aufgabe (a):

   * Gegeben ist $F = \overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}$
   * Das Komplement lautet:
     $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}}$$
   * Wenn in der Prüfungsaufgabe nicht erfordert wird, den Ausdruck in DNF zu vereinfachen, dann bis here ist es einfach fertig.

3. Aber wenn $\overline{F}$ in DNF dargestellt werden soll:

   * Mit **De Morgans Gesetz** ($\overline{A \land B} = \overline{A} \lor \overline{B}$):
     $$\overline{F} = \overline{\overline{A} \ \overline{B} \ C \lor \overline{A} \ B \ \overline{C} \lor A \ B \ \overline{C}} \\ = \overline{\overline{A} \ \overline{B} \ C} \land \overline{\overline{A} \ B \ \overline{C}} \land \overline{A \ B \ \overline{C}} \\ = (\overline{\overline{A}} \lor \overline{\overline{B}} \lor \overline{C}) \land (\overline{\overline{A}} \lor \overline{B} \lor \overline{\overline{C}}) \land (\overline{A} \lor \overline{B} \lor \overline{\overline{C}})$$
   * Mit **Doppelnegation** ($\overline{\overline{A}} = A$):
     $$\overline{F} = (A \lor B \lor \overline{C}) \land (A \lor \overline{B} \lor C) \land (\overline{A} \lor \overline{B} \lor C)$$
   * Mit **Distributivgesetz** ($A \lor (B \land C) = (A \lor B) \land (A \lor C)$), **Komplementgesetz** ($A \land \overline{A} = 0$) und **Identitätsgesetz** ($A \lor 0 = A$):
     $$(A \lor \overline{B} \lor C) \land (\overline{A} \lor \overline{B} \lor C) \\= ((\overline{B} \lor C) \lor A) \land ((\overline{B} \lor C) \lor \overline{A}) \\ = (\overline{B} \lor C) \lor (A \land \overline{A}) \\ = (\overline{B} \lor C)$$
   * Somit:
     $$\overline{F} = (A \lor B \lor \overline{C}) \land (\overline{B} \lor C)$$

4. Für die Aufgaben (b) und (c) üben Sie bitte selbst und vergleichen Sie mit den Musterlösungen. Bei Fragen schreiben Sie mir oder meinem Kollegen eine E-Mail.

## Aufgabe 1.4

1. Das **RS-Latch** ist ein Speicher mit zwei Zuständen, mit Ausgang $Q = 0$ oder $1$. Aus seiner Struktur:

   * Wenn Set ($S=1$) und Reset ($R=0$), dann $Q = 1$
   * Wenn Set ($S=0$) und Reset ($R=1$), dann $Q = 0$
   * Wenn Set ($S=0$) und Reset ($R=0$), behält $Q$ seinen Zustand
   * Wenn Set ($S=1$) und Reset ($R=1$), dann $Q$ und $\overline{Q} = 0$, was einen metastabilen Zustand darstellt („don’t care“)

2. Das **Logikautomaten-Diagramm** listet alle Ausgangszustände und alle möglichen Zustandsübergänge auf, zusammen mit den Eingangsbedingungen für jeden Übergang.

3. Dieses RS-Latch hat vier Ausgangskombinationen:
   $$00 = \overline{Q_1} \ \overline{Q_0}, \quad 01 = \overline{Q_1} \ Q_0, \quad 10 = Q_1 \ \overline{Q_0}, \quad 11 = Q_1 \ Q_0$$

4. Angenommen, der Anfangszustand ist $00 = \overline{Q_1} \ \overline{Q_0}$:

   * Um diesen Zustand beizubehalten: $\text{SR} = 11$
   * Um zu $11 = Q_1 \ Q_0$ zu wechseln: $\text{SR} = 00$ (d.h. $\overline{S}\overline{R}$)
   * Um zu $10 = Q_1 \ \overline{Q_0}$ zu wechseln: $\text{SR} = 10$ (d.h. $S\overline{R}$)
   * Um zu $01 = \overline{Q_1} \ Q_0$ zu wechseln: $\text{SR} = 01$ (d.h. $\overline{S}R$)

5. Für die Übergänge anderer Ausgangskombinationen siehe die Lösung und üben Sie selbst.

6. Hinweis: „Bedingung 1“ bedeutet, dass die Eingabekombination $SR$ egal ist; der Zustand $Q_1 Q_0$ wechselt immer zu $\overline{Q_1} \ \overline{Q_0}$.

7. Die **reduzierte Schaltwerktabelle** entspricht der Wahrheitstabelle des RS-Latch.

8. Notation: $^n{Q}$ bezeichnet den **neuen Q-Zustand**, während $^a{Q}$ den **alten Q-Zustand** bezeichnet.

