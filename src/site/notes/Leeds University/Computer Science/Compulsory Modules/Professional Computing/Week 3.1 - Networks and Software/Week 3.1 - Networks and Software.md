---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/professional-computing/week-3-1-networks-and-software/week-3-1-networks-and-software/"}
---

#### Network Convergence

```mermaid
graph TD
subgraph Wired
	direction TB
	A[Simple Lead]
	<--> B[USB Cable]
	<--> C[Ethernet RJ45 Cable]
	<--> D[Fibre Optic]
end
subgraph identifier[" "]
	direction TB
	K[Phone Networks]
	<---> J[Internet]
end
subgraph Wireless
	direction TB
	E[Very Low RF]
	<--> F[ZigBee]
	<--> G[Bluetooth]
	<--> H[Wi-Fi]
	<--> I[Ethernet RJ45 Cable]
end
D <--> J
J <--> I
```
