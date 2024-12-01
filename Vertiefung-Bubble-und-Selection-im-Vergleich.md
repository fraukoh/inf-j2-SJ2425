# BubbleSort und SelectionSort im Vergleich


Bevor wir die beiden Suchalgorithmen vergleichen, legen wir für sie
jeweils eine Funktion.

``` python
# Funktion für BubbleSort
def bubble_sort(arr):
    laenge = len(arr)
    for i in range(laenge):
        for j in range(0, laenge-i-1):
            if arr[j] > arr[j+1]:
                # Tausch
                zwischenspeicher = arr[j]
                arr[j] = arr[j+1]
                arr[j+1] = zwischenspeicher
    #Ausgabe
    print("Ergebnis von BubbleSort:")
    print(arr)



# Funktion für SelectionSort
def selection_sort(arr):
    laenge = len(arr)
    for akt_idx in range(laenge-1):
        min_idx = akt_idx
        for j in range(akt_idx + 1, laenge):
            #Suche nach der niedrigsten Zahl
            if arr[j] < arr[min_idx]:
                min_idx = j
        #Tausch
        zwischenspeicher = arr[akt_idx]
        arr[akt_idx] = arr [min_idx]
        arr[min_idx] = zwischenspeicher

    #Ausgabe
    print("Ergebnis von SelectionSort:")
    print(arr)
```

Und testen die Funktionen:

``` python
vektor = [23, 67, 5, 1, 2, 4, 3]
bubble_sort(vektor)
selection_sort(vektor)
```

    Ergebnis von BubbleSort:
    [1, 2, 3, 4, 5, 23, 67]
    Ergebnis von SelectionSort:
    [1, 2, 3, 4, 5, 23, 67]

Wir modifizieren die Funktionen so, dass sie die Anzahl der
Tauschvorgänge zählen, die Dauer von beiden Algorithmen messen und
ausgeben.

``` python
import time
# Funktion für BubbleSort
def bubble_sort(arr):
    anz_tausch = 0
    laenge = len(arr)
    start_time = time.time()
    for i in range(laenge):
        for j in range(0, laenge-i-1):
            if arr[j] > arr[j+1]:
                # Tausch
                zwischenspeicher = arr[j]
                arr[j] = arr[j+1]
                arr[j+1] = zwischenspeicher
                anz_tausch = anz_tausch + 1
    stop_time = time.time()
    #Ausgabe
    print("Ergebnis von BubbleSort:")
    print(arr)
    print("Anzahl der Tauschvorgänge", anz_tausch)
    print("Dauer:", stop_time - start_time, "Sek.")



# Funktion für SelectionSort
def selection_sort(arr):
    anz_tausch = 0
    laenge = len(arr)
    start_time = time.time()
    for akt_idx in range(laenge-1):
        min_idx = akt_idx
        for j in range(akt_idx + 1, laenge):
            #Suche nach der niedrigsten Zahl
            if arr[j] < arr[min_idx]:
                min_idx = j
        #Tausch
        zwischenspeicher = arr[akt_idx]
        arr[akt_idx] = arr [min_idx]
        arr[min_idx] = zwischenspeicher
        anz_tausch = anz_tausch + 1
    stop_time = time.time()
    #Ausgabe
    print("Ergebnis von SelectionSort:")
    print(arr)
    print("Anzahl der Tauschvorgänge", anz_tausch)
    print("Dauer:", stop_time - start_time, "Sek.")
```

``` python
vektor = [23, 67, 5, 1, 2, 4, 3]
bubble_sort(vektor)
selection_sort(vektor)
```

    Ergebnis von BubbleSort:
    [1, 2, 3, 4, 5, 23, 67]
    Anzahl der Tauschvorgänge 15
    Dauer: 2.0503997802734375e-05 Sek.
    Ergebnis von SelectionSort:
    [1, 2, 3, 4, 5, 23, 67]
    Anzahl der Tauschvorgänge 6
    Dauer: 1.430511474609375e-05 Sek.
