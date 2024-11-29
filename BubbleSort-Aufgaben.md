# Aufgabe 1: Bubble Sort – Lottozahlen


Die Zahlen der aktuellen Lottoziehung liegen in der Reihenfolge der
Ziehung in einem Array lotto vor `[48, 5, 17, 32, 7, 29]` und sollen
noch sortiert werden. Sie erhalten den Auftrag, ein entsprechendes
Programm zu entwickeln, das die Lottozahlen mit Hilfe des
Sortieralgorithmus ‘Bubble Sort’ sortiert und die sortierten Zahlen in
der Konsole ausgibt.

``` python
messwerte = [48, 5, 17, 32 , 7, 29]
laenge = len(messwerte)

#Sortieren
for i in range(1,laenge):
    for j in range(0,laenge-i):
        if messwerte[j] > messwerte[j+1]:
            zwischenspeicher = messwerte[j]
            messwerte[j] = messwerte[j+1]
            messwerte[j+1] = zwischenspeicher

#Ausgabe
print(messwerte)
```

    [5, 7, 17, 29, 32, 48]

[Struktogramm](BubbleSort-Aufgaben_files/figure-html/673b392b-1-image.png)

# Aufgabe 2: Sortieren von Büchern

In einer Bibliothek sind die Bücher einer Kategorie
durcheinandergeraten. Die Bücher sind durch ihre ISBN-Nummern
repräsentiert und in einem Array buecher gespeichert,  
z.B.
`[9783866801929, 9783957311320, 9783442267743, 9783423214599, 9783442314928]`.

Schreiben Sie ein Programm, das die ISBN-Nummern mit dem
Bubblesort-Algorithmus aufsteigend sortiert und die sortierten
ISBN-Nummern in der Konsole ausgibt.

``` python
messwerte = [9783866801929, 9783957311320, 9783442267743, 9783423214599, 9783442314928]
laenge = len(messwerte)

#Sortieren
for i in range(1,laenge):
    for j in range(0,laenge-i):
        if messwerte[j] > messwerte[j+1]:
            zwischenspeicher = messwerte[j]
            messwerte[j] = messwerte[j+1]
            messwerte[j+1] = zwischenspeicher

#Ausgabe
print(messwerte)
```

    [9783423214599, 9783442267743, 9783442314928, 9783866801929, 9783957311320]

# Aufgabe 3: Sortieren von Messwerten

In einem wissenschaftlichen Experiment wurden Messwerte erfasst und in
einem Array messwerte gespeichert,  
z.B. `[12.5, 7.8, 3.14, 9.7, 6.2]`. Die Messwerte sollen nun für die
weitere Analyse aufsteigend sortiert werden.

Entwickeln Sie ein Programm, welches die Messwerte mittels Bubblesort
sortiert und sowohl die unsortierten als auch die sortierten Werte in
der Konsole ausgibt.

``` python
messwerte = [12.5, 7.8, 3.14, 9.7, 6.2]
laenge = len(messwerte)

#Sortieren
for i in range(1,laenge):
    for j in range(0,laenge-i):
        if messwerte[j] > messwerte[j+1]:
            zwischenspeicher = messwerte[j]
            messwerte[j] = messwerte[j+1]
            messwerte[j+1] = zwischenspeicher

#Ausgabe
print(messwerte)
```

    [3.14, 6.2, 7.8, 9.7, 12.5]
