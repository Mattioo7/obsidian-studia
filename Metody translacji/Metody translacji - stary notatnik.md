Metody translacji:
user: s6-mt
pass: mini-i1234


Kolokwium:
- przedostatnie zajęcia (30 maja?)
- 4-5 zadania:
  - 1 z generowania kodu
  - 1 że jest opisana cecha kodu w języku naturanlym i trzeba napisać gramatykę, która będzie ten język opisywała

Ankiety:
- nipodobają mi się wciecia klamer

W1:
Drzewo wywodu (parse tree) a drzewo struktury (syntax tree)

Brakuje szczegółowego rozdziału o optmalizacji


W2:
Str.11 - Zmienne nieograniczone - np. takie utworzone przez new i zostawione same sobie
Zmienne automatyczne vs sterowane (kontrolowane)?

Wiązanie statyczne - tak jak funkcje są deklarowane - która w której
Wiązanie dynamiczne - kolejność wywołań metod decyduj o tym, która jest zewnętrzna i wewnętrzna

Zmienne nielokalne - zmienne zadeklarowane w procedurach zewnętrzenych

Obszar informacji organizacyjnych (str. 13) - zawiera np:
- adres powrotu
- adres rekordu aktywacji funkcji wywołującej (bo adres rekordu obecjen funkcji jest najczęściej w rejestrze, bo nie może być w samym siebie)
- (miejsce na zwracany wynik)

W3:
- sekwencja wywołania oraz sekwencja powrotu dotyczą modelu stosowego dla języków bez procedur lokalnych
- rekord aktywacji (ramka stosu)
  - obszar argumentów
  - obszar informacji organizacyjnych:
    - adres powrotu - adres linijki kodu po wywołaniu metody
    - control link - adres rekordu aktywacji procedury wywołującej, (raczej nie pokazuje na początek rekordu aktywacji tylko na miejsce, gdzie jest zapisany jeszcze poprzedni control link)
  - obszar zmiennych lokalnych
  - obszar zmiennych roboczych
- w rekordzie aktywacji często (np. język C, printf, scanf) kompilator zajmuje się parametrami funkcji od końca, aby umieścić je od końca na stosie. Robimy tak, ponieważ aby dostać się do nich idziemy od control link wstecz i musimy mieć je zawsze w takiej samej odległości (patrz rekord aktywacji wykłąd str. 24)
- str. 27 [konwencja na wykładzie] - gdy procedura jest zadeklarowana bezpośrednio w programie głównym to ma pusty access link






# Bardzo dużo

## TRochę mniej


```
var c = aa;
```

