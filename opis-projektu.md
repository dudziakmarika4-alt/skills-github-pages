# Opis projektu – Blog turystyczny „Budapeszt"

---

## Strona tytułowa

| | |
|---|---|
| **Temat** | Blog turystyczny poświęcony Budapesztowi – serwis internetowy z elementami zwiększającymi dostępność dla niepełnosprawnych użytkowników |
| **Osoby realizujące projekt** | _[imię i nazwisko]_, _[imię i nazwisko]_ |
| **Data** | Kwiecień 2026 |
| **Rok akademicki** | 2025/2026 |
| **Kierunek** | Turystyka i Rekreacja |
| **Specjalność** | _[specjalność]_ |
| **Rok studiów** | V rok |
| **Przedmiot** | Dostępność Serwisów Internetowych |

---

## 1. Wprowadzenie

### Idea i krótki opis

Projekt polega na stworzeniu serwisu internetowego w formie bloga turystycznego poświęconego **Budapesztowi** – stolicy Węgier. Strona pełni rolę przewodnika, który w przystępny i estetyczny sposób prezentuje najważniejsze informacje dla potencjalnych turystów: atrakcje, transport, gastronomię, noclegi oraz dane kontaktowe.

Głównym celem technicznym projektu było zaprojektowanie serwisu zgodnie z zasadami **dostępności cyfrowej (WCAG 2.1, poziom AA)**, tak aby mógł być wygodnie używany przez możliwie najszerszą grupę odbiorców – w tym osoby z niepełnosprawnościami wzrokowymi, słuchowymi i ruchowymi.

### Motywacja

Budapeszt to jedno z najchętniej odwiedzanych miast Europy Środkowej, a mimo to polskojęzycznych, dostępnych cyfrowo przewodników po nim jest niewiele. Projekt łączy dwa cele: stworzenie użytecznego źródła informacji turystycznych oraz demonstrację dobrych praktyk w projektowaniu dostępnych stron internetowych.

### Odbiorca

Serwis jest skierowany do:
- Turystów planujących wyjazd do Budapesztu
- Osób z niepełnosprawnościami, które potrzebują dostępnej cyfrowo informacji turystycznej
- Studentów i dydaktyków zainteresowanych przykładem wdrożenia wytycznych WCAG

---

## 2. Dane

### Źródła treści

Treści tekstowe opisujące atrakcje, transport i gastronomię zostały opracowane na podstawie ogólnodostępnej wiedzy o Budapeszcie i zredagowane na potrzeby projektu.

### Źródła zdjęć

Wszystkie zdjęcia użyte w serwisie zostały pobrane z **Wikimedia Commons** (licencja Creative Commons) oraz od dostawców treści (images.immediate.co.uk, globtroterek.com, buxida.pl) i są przechowywane lokalnie w repozytorium (`assets/images/`), co eliminuje zależność od zewnętrznych serwerów i ryzyko niedostępności materiałów graficznych.

| Plik | Źródło | Temat |
|---|---|---|
| `hero-budapeszt.jpeg` | images.immediate.co.uk | Panorama Budapesztu |
| `parlament.jpg` | globtroterek.com | Parlament Węgierski |
| `most-lancuchowy.jpg` | Wikimedia Commons | Most Łańcuchowy |
| `termy.jpg` | buxida.pl | Kąpieliska termalne |
| `baszta-rybacka.jpg` | Wikimedia Commons | Baszta Rybacka |
| `szimpla-kert.jpg` | Wikimedia Commons | Ruin bar Szimpla Kert |
| `metro-m1.jpg` | Wikimedia Commons | Metro linia M1 |
| `gulasz.jpg` | Wikimedia Commons | Tradycyjny gulasz |
| `budapeszt-noc.jpg` | Wikimedia Commons | Panorama nocna |
| `new-york-cafe.jpg` | Wikimedia Commons | New York Café |
| `gresham-palace.jpg` | Wikimedia Commons | Gresham Palace |
| `apartamenty.jpg` | Wikimedia Commons | Architektura Pesztu |
| `hostel.jpg` | Wikimedia Commons | Hostel |

### Selekcja i kompilacja danych

Zdjęcia zostały wybrane według kryteriów:
- Tematyczne dopasowanie do opisywanej sekcji
- Wysoka jakość graficzna przy rozsądnym rozmiarze pliku (do ~650 KB po przeskalowaniu)
- Dostępność na wolnych licencjach

Zdjęcia zostały pobrane programowo i przeskalowane do szerokości 1280 px, aby nie spowalniać ładowania strony.

