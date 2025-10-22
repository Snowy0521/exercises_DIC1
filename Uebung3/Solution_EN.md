## Task 3.1
### a)
1. According to equation (2.11) of the reference book $$V_{T0} = \phi_{GC} - 2\phi_F - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
2. For NMOS: $$V_{T0n} = \phi_{GC} - 2\phi_{Fp} - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
    + $$\phi_{GC} = \phi_{Fp} - \phi_{G} = ( -0.44 - 0.55 ) \mathrm{V} = -0.99  \mathrm{V}$$
    + $$2\phi_{Fp} = -0.88 \mathrm{V}$$
    + $$\frac{Q_{B0}(\text{elctrons})}{C_{ox}} = \frac{- \sqrt{2qN_A \epsilon_{si}|-2\phi_F|}}{\frac{\epsilon_{ox}}{t_{ox}}} = -0.188 \mathrm{V}$$
    + $$\frac{Q_{ox}}{C_{ox}} = \frac{N_{SS}q}{C_{ox}} = 0.06 \mathrm{V}$$

3. For PMOS: $$V_{T0p} = \phi_{GC} - 2\phi_{Fn} - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
    + $$\phi_{GC} = \phi_{Fn} - \phi_{G} = (0.44 - (-0.55) ) \mathrm{V} = 0.99  \mathrm{V}$$
    + $$2\phi_{Fn} = 0.88 \mathrm{V}$$
    + $$\frac{Q_{B0}(\text{holes})}{C_{ox}} = \frac{+ \sqrt{2qN_A \epsilon_{si}|-2\phi_F|}}{\frac{\epsilon_{ox}}{t_{ox}}} = 0.188 \mathrm{V}$$
    + $$\frac{Q_{ox}}{C_{ox}} = \frac{N_{SS}q}{C_{ox}} = 0.06 \mathrm{V}$$

### b)
1. donors are elctrons, acceptors are holes 
2. If a PMOS gate is doped with electrons instead of acceptors:
$$\phi_{GC} = \phi_{Fn} - \phi_{G} = (0.44 - 0.55)  \mathrm{V} = -0.11  \mathrm{V}$$
3. The new $V_{T0p} = (-0.11 \mathrm{V}) - (0.88 \mathrm{V}) - (0.188 \mathrm{V}) - (0.06 \mathrm{V}) = -1.24 \mathrm{V}$
4. Notation: 
    + For NMOS, it has P-substrate, $\phi_{Fp} < 0$, i.e., $\phi_{Fp} = -0.44 \mathrm{V}$:
        + If its gate is doped with elctrons $\phi_G = 0.55 \mathrm{V}$
        + If its gate is doped with holes $\phi_G = -0.55 \mathrm{V}$
    + For PMOS, it has N-substrate, $\phi_{Fn} > 0$, i.e., $\phi_{Fn} = 0.44 \mathrm{V}$:
        + If its gate is doped with elctrons $\phi_G = 0.55 \mathrm{V}$
        + If its gate is doped with holes $\phi_G = -0.55 \mathrm{V}$

### c)
1. Calculate the amount implanted icons per square centmeter to reach the desired $V_{T0n} = 0.4 \mathrm{V}$ and $V_{T0p} = -0.4 \mathrm{V}$
2. According the capacitor voltage equation: $$Q = q \times N_I = C_{ox} \times (V_d-V_a)$$

### d)
1. To make sure that absolute value of threshold voltage isn't greater than $V_{DD}$
2. With $0.13 \mathrm{\mu m}$ technology node, the supply voltage $V_{DD} = 1.2 \mathrm{V}$

### e)
1. According to the equation (2.21) on page 59 of reference book:
    $$\mu_e = \frac{\mu_0}{1 + (\frac{V_{GS}- V_{T}}{\theta \cdot t_{ox}})^{\eta}}$$
    + given the nomimal mobility $\mu_0 = 130 \mathrm{cm}^2\mathrm{V}^{-1}\mathrm{s}^{-1}$
    + $\theta = 4 \cdot 10^6 \mathrm{Vcm}^{-1}$
    + $\eta = 1.85$
    + In the $0.13 \mathrm{\mu m}$ technology, the thickness of the oxide $t_{ox} = 22 \text{\r{A}} = 22 \times 10^{-8} \mathrm{cm} $
    + $V_{GS} - V_{T} = 1.2 \mathrm{V} - 0.4 \mathrm{V} = 0.8 \mathrm{V}$

## Task 3.2
### a)
1. According to the equation (2.22) on page 60 of reference book:
    + The electric field of $E_{cn} = 6 \cdot 10^4$ V/cm for electrons and $E_{cp} = 24 \cdot 10^4$ V/cm for holes.
    + $E_{cn}L = 6 \cdot 10^4 \cdot 200 \cdot 10^{-7} = 1.2 \mathrm{V}$
    + $E_{cp}L = 24 \cdot 10^4 \cdot 200 \cdot 10^{-7} = 4.8 \mathrm{V}$
2. According to the equation (2.28) on page 62 of reference book:
    + $$V_{Dsat} = \frac{(V_{GS}-V_T)E_cL}{(V_{GS}-V_T) + E_cL}$$
