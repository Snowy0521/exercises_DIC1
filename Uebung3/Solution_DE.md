## Task 3.1
### a)
1. Nach Gleichung (2.11) des Referenzbuches gilt $$V_{T0} = \phi_{GC} - 2\phi_F - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
2. Für NMOS: $$V_{T0n} = \phi_{GC} - 2\phi_{Fp} - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
    + $$\phi_{GC} = \phi_{Fp} - \phi_{G} = ( -0.44 - 0.55 ) \mathrm{V} = -0.99  \mathrm{V}$$
    + $$2\phi_{Fp} = -0.88 \mathrm{V}$$
    + $$\frac{Q_{B0}(\text{Elektronen})}{C_{ox}} = \frac{- \sqrt{2qN_A \epsilon_{si}|-2\phi_F|}}{\frac{\epsilon_{ox}}{t_{ox}}} = -0.188 \mathrm{V}$$
    + $$\frac{Q_{ox}}{C_{ox}} = \frac{N_{SS}q}{C_{ox}} = 0.06 \mathrm{V}$$

3. Für PMOS: $$V_{T0p} = \phi_{GC} - 2\phi_{Fn} - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
    + $$\phi_{GC} = \phi_{Fn} - \phi_{G} = (0.44 - (-0.55) ) \mathrm{V} = 0.99  \mathrm{V}$$
    + $$2\phi_{Fn} = 0.88 \mathrm{V}$$
    + $$\frac{Q_{B0}(\text{Löcher})}{C_{ox}} = \frac{+ \sqrt{2qN_A \epsilon_{si}|-2\phi_F|}}{\frac{\epsilon_{ox}}{t_{ox}}} = 0.188 \mathrm{V}$$
    + $$\frac{Q_{ox}}{C_{ox}} = \frac{N_{SS}q}{C_{ox}} = 0.06 \mathrm{V}$$

### b)
1. **Donatoren sind Elektronen, Akzeptoren sind Löcher.**
2. Wenn ein PMOS-Gate mit Elektronen anstelle von Akzeptoren dotiert wird:
$$\phi_{GC} = \phi_{Fn} - \phi_{G} = (0.44 - 0.55)  \mathrm{V} = -0.11  \mathrm{V}$$
3. Der neue $V_{T0p} = (-0.11 \mathrm{V}) - (0.88 \mathrm{V}) - (0.188 \mathrm{V}) - (0.06 \mathrm{V}) = -1.24 \mathrm{V}$
4. Notation:
    + Für NMOS hat es ein P-Substrat, $\phi_{Fp} < 0$, d.h. $\phi_{Fp} = -0.44 \mathrm{V}$:
        + Wenn sein Gate mit **Elektronen** dotiert ist $\phi_G = 0.55 \mathrm{V}$
        + Wenn sein Gate mit **Löchern** dotiert ist $\phi_G = -0.55 \mathrm{V}$
    + Für PMOS hat es ein N-Substrat, $\phi_{Fn} > 0$, d.h. $\phi_{Fn} = 0.44 \mathrm{V}$:
        + Wenn sein Gate mit **Elektronen** dotiert ist $\phi_G = 0.55 \mathrm{V}$
        + Wenn sein Gate mit **Löchern** dotiert ist $\phi_G = -0.55 \mathrm{V}$

### c)
1. Berechnung der implantierten Ionen pro Quadratzentimeter, um die gewünschten $V_{T0n} = 0.4 \mathrm{V}$ und $V_{T0p} = -0.4 \mathrm{V}$ zu erreichen
2. Gemäß der Kondensatorspannungsgleichung: $$Q = q \times N_I = C_{ox} \times (V_d-V_a)$$

### d)
1. Um sicherzustellen, dass der absolute Wert der Schwellenspannung nicht größer als $V_{DD}$ ist.
2. Bei der $0.13 \mathrm{\mu m}$ Technologie beträgt die Versorgungsspannung $V_{DD} = 1.2 \mathrm{V}$

### e)
1. Gemäß Gleichung (2.21) auf Seite 59 des Referenzbuches:
    $$\mu_e = \frac{\mu_0}{1 + (\frac{V_{GS}- V_{T}}{\theta \cdot t_{ox}})^{\eta}}$$
    + Gegeben ist die Nennbeweglichkeit (nominal mobility) $\mu_0 = 130 \mathrm{cm}^2\mathrm{V}^{-1}\mathrm{s}^{-1}$
    + $\theta = 4 \cdot 10^6 \mathrm{Vcm}^{-1}$
    + $\eta = 1.85$
    + In der $0.13 \mathrm{\mu m}$ Technologie beträgt die Dicke des Oxids $t_{ox} = 22 \text{\r{A}} = 22 \times 10^{-8} \mathrm{cm} $
    + $V_{GS} - V_{T} = 1.2 \mathrm{V} - 0.4 \mathrm{V} = 0.8 \mathrm{V}$

***

## Task 3.2
### a)
1. Gemäß Gleichung (2.22) auf Seite 60 des Referenzbuches:
    + Das elektrische Feld $E_{cn} = 6 \cdot 10^4$ V/cm für Elektronen und $E_{cp} = 24 \cdot 10^4$ V/cm für Löcher.
    + $E_{cn}L = 6 \cdot 10^4 \cdot 200 \cdot 10^{-7} = 1.2 \mathrm{V}$
    + $E_{cp}L = 24 \cdot 10^4 \cdot 200 \cdot 10^{-7} = 4.8 \mathrm{V}$
2. Gemäß Gleichung (2.28) auf Seite 62 des Referenzbuches:
    + $$V_{Dsat} = \frac{(V_{GS}-V_T)E_cL}{(V_{GS}-V_T) + E_cL}$$
