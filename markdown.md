# 📸 SocialApp – Webowa Platforma Społecznościowa (Instagram)

## 1. Architektura systemu

Projekt oparty jest na architekturze klient–serwer (Client–Server), zapewniającej wyraźny podział na warstwę prezentacji, logiki biznesowej oraz bazę danych.

System składa się z trzech głównych warstw:

---

## 2. Warstwa prezentacji (Frontend)

Technologie: HTML, CSS, JavaScript

Frontend odpowiada za:
- renderowanie interfejsu użytkownika,
- wyświetlanie feedu postów,
- obsługę interakcji (like, komentarze),
- komunikację z backendem poprzez zapytania HTTP (Fetch / AJAX).

Cechy:
- responsywny design (RWD),
- dynamiczne aktualizowanie danych bez przeładowania strony,
- intuicyjny interfejs inspirowany nowoczesnymi mediami społecznościowymi.

---

## 3. Warstwa logiki aplikacji (Backend)

Technologia: PHP

Backend odpowiada za:
- obsługę autoryzacji i uwierzytelniania użytkowników,
- zarządzanie sesjami,
- przetwarzanie danych przesyłanych z frontendu,
- obsługę systemu polubień i komentarzy,
- kontrolę dostępu do zasobów.

Architektura backendu oparta jest na modularnych endpointach (np. logowanie, dodawanie postów, obsługa lajków), co pozwala na łatwą rozbudowę systemu w przyszłości.

---

## 4. Warstwa danych (Baza danych)

Technologia: MySQL

System wykorzystuje relacyjną bazę danych z odpowiednio zaprojektowanymi relacjami między tabelami:

- users – dane użytkowników
- posts – przechowywanie postów
- likes – relacje polubień
- comments – system komentarzy

Zastosowanie kluczy obcych zapewnia spójność danych i integralność relacji.

---

## 5. Bezpieczeństwo

System uwzględnia:
- szyfrowanie haseł (password_hash),
- zarządzanie sesją użytkownika,
- walidację danych wejściowych,
- zabezpieczenie przed wielokrotnym polubieniem tego samego posta.

---

## 6. Skalowalność i rozwój

Architektura umożliwia:
- łatwe dodanie systemu obserwowania użytkowników,
- wprowadzenie prywatnych wiadomości,
- implementację powiadomień w czasie rzeczywistym,
- migrację do frameworków (np. Laravel) w przyszłości.

---

## 7. Podsumowanie

Projekt stanowi nowoczesną, skalowalną aplikację społecznościową opartą na technologii webowej. 
Dzięki podziałowi na warstwy (Frontend – Backend – Baza danych) system jest przejrzysty, bezpieczny i gotowy do dalszego rozwoju.
