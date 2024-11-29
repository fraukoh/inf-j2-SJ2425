# Wiederholungsaufgabe:


Gegeben ist ein Array arr = \[2,3,4\]

1.  Hängen Sie ein neues Element (Zahl 100) an das Array.
2.  Geben Sie das aktualisierte Array in der Schleife aus.

``` python
arr = [2,3,4]
arr.append(100)
for i in range(len(arr)):
    print(arr[i])
```

## Elemente im Array tauschen

1.  Tauschen Sie das letzte und das vorletzte Element im Array arr.
2.  Geben Sie das aktualisierte Array in der Schleife aus.

``` python
arr = [2,3,4,100]
zwischengespeichert = arr[2]
arr[2] = arr[3]
arr[3] = zwischengespeichert
for i in range(len(arr)):
    print(arr[i])
```

## Elemente in ein Array an beliebiger Stelle einfügen

Neben den Möglichkeiten des Zugriffs auf Arrayelemente zur Ausgabe und
Veränderung der Inhalte, besteht auch die Möglichkeit Arrayelemente
hinzuzufügen. Ein zusätzliches Arrayelement wird mit Python
grundsätzlich am Ende des Arrays eingefügt. Die Position, an welcher der
neue Inhalt im Array stehen soll, kann über den Index dieser Position
angegeben werden. Bis zu dieser Stelle wird das neue Element Schritt für
Schritt “nach vorne” verschoben.

Beispiel:

Folgenes Array ist gegeben: orte = \[“Mannheim”, “Stuttgart”,
“Freiburg”, “Konstanz”\]

Zwischen die beiden Einträge ‘Stuttgart’ und ‘Freiburg’ soll der Ort
‘Esslingen’ eingefügt werden. Über die Funktion append() kann Esslingen
an das Ende des bestehenden Arrays angehängt werden.

``` python
orte = ["Mannheim", "Stuttgart", "Freiburg", "Konstanz"]
stelle = 3
orte.append("Esslingen")
for i in range(len(orte)-1,stelle,-1):
    zwischengespeichert = orte[i]
    orte[i] = orte[i-1]
    orte[i-1] = zwischengespeichert
print(orte)
```

## Aufgabe: Inhalte einfügen

Die Software des Trainers der Abteilung Volleyball des Sportvereines
Mühlberger SC enthält ein Array mit allen Spielernamen des
Mannschaftskaders.  
`kader =  ["Armin", "Batu", "Kai", "Sven", "Paul", "Milan", "Goran", "Chris", "Nico", "Dennis", "Emin", "Luca"]`  
Mit Hilfe der Software soll es möglich sein, an einer bestimmten Stelle
einen weiteren Spielernamen einzutragen, z.B. an der Stelle mit dem
Index 6.

Implementieren Sie eine Funktion `einfuegen_spieler()`, mit der ein
Spieler an einer vom Anwender einzugebenden Stelle, in das Array
eingefügt wird.  
z. B.: Spielername: Tom - Index: 6  
Das Array kader soll danach folgenden Inhalt haben:  
`["Armin", "Batu", "Kai", "Sven", "Paul", "Milan", "Tom", "Goran", "Chris", "Nico","Dennis", "Emin", "Luca"]`

``` python
#Hier den Programmcode eingeben und mit STRG+ENTER ausführen
kader = ["Armin", "Batu", "Kai", "Sven", "Paul", "Milan", "Goran", "Chris","Nico", "Dennis", "Emin", "Luca"]

def kader_ausgeben():
    print("------------------------")
    print("Kader")
    print("------------------------")
    for i in range(len(kader)):
        print(kader[i])

def einfuegen_spieler():
    spielername = input("Spielername: ")
    index = int(input("Index: "))
    
    #Einfügen an letzter Stelle
    kader.append(spielername)                              
    
    #Nach vorne wandern, bis an die richtige Position
    for i in range(len(kader)-1, index,-1):    
        zwischenspeicher = kader[i-1]
        kader[i-1] = kader[i]
        kader[i] = zwischenspeicher
    
    kader_ausgeben()

#Funktionsaufruf
einfuegen_spieler()
```

[Struktogramm](Array-Inhalte-einfuegen_files/figure-html/003b398a-cde3-4b25-8d27-4f826a386b18-1-3c4804c3-5591-47ef-aa18-f60f5d892c97.png)
