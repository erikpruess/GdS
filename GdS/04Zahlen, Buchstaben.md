$k$ Bits, erlaubt $2^k$ Unterscheidungen
Zahlen $0 ... 2^k-1$
$\sum ^{k-1}_{i=0}2^{i}b_{i}$ = Dualzahlinterpretation
>[!Example]
>$1001 = 2^3+2^0=9$

1. Vorzeichenbit
	$(1-2s)\sum^{k-2}_{i=0}2^{i}b_{i}$
	Erstes Bit ist Vorzeichenbit: $1=-$
	Nachteil: 
	- Addition kompliziert, da Fallunterscheidung notwendig
	- zwei Nullen ($+0, -0$)
	Vorteil: 
	- Multiplikation ist einfach, da unterschiedliche Bits $-$ werden und gleiche $+$
	- Negation ist trivial
	- Fallunterscheidung trivial (es muss nur das erste Bit berechnet werden)
	- intuitiv
2. Einerkomplement
	- "Vorzeichenbit" bedeutet, dass nachfolgende Bits geflippt werden
	- $001=1$
	- $101=-2$
	- Vor- und Nachteile sind wie Vorzeichenbit
	- Sonderall bei Nullüberschreitender Addition (Nachteil)
3. Zweierkomplement
	$\left( \sum^{k-2}_{i=0}2^{i}b_{i} \right)-b_{k-1}\cdot2^{k}$
	$1001 = -8 + 1 = -7$
	$0000 = 0$
	Vorteil:
	- Fallunterscheidung trivial
	- alle Rechenoperation sind einfach
	- Negation leicht schwieriger (jedes Bit invertieren und $+1$ rechnen)
	- WARUM?
	- nur eine Null	
	Berechnung:
	- $-5= 1111011$, also alle, außer $|5| - 1$ 
	- kürzer: alles Invertiere und $+1$
4. Fließkommazahl (IEEE754)
	- $x = (-1)^{s} \cdot m \cdot 2^{e}$
	- $s$ ist Vorzeichenbit
	- $m \in [1, 2)$
	- $\tilde{m} = \sum_{k=0}^{22} 2^{k-23} \cdot m_{k}$ (somit $\frac{1}{2} \cdot m_{k}+ \frac{1}{4} \cdot m_{k}\dots \frac{1}{2^{-23}} \cdot m_{k}$)
			- $m = 1 + \frac{\hat{m}}{2^{23}}$ (die 1 ist implizit. Es entsteht immer eine Zahl <1, die dann mit 1 addiert wird. $\frac{2^{2}}{2^{23}}=1^{2-23}$)
	- $(m-1)\cdot2^{23}=\tilde{m}$
	- $e=\tilde{e}-127$
	- ![[Screenshot 2023-12-06 at 16.05.04.png]]
	- ![[Screenshot 2023-12-09 at 14.00.20.png|500]]
	- bei Addition von sehr großen und kleinen Zahlen können kleine unter den Tisch fallen

##### Buchstaben
- ASCII: 7 Bits, die für Sonderzeichen, Zahlen und englisches Alphabet reichen
- UTF-8 (Unicode): erstes Zeichen gibt an, wie viele folgen
- enthält Redundanzbits
![[Screenshot 2023-12-09 at 14.20.56.png|400]]

