# 📸 SocialApp – Webowa Platforma Społecznościowa (Instagram)

## 1. Architektura systemu
Projekt oparty jest na sprawdzonej **architekturze klient–serwer (Client–Server)**, która zapewnia wyraźny podział na:

- Warstwę prezentacji (Frontend)
- Warstwę logiki biznesowej (Backend)
- Warstwę danych (Baza danych)

Takie podejście gwarantuje przejrzystość systemu, łatwość rozwoju oraz bezpieczeństwo danych.

---

## 2. Warstwa prezentacji (Frontend)
**Technologie:** HTML, CSS, JavaScript  

Frontend odpowiada za:

- Renderowanie interfejsu użytkownika
- Wyświetlanie feedu postów
- Obsługę interakcji (lajki, komentarze)
- Komunikację z backendem poprzez zapytania HTTP (Fetch / AJAX)

**Cechy wyróżniające:**

- Responsywny design (RWD)
- Dynamiczne aktualizowanie danych bez przeładowania strony
- Intuicyjny interfejs inspirowany nowoczesnymi mediami społecznościowymi

---

## 3. Warstwa logiki aplikacji (Backend)
**Technologia:** PHP  

Backend odpowiada za:

- Autoryzację i uwierzytelnianie użytkowników
- Zarządzanie sesjami
- Przetwarzanie danych przesyłanych z frontendu
- Obsługę systemu polubień i komentarzy
- Kontrolę dostępu do zasobów

**Architektura backendu:**  
Modularne endpointy (logowanie, dodawanie postów, obsługa lajków) umożliwiają łatwe rozbudowywanie systemu w przyszłości.

---

## 4. Warstwa danych (Baza danych)
**Technologia:** MySQL  

Baza danych jest relacyjna, z logicznie zaprojektowanymi relacjami między tabelami:

- `users` – dane użytkowników
- `posts` – przechowywanie postów
- `likes` – relacje polubień
- `comments` – system komentarzy

Zastosowanie **kluczy obcych** zapewnia spójność danych i integralność relacji.

---

## 5. Bezpieczeństwo
System uwzględnia:

- **Szyfrowanie haseł** (`password_hash`) – chroni dane logowania użytkowników
- **Walidacja i filtrowanie danych wejściowych** – zabezpiecza przed atakami typu XSS i SQL Injection
- **Zabezpieczenie sesji użytkownika** – uniemożliwia nieautoryzowane logowanie
- **Ograniczenie wielokrotnego polubienia tego samego posta**
- **Bezpieczne operacje po stronie backendu** – wszystkie krytyczne działania (dodawanie postów, polubienia, komentarze) są przetwarzane tylko na serwerze, co chroni przed manipulacją w konsoli przeglądarki
- **Oddzielenie danych wrażliwych od frontendowego DOM** – np. nie przechowujemy haseł czy tokenów w `localStorage`

---

## 6. Skalowalność i rozwój
Architektura umożliwia:

- Dodanie systemu obserwowania użytkowników
- Wprowadzenie prywatnych wiadomości
- Implementację powiadomień w czasie rzeczywistym
- Migrację do frameworków PHP (np. Laravel) w przyszłości

---

## 7. Podsumowanie
**SocialApp** to nowoczesna, skalowalna aplikacja społecznościowa oparta na technologii webowej.  
Dzięki wyraźnemu podziałowi na **Frontend – Backend – Baza danych**, system jest:

- Przejrzysty
- Bezpieczny
- Gotowy do dalszego rozwoju i integracji nowych funkcjonalności
