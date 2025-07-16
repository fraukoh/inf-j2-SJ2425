---
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
    zwischen = snacks[i-1]
    snacks[i-1] = snacks[i]
    snacks[i] = zwischen
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

