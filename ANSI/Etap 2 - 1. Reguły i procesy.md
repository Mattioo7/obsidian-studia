

# Obiekty

1. Jest wielu organizatorów.
2. Każdy organizator ma wiele wydarzeń
3. Każde wydarzenie ma wielu uczestników
4. Niektóre wydarzenia mają schemat miejsc


# Reguły 

## Dotyczące tworzenia wydarzeń
#### Nie do złamania
1. Wydarzenia płatne muszą mieć ograniczoną liczbę miejsc.
2. Wydarzenie musi być publiczne lub prywatne.
3. Użytkownik może utworzyć maksymalnie 10 wydarzeń.
#### Miękkie
1. Wydarzenie powinno zawierać miejsce odbywania się.
2. Wydarzenie powinno mieć limit osób.


## Dotyczące kupna / rezerwacji
#### Nie do złamania
1. Użytkownik może zrezygnować z biletu maksymalnie na 1h przed wydarzeniem.
2. Jeden użytkownik może kupić maksymalnie 10 biletów.
3. Użytkownik może zapisać się na **prywatne** wydarzenie jedynie przez zaproszenie (w formie linku lub zaproszenia w aplikacji).
4. Można zarezerwować miejsce tylko na aktywne wydarzenia.
5. W przypadku wydarzeń z miejscami po wybraniu miejsca jest ono blokowane na 10 min i w tym czasie musi rozpocząć się proces płatności.
#### Miękkie
1. Proces płatności nie może przekroczyć 30 minut. 

## Dotyczące edycji wydarzenia
#### Nie do złamania
1. Po edycji wydarzenia użytkownik musi mieć możliwość rezygnacji z wydarzenia (w przypadku płatnych wydarzeń wiąże się to ze zwrotem płatności).
2. Można zmienić liczbę miejsc, ale nie poniżej liczby już zarezerwowanych.
#### Miękkie
1. Widoczność (prywatne/publiczne) wydarzenia nie powinno być modyfikowana, ale jeśli chcemy zmienić to tylko z prywatnego na publiczne (po weryfikacji emailem).


# Procesy

## Tworzenie wydarzenia
1. Prośba systemu o rozpoczęcie procesu
2. System sprawdza liczbę stworzonych wydarzeń
3. System akceptuje / odrzuca (i informuje o liczba utworzonych wydarzeń)
4. Nadanie nazwy
5. Określenie daty
6. Określenie godziny (opcjonalne)
7. Wybór widoczności wydarzenia (prywatne / publiczne)
8. Wybranie kategorii (1/wiele) wydarzenia
9. Wybranie miejsca (opcjonalne)
10. Określenie liczby miejsc (lub brak limitu)
11. Określenie ceny (lub bezpłatne)
12. Dodanie opisu wydarzenia (opcjonalne)

## Kupno biletu
1. Użytkownik wybiera wydarzenie (publiczne) / dostaje link z zaproszeniem (prywatne)
2. Użytkownik wybiera miejsce (jeśli jest taka opcja)
	1. System rezerwuje tymczasowo miejsce (wydarzenie z miejscami) / zmniejsza licznik wolnych biletów (wydarzenie z limitem osób, ale bez miejsc)
3. Użytkownik wybiera metodę płatności
4. Użytkownik płaci za zamówienie
5. System rezerwuje miejsce na stałe / zmiejsza liczbę wolnych miejsc
6. System wysyła potwierdzenie zakupu wraz z biletem

## Rezerwacja miejsca (niepłatne wydarzenie, bez limitu miejsc)
1. Użytkownik wybiera wydarzenie
2. System zwiększa licznik uczestników

## Rezerwacja miejsca (niepłatne wydarzenie, z limitem miejsc)
1. Użytkownik wybiera wydarzenie
2. Użytkownik wybiera miejsce
	1. System rezerwuje tymczasowo miejsce (wydarzenie z miejscami) / zmniejsza licznik wolnych biletów (wydarzenie z limitem osób, ale bez miejsc)
3. Użytkownik zatwierdza dokonany wybór
4. System rezerwuje miejsce na stałe / zmiejsza liczbę wolnych miejsc
5. System wysyła potwierdzenie uczestnictwa

## Edycja wydarzenia (płatnego lub bezpłatnego z limitem miejsc)
1. Użytkownik (właściciel wydarzenia) wybiera swoje wydarzenie do edycji
2. Użytkownik edytuje nazwę wydarzenia
3. Użytkownik edytuje datę
4. Użytkownik edytuje godzinę
5. Użytkownik edytuje widoczność (tylko jeśli wydarzenie jest prywatne)
6. Użytkownik edytuje kategorie
7. Użytkownik edytuje miejsce wydarzenia (jeśli wydarzenie nie ma schematu siedzeń)
8. Użytkownik edytuje liczbę miejsc ((tylko dla wydarzeń bez schematu miejsc)), (błąd jeśli wybrana liczba jest mniejsza niż liczba rezerwacji) lub znosi limit miejsc
9. Użytkownik edytuje cenę
10. Użytkownik edytuje opis wydarzenia
11. Użytkownik potwierdza edycję wydarzenia
12. System wysyła uczestnikom powiadomienie o zmianie szczegółów wydarzenia z możliwością rezygnacji z uczestnictwa.
13. Jeśli uczestnik rezygnuje to :
	1. Odblokowujemy miejsce na schemacie / zwiększamy licznik wolnych miejsc
	2. Jeśli wydarzenie było płatne następuje zwrot środków