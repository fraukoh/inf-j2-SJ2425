# Aufgabe 1 \[3 P\]:


Erstellen Sie ein Array mit den Lieblingsfächern
`["Mathematik", "Biologie", "Informatik", "Chemie", "Geschichte"]` und
geben Sie jedes Fach mit dem Text “Lieblingsfach:” davor aus.

``` python
lieblingsfaecher = ["Mathematik", "Biologie", "Informatik", "Chemie", "Geschichte"]
for i in range(len(lieblingsfaecher)):
    print("Lieblingsfach: " + lieblingsfaecher[i])
```

    Lieblingsfach: Mathematik
    Lieblingsfach: Biologie
    Lieblingsfach: Informatik
    Lieblingsfach: Chemie
    Lieblingsfach: Geschichte

# Aufgabe 2 \[4 P\]:

Erstellen Sie ein Array mit den monatlichen Ausgaben
`[200, 250, 300, 150, 400, 350, 280, 320, 370, 410, 380, 450]` und
berechnen Sie die Gesamtausgaben der **ersten Hälfte** des Jahres.

Hinweis: Verwenden Sie dafür eine Schleife

``` python
ausgaben = [200, 250, 300, 150, 400, 350, 280, 320, 370, 410, 380, 450]
erste_haelfte_ausgaben = 0
for i in range(6):
    erste_haelfte_ausgaben = erste_haelfte_ausgaben + ausgaben[i]
print("Die Gesamtausgaben der ersten Hälfte des Jahres sind:", erste_haelfte_ausgaben)
```

    Die Gesamtausgaben der ersten Hälfte des Jahres sind: 1650

# Aufgabe 3 \[4 P\]:

Erstellen Sie ein Array mit den Projekten des Schuljahres
`["Kunstausstellung", "Sporttag", "Wissenschaftsmesse"]` und fügen Sie
das Projekt “Schulwebsite” an der ersten Stelle (=ganz am Anfang) hinzu.

``` python
projekte = ["Kunstausstellung", "Sporttag", "Wissenschaftsmesse"]
projekte.append("Schulwebsite")
for i in range(len(projekte)-1, 0, -1):
    zwischengespeichert = projekte[i]
    projekte[i] = projekte[i-1]
    projekte[i-1] = zwischengespeichert
print("Aktualisierte Projekte:", projekte)
```

    Aktualisierte Projekte: ['Schulwebsite', 'Kunstausstellung', 'Sporttag', 'Wissenschaftsmesse']

# Aufgabe 4 \[4 P\]:

Gegeben sind zwei Arrays:

`kunden = ["Max Mustermann", "Erika Musterfrau", "Hans Müller", "Anna Schmidt", "Peter Meier"]`  
`kundennummern = ["001", "002", "003", "004", "005"]`

Schreiben Sie ein Programm, das bei Eingabe einer oben genannten
Kundennummer den jeweiligen Kundennamen anzeigt.

``` python
kunden = ["Max Mustermann", "Erika Musterfrau", "Hans Müller", "Anna Schmidt", "Peter Meier"]
kundennummern = ["001", "002", "003", "004", "005"]

eingabe_nummer = input("Bitte geben Sie die Kundennummer ein: ")
for i in range(len(kundennummern)):
    if eingabe_nummer == kundennummern[i]:
        print("Der Kunde mit der Kundennummer", eingabe_nummer, "ist:", kunden[i])
```

    Der Kunde mit der Kundennummer 003 ist: Hans Müller

# Aufgabe 5 \[6 P\]:

Erstellen Sie ein Array mit den Namen von Autoren
`["Hermann Hesse", "Franz Kafka", "Thomas Mann", "Bertolt Brecht"]` und
sortieren Sie sie alphabetisch mit BubbleSort.

``` python
autoren = ["Hermann Hesse", "Franz Kafka", "Thomas Mann", "Bertolt Brecht"]
n = len(autoren)

# BubbleSort Algorithmus
for i in range(n):
    for j in range(0, n-i-1):
        if autoren[j] > autoren[j+1]:
            zwischengespeichert = autoren[j]
            autoren[j] = autoren[j+1]
            autoren[j+1] = zwischengespeichert

print("Sortierte Autoren:", autoren)
```

    Sortierte Autoren: ['Bertolt Brecht', 'Franz Kafka', 'Hermann Hesse', 'Thomas Mann']
