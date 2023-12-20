Leistungsbeurteilung einer CPU (bzw. Core):
- erfolgt durch Metriken (bestimmbare und quantifizierbare Systemeigenschaft)
- Metrik brauchen Messung mit Maß (Einheit)
- Metrik sollte **objektiv** (unabhängig vom Messer sein), **valide** (relevant für gewünschte Einschätzung) und wiederholbar (**reliabel** ohne Messfehler) sein 
- bei Computern: Validität und Objektivität gegeben, Reliablität nicht unbedingt (andere Programme laufen, Internet schlecht, Akkumulator niedrig, Prozessor heiß)

###### Programmausführungszeit
T= t_Ende - t_Start
CPU time (wie lange hat sich die CPU mit diesem Programm beschäftigt? Macht Messung unabhängig von parallel laufenden Programmen)
es gibt nicht eine spezifische Ausführungszeit
interessant für einen PC

###### Durchsatz (throughput)
Anzahl der beendeten Aufgaben oder Programme / Zeiteinheit
bei schnellem Wechsel zwischen Aufgaben leidet der Durchsatz, da zwischen Aufgaben wechseln auch CPU Zeit kostet
wichtige Metrik in Rechenzentren
###### Energieeffizienz
- absoluter Energieverbrauch nicht aussagekräftigt
- stattdessen: durchgeführte Instruktionen / benötigte elektrische Energie [] = Instruktionen / Joule
- Strommessung ist schwierig
- immer relevant

Beispiel: Ausführungszeit
CPI (cycles per instruction)
![[Screenshot 2023-12-05 at 11.46.54.png|300]]

![[Screenshot 2023-12-05 at 11.53.48.png|400]]

![[Screenshot 2023-12-05 at 11.55.13.png|400]]
Takt: hier eine Mikroinstruktion
Einflussfaktor: Zyklen pro Instruktion, CPI, Taktfrequenz
![[Screenshot 2023-12-05 at 12.10.02.png|400]]
Um CPUs vergleichbar zu machen: Benchmarks

Auslastung in Prozent keine gute Metrik, da leicht zu verfälschen
auch MIPS (millions instructions per second): führt zu 0 + 0 = 0
- Zuverlässigkeit
- oder steady state availability (Wahrscheinlichkeit das System zu einem zufälligen Zeitpunkt operationsbereit vorzufinden)
- Mean time to failure, mean time to repair, 