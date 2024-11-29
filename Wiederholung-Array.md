# Wiederholung zu Arrays in Python


# Aufgabe 1:

Erzeuge ein leeres Array namens `mein_array`.

``` python
mein_array = []
print(mein_array)
```

    []

# Aufgabe 2:

Füge die Zahlen 1 bis 5 zu `mein_array` hinzu.

``` python
mein_array = [1, 2, 3, 4, 5]
print(mein_array)
```

    [1, 2, 3, 4, 5]

# Aufgabe 3:

Erzeuge ein Array mit den Wochentagen.

``` python
tage = ["Montag", "Dienstag", "Mittwoch", "Donnerstag", "Freitag", "Samstag", "Sonntag"]
print(tage)
```

    ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag', 'Samstag', 'Sonntag']

# Aufgabe 4:

Lies das erste Element von `tage` aus.

``` python
erstes_element = tage[0]
print(erstes_element)
```

    Montag

# Aufgabe 5:

Lies das letzte Element von `tage` aus.

``` python
letztes_element = tage[-1]
print(letztes_element)
```

# Aufgabe 6:

Bestimme die Länge von `mein_array`.

``` python
laenge_mein_array = len(mein_array)
print("Die Länge von mein_array:", laenge_mein_array)
```

    Die Länge von mein_array: 5

# Aufgabe 7:

Bestimme die Länge von `tage`.

``` python
laenge_tage = len(tage)
```

# Aufgabe 8:

Schleife durch `mein_array` und gib jedes Element aus.

``` python
for ind in range(len(mein_array)):
    print(mein_array[ind])
```

    1
    2
    3
    4
    5

# Aufgabe 9:

Schleife durch `tage` und gib jedes Element aus.

``` python
for ind in range(len(tage)):
    print(tage[ind])
```

    Montag
    Dienstag
    Mittwoch
    Donnerstag
    Freitag
    Samstag
    Sonntag

# Aufgabe 10:

Erzeuge ein Array mit den Zahlen 10 bis 20. Verwende dabei den
range-Befehl

``` python
zahlen = range(10, 21)
print(zahlen)
```

    range(10, 21)

# Aufgabe 11:

Gib die geraden Zahlen aus `zahlen` aus. \> Hinweis: Um zu überprüfen,
ob die Zahl gerade ist, verwendet man den %-Operator. Recherchiere
selber, wie der %-Operator funktioniert.

``` python
for ind in range(len(zahlen)):
    if zahlen[ind] % 2 == 0:
        print(zahlen[ind])
```

    10
    12
    14
    16
    18
    20

# Aufgabe 12:

Gib die ungeraden Zahlen aus `zahlen` aus.

``` python
for ind in range(len(zahlen)):
    if zahlen[ind] % 2 != 0:
        print(zahlen[ind])
```

    11
    13
    15
    17
    19

# Aufgabe 13:

Erzeuge ein Array mit den ersten fünf Buchstaben des Alphabets.

``` python
buchstaben = ['A', 'B', 'C', 'D', 'E']
```

# Aufgabe 14:

Lies das dritte Element von `buchstaben` aus.

``` python
drittes_element = buchstaben[2]
print(drittes_element)
```

    C

# Aufgabe 15:

Ändere das vierte Element von `buchstaben` zu ‘Z’.

``` python
buchstaben[3] = 'Z'
print(buchstaben)
```

    ['A', 'B', 'C', 'Z', 'E']

# Aufgabe 16:

Schleife durch `buchstaben` und gib die Buchstaben aus.

``` python
for ind in range(len(buchstaben)):
    print(buchstaben[ind])
```

    A
    B
    C
    Z
    E

# Aufgabe 17:

Erzeuge ein Array `zufallszahlen` mit 10 Zufallszahlen zwischen 1 und
100. \> Hinweis: recherchiere selber, wie man eine Zufallszahl in python
erzeugen kann.

``` python
import random
zufallszahlen = []
for ind in range(10):
    zufallszahlen.append(random.randint(1, 100))
print(zufallszahlen)
```

    [2, 93, 98, 90, 59, 25, 70, 20, 33, 44]

# Aufgabe 18:

Bestimme die Summe der Zahlen in `zufallszahlen`.

``` python
summe_zufallszahlen = 0
for ind in range(len(zufallszahlen)):
    summe_zufallszahlen = summe_zufallszahlen + zufallszahlen[ind]
print("Summe der Zahlen:", summe_zufallszahlen)
```

    Summe der Zahlen: 534

# Aufgabe 19:

Finde die größte Zahl in `zufallszahlen`.

``` python
groesste_zahl = zufallszahlen[0]
for ind in range(len(zufallszahlen)):
    if zufallszahlen[ind] > groesste_zahl:
        groesste_zahl = zufallszahlen[ind]
print("Die größte Zahle:", groesste_zahl)
```

    Die größte Zahle: 98

# Aufgabe 20:

Finde die kleinste Zahl in `zufallszahlen`.

``` python
kleinste_zahl = zufallszahlen[0]
for ind in range(len(zufallszahlen)):
    if zufallszahlen[ind] < kleinste_zahl:
        kleinste_zahl = zufallszahlen[ind]
print("Die kleinste Zahle:", kleinste_zahl)
```

    Die kleinste Zahle: 2

# Aufgabe 21:

Erstelle ein Array mit den Namen deiner drei Lieblingsfilme.

``` python
filme = ["Inception", "Interstellar", "Matrix"]
print(filme)
```

    ['Inception', 'Interstellar', 'Matrix']

# Aufgabe 22:

Füge einen weiteren Film zu `filme` hinzu.

``` python
filme.append("Avatar")
print(filme)
```

    ['Inception', 'Interstellar', 'Matrix', 'Avatar']

# Aufgabe 23:

Erzeuge ein Array mit den Zahlen 1 bis 10 und quadriere jede Zahl.

``` python
zahlen = list(range(1, 11))
quadrate = []
for ind in range(len(zahlen)):
    quadrate.append(zahlen[ind]**2)
print(quadrate)
```

    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# Aufgabe 24:

Multipliziere jedes Element in `zahlen` aus der oberen Aufgabe mit 2.

``` python
zahlen = list(range(1, 11))
multipliziert_mit_2 = []
for ind in range(len(zahlen)):
    multipliziert_mit_2.append(zahlen[ind]*2)
print(multipliziert_mit_2)
```

    [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

# Aufgabe 25:

Erzeuge ein Array von 5 Benutzernamen und gib sie in umgekehrter
Reihenfolge aus.

``` python
benutzernamen = ["alice", "bob", "charlie", "dave", "eve"]
for ind in range(len(benutzernamen)-1, -1, -1):
    print(benutzernamen[ind])
```

    eve
    dave
    charlie
    bob
    alice

# Aufgabe 26:

Überprüfe, ob der Name ‘bob’ in `benutzernamen` enthalten ist.

``` python
ist_bob_drin = False
for ind in range(len(benutzernamen)):
    if benutzernamen[ind] == 'bob':
        ist_bob_drin = True
print("Ist bob drin?", ist_bob_drin)
```

    Ist bob drin? True
