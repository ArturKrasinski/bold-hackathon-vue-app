**Opis**

Repozytorium startowe aplikacji - Bold FE Hackathon#1. Aplikacja wykorzystuje vue + vuetify. Docelowo aplikacja ma zostać zrealizowana przy pomocy 
zdalnej "bazy danych" firebase przy wykorzystaniu VueFire oraz w oparciu o Vuex, czyli wzorzec zarządzania stanem aplikacji Vue.


**Instalacja**

1. Zainstaluj środowisko uruchomieniowe JavaScript **Node.js** + npm
2. Zainstaluj vue command line interface: _npm install --global vue-cli_
3. Zainstaluj zależności które wymagane są przez projekt: _npm install_ 

**Uruchomienie**

Po poprawnej instalacji wszystkich potrzebnych modułów uruchomienie środowiska deweloperskiego (serwer + livereload) powinno być możliwe poprzez 
użycie: _npm run dev_


**Opis aplikacji**

**Część 1: VUE - przykładowa aplikacja** (architektura aplikacji, events bubbling issue)

1. **Stworzenie projektu firebase, konfiguracja z vue cli, pobranie danych i wyświetlenie**
   1. pobranie "zerowego stanu aplikacji z git"
   2. założenie nowego "projektu" w firebase
   3. import danych (plik z danymi: _static/data.json_) do firebase
   4. zaimportowanie configa z firebase do projektu 
   5. nawiązanie połączenia z bazą i wyświetlanie pobieranych danych
   
2. **Stworzenie głównego komponentu**
   1. Stworzenie komponentu tabeli danych według wzorca (wyświetlanie atrybutów po lewej, następne kolumny to kolejne produkty)
   2. Wyodrębnienie "komponentu produktowego" (zdjęcie, przyciski, nazwa, ceny)
   3. Import komponentu produktu do głównego komponentu i przekazanie danych
   4. *zadanie dodatkowe: style napisane w BEM (blok element modyfikator) w SASS (wymaga dodania do konfiguracji webpacka preprocesora CSS)
   
   
3. **Wyodrębnienie child komponentów z "komponentu produktowego": image, price, title, availability, buttons**
   1. przygotowanie plików małych komponentów
   2. zaimportowanie ich do komponentu produktu
   3. obsłużenie różnych stanów dla komponentu price i availability
      1. stany price: simple, special, special + old price (przekreslona cena)
      2. stany availability: dostepny, niedostepny (qty > 0, qty === 0)
      
5. **podzielenie button na dwa oddzielne buttony i obsłużenie eventu**
   1. stworzenie komponentu button dodaj do koszyka
      1. stworzenie przycisku
      2. stworzenie inputa (qty)
      3. obsłużenie emitowania zdarzenia z kliknięciem przycisku "Do koszyka"
   1. stworzenie komponentu button dodaj do wishlisty
      1. przygotowanie html przycisku
      2. obsłużenie emitowania zdarzenia kliknięcia przycisku
   1. import child komponentów do głównego komponentu buttons
   2. obsłużenie reakcji na zdarzenia emitowane z child buttonów (events bubbling)
   
6. **dodanie funkcjonalności wyświetlania listy koszyka / listy życzeń**
   1. przygotowanie komponentów
   2. import do głównego modułu
   3. aktualizacja list w zależności na kliknięcia w przyciski
      1. wyświetlanie produktów dodanych do konkretnej listy
   4. *zadanie dodatkowe: zapisywanie stanu koszyka w firebase


**Część 2: VUEX** (zmiana architektury)

1. Teoria na temat VUEX
2. Podpięcie VUEX do projektu
   1. instalacja modułu node
   2. import do głównego modułu
3. Przygotowanie metod
   1. obsłużenie dodaj / usuń itemu z kolekcji + pobranie całej kolekcji koszyka
   2. obsłużenie dodaj / usuń itemu z kolekcji + pobranie całej kolekcji wishlisty
4. Wyświetlanie wszystkich danych na podstawie globalnego store (produkty, atrybuty)
