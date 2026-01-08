## Task 2.1
### a)
1. Angenommen, die Verzögerung eines Inverter beträgt $2 \mathrm{ns}$, dass ein Eingang A bei $t_d = 0$ ein Ausgangssignal $\overline{A}$ bei $t_d = 2 \mathrm{ns}$ erzeugt.
2. Wenn ein weiterer Inverter mit derselben Verzögerung in Reihe verbindet wird, bedeutet es, dass der Eingang $\overline{A} bei at $t_d = 2 \mathrm{ns}$ ein Ausgangssignal $\overline{\overline{A}} = A$ bei $t_d = 4 \mathrm{ns}$ erzeugt.
3. Ebenso, wenn fünf identische Inverter in Reihe geschaltet werden, dann is bei $t_d = 2 \mathrm {ns} \times 5 = 10 \mathrm{ns}$ der Ausgang $B = \overline{A}$


### b)
1. Wenn A und B verbunden sind, dann gilt bei $t_d = 10 \mathrm{ns}$, $A = (B = \overline{A})$.
2. Angenommen, der Anfangswert von A ist 0, dann ändert sich A bei $t_d = 10 \mathrm{ns}$ von 0 auf 1.
3. Ebenso ändert sich A bei $t_d = 20 \mathrm{ns}$ von 1 auf 0.
4. Dager beträgt eine Periode $20 \mathrm{ns}$.
5. Nach der Frequenzgleichung $T = 1/f$ beträgt die Frequenz $50 \mathrm{MHz}$.


## Task 2.2
1. Die Struktur und das Symbol eines NMOS können im Referenzbuch im Abbildung 2.1 gefunden, deswegen zeichne ich hier nicht mehr.
2. Am Anfang befindet sich die Schaltung in einem instabilen Zustand: Wenn $V_{GS}$ steigt, tritt der NMOS in den linearen oder Sättigungsbereich ein, und $V_{OL}$ fällt von 5 V to 1 V.
3. Aufgrund parasitärer Kapazitäten $C_{DS}$ und $C_{GD}$, wenn $V_{OL}$ fällt innerhalb sehr kurzer Zeit z.B. einige zehn Nanosekunden, ein großer transitorischer Strom wird erzeugt gemäß der Kapazitorstromgleichung.
4. Der stationäre Zustand bedeutet, dass die Drain Spannung stabil wird, wobei $$I_{DC} = \frac{V_{DD}}{R_L + R_{on}} = \frac{V_{DD}-V_{OL}}{R_L}$$ gilt, $I_{DC}$ stellt einen rein ohmischen Strom dar.

## Task 2.3
### a)
1. Nach Gleichung 2.4 auf Seite 43 des Referenzbuches ist das Potential $\phi_{Fp}$ eines p-Typ-Halbleiters die Differenz zwischen dem tatsächlichen Fermi-Level $E_{Fp}$ und dem intrinsischen Energylevel $E_{i}$:
$$
\phi_{Fp} = \frac{kT}{q}\ln\frac{n_i}{N_A}
$$
2. Laut der Beschreibung auf den Seiten 44 und 46 des Refernzbuches wird starke Inversion als der Zustand definiert,  bei dem die Elektronenkonzentration an der Oberfläche der Lochkonzentration im Substrat entspricht. Somit gilt $\phi_s = - \phi_{Fp}$, und der Bandverbiegungsgrad ist:
$$
2|\phi_{Fp}| = |\phi_s - \phi_{Fp}|
$$
3. Thermische Spannung: $kT/q = V_T \approx 26\ \mathrm{mV}$
4. Gegeben ist die Dotierung des p-Substrats: $N_A=3\times10^{17}\ \mathrm{cm^{-3}}$
5. Die intrinsische Trägerkonzentration: $n_i =1.45\times10^{10} \mathrm{cm^{-3}} $

### b)
1. Die Breite der Raumladungszone ist Thickness $X_d$ der Depletion region
2. Nach Gleichung (2.7) auf Seite 47 des Referenzbuches: $$X_d = (\frac{2\epsilon_{si}|\phi_s-\phi_F|}{qN_A})^{1/2}$$
    * Dielectric constant of silicon $\epsilon_{si} = 11.7 \times \epsilon_0 (8.85 \times 10^{-14} \mathrm{As/cm})$ that dielectric constant of vacuum
    * Aus Unteraufgabe a)，$|\phi_s-\phi_F| = 0.88 \mathrm{V}$
    * Electron charge $q = 1.6 \times 10^{-19} \mathrm{As}$
    * The acceptor concentrations $N_A = 3 \times 10^{17} \mathrm{cm^3}$

3. Nach Gleichung (2.9a) ist die feste negative Ladung $$Q_{B0} = - \sqrt{2qN_A \epsilon_{si}|-2\phi_F|}$$

### c)
1. Nach Gleichung (2.5)$$C_{ox} = \frac{\epsilon_{ox}}{t_{ox}}$$
    * $\epsilon_{ox}$ is the dielectric constant of oxide $\epsilon_{ox} \approx 4 \epsilon_0$
    * $t_{ox}$ is the thickness of the oxide $t_{ox} = 22 \text{\r{A}} = 22 \times 10^{-8} \mathrm{cm} $
2. Nach Gleichung (2.12) der Body-Faktor $$\lambda = \frac{1}{C_{ox}}\sqrt{2q\epsilon_{si}N_A}$$

### d)
1. Nach Gleichung (2.11) $$V_{T0} = \phi_{GC} - 2\phi_F - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
2. Laut Abbildung (2.6) $\phi_{GC} = \Phi_G - \Phi_C = \phi_{Fp} - \phi_G$
3. Laut Abbildung (2.4) beträgt die Bandgap energy von Silicon $1.1 \mathrm{eV}$, $E_i$ liegt in der Mitte zwischen Leistungsband und Valenzband, somit  $\phi_{GC} = -0.44 \mathrm{V} - 0.55 \mathrm{V} = -0.99 \mathrm{V}$
4. Aus den Unteraufgaben b) und c) erhalten wir $Q_{B0}/C_{ox}$
5. $$\frac{Q_{ox}}{C_{ox}} = \frac{N_{ox}q}{C_{ox}}$$
6. Gate Dotierung: 
    + Angnommen einer $n^+$ Gate-Dotierung, sodass das Fermi level im Gate den Leistungsband entspricht. 
    + Elektrostatik-Potential des Gates $\Phi_G = 0.55 \mathrm{V}$
    + Wenn das Gate $p^+$ doptiert wäre, ergäbe sich $V_{T0} =(-0.44 + 0.55 - (-0.88) - (-0.188) - 0.002) \mathrm{V} = 1.18 \mathrm{V}$, es ist zu groß. Der gewünschte Wert von $V_{T0} = 0.4 \mathrm{V}$

### e)
1. Nach der Kapazitor-Spannungsgleichung $$V_T = \frac{Q}{C_{ox}} = \frac{qN}{C_{ox}}$$
2. Daher gilt: $$N_I = \frac{C_{ox}\Delta V }{q} $$


