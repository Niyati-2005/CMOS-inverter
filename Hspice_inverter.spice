* HSPICE Code
*inverter using Finfet
.include "7nm_TT_160803.txt"
.option post
Vdd 3 0 dc 0.8
M1 2 1 0 0 nmos_lvt
M2 2 1 3 3 pmos_lvt
Vin 1 0 pulse(0 0.8 0.1p 0.1p 0.1p 10n 20n)
.tran 1p 40n
.measure tphl trig V(1) val=0.4 rise=1 targ V(2) val=0.4 fall=1
.measure tplh trig V(1) val=0.4 fall=1 targ V(2) val=0.4 rise=1
.measure trise trig V(1) val=0.08 rise=1 targ V(2) val=0.72 rise=1
.measure tfall trig V(1) val=0.72 fall=1 targ V(2) val=0.08 fall=1
.measure AvgPower AVG P(Vdd)
.print V(2)
.end
