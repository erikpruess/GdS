Schaltwerk sind Flip Flops
Schaltnetz braucht im Gegensatz zu Schaltwerk Zeit für Änderung
Schaltnetz besteht aus mindestens zwei Funktionen (für Ausgabe und nächsten Zustand)
endlicher Automat hat endlich viele Zustände, Eingaben und erzeugbare Ausgaben
### Variante 1: Mealy
![[Screenshot 2023-11-07 at 11.21.22.png]]
Ausgabe wird aus Zustand vor der Eingabe berechnet? (es wird vom neuen Ergebnis ausgegangen)

![[Screenshot 2023-11-07 at 11.28.47.png]]
Übergang von s1 zu s2 passiert zwischen Takt des Computer. 
jedes Taktsignal kann als Ereignis werden, allerdings nicht zwingend Ausgabeänderung
Zustandsänderung nur zu Taktzeiten. Implizit, kann daher weggelassen werden.
Mealy-Automat ein sehr allgemeiner Automat
Falls keine Ausgabe, aber Funktion, die Zustand änder, wird eine leere eMenge ausgegeben


für Speicher zu Speicher:
1. von Register zu Register, mehr Zeit (hier nochmal in der Vorlesung anchschauen: 07.11 1540)
2. Speicher zu Speicher mit zwei Addressbussen
