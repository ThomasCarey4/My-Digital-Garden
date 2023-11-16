---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/cw-1-notes/","tags":["Hidden"]}
---

###### That really fucking annoying question:

$$
\begin{align*}
200 &= 0000 \\
201 &= 0001 \\
202 &= 0000 \\
203 &= 0001 \\
204 &= x \\ \\
201 \to AC &= 0001 \\
AC \to 202 &= 0001 \\ \\
200 \to AC &= 0000 \\
201\ +\ AC &= 0001 \\
AC \to 201 &= 0001 \\
202 \to AC &= 0001 \\
AC \to 200 &= 0001 \\
204 \to AC &= x \\
AC\ -\ 203; AC &= x - 0001 \\
\text{If AC} &= 0\text{; END} \\
AC \to 204 &= x - 0001 \\
RES&TART

\end{align*}
$$

After first run...
202 = 201 = 1
201 = 200 + 201 = 1
200 = 201 = 1
After the others
202 = 201
201 = 201 + 201
200 = 201


| x | v200 | v201 |
|:-:|:-:|:-:|
|1|1|1|
|2|1|2|
|3|2|3|
|4|3|5|
|5|5|8|
|6|8|13|
|7|13|21|
|8|21|34|

###### what the fuck is going on
$x = 1010$
$\set{1,10,11,100}$
$Parity = \set{1,10,100}$
$Data = \set{11}$