3. Für NMOS: $$V_{Dsat} = \frac{(V_{GS}-V_{TN})E_{cn}L}{(V_{GS}-V_{TN}) + E_{cn}L} = \frac{(1.8 - 0.5)(1.2)}{1.8 - 0.5 + 1.2} \mathrm{V} = 0.6 \mathrm{V} $$

4. Für PMOS: $$V_{Dsat} = \frac{(V_{SG}-|V_{TP}|)E_{cp}L}{(V_{SG}-|V_{TP}|) + E_{cp}L} = \frac{(1.8 - 0.5)(4.8)}{1.8 - 0.5 + 4.8} \mathrm{V} = 1.0 \mathrm{V} $$

### b)
1. Das Gleiche wie a)
2. Für NMOS $$V_{Dsat} = \frac{(V_{GS}-V_{TN})E_{cn}L_n}{(V_{GS}-V_{TN}) + E_{cn}L_n} = \frac{(1.2 - 0.4)(0.6)}{1.2 - 0.4 + 0.6} \mathrm{V} = 0.34 \mathrm{V} $$

3. Für PMOS: $$V_{Dsat} = \frac{(V_{SG}-|V_{TP}|)E_{cp}L_p}{(V_{SG}-|V_{TP}|) + E_{cp}L_p} = \frac{(1.2 - 0.4)(2.4)}{1.2 - 0.4 + 2.4} \mathrm{V} = 0.6 \mathrm{V} $$

### c)
1. Gemäß Gleichung (2.29) auf Seite 64 des Referenzbuches:
$$\frac{I_{DsatN}}{I_{DsatP}} = \frac{W_N v_{sat} C_{ox}(V_{GS}-V_{TN})^2/(V_{GS} - V_{TN} + E_{cn}L_n)}{W_P v_{sat} C_{ox}(V_{SG}-|V_{TP}|)^2/(V_{SG} - |V_{TP}| + E_{cp}L_p)}$$

2. Vereinfacht zu $$\frac{I_{DsatN}}{I_{DsatP}} = \frac{(V_{GS}-V_{TN})^2/(V_{GS} - V_{TN} + E_{cn}L_n)}{(V_{SG}-|V_{TP}|)^2/(V_{SG} - |V_{TP}| + E_{cp}L_p)} = \frac{(1.2-0.4)^2/(1.2 - 0.4 + 0.6)}{(1.2-0.4)^2/(1.2 - 0.4 + 2.4)}$$

3. Vereinfacht zu $$\frac{I_{DsatN}}{I_{DsatP}} = \frac{1.2 - 0.4 + 2.4}{1.2 - 0.4 + 0.6} \approx 2.3$$

***

## Task 3.3
### a)
1. Aus der vorherigen Aufgabe wissen wir, dass $$\frac{I_{DsatN}}{I_{DsatP}} = 2.3$$
2. Daher ist, wenn die Breiten-zu-Längen-Verhältnisse von NMOS und PMOS gleich sind, der $I_{DsatN}$ eines $1 \times NMOS$ **2,3-mal** der $I_{DsatP}$ eines $1 \times PMOS$.
3. Wenn also die PMOS-Breite $W_P = 2 W_N$ ist, ist nach Gleichung (2.29) das Verhältnis des $I_{Dsat}$ für $1 \times NMOS$ und $2 \times PMOS$ **2.3/2**.
4. Ebenso, wenn die PMOS-Breite $W_P = 3 W_N$ ist, ist das Verhältnis des $I_{Dsat}$ für $1 \times NMOS$ und $3 \times PMOS$ **2.3/3**.
5. Für denselben NMOS oder PMOS ändert sich sein $I_{Dsat}$ auch mit der Änderung von $V_{SG}$ (oder $V_{GS}$).
6. Daher ist nach Gleichung (2.29) das Verhältnis des $I_{Dsat}$ für $1 \times PMOS$ mit $V_{SG} = 1.2 \mathrm{V}$ und $1 \times PMOS$ mit $V_{SG} = 0.8 \mathrm{V}$ **8/1**.
7. Wenn $V_{SG} = 0.4 \mathrm{V} = |V_{TP}|$ ist, befindet sich der PMOS an der Grenze des **Sperrbereichs** (cutoff region), sodass idealerweise, unter Vernachlässigung von Faktoren wie Unterschwellenleitung (subthreshold conduction), Kanallängenmodulation (channel length modulation) oder Body-Effekt, die $I_{DsatN}$ des NMOS und die $I_{DsatP}$ des PMOS beide **0** sind.

### b)
1. Für NMOS gilt, wenn $V_{GS} \leq V_{TN}$, dass es sich im **Sperrbereich** (cutoff region) befindet, also ist $I_{DS} = 0$ in der idealen Situation.
2. Wenn $V_{GS} > V_{TN}$ und $V_{DS} \geq V_{GS} - V_{TN} \to V_{GS} \leq V_{DS} + V_{TN}$, befindet es sich im **Sättigungsbereich** (saturation region), also $$I_{DS} = \frac{1}{2}\mu_n c_{ox} \frac{W}{L}(V_{GS} - V_{TN})^2$$ (z.B. 2.19), Vernachlässigung von $\lambda$ (Kanallängenmodulation).
3. Wenn $V_{GS} > V_{TN}$ und $V_{DS} < V_{GS} - V_{TN} \to V_{GS} > V_{DS} + V_{TN}$, befindet es sich im **Linearen Bereich** (linear region), also $$I_{DS} = \mu_n c_{ox} \frac{W}{L}(V_{GS} - V_{TN} - \frac{V_{DS}}{2})V_{DS}$$ (z.B. 2.17b).

***

## Task 3.4
1. **Mathematische Berechnungsaufgabe.** Führen Sie die Berechnung selbst durch und vergleichen Sie mit der Referenzlösung.