3. For NMOS: $$V_{Dsat} = \frac{(V_{GS}-V_{TN})E_{cn}L}{(V_{GS}-V_{TN}) + E_{cn}L} = \frac{(1.8 - 0.5)(1.2)}{1.8 - 0.5 + 1.2} \mathrm{V} = 0.6 \mathrm{V} $$

4. For PMOS: $$V_{Dsat} = \frac{(V_{SG}-|V_{TP}|)E_{cp}L}{(V_{SG}-|V_{TP}|) + E_{cp}L} = \frac{(1.8 - 0.5)(4.8)}{1.8 - 0.5 + 4.8} \mathrm{V} = 1.0 \mathrm{V} $$

### b)
1. the same as a)
2. For NMOS $$V_{Dsat} = \frac{(V_{GS}-V_{TN})E_{cn}L_n}{(V_{GS}-V_{TN}) + E_{cn}L_n} = \frac{(1.2 - 0.4)(0.6)}{1.2 - 0.4 + 0.6} \mathrm{V} = 0.34 \mathrm{V} $$

3. For PMOS: $$V_{Dsat} = \frac{(V_{SG}-|V_{TP}|)E_{cp}L_p}{(V_{SG}-|V_{TP}|) + E_{cp}L_p} = \frac{(1.2 - 0.4)(2.4)}{1.2 - 0.4 + 2.4} \mathrm{V} = 0.6 \mathrm{V} $$

### c)
1. According to the equation (2.29) on page 64 of reference book:
$$\frac{I_{DsatN}}{I_{DsatP}} = \frac{W_N v_{sat} C_{ox}(V_{GS}-V_{TN})^2/(V_{GS} - V_{TN} + E_{cn}L_n)}{W_P v_{sat} C_{ox}(V_{SG}-|V_{TP}|)^2/(V_{SG} - |V_{TP}| + E_{cp}L_p)}$$

2. Simplified as $$\frac{I_{DsatN}}{I_{DsatP}} = \frac{(V_{GS}-V_{TN})^2/(V_{GS} - V_{TN} + E_{cn}L_n)}{(V_{SG}-|V_{TP}|)^2/(V_{SG} - |V_{TP}| + E_{cp}L_p)} = \frac{(1.2-0.4)^2/(1.2 - 0.4 + 0.6)}{(1.2-0.4)^2/(1.2 - 0.4 + 2.4)}$$

3. Simplified as $$\frac{I_{DsatN}}{I_{DsatP}} = \frac{1.2 - 0.4 + 2.4}{1.2 - 0.4 + 0.6} \approx 2.3$$


## Task 3.3
### a)
1. From the previous Task, we know that $$\frac{I_{DsatN}}{I_{DsatP}} = 2.3$$
2. Therefore, when the width-to-length ratios of NMOS and PMOS are the same, the $I_{DsatN}$ of $1 \times NMOS$ is 2.3 times the $I_{DsatP}$ of $1 \times PMOS$.
3. Thus, when the PMOS width is $W_P = 2 W_N$, from equation (2.29), the ratio of $I_{Dsat}$ for $1 \times NMOS$ and $2 \times PMOS$ is $2.3/2$.
4. Similarly, when the PMOS width is $W_P = 3 W_N$, the ratio of $I_{Dsat}$ for $1 \times NMOS$ and $3 \times PMOS$ is $2.3/3$.
5. For the same NMOS or PMOS, its $I_{Dsat}$ also changes with the change in $V_{SG}$ (or $V_{GS}$).
6. Therefore, according to equation (2.29), the ratio of $I_{Dsat}$ for $1 \times PMOS$ with $V_{SG} = 1.2 \mathrm{V}$ and $1 \times PMOS$ with $V_{SG} = 0.8 \mathrm{V}$ is $8/1$.
7. When $V_{SG} = 0.4 \mathrm{V} = |V_{TP}|$, the PMOS is at the boundary of the cutoff region, so ideally, neglecting factors such as subthreshold conduction, channel length modulation, or body effect, the $I_{DsatN}$ of NMOS and the $I_{DsatP}$ of PMOS are both 0.

### b)
1. For NMOS, when $V_{GS} \leq V_{TN}$, it is in the cutoff region, so $I_{DS} = 0$ in the ideal situation.
2. When $V_{GS} > V_{TN}$ and $V_{DS} \geq V_{GS} - V_{TN} \to V_{GS} \leq V_{DS} + V_{TN}$, it is in the saturation region, so $$I_{DS} = \frac{1}{2}\mu_n c_{ox} \frac{W}{L}(V_{GS} - V_{TN})^2$$ (e.g. 2.19), neglecting $\lambda$, channel length modulation.
3. When $V_{GS} > V_{TN}$ and $V_{DS} < V_{GS} - V_{TN} \to V_{GS} > V_{DS} + V_{TN}$, it is in the linear region, so $$I_{DS} = \mu_n c_{ox} \frac{W}{L}(V_{GS} - V_{TN} - \frac{V_{DS}}{2})V_{DS}$$ (e.g. 2.17b).

## Task 3.4
1. Mathematical calculation problem. Do it yourself and compare with the reference answer.