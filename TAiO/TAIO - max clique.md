
Ogólnie
Algorytm przechowuje Q - obecnie rozważaną klikę oraz Q_max, czyli największą znalezioną do tej pory klikę. Zbiór R jest zbiorem wierzchołków-kandydatów i na początku równa się V. Działamy w następujący sposób: wybieramy wierzchołek p ze zbioru R i dodajemy go do Q. Następnie ze zbioru R wybieramy sąsiadów p i to przecięcie R z sąsiadami to nowe R. Wywołujemy się rekursywnie.

Gdy R = zbiór_pusty jest osiągnięte to sprawdzamy czy Q > Q_max i jeśli tak to podmieniamy. Następnie wracamy, usuwając ostatnio wybrany wierzchołek p i wracając do poprzedniego R. 

Pruning
Aby nałożyć ograniczenie na rozmar kliki na początku przeprowadzamy kolorowanie aproksymacyjne. Kolorujemy wierzchołki w taki sposób, że jeśli wierzchołek ma kolor k to ma sąsiadów o kolorach 1,2,...,k-1. **Dzięki czemu wiemy, że rozmiar kliki jest co najwyżej równy liczbie kolorów.** Możemy to osiągnąć wykonując greedy coloring, czyli nadając wirzchołkowi zawsze najmniejszy możliwy kolor ze względu na jego sąsiadów (czy to prawda?), a następnie sortujemy wierzchołki ze względu na ich kolor. Następuje to w czasie O(|R|^2). 
Po zastosowaniu NUMBER-SORT w EXPAND(R, N) największa klika zawiera wierzchołek p z R taki, że jego kolor jest większy lub równy rozmiarowi tej kliki (większy, bo kolorowanie aproks). Spodziewamy się, że wierzchołek o najwyższym kolorze z R ma największą szansę na bycie w maksymalnej klice, więc od niego zaczynamy przeszukiwania. 

Wstępne kolorowanie i sortowanie
Przed wywołaniem algorytmu sortujemy wierzchołki rosnąco ze względu na ich stopnie. Następnie kolorujemy w następujący sposób: Pierwszym (maksymalny stopień wierzchołka) wierzchołkom nadajemy kolor równy ich indeksowi+1, a pozostałym (maksymalny stopień wierzchołka)+1