---

## 3. Interfejs użytkownika

### Struktura wizualna strony

Każda podstrona zbudowana jest z tych samych, powtarzalnych elementów:

```
┌─────────────────────────────────────────────────┐
│  NAGŁÓWEK (logo + nawigacja)  ← sticky, zawsze  │
│                                    na górze      │
├─────────────────────────────────────────────────┤
│  HERO (tylko strona główna) lub PASEK TYTUŁOWY  │
├─────────────────────────────────────────────────┤
│  KOLOROWY PASEK ROZDZIELAJĄCY                   │
├─────────────────────────────────────────────────┤
│                                                 │
│  TREŚĆ GŁÓWNA (sekcje i artykuły)               │
│                                                 │
├─────────────────────────────────────────────────┤
│  STOPKA (nawigacja, info o projekcie)           │
└─────────────────────────────────────────────────┘
```

### Kolorystyka

Serwis korzysta z czterech kolorów głównych inspirowanych barwami węgierskiej flagi i historyczną architekturą Budapesztu:

| Kolor | Wartość | Zastosowanie |
|---|---|---|
| Czerwień | `#A93226` | Nagłówki, obramowania sekcji, nawigacja |
| Złoto | `#B7950B` | Akcenty, odznaki, kolorowe pasy |
| Zieleń | `#1E8449` | Przyciski, banery dostępności |
| Niebieski | `#1A5276` | Nagłówki artykułów, informacje |

Tło strony to ciepła biel (`#FFFDF7`), a tekst ciemny grafit (`#1A1A1A`), co zapewnia wysoki kontrast.

---

## 4. Struktura serwisu

### Mapa strony

```
index.html              ← Strona główna (hero, karty nawigacyjne, fakty)
│
├── atrakcje.html       ← Atrakcje (Parlament, Most, Termy, Baszta, Ruin bary)
├── transport.html      ← Transport (metro, tramwaje, autobusy, bilety)
├── baza gastronomiczna
│   i noclegowa.html    ← Gastronomia i noclegi (kuchnia, restauracje, hotele)
└── kontakt.html        ← Kontakt (formularz, info o projekcie)
```

### Pliki projektu

```
/
├── index.html                          ← Strona główna
├── atrakcje.html                       ← Podstrona Atrakcje
├── transport.html                      ← Podstrona Transport
├── baza gastronomiczna i noclegowa.html← Podstrona Gastronomia i noclegi
├── kontakt.html                        ← Podstrona Kontakt
├── assets/
│   ├── css/
│   │   └── style.css                  ← Cały styl wizualny (691 linii)
│   └── images/
│       ├── hero-budapeszt.jpeg
│       ├── parlament.jpg
│       └── ... (13 plików zdjęć)
└── _config.yml                         ← Konfiguracja GitHub Pages
```

### Technologie

| Technologia | Do czego służy |
|---|---|
| **HTML5** | Budowanie struktury i treści każdej podstrony |
| **CSS3** | Stylizacja – kolory, układ, responsywność |
| **GitHub Pages** | Bezpłatny hosting – strona działa pod adresem `github.io` |
| **Zmienne CSS** (`--kolor-...`) | Spójna paleta kolorów zarządzana w jednym miejscu |
| **CSS Grid i Flexbox** | Elastyczny układ siatki kart i stopki |
| **Media queries** | Dostosowanie wyglądu do ekranów telefonów i tabletów |

### Rozdzielenie treści od formy

Serwis ściśle oddziela **treść** (HTML) od **formy** (CSS):
- Pliki `.html` zawierają wyłącznie tekst, nagłówki, obrazki i semantyczne znaczniki
- Plik `style.css` zawiera wyłącznie reguły wizualne – kolory, marginesy, czcionki
- Zmiana wyglądu całego serwisu wymaga edycji tylko pliku CSS, bez dotykania treści

---

## 5. Elementy zwiększające dostępność strony

Serwis spełnia wytyczne **WCAG 2.1 na poziomie AA**. Poniżej wyjaśnienie każdego zastosowanego elementu prostym językiem.

---

### 5.1 Link „Pomiń nawigację" (Skip Navigation)

**Co to jest?**
Ukryty link na samym początku każdej strony, niewidoczny dla zwykłych użytkowników, ale dostępny dla osób poruszających się klawiaturą (klawisz `Tab`).

**Dlaczego pomaga?**
Osoby niewidome lub z niepełnosprawnością ruchową używają klawiatury lub czytnika ekranu. Bez tego linku musiałyby za każdym razem „przeklikiwać" przez całą nawigację, zanim dotrą do treści. Link pozwala od razu przeskoczyć do głównej treści strony.

