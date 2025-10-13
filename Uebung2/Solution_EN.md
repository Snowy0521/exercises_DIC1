## Task 2.1
### a)
1. Given that the delay of one inverter is $2 \mathrm{ns}$, it means that an input A at $t_d = 0$ will process an output $\overline{A}$ at $t_d = 2 \mathrm{ns}$
2. If another inverter with the same delay is connected in series, it means that the input $\overline{A}$ at $t_d = 2 \mathrm{ns}$ will process an output $\overline{\overline{A}} = A$ at $t_d = 4 \mathrm{ns}$
3. In the same way, if five identical inverters are connected in series, then at $t_d = 2 \mathrm {ns} \times 5 = 10 \mathrm{ns}$, the output $B = \overline{A}$

### b)
1. If A and B are connected, then at $t_d = 10 \mathrm{ns}$, $A = (B = \overline{A})$.
2. Assuming the initial value of A is 0, then at $t_d = 10 \mathrm{ns}$, A changes from 0 to 1.
3. Similarly, at $t_d = 20 \mathrm{ns}$, A changes from 1 to 0.
4. Therefore, one period is $20 \mathrm{ns}$.
5. According to the frequency equation $T = 1/f$, so the frequency is $50 \mathrm{MHz}$


## Task 2.2
1. The structure and symbol of an NMOS transistor can we find in reference book figure 2.1, so I won't drawn it here.
2. Initially, the circuit is in an unstable state: as $V_{GS}$ increases, the NMOS enters the linear or saturation region, and $V_{OL}$ decreases from 5 V to 0 V
3. Due to parasitic capacitances $C_{DS}$ and $C_{GD}$, if $V_{OL}$ changes within a very short time for example, tens of nanoseconds, a large transient current will be generated according the capacitor current equation.
4. The steady state means the drain voltage becomes stable, where $$I_{DC} = \frac{V_{DD}}{R_L + R_{on}} \frac{V_{DD}-V_{OL}}{R_L}$$, the $I_{DC}$ represents a pure resistive current.  

## Task 2.3
### a)
1. According to equation (2.4) on page 43 of the reference book, the potential $\phi_{Fp}$ of a p-type semiconductor is the difference between the actual Fermi level $E_{Fp}$ and the intrinsic energy level $E_{i}$:
$$
\phi_{Fp} = \frac{kT}{q}\ln\frac{n_i}{N_A}
$$
2. According the decription on pages 44 and 46 of the reference book, strong inversion is defined as the condition when surface electron concentration equals the hole concentration in the substrate. so $\phi_s = - \phi_{Fp}$, so the degree of band-bending is:
$$
2|\phi_{Fp}| = |\phi_s - \phi_{Fp}|
$$
3. Thermal voltage: $kT/q = V_T \approx 26\ \mathrm{mV}$
4. Given the doping level in the p-substrate:$N_A=3\times10^{17}\ \mathrm{cm^{-3}}$
5. The intrinsic carrier concentration: $n_i =1.45\times10^{10} \mathrm{cm^{-3}} $

### b)
1. the width of space charge region is the thickness $X_d$ of the depletion region
2. According to equation (2.7) on page 47 of the reference book: $$X_d = (\frac{2\epsilon_{si}|\phi_s-\phi_F|}{qN_A})^{1/2}$$
    * Dielectric constant of silicon $\epsilon_{si} = 11.7 \times \epsilon_0 (8.85 \times 10^{-14} \mathrm{As/cm})$ that dielectric constant of vacuum
    * From subtask a)，$|\phi_s-\phi_F| = 0.88 \mathrm{V}$
    * Electron charge $q = 1.6 \times 10^{-19} \mathrm{As}$
    * The acceptor concentrations $N_A = 3 \times 10^{17} \mathrm{cm^3}$

3. According to equation (2.9a): the fixed negative charge $$Q_{B0} = - \sqrt{2qN_A \epsilon_{si}|-2\phi_F|}$$

### c)
1. According to equation (2.5)$$C_{ox} = \frac{\epsilon_{ox}}{t_{ox}}$$
    * $\epsilon_{ox}$ is the dielectric constant of oxide $\epsilon_{ox} \approx 4 \epsilon_0$
    * $t_{ox}$ is the thickness of the oxide $t_{ox} = 22 \text{\r{A}} = 22 \times 10^{-8} \mathrm{cm} $
2. According to equation (2.12) body factor $$\lambda = \frac{1}{C_{ox}}\sqrt{2q\epsilon_{si}N_A}$$

### d)
1. According to equation (2.11) $$V_{T0} = \phi_{GC} - 2\phi_F - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
2. According to Figure(2.6) $\phi_{GC} = \Phi_G - \Phi_C = \phi_{Fp} - \phi_G$
3. According to Figure(2.4) The band gap energy of silicon is $1.1 \mathrm{eV}$, $E_i$ is located at the middleway of conduction band and valence band, so $\phi_{GC} = -0.44 \mathrm{V} - 0.55 \mathrm{V} = -0.99 \mathrm{V}$
4. From subtask b) and c) we get $Q_{B0}/C_{ox}$
5. $$\frac{Q_{ox}}{C_{ox}} = \frac{N_{ox}q}{C_{ox}}$$
6. Gate doping: 
    + Assuming the $n^+$ gate doping so that the Fermi level in the gate corresponds with the conduction band. 
    + The electrostatic potential of $\Phi_G = 0.55 \mathrm{V}$
    + If the gate were $p^+$ doped, the value of $V_{T0} =(-0.44 + 0.55 - (-0.88) - (-0.188) - 0.002) \mathrm{V} = 1.18 \mathrm{V}$, too larger, the desired value of $V_{T0} = 0.4 \mathrm{V}$

### e)
1. According to the capacitor voltage equation $$V_T = \frac{Q}{C_{ox}} = \frac{qN}{C_{ox}}$$
2. Therefore, we can get $$N_I = \frac{C_{ox}\Delta V }{q} $$


