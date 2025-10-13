## Task 2.1
### a)
1. 已知一个inverter的delay是2ns，那么意味着在$t_d=0$时刻的输入A，在$t_d=2ns$时刻得到输出$\overline{A}$
2. 在他之后串联一个相同delay的inveter，那么意味着在$t_d=2ns$时刻的输入$\overline{A}$, 在$t=4ns$时刻得到输出$\overline{\overline{A}} = A$
3. 以此类推，如果5个相同的inverter串联，那么在 $t_d = 2 ns\cdot 5 = 10 ns $时，$B = \overline{A}$

### b)
1. 如果 A 和 B 相连，那么在$t_d = 10 ns$时，$A = B = \overline{A}$
2. 假设A的初始值时0，那么在$t_d = 10ns$时，A从0跳变成了1
3. 同理，在$t_d = 20ns$时，A从1跳变成了0
4. 所以一个周期是20ns
5. 根据频率公式$T = 1/f = 50 MHz$

## Task 2.2
1. NMOS transistor 的 structure 和 symbol可以网上或者书里找到，这里我就不画了
2. 刚开始是不稳态：当$V_{GS}$升高，NMOS进入线性区或者饱和区，$V_{OL}$ 下降从$5 \mathrm{V}$到$0 \mathrm{V}$
3. 由于寄生电容$C_{DS}$和$C_{GD}$,如果$V_{OL}$ 在很短时间内比如几十纳秒，根据电容电流公式，会产生一个瞬时大电流。
3. 当漏极电压稳定时，这是就是steady state， $$I_{DC} = \frac{V_{DD}}{R_L + R_{on}} \frac{V_{DD}-V_{OL}}{R_L}$$，纯电阻电流

## Task 2.3
### a)
1. 根据参考书第二章43页的公式（2.4）p型半导体体势, 也就是实际费米能级$E_{Fp}$与本征能级$E_{i}$之差定义为:
$$
\phi_{Fp} = \frac{kT}{q}\ln\frac{n_i}{N_A}
$$
2. 同在该参考书的44页和46页可知，强反型定义为表面电子浓度等于体内空穴浓度，这时能带弯曲使表面本征能级相对于体内翻转，其条件为
$$
2|\phi_{Fp}| = |\phi_s - \phi_{Fp}|
$$
3. Thermal voltage: $kT/q = V_T \approx 26\ \mathrm{mV}$
4. The doping level in the p-substrate:$N_A=3\times10^{17}\ \mathrm{cm^{-3}}$
5. The intrinsic carrier concentration: $n_i =1.45\times10^{10} \mathrm{cm^{-3}} $

### b)
1. the width of space charge region is the thickness $X_d$ of the depletion region
2. 根据参考书第47页公式(2.7): $$X_d = (\frac{2\epsilon_{si}|\phi_s-\phi_F|}{qN_A})^{1/2}$$
    * Dielectric constant of silicon $\epsilon_{si} = 11.7 \times \epsilon_0 (8.85 \times 10^{-14} \mathrm{As/cm})$ that dielectric constant of vacuum
    * 根据a)可知，$|\phi_s-\phi_F| = 0.88 \mathrm{V}$
    * Electron charge $q = 1.6 \times 10^{-19} \mathrm{As}$
    * The acceptor concentrations $N_A = 3 \times 10^{17} \mathrm{cm^3}$

3. 根据公式(2.9a)： the fixed negative charge $$Q_{B0} = - \sqrt{2qN_A \epsilon_{si}|-2\phi_F|}$$

### c)
1. 根据公式(2.5)$$C_{ox} = \frac{\epsilon_{ox}}{t_{ox}}$$
    * $\epsilon_{ox}$ is the dielectric constant of oxide $\epsilon_{ox} \approx 4 \epsilon_0$
    * $t_{ox}$ is the thickness of the oxide $t_{ox} = 22 \text{\r{A}} = 22 \times 10^{-8} \mathrm{cm} $
2. 根据公式(2.12)body factor $$\lambda = \frac{1}{C_{ox}}\sqrt{2q\epsilon_{si}N_A}$$

### d)
1. 根据公式(2.11) $$V_{T0} = \phi_{GC} - 2\phi_F - \frac{Q_{B0}}{C_{ox}} - \frac{Q_{ox}}{C_{ox}}$$
2. 根据Figure(2.6) $\phi_{GC} = \Phi_G - \Phi_C = \phi_{Fp} - \phi_G$
3. 根据Figure(2.4) The band gap energy of silicon is $1.1 \mathrm{eV}$, $E_i$ 处在conduction band 和 valence band之间，所以 $\phi_{GC} = -0.44 \mathrm{V} - 0.55 \mathrm{V} = -0.99 \mathrm{V}$
4. from subtask b) and c) we get $Q_{B0}/C_{ox}$
5. $$\frac{Q_{ox}}{C_{ox}} = \frac{N_{ox}q}{C_{ox}}$$
6. Gate doping: 
    + Assuming the $n^+$ gate doping so that the Fermi level in the gate corresponds with the conduction band. 
    + The electrostatic potential of $\Phi_G = 0.55 \mathrm{V}$
    + If the gate were $p^+$ doped, the value of $V_{T0} =(-0.44 + 0.55 - (-0.88) - (-0.188) - 0.002) \mathrm{V} = 1.18 \mathrm{V}$, too larger, the desired value of $V_{T0} = 0.4 \mathrm{V}$

### e)
1. 根据电容电压公式$$V_T = \frac{Q}{C_{ox}} = \frac{qN}{C_{ox}}$$
2. 所以可以得到$$N_I = \frac{C_{ox}\Delta V }{q} $$


