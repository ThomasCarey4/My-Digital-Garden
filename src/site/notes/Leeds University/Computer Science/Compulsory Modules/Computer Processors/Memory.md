---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-processors/memory/"}
---

#TODO i missed half of it
#TODO Truth tables
#### Shift [[Leeds University/Computer Science/Compulsory Modules/Computer Processors/Registers\|Registers]] (Serial IN $\rightarrow$ Serial OUT)
![Shift Register.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Processors/images/Shift%20Register.png)
FF = Flip Flop
#### Serial IN $\rightarrow$ Parallel OUT (SIPO)
![SIPO Diagram.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Processors/images/SIPO%20Diagram.png)
#### Parallel IN $\rightarrow$ Serial OUT
![PISO Diagram.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Processors/images/PISO%20Diagram.png)
Shift/Load alternates signal
Parallel input is ‘moved’ along the bottom and ‘squeezed’ out of the output in serial
#### Counter
Can do three things
- Increment by 1
- Set to a specific value
- Reset
(Think Program Counter)
(Why are we count 1-2-4-3)
![Counter.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Processors/images/Counter.png)
$D_{0}=\neg Q_{0}$ (because its the 1 bit)
$D_{1}=(Q_{0} \land \neg{Q_{1}}) \lor (\neg{Q_{0}}\land Q_{1})$
$D_{2}=(\neg{Q_{1}}\land Q_{2})\lor(\neg{Q_{0}}\land Q_{2})\lor(Q_{0}\land Q_{1} \land \neg{Q_2})$
$\ \ \ \ \ =((\neg{Q_{0}}\lor \neg Q_{1})\land Q_{2}) \lor (Q_{0}\land Q_{1}\land \neg{Q_{2}})$
$D_{3}=((\neg{Q_{0}}\lor\neg{Q_{1}}\lor\neg{Q_{2}})\land Q_{2})\lor(Q_{0} \land Q_{1} \land Q_{2} \land \neg{Q_{3}})$
![Counter Diagram?.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Processors/images/Counter%20Diagram?.png)
wtf is going on
