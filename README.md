# HomeTracker — interaktywna oferta dla partnerów

Gotowa statyczna strona internetowa, którą można wdrożyć na **GitHub Pages** bez Node.js, instalacji pakietów i osobnego serwera.

## Uruchomienie na GitHub Pages

1. Utwórz repozytorium GitHub, np. `hometracker-oferta`.
2. Wgraj **zawartość tego folderu**, a nie sam plik ZIP: `index.html`, `styles.css`, `app.js`, katalog `assets/` oraz `README.md` i ewentualnie pozostałe pliki dokumentacji.
3. W repozytorium przejdź do **Settings → Pages → Build and deployment**.
4. Ustaw **Source: Deploy from a branch**, **Branch: main**, **Folder: / (root)**, zapisz.
5. Po wdrożeniu link będzie miał strukturę `https://NAZWA-UZYTKOWNIKA.github.io/hometracker-oferta/` (lub własną domenę po konfiguracji DNS).

## Co działa bez backendu

- responsywny design, mobilne menu i nawigacja;
- interaktywny podgląd analiz A/B i osobno przykładowy scenariusz diagnostyczny;
- kalkulator pakietów: wszystkie dziewięć progów i warianty testu; roczne rozliczenie -40% jako opcja alternatywna;
- kalkulator prowizji od kredytu (0,8%) i od usług prawnych (8%);
- rozwijane scenariusze usług `coming soon` i historie użycia dla agencji, dewelopera, usługodawcy;
- 12 pełnych, nieredagowanych rozdziałów dotychczasowej oferty w części „Pełna treść źródłowa”;
- formularz **przygotowujący e-mail** i alternatywna kopia wiadomości do schowka. **Nie wysyła danych na serwer i nie tworzy zgłoszeń w CRM.**

## Przed opublikowaniem

- **Zatwierdź szczegóły programu hipotecznego.** W dokumencie agencyjnym z 13.10.2026 r. podano 0,8% dla strony nazwanej „Agentem”, po uruchomieniu kredytu i wpływie pełnego wynagrodzenia do „Zleceniodawcy”, przy dodatkowych warunkach klienta i zgody. Nie utożsamiaj tego bez osobnej umowy z automatycznie należną prowizją każdego użytkownika HomeTracker.
- **Uzgodnij podstawę 8% w programie prawnym**: netto/brutto, status usługi, moment wymagalności, przypadki odrzucenia, RODO. Kalkulator to symulacja przykładowa.
- **Uzgodnij szczegóły 20% przy sprzedawcach prywatnych**: faktycznie otrzymana przez agencję prowizja, kwalifikacja, pochodzenie leada, zamknięcie transakcji, rozliczenia i ewentualna wyłączność.
- Ustal politykę prywatności / ochrony danych dla właściwego modelu działalności. Na obecnej statycznej stronie żadne dane formularza nie są automatycznie zbierane.
- Zaplanuj integrację z CRM lub działającym endpointem i zgody marketingowe, jeśli formularz ma w przyszłości **realnie wysyłać zgłoszenia**.
- Zweryfikuj aktualność cennika przed kampanią oraz domyślny adres `sales@hometracker.pro`.
- Zamień oznaczenia `w przygotowaniu` na `aktywne` dopiero po uruchomieniu i zatwierdzeniu zasad programu.

## Zawartość

```
index.html          — pełna oferta i wszystkie 12 rozdziałów kanonicznej treści
styles.css          — responsywny autorski układ
app.js              — kalkulatory, przełączniki, scenariusze, formularz
assets/             — oryginalne logo HomeTracker i favicon
README.md           — instrukcja wdrożenia i warunki publikacji
WARUNKI_I_ZRODLA.md — pochodzenie liczb, rozróżnienie faktów i założeń
```

## Lokalny podgląd

Otwórz `index.html` w przeglądarce (większość funkcji działa bez serwera) lub, jeśli masz Pythona:

```bash
python -m http.server 8000
```

Następnie wejdź na `http://localhost:8000`.

## Technologia / dostępność

HTML, CSS, JavaScript ES2020+, bez zewnętrznych bibliotek, trackerów, fontów CDN i nieuzasadnionych obrazów stockowych. Menu i rozdziały obsługiwane klawiaturą; ograniczenie ruchu zgodne z `prefers-reduced-motion`.
