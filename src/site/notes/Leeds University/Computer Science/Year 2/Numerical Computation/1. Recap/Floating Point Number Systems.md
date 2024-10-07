---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/numerical-computation/1-recap/floating-point-number-systems/"}
---


###### Scientific Notation:
$1294.8=1.2948\times10^{3}$
$-0.034=-3.4\times10^{-2}$
$\pi=3.1415926\dots\times10^{0}$
###### Computer Representation:
Any finite precision number ${\color{red} x}$ can be *uniquely* written using the ***Normalised Floating Point Representation System***
$$
\large
{\color{red} x}=\pm0.b_{1}b_{2}b_{3}\dots b_{t-1}b_{t}\times\beta^{\color{lightgreen} e}
$$
where
- $\beta$ is the base – a *positive* integer. (e.g. 2 for binary)
- ${\color{lightgreen} e}$ is the exponent – an integer: $L\leq {\color{lightgreen} e}\leq U$
- $b_{i}$ are integers: $0< b_{1}\leq \beta-1$ and $0\leq b_{i}\leq\beta-1,(i=2,3,\cdots t)$
	- The first $b$ *cannot* be $0$ because it is ***Normalised***

$(\beta,t,L,U)$ fully defines a finite precision number system.
$(\text{Base, Decimal Points, Minimum Exponent, Maximum Exponent})$

The IEEE *single precision standard* is $(\beta,t,L,U)=(2,23,-127,128)$
```{python} numpy.single```
The IEEE *double precision standard* is $(\beta,t,L,U)=(2,52,-1023,1024)$
```{python} numpy.double```
