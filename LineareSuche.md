# Aufgabe 1:


Implementieren Sie ein Programm, das überprüft, ob ein Besucher der
Mitgliederversammlung zu-gangsberechtigt ist. Dafür soll am Eingang die
Mitgliedsnummer in das Programm eingegeben werden. Nach der Eingabe der
Mitgliedsnummer wird geprüft, ob die eingegebene Nummer existiert. Alle
ver¬gebenen Mitgliedsnummern des Vereins sind im Array `mnr` erfasst.  
`mnr =  [1001, 1019, 1014, 1009, 1005, 1002, 1018, 1008, 1003, 1010, 1007, 1004, 1020, 1013, 1015, 1011, 1017, 1012, 1006, 1016]`  
Wird die eingegebene Mitgliedsnummer gefunden, soll die Meldung „Zutritt
gewährt“ ausgegeben werden. Wird die Nummer nicht gefunden, soll die
Meldung „Zutritt verweigert“ erscheinen.

``` python
#Mitgliedsnummern
mnr = [1001, 1019, 1014, 1009, 1005, 1002, 1018, 1008, 1003, 1010, 1007, 1004, 1020, 1013, 1015, 1011, 1017, 1012, 1006, 1016]

#Eingabe
nummer = int(input("Mitgliedsnummer eingeben: "))

laenge = len(mnr)
gefunden = False

#Suche
for i in range(laenge):
    if mnr[i] == nummer:
        gefunden = True

#Ausgabe
if gefunden:
    print("Zutritt gewährt")
else:
    print("Zutritt verweigert")
```

    Mitgliedsnummer eingeben:  1008
    Zutritt gewährt

[Struktogramm](LineareSuche_files/figure-markdown_strict/cell-3-1-24a4adc0-270a-420e-aefd-db9fe1eebc64.png)

# Aufgabe 2: Lineare Suche – Verschlüsselung von Buchstaben

Die Verschlüsselung wird im Zeitalter der Digitalisierung immer
wichtiger. Mit Hilfe einer einfachen Verschlüsselungstechnik
(Transposition) sollen einzelne Großbuchstaben verschlüsselt werden.
Dazu wurden die Buchstaben des Alphabets im Array `alphabet_klar` und
die Buchstaben für die Verschlüsselung im Array `alphabet_geheim`
erfasst.

<table>
<tbody>
<tr class="odd">
<td>Klartext:</td>
<td>A</td>
<td>B</td>
<td>C</td>
<td>D</td>
<td>E</td>
<td>F</td>
<td>usw.</td>
<td>Array: alphabet_klar</td>
</tr>
<tr class="even">
<td>verschlüsselter Text:</td>
<td>A</td>
<td>D</td>
<td>Z</td>
<td>V</td>
<td>P</td>
<td>H</td>
<td>usw.</td>
<td>Array: alphabet_geheim</td>
</tr>
</tbody>
</table>

Gibt der Benutzer beispielsweise den Großbuchstaben B ein, soll er als
Ausgabe den verschlüsselten Buchstaben D enthalten, gibt er ein E ein
soll er eine Ausgabe mit dem Buchstaben P erhalten usw. So kann der
Benutzer nach und nach einen Text verschlüsseln. Implementieren Sie
unter Anwendung der linearen Suche eine Lösung für die beschriebene
Aufga-benstellung.

``` python
#Alphabete
alphabet_klar = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
alphabet_geheim = ["A", "D", "Z", "V", "P", "H", "W", "X", "B", "Q", "R", "C", "O", "Y", "E", "G", "U", "L", "M", "F", "J", "S", "T", "I", "K", "N"]

#Eingabe
buchstabe_klar = input("Klarbuchstabe: ")

for i in range(len(alphabet_klar)):
    if buchstabe_klar == alphabet_klar[i]:
        buchstabe_geheim = alphabet_geheim[i]

#Ausgabe
print("Geheimbuchstabe:", buchstabe_geheim)
```

    Klarbuchstabe:  D
    Geheimbuchstabe: V

[Struktogramm](LineareSuche_files/figure-markdown_strict/cell-6-1-99d13177-02c6-48f0-9671-365e2dcf9918.png)

# Aufgabe 3: Volleyball – Spieler suchen

Der Trainer der Abteilung Volleyball des Sportvereins Mühlberger SC
möchte eine Erweiterung seiner Software.  
Nach der Eingabe eines Spielernamens möchte er eine Information
angezeigt bekommen, ob der Spieler im Mannschaftskader ist oder nicht.  
Die Namen aller Spieler des Mannschaftskaders sind in dem Array kader
erfasst.

`kader = ['Armin', 'Batu', 'Kai', 'Sven', 'Paul', 'Milan', 'Goran', 'Chris', 'Nico', 'Dennis', 'Emin', 'Luca']`

Der erforderliche Algorithmus soll so optimiert sein, dass die Suche im
Array kader beendet wird, sobald der gesuchte Spieler gefunden wurde.

``` python
kader = ["Armin", "Batu", "Kai", "Sven", "Paul", "Milan", "Goran", "Chris", "Nico", "Dennis", "Emin", "Luca"]

spielername = input("Gesuchter Spielername: ")
gefunden = False
zaehler = 0

#Suche
while gefunden == False and zaehler < len(kader):
    if spielername == kader[zaehler]:
        gefunden = True
    else:
        zaehler = zaehler + 1

#Ausgabe
if gefunden:
    print("Spieler ist im Mannschaftskader")
else:
    print("Spieler ist nicht im Mannschaftskader")
```

    Gesuchter Spielername:  Chris
    Spieler ist im Mannschaftskader

[Struktogramm](/LineareSuche_files/figure-markdown_strict/cell-9-1-18b9c6b5-9852-4187-b16d-562a1c318d99.png)
