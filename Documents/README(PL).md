## Opis projektu

### Cel:

Projekt "Dinosaur Game" ma na celu stworzenie wiernej kopii popularnej gry offline dostępnej w przeglądarce Google Chrome. Gra będzie działać jako samodzielna aplikacja, oferując użytkownikom tę samą rozrywkę, z dodatkowymi możliwościami, takimi jak personalizacja postaci oraz zapis wyników.

### Opis funkcji:

- **Podstawowa rozgrywka:** Gracz steruje dinozaurem, który unika przeszkód, takich jak kaktusy i ptaki, skacząc lub kucając.
- **Personalizacja:** Możliwość zmiany wyglądu dinozaura oraz tła gry.
- **Tablica wyników:** Zapisywanie i przeglądanie najlepszych wyników gracza.
- **Tryb nocny:** Automatyczna zmiana tła w zależności od pory dnia.
- **Dostępność offline:** Gra działa bez potrzeby połączenia z internetem.

## Analiza wymagań

### Wymagania funkcjonalne:

- **Rozgrywka:** Gracz steruje dinozaurem za pomocą klawiatury (strzałki, spacja) lub ekranu dotykowego.
- **Zapis wyników:** Aplikacja rejestruje najlepsze wyniki i wyświetla je w tablicy liderów.
- **Personalizacja:** Użytkownik może wybrać wygląd dinozaura, takie jak kolor lub akcesoria (np. czapki).
- **Tryb nocny:** Tło gry zmienia się automatycznie lub na żądanie użytkownika.
- **Pauza i reset:** Opcje wstrzymania gry oraz rozpoczęcia nowej rozgrywki.

### Wymagania niefunkcjonalne:

- **Płynność gry:** Rozgrywka ma być płynna, bez opóźnień.
- **Dostępność na różnych platformach:** Gra powinna działać zarówno na komputerach, jak i urządzeniach mobilnych.
- **Intuicyjność:** Prosty i przejrzysty interfejs, łatwy w obsłudze nawet dla początkujących graczy.
- **Optymalizacja:** Niskie wymagania sprzętowe, umożliwiające grę na starszych urządzeniach.

## Projekt interfejsu

### Szkice/wizualizacje interfejsu:

- _Ekran główny:_ Menu z przyciskami „Start”, „Tablica wyników”, „Opcje”.
- _Ekran gry:_ Widok dinozaura biegnącego po pustyni, z przeszkodami i licznikiem punktów w górnym rogu.
- _Ekran wyników:_ Lista najlepszych wyników z nazwami graczy i punktacją.

### Mapa strony:

- _Strona główna_
  - Start gry
  - Tablica wyników
  - Opcje
- _Ekran gry_
  - Dinozaur biegnący po torze przeszkód
  - Licznik punktów
  - Przycisk pauzy
- _Tablica wyników_
  - Lista wyników
  - Opcja powrotu do menu
- _Opcje_
  - Personalizacja dinozaura
  - Tryb nocny
  - Reset ustawień

## Architektura systemu

### Opis struktury danych:

Aplikacja przechowuje dane związane z rozgrywką, w tym:

- **Wyniki:** Tablica rekordów graczy z punktacją.
- **Ustawienia personalizacji:** Wybrane kolory i akcesoria dinozaura.
- **Postęp gry:** Aktualne statystyki rozgrywki, takie jak liczba punktów.

### Diagramy architektury:

Architektura opiera się na wzorcu MVC:

- **Model:** Zarządza logiką gry (np. generowaniem przeszkód, naliczaniem punktów).
- **Widok (View):** Odpowiada za graficzną reprezentację gry.
- **Kontroler (Controller):** Obsługuje interakcje użytkownika i synchronizuje je z modelem.

## Implementacja

### Opis technologii:

- **Frontend:** HTML5, CSS3, JavaScript (Canvas API do grafiki 2D).
- **Backend:** Node.js (opcjonalnie, jeśli wymagane są funkcje online, np. globalne tablice wyników).
- **Baza danych:** SQLite (do lokalnego przechowywania wyników i ustawień).

### Struktura kodu:

- _Katalogi/pliki_:
  - `game.js` (logika gry)
  - `style.css` (stylizacja)
  - `index.html` (strona główna)
  - `settings.js` (zarządzanie personalizacją)
- _Style pisania kodu_: Modularne podejście z dokumentacją funkcji w komentarzach.

## Testowanie

### Plan testów:

- **Testy jednostkowe:** Sprawdzanie funkcji obsługi ruchu dinozaura, generowania przeszkód i naliczania punktów.
- **Testy integracyjne:** Sprawdzanie współpracy między modułami, np. logiki gry i widoku.
- **Testy interfejsu użytkownika:** Testowanie interakcji z menu i rozgrywką na różnych urządzeniach.
- **Testy wydajnościowe:** Ocena płynności gry przy różnych prędkościach i liczbie przeszkód.

### Procedury testowania:

- Tworzenie przypadków testowych dla każdej funkcji.
- Raportowanie błędów z sugestiami ich rozwiązania.

## Wdrożenie i konserwacja

### Plan wdrożenia:

- **Etapy wdrażania:**
  - Implementacja podstawowej mechaniki gry.
  - Dodanie personalizacji i tablicy wyników.
  - Testowanie i optymalizacja.
  - Publikacja aplikacji na platformach desktop i mobilnych.
- **Terminy:** Podział prac na krótkie iteracje sprintowe.

### Procedury konserwacji:

- **Wsparcie techniczne:** Kanał komunikacji do zgłaszania problemów przez graczy.
- **Aktualizacje:** Regularne poprawki błędów i dodawanie nowych funkcji, takich jak dodatkowe motywy graficzne.
