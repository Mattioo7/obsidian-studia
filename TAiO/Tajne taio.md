1. Czy funkcją częściowo rekursywną można policzyć każdy problem NP?
	1. EDIT: TAK, bo: ❔ ❔ ❔ 
		problem NP -> istnieje NDMT go rozwiązująca -> oznaczmy S(n) jako złożoność pamięciową algorytmu NDMT -> (Savitch) istnieje DMT akceptująca ten sam język [i coś tam jeszcze] -> maszynie DMT odpowiada jakaś funkcja częsciowo rekursywna -> Tak ?

2. Czy problem NP-zupełny to taki, do ktrórego da się sprowadzić każdy NP w czasie wielomianowym?
	1. NIE, jeśli tylko tyle to NP-trudny. Problem sam musi być NP i każdy NP się do niego redukować w czasie wielomianym, żeby był NP-zupełny

3. Czy da się stworzyć MT to czy się zatrzyma na każdym wejściu?
	1. NIE

4. TW Savitza??? 
	1. yes

5. Czy w TW Cooka do dowodu poprawności na P(n) zmiennych potrzeba P(n) w MT?
	1. NIE, w TW Cooka, potrzebujemy O(p^2(n)) zmiennych w formule boolowskiej.

6. Czy na maszynie RAM dodanie / dodanie i odwrócenie ma zł. O(n)?
	1. Odwrócenie ma O(n^2)