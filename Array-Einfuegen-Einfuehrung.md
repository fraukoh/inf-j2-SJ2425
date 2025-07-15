---
title: "Array-Einfuegen-Einfuehrung"
format: revealjs
---

---

# Einführung: Elemente in ein Array (Liste) einfügen mit Python

---

## Was ist ein Array (bzw. eine Liste) in Python?

Ein Array (in Python: Liste) ist eine Sammlung von Elementen, die in einer bestimmten Reihenfolge gespeichert sind.

**Beispiel:**
```python
zahlen = [2, 3, 4]
```

---

## Ziel: Ein neues Element einfügen

Stell dir vor, du hast eine Liste und möchtest ein neues Element an einer bestimmten Stelle einfügen.

**Neues Beispiel:**
Wir haben die Liste der Lieblingssnacks in der Pause:
```python
snacks = ["Chips", "Schokolade", "Gummibärchen", "Kekse"]
```
Jetzt bringt Max plötzlich einen Döner mit und möchte, dass sein Döner an dritter Stelle (Index 2) steht!

---

## Wie funktioniert das Einfügen mit append und Verschieben?

### 1. Am Ende einfügen (append)

Das neue Element wird immer zuerst am Ende der Liste angehängt:
```python
snacks.append("Döner")
print(snacks)
# Ausgabe: ['Chips', 'Schokolade', 'Gummibärchen', 'Kekse', 'Döner']
```

---

### 2. Nach dem Anhängen: Verschieben durch Tauschen

Jetzt muss Döner an die richtige Stelle (Index 2). Dafür wird von hinten nach vorne getauscht, bis Döner an der gewünschten Position steht.


Vorher:
```
Index:   0         1            2             3        4
        Chips   Schokolade   Gummibärchen   Kekse   Döner
```

**Tausch-Schritte:**

1. Döner und Kekse tauschen:
```
[Chips] [Schokolade] [Gummibärchen] [Döner] [Kekse]
```
2. Döner und Gummibärchen tauschen:
```
[Chips] [Schokolade] [Döner] [Gummibärchen] [Kekse]
```
Jetzt steht Döner an der gewünschten Stelle (Index 2)!

---

### 3. Python-Code: Einfügen mit append und Tausch (ohne Funktion)

```python
snacks = ["Chips", "Schokolade", "Gummibärchen", "Kekse"]

snack = input("Welchen Snack möchtest du einfügen? ")
index = int(input("An welcher Stelle (Index) soll der Snack stehen? "))
snacks.append(snack)  # Schritt 1: Am Ende anhängen
# Schritt 2: Von hinten nach vorne tauschen
for i in range(len(snacks)-1, index, -1):
    snacks[i], snacks[i-1] = snacks[i-1], snacks[i]
print(snacks)
```

---

## Zusammenfassung

- Das neue Element wird immer mit append am Ende angehängt.
- Danach wird es durch Tauschen von hinten bis zur gewünschten Stelle verschoben.
- So bleibt die Reihenfolge der anderen Elemente erhalten.

---

## Übung 1

Füge in die folgende Liste `"Pizza"` an der Stelle mit Index 1 ein (erst mit append, dann mit Tausch):
```python
snacks = ["Chips", "Schokolade", "Gummibärchen", "Kekse"]
# ... dein Code hier ...
```

---

## Tipp

Stell dir vor, die Snacks stehen in einer Reihe. Wenn jemand Neues reinkommt, stellt er sich hinten an und drängelt sich dann durch Tauschen nach vorne bis zur gewünschten Position!

```
[Chips] [Schokolade] [Gummibärchen] [Kekse] [Pizza]
                                 ^
                            Pizza will nach vorne!
```

---

## Weiterführende Beispiele und Erklärungen

### Beispiel 1: Mehrere Snacks nacheinander einfügen (immer mit append und Tausch)

```python
snacks = ["Chips", "Schokolade", "Gummibärchen"]
# Erst kommt "Pizza" an Stelle 1 rein
snacks.append("Pizza")
for i in range(len(snacks)-1, 1, -1):
    snacks[i], snacks[i-1] = snacks[i-1], snacks[i]
# Dann kommt "Eis" an Stelle 3 rein
snacks.append("Eis")
for i in range(len(snacks)-1, 3, -1):
    snacks[i], snacks[i-1] = snacks[i-1], snacks[i]
print(snacks)
# Ausgabe: ['Chips', 'Pizza', 'Schokolade', 'Eis', 'Gummibärchen']
```
---
### Beispiel 2: Einfügen am Anfang der Liste

```python
snacks = ["Chips", "Schokolade", "Gummibärchen"]
snacks.append("Kaugummi")
for i in range(len(snacks)-1, 0, -1):
    snacks[i], snacks[i-1] = snacks[i-1], snacks[i]
print(snacks)
# Ausgabe: ['Kaugummi', 'Chips', 'Schokolade', 'Gummibärchen']
```
---
### Beispiel 3: Einfügen am Ende (nur append, kein Tausch nötig)

```python
snacks = ["Chips", "Schokolade", "Gummibärchen"]
snacks.append("Limo")
print(snacks)
# Ausgabe: ['Chips', 'Schokolade', 'Gummibärchen', 'Limo']
```
---
### Beispiel 4: Einfügen an beliebiger Stelle

```python
snacks = ["Chips", "Schokolade", "Gummibärchen"]
# Wir wollen "Popcorn" an Stelle 2 einfügen
snacks.append("Popcorn")
for i in range(len(snacks)-1, 2, -1):
    snacks[i], snacks[i-1] = snacks[i-1], snacks[i]
print(snacks)
# Ausgabe: ['Chips', 'Schokolade', 'Popcorn', 'Gummibärchen']
```

---

## Übung 2

Schreibe ein Programm, das einen beliebigen Snack an einer beliebigen Stelle in die Snack-Liste einfügt (immer mit append und Tausch). Teste es mit verschiedenen Snacks und Positionen!

---

## Merke
- Das Einfügen in Listen funktioniert mit append und anschließendem Verschieben durch Tauschen.
- So kannst du an jeder beliebigen Stelle ein neues Element einfügen, ohne insert zu verwenden!

---

Viel Erfolg beim Ausprobieren und Programmieren! 