**Gdzie jest w kodzie?**
```html
<a href="#tresc-glowna" class="pomin-nawigacje">
  Przejdź do treści głównej
</a>
```

---

### 5.2 Atrybuty `alt` przy zdjęciach

**Co to jest?**
Każde zdjęcie na stronie ma atrybut `alt` z opisem słownym tego, co przedstawia.

**Dlaczego pomaga?**
Czytniki ekranu (programy dla osób niewidomych) nie „widzą" obrazków – zamiast tego odczytują tekst `alt` na głos. Bez `alt` osoba niewidoma nie ma żadnej informacji o tym, co pokazuje zdjęcie.

**Przykład:**
```html
<img
  src="assets/images/parlament.jpg"
  alt="Neogotycki Parlament Węgierski oświetlony nocą,
       odbijający się w wodach Dunaju"
>
```

---

### 5.3 Semantyczne znaczniki HTML5

**Co to jest?**
Zamiast używać ogólnych znaczników `<div>` do wszystkiego, serwis używa znaczników opisujących rolę danego fragmentu:

| Znacznik | Co oznacza |
|---|---|
| `<header>` | Nagłówek strony (logo i nawigacja) |
| `<nav>` | Blok nawigacyjny |
| `<main>` | Główna treść strony |
| `<article>` | Samodzielny artykuł (np. opis atrakcji) |
| `<section>` | Sekcja tematyczna |
| `<aside>` | Treść poboczna (np. panel informacyjny) |
| `<footer>` | Stopka strony |

**Dlaczego pomaga?**
Czytniki ekranu i wyszukiwarki rozumieją strukturę strony. Użytkownik korzystający z czytnika może szybko przeskakiwać między sekcjami (np. „przejdź do nawigacji", „przejdź do treści głównej").

---

### 5.4 Atrybuty ARIA

**Co to jest?**
ARIA (Accessible Rich Internet Applications) to dodatkowe atrybuty HTML, które dostarczają czytnikom ekranu informacji, których same znaczniki nie przekazują.

**Zastosowane atrybuty:**

- `aria-label` – opisuje element, gdy jego treść wizualna nie wystarczy
  ```html
  <nav aria-label="Główna nawigacja">
  ```
- `aria-current="page"` – wskazuje czytnikowi ekranu, która strona jest aktualnie aktywna w nawigacji
  ```html
  <a href="atrakcje.html" aria-current="page">Atrakcje</a>
  ```
- `aria-required="true"` – informuje, że pole formularza jest obowiązkowe
  ```html
  <input aria-required="true" required>
  ```
- `aria-hidden="true"` – ukrywa element dekoracyjny przed czytnikami ekranu (np. emoji, ikonki)
  ```html
  <span aria-hidden="true">🏛️</span>
  ```
- `aria-labelledby` – łączy sekcję z jej nagłówkiem, co pomaga w nawigacji
  ```html
  <section aria-labelledby="tytul-atrakcje">
    <h2 id="tytul-atrakcje">Atrakcje</h2>
  ```
- `role="list"` / `role="listitem"` – informuje czytnik, że dany element jest listą

---

### 5.5 Widoczny fokus klawiatury

**Co to jest?**
Kiedy użytkownik porusza się po stronie klawiaturą (klawisz `Tab`), aktualnie wybrany element jest podświetlony żółtą ramką.

**Dlaczego pomaga?**
Osoby z niepełnosprawnością ruchową, które nie mogą używać myszy, muszą wiedzieć, gdzie aktualnie „jest" kursor na stronie. Bez widocznego fokusa strona jest dla nich nieużyteczna.

**Kod CSS:**
```css
:focus-visible {
  outline: 3px solid #F39C12; /* żółta ramka */
  outline-offset: 3px;
}
```

---

### 5.6 Wysoki kontrast kolorów

**Co to jest?**
Stosunek jasności między kolorem tekstu a tłem musi być wystarczająco duży, aby osoby słabowidzące mogły bez trudu przeczytać treść.

**Standard WCAG AA wymaga:**
- Minimum **4,5:1** dla normalnego tekstu
- Minimum **3:1** dla dużych nagłówków

**Jak to jest spełnione w serwisie:**
- Ciemny tekst `#1A1A1A` na białym tle `#FFFFFF` → kontrast **21:1** ✓
- Biały tekst na czerwonym tle nawigacji `#7B241C` → kontrast **9,4:1** ✓
- Ciemny tekst na kremowym tle `#FFFDF7` → kontrast **19:1** ✓

