# Übungsaufgaben zu Arrays in python


# Aufgabe 1

## Ausgabe von Arrays – Vereinsmeisterschaften

Der Mühlberger SC ist ein Sportverein mit mehreren Abteilungen. Im Jahr
2016 eröffnete der Mühlberger SC die Abteilung DART. Seit dem Jahr 2017
finden auch Vereinsmeisterschaften statt.

Die Vereinsmeisterschaft in diesem Jahr war ein großer Erfolg. Die
Spieler lieferten sich einen spannenden Wettkampf vor vielen Zuschauern.
Der Mühlberger SC möchte die Ergebnisse des Wettkampfs veröffentlichen.
Nutzer sollen die Möglichkeit haben, sich an einem Computer eine
Platzierung ausgeben zu lassen. Möchte der Nutzer den Erstplatzierten
ausgegeben bekommen, muss er bspw. eine „1“ eingeben. Außerdem soll die
Teilnehmerzahl angezeigt werden. Die Teilnehmer an der Meisterschaft
sind in dem Array platzierungen in der Reihenfolge ihrer Platzierung
gespeichert:

\[“Matthias Schmitt”, “Felix Holzmann”, “Sabrina Eggers”, “Sebastian
Wolf”, “Niklas Eisenbaum”, “Florian Kuster”, “Jan Ackerman”, “Erika
Ebersbacher”\]

``` python
platzierungen = ["Matthias Schmitt", "Felix Holzmann", "Sabrina Eggers", "Sebastian Wolf", "Niklas Eisenbaum", "Florian Kuster", "Jan Ackerman", "Erika Ebersbacher"]
platz=int(input("Platzierung?: "))
print("Platzierung:", platzierungen[platz-1])
print("Teilnehmerzahl:", len(platzierungen))
```

    Platzierung?:  1
    Platzierung: Matthias Schmitt
    Teilnehmerzahl: 8

[Struktogramm](Array-Aufgaben_files/figure-html/d84b5e0c-15f0-49ea-b46c-3460aa237d32-1-4fa2810a-0460-4e1b-beda-b3213590157d.png)

# Aufgabe 2:

### Implementierung von Arrays – Gewinnziehung

Der Mühlberger SC ist ein Sportverein mit mehreren Abteilungen. Im Jahr
2016 eröffnete der Mühlberger SC die Abteilung DART. Seit 2016
veranstaltet der Verein jährlich einen großen Darts-Event. Bei dem
Dart-Event gibt es eine große Gewinnlotterie mit großartigen
Sachpreisen. Dafür konnten sich Interessierte ein Los kaufen. Am Abend
des Dart-Events findet die Ziehung der Gewinnerlose statt. Der
Ziehungsleiter soll die Möglichkeit erhalten, die gezogenen Losnummern
in einem Array zu speichern. Nachdem die fünf Losnummern mit Gewinnen
gezogen worden sind, sollen sie ausgegeben werden.

``` python
# Deklaration und Initialisierung des Arrays
losnummern = []

# Einlesen von 5 Gewinnerlosen
for i in range(5):
    nr = input("Gezogene Losnummer: ")
    losnummern.append(nr)

# Ausgabe des Arrays
print("---Gewinnlose---")

for i in range(5):
    print(losnummern[i])
```

    Gezogene Losnummer:  1254
    Gezogene Losnummer:  2365
    Gezogene Losnummer:  4587
    Gezogene Losnummer:  5698
    Gezogene Losnummer:  3146
    ---Gewinnlose---
    1254
    2365
    4587
    5698
    3146

[Struktogramm](Array-Aufgaben_files/figure-html/156a1a61-6407-41fd-9109-8c75ba776514-1-187ffba3-305f-43ff-abe9-677e6d14b14b.png)

# Aufgabe 3:

# Implementierung von Arrays – Trainingsanalyse

Im Training für die Vereinsmeisterschaften wirft jeder Dartspieler 6
Pfeile auf die Dartscheibe bevor der nächste Dartspieler an der Reihe
ist. Sie sollen ein Programm schreiben, das aufgrund der 6 geworfenen
Pfeile eine Analyse durchführt.  
Es sollen folgende Angaben in der Konsole ausgegeben werden: Höchste
Punktzahl, niedrigste Punktzahl und die durchschnittliche Punktzahl. Die
Eingaben der Wurfergebnisse erfolgten ebenfalls über die Konsole (Bei
einem Wurf sind maximal 60 Punkte erreichbar.)

``` python
#Deklaration und Initialisierung leeres Array
wuerfe = []

# Einlesen der Würfe
for i in range(6):
    wurf = int(input("Wurf: "))
    wuerfe.append(wurf)

#Deklaration und Initialisierung der Variablen
maxP = wuerfe[0]
minP = wuerfe[0]
mittelP = 0

# Bester Wurf
for i in range(len(wuerfe)):
    if wuerfe[i] > maxP:
        maxP = wuerfe[i]

# Schlechtester Wurf
for i in range(len(wuerfe)):
    if wuerfe[i] < minP:
        minP = wuerfe[i]
        
# Durchschnittliche Punktzahl pro Wurf
for i in range(len(wuerfe)):
    mittelP = mittelP + wuerfe[i]

mittelP = mittelP / len(wuerfe)

#Ausgabe
print("Bester Wurf:", maxP)
print("Schlechtester Wurf:", minP)
print("Durchschnittliche Punktzahl:", mittelP)
```

    Wurf:  5
    Wurf:  40
    Wurf:  3
    Wurf:  60
    Wurf:  30
    Wurf:  20
    Bester Wurf: 60
    Schlechtester Wurf: 3
    Durchschnittliche Punktzahl: 26.333333333333332

[Struktogramm](Array-Aufgaben_files/figure-html/e1f15f8b-c1a7-4a15-a428-e44cb9319f06-1-78615a06-b0ad-4257-aaa2-e7ac6f09fae3.png)
