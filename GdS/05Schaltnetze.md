- Transistor: elektrischer Schalter
- $k$ Eingabebits haben $2^{k}$ Zeilen und $2^{2^{k}}$ Ausgaben

| A   | B   | A XOR B |
| --- | --- | -------- |
| 0   | 0   | 0        |
|  1  | 0   | 1        |
| 0   | 1   | 1        |
| 1  | 1   | 0        |

 - alles mit NAND und NOR darstellbar
- $(A \bar{\land} B) \bar{\land} (A n\bar{\cap} B) \equiv A \land B$
- $(A \bar{\land}A) \equiv \bar{A}$
- $\bar{A} \bar{\land} \bar{B} \equiv A \lor B$
- $[A \bar{\land} (A \bar{\land} B)] \bar{\land}[B\bar{\land}(A \bar{\land} B)] \equiv A \text{ XOR } B$  

hier nochmal üben, da Klausuraufgaben
Hauptsatz der Schaltalgebra
- Erzeugendensysteme, die jede binäre Funktion darstellen können (NAND, XOR)
- Normalformen: disjunktive Normalform (DNF) und konjunktive Normalform (KNF)
- Hilfsfunktion oder Minterm (nur 1 bei einem spezifischem Fall) verodert
- jeder Input ist 1 oder wird verneint
- DNF: $(A \land \neg B) \lor (\neg A \land \neg B)$ 
- KNF: $(A \lor B) \land(\neg A \lor\neg B)$ 
- nicht mischen (nachfragen)
- 555c
- Vorteil: leicht ablesbar
- Nachteile: groß, viele Grundkomponenten
![[Screenshot 2023-12-09 at 17.27.51.png|300]]
- Konvention: Verneinungsknubbel erlaubt
- offene Knubbel sind Start oder Ende
- geschlossene Teile Leitungen oder vereinigen
![[Screenshot 2023-12-12 at 19.40.31.png|300]]
- ein & repräsentiert ein Teil der DNF

###### Dekodierer
- $k$ Eingänge
- $2^{k}$ Ausgänge
- genau einer ist 
![[Screenshot 2023-12-12 at 19.54.04.png|300]]![[Screenshot 2023-12-12 at 19.54.23.png|300]]
###### Kodierer
- $2^{k}$ Eingänge, wobei nur einer $1$ sein darf, sonst undefiniert
- $k$ Ausgänge
- DEC andersherum
###### Multiplexer
- $n$ Steuereingängen
- $2^{n}$ Eingabeeingängen
- Steuerleitungen geben an, welche Eingabeeingänge an den Output weitergeleitet werden
- falls sich Eingänge langsamer verändern als periodisches Umschalten der Steuerleitungen dauert und es keine Überlappung der Signale gibt, können Eingangssignale vereinigt werden
- "tauscht" Zeit für weniger Kabel
![[Screenshot 2023-12-12 at 20.09.39.png|250]]
###### Demux
- Gegenteil des Muxs
- verteilt schnelle Eingabe auf mehrere Kabel

Komparator zum Vergleich von zwei 2-Bit Zahlen bauen (1, wenn erste größer gleich zweiter)
(KNF)
![[Screenshot 2023-12-13 at 15.56.04.png|400]]

Zeit
- Gatter sind Schalter mit nicht vernachlässigbaren Verzögerungen
- Gatter schalten in gewisser Zeit
- t ~ Anzahl in Reihe geschalteter Gatter (Grundelemente)
- NAND ist Grundschaltnetz, deswegen schneller als NOT usw.
- dies ist aber vernachlässigbar