---

### 5.7 Responsywność (dostępność mobilna)

**Co to jest?**
Strona automatycznie dopasowuje swój wygląd do rozmiaru ekranu – wygląda dobrze zarówno na komputerze, tablecie, jak i smartfonie.

**Dlaczego pomaga?**
Osoby z niepełnosprawnościami często korzystają ze specjalnych urządzeń lub powiększają ekran, co zmienia jego efektywny rozmiar. Responsywna strona nie „psuje się" w takich warunkach.

**Kod CSS (przykład):**
```css
@media (max-width: 768px) {
  nav ul { flex-wrap: wrap; }
  main   { padding: 1.5rem 1rem; }
}
```

---

### 5.8 Obsługa trybu wysokiego kontrastu systemu operacyjnego

**Co to jest?**
Systemy Windows i macOS oferują tryb wysokiego kontrastu dla użytkowników słabowidzących. Strona reaguje na ten tryb i dostosowuje swój wygląd.

**Kod CSS:**
```css
@media (forced-colors: active) {
  .karta, article {
    border: 2px solid ButtonText;
  }
}
```

---

### 5.9 Redukcja ruchu animacji

**Co to jest?**
Niektóre osoby (np. z epilepsją lub zaburzeniami przedsionkowymi) są wrażliwe na animacje. System operacyjny może zgłaszać preferencję „zmniejsz ruch".

**Kod CSS:**
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    transition: none !important;
    animation: none !important;
  }
}
```

---

### 5.10 Etykiety w formularzu kontaktowym

**Co to jest?**
Każde pole formularza ma wyraźną etykietę `<label>` połączoną z polem przez atrybut `for`/`id`.

**Dlaczego pomaga?**
Czytniki ekranu odczytują etykietę, gdy użytkownik przechodzi do pola. Bez etykiety osoba niewidoma nie wie, co wpisać. Dodatkowo oznaczenie pól obowiązkowych (`*`) jest opisane słownie dla czytników.

**Przykład:**
```html
<label for="email">
  Adres e-mail
  <span aria-hidden="true">*</span>
</label>
<input id="email" type="email" aria-required="true">
```

---

### 5.11 Lazy loading zdjęć

**Co to jest?**
Atrybut `loading="lazy"` na zdjęciach sprawia, że przeglądarka ładuje obrazki dopiero wtedy, gdy użytkownik przewinie stronę do miejsca, gdzie są widoczne.

**Dlaczego pomaga?**
Osoby z wolniejszym łączem lub korzystające z asystywnych technologii (które mogą działać wolniej) nie muszą czekać na załadowanie wszystkich zdjęć naraz. Strona działa szybciej.

---

### 5.12 Właściwa hierarchia nagłówków

**Co to jest?**
Nagłówki są używane zgodnie z hierarchią: `<h1>` tylko raz na stronie (tytuł), `<h2>` dla sekcji, `<h3>` dla podsekcji.

**Dlaczego pomaga?**
Czytniki ekranu pozwalają użytkownikom nawigować po stronie skacząc między nagłówkami (jak spis treści). Prawidłowa hierarchia sprawia, że ta nawigacja ma sens.

---

## 6. Podsumowanie elementów dostępności

| Element | Standard WCAG | Poziom |
|---|---|---|
| Kontrast kolorów (tekst/tło) | 1.4.3 Contrast (Minimum) | AA |
| Opisy alternatywne zdjęć (`alt`) | 1.1.1 Non-text Content | A |
| Obsługa klawiatury | 2.1.1 Keyboard | A |
| Widoczny fokus | 2.4.7 Focus Visible | AA |
| Skip navigation | 2.4.1 Bypass Blocks | A |
| Etykiety formularzy | 1.3.1 Info and Relationships | A |
| Semantyczne znaczniki | 1.3.1 Info and Relationships | A |
| Język strony (`lang="pl"`) | 3.1.1 Language of Page | A |
| Responsywność | 1.4.4 Resize Text | AA |
| Redukcja ruchu | 2.3.3 Animation from Interactions | AAA* |
| Tryb wysokiego kontrastu | 1.4.11 Non-text Contrast | AA |

*Kryterium AAA – wykracza poza wymagania AA, zaimplementowane jako element dodatkowy.

---

## 7. Wkład pracy poszczególnych osób

| Osoba | Zakres prac |
|---|---|
| _[imię i nazwisko]_ | _[opis wkładu]_ |
| _[imię i nazwisko]_ | _[opis wkładu]_ |
