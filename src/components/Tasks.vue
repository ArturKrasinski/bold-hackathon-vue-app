<style scoped>
 ol ol {
     margin-left: 20px;
 }
 p {
     margin: 20px 0;
     font-weight: bold;
     font-size: 16px;
 }
</style>

<template>
<div class="main">
<p class="unchanged rich-diff-level-one">Część 1: VUE - przykładowa aplikacja
(architektura aplikacji, problem zagnieżdżania zdarzeń)</p>
<ol class="unchanged rich-diff-level-one">
<li class="unchanged">stworzenie projektu <a href="https://firebase.google.com/">firebase</a>, <a href="https://medium.com/codingthesmartway-com-blog/vue-js-2-firebase-e4b2479e35a8">konfiguracja</a> z vue cli, pobranie danych i wyświetlenie (~1h)
<ol class="unchanged">
<li class="unchanged">założenie projektu w firebase</li>
<li class="unchanged">import danych z json do firebase</li>
<li class="unchanged">zaciągnięcie czystego projektu (przygotowanego wcześniej w git)</li>
<li class="unchanged">import configu do projektu</li>
<li class="unchanged">nawiązanie połączenia z bazą</li>
<li class="unchanged">wyświetlanie pobieranych danych</li>
</ol>
</li>
<li class="unchanged">wyświetlenie komponentu tabeli gdzie będą v-for’y wyświetlające całość danych (~0,5)
<ol class="unchanged">
<li class="unchanged">stworzenie komponentu tabeli i zaimportowanie go do głównego komponentu</li>
<li class="unchanged">pobranie danych w głównym komponencie i przekazanie go do komponentu tabeli</li>
<li class="unchanged">wrzucenie paczki ze stylami (sass) do komponentu tabeli</li>
</ol>
</li>
<li class="unchanged">wyodrębnienie komponentu table product (0,5)
<ol class="unchanged">
<li class="unchanged">stworzenie nowego komponentu “table product”</li>
<li class="unchanged">zaimportowanie komponentu do komponentu tabeli</li>
</ol>
</li>
<li class="unchanged">w komponencie table product wyodrębnienie child komponentów: image, price, title, availability, buttons (1)
<ol class="unchanged">
<li class="unchanged">przygotowanie plików małych komponentów</li>
<li class="unchanged">zaimportowanie ich do komponentu produktu</li>
<li class="unchanged">obsłużenie różnych stanów dla komponentu price i availability
<ol class="unchanged">
<li class="unchanged">stany price: zwykla, special, special z przekreslona cena</li>
<li class="unchanged">stany availability: dostepny, niedostepny, na zamówienie</li>
</ol>
</li>
</ol>
</li>
<li class="unchanged">podzielenie button na dwa oddzielne buttony i obsłużenie eventu (0,5)
<ol class="unchanged">
<li class="unchanged">stworzenie komponentu button dodaj do koszyka
<ol class="unchanged">
<li class="unchanged">stworzenie przycisku</li>
<li class="unchanged">stworzenie inputa (qty)</li>
<li class="unchanged">obsłużenie emitowania zdarzenia z kliknięciem przycisku dodaj do koszyka</li>
</ol>
</li>
<li class="unchanged">stworzenie komponentu button dodaj do wishlisty
<ol class="unchanged">
<li class="unchanged">przygotowanie html przycisku</li>
<li class="unchanged">obsłużenie emitowania zdarzenia kliknięcia przycisku</li>
</ol>
</li>
<li class="unchanged">import child komponentów do głównego komponentu buttons</li>
<li class="unchanged">obsłużenie reakcji na zdarzenia emitowane z child buttonów</li>
</ol>
</li>
<li class="unchanged">dodanie funkcjonalności wyświetlania listy koszyka / listy życzeń (podstawowe czyli tytuł produktu i label listy) (0,5)
<ol class="unchanged">
<li class="unchanged">przygotowanie komponentów</li>
<li class="unchanged">import do głównego modułu</li>
<li class="unchanged">aktualizacja list w zależności na kliknięcia w przyciski
<ol class="unchanged">
<li class="unchanged">wyświetlanie produktów dodanych do konkretnej listy</li>
</ol>
</li>
</ol>
</li>
</ol>
<p class="unchanged rich-diff-level-one">Część 2: VUEX
(teoria / prezentacja + wdrożenie)</p>
<ol class="unchanged rich-diff-level-one">
<li class="unchanged">Teoria na temat VUEX (1)</li>
<li class="unchanged">Podpięcie VUEX do projektu (1)
<ol class="unchanged">
<li class="unchanged">instalacja modułu node</li>
<li class="unchanged">import do głównego modułu</li>
</ol>
</li>
<li class="unchanged">Przygotowanie metod (1)
<ol class="unchanged">
<li class="unchanged">obsłużenie dodaj / usuń itemu z kolekcji + pobranie całej kolekcji koszyka</li>
<li class="unchanged">obsłużenie dodaj / usuń itemu z kolekcji + pobranie całej kolekcji wishlisty</li>
</ol>
</li>
<li class="unchanged">Wyświetlanie wszystkich danych na podstawie globalnego store</li>
</ol>
<br>
<h4>Linki</h4>
<ul>
<li><a href="https://material.io/icons/">Ikony dla Vuetify</a></li>
<li><a href="https://firebase.google.com/">Firebase</a></li>
<li><a href="https://medium.com/codingthesmartway-com-blog/vue-js-2-firebase-e4b2479e35a8">Konfiguracja firebase + vue-cli: </a></li>
</ul>
</div>
</template>
