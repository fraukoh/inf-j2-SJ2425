# Vorbereitung auf die KA-1


## Aufgabe 1:

Erstelle ein Array mit den Namen von fünf Schülern
`["Anna", "Ben", "Clara", "David", "Eva"]` und gib jeden Namen mit dem
Text “Schüler:” davor aus.

``` python
schueler = ["Anna", "Ben", "Clara", "David", "Eva"]
for name in schueler:
    print("Schüler: " + name)
```

    Schüler: Anna
    Schüler: Ben
    Schüler: Clara
    Schüler: David
    Schüler: Eva

## Aufgabe 2:

Erstelle ein Array mit den Noten von fünf Schülern
`noten = [3.0, 2.5, 1.7, 4.0, 2.0]` und finde die beste Note.

``` python
noten = [3.0, 2.5, 1.7, 4.0, 2.0]
beste_note = noten[0]
for i in range(len(noten)):
    if noten[i] < beste_note:
        beste_note = noten[i]
print("Die beste Note ist:", beste_note)
```

    Die beste Note ist: 1.7

## Aufgabe 3:

Erstelle ein Array mit den Alter von Schülern.
`alter = [15, 18, 18, 17, 15, 16]` Ermittle die Anzahl der nicht
volljährigen Schüler und gebe sie aus.

``` python
alter = [15, 18, 18, 17, 15, 16]
anzahl = 0
for i in range(len(alter)):
    if alter[i] < 18:
        anzahl = anzahl + 1
print("Die Anzahl der Schüler unter 18:", anzahl)
```

    Die Anzahl der Schüler unter 18: 4

## Aufgabe 4:

Erstelle ein Array mit den Fächern
`["Mathematik", "Biologie", "Chemie"]` und füge das Fach “Informatik”
hinzu.

Das Fach “Informatik” soll an die zweite Stelle (= nach Mathematik)
kommen.

``` python
faecher = ["Mathematik", "Biologie", "Chemie"]
faecher.append("Informatik")
stelle = 1
for i in range(len(faecher)-1, stelle, -1):
    zwischengespeichert = faecher[i]
    faecher[i] = faecher[i-1]
    faecher[i-1] = zwischengespeichert 
print("Aktualisierte Fächer:", faecher)
```

    Aktualisierte Fächer: ['Mathematik', 'Informatik', 'Biologie', 'Chemie']

## Aufgabe 5:

Erstelle ein Array mit den Hobbys
`["Fußball", "Lesen", "Schwimmen", "Musik"]` und entferne das zweite
Element aus diesem Array.

``` python
hobbys = ["Fußball", "Lesen", "Schwimmen", "Musik"]
stelle = 1
for i in range(1, len(hobbys)-1):
    hobbys[i] = hobbys[i+1]
hobbys = hobbys[0:len(hobbys)-1]
print("Aktualisierte Hobbys:", hobbys)
```

    Aktualisierte Hobbys: ['Fußball', 'Schwimmen', 'Musik']

## Aufgabe 6:

Erstelle ein Array mit den Namen von Projekten
`["Webseite", "App", "Datenbank", "Spiel"]` und sortiere sie
alphabetisch mit BubbleSort.

``` python
projekte = ["Webseite", "App", "Datenbank", "Spiel"]
n = len(projekte) # Länge des Arrays

# BubbleSort Algorithmus
for i in range(n): # wiederhole so oft, wie viele Elemente im Array sind
    for j in range(0, n-i-1): # gehe die Elemete durch. Die Länge des Vektors wird immer kleiner
        if projekte[j] > projekte[j+1]: # wenn das aktuelle Element größer ist als der rechte Nachbar
            # Tauschen
            zwischengespeichert = projekte[j]
            projekte[j] = projekte[j+1]
            projekte[j+1] = zwischengespeichert
# Ausgeben des sortirten Arrays
print("Sortierte Projekte:", projekte)
```

    Sortierte Projekte: ['App', 'Datenbank', 'Spiel', 'Webseite']

## Aufgabe 7:

Gegeben sind zwei Arrays:

Lehrernamen:
`lehrer = ["Lisa Mayer", "Manfred Lutz", "Johannes Klug", "Markus Sommer", "Jutta Kaiser"]`  
Jeweilige Lehrerkürzel: `kuerzel = ["ma", "lu", "kl", "so", "ka"]`

Schreibe ein Programm, dass bei Eingabe eines oben genannten Kürzels der
jeweilige Lehrername angezeigt wird.

``` python
lehrer = ["Lisa Mayer", "Manfred Lutz", "Johannes Klug", "Markus Sommer", "Jutta Kaiser"]
kuerzel = ["ma", "lu", "kl", "so", "ka"]

kur = input("Bitte Lehrerkürzel eingeben:")
for i in range(len(kuerzel)):
    if kuerzel[i] == kur:
        print("Der volle Name der Lehrkraft mit dem Kürzel", kur, "ist", lehrer[i])
```

    Der volle Name der Lehrkraft mit dem Kürzel kl ist Johannes Klug
