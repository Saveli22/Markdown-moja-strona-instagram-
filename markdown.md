# 📸 Projekt: Prosty Instagram

## 1. Opis projektu

Celem projektu jest stworzenie prostej aplikacji webowej wzorowanej na Instagramie. 
Użytkownicy będą mogli zakładać konta, logować się, dodawać posty ze zdjęciem, lajkować oraz komentować inne posty.

Projekt zostanie wykonany przy użyciu technologii:
- HTML
- CSS
- JavaScript
- PHP
- MySQL

---

## 2. Funkcjonalności aplikacji

### ✅ Rejestracja i logowanie
- Użytkownik może założyć konto (rejestracja).
- Użytkownik może się zalogować.
- Dane logowania będą sprawdzane w bazie danych.
- Hasła będą przechowywane w formie zaszyfrowanej (password_hash).
- Sesja użytkownika będzie obsługiwana przez session_start().

### ✅ Profil użytkownika
- Każdy użytkownik posiada swój profil.
- Na profilu widoczna będzie nazwa użytkownika.
- Wyświetlane będą wszystkie posty danego użytkownika.
- Możliwość wylogowania się.

### ✅ Dodawanie postów
- Użytkownik może dodać post (zdjęcie + opis).
- Post zapisywany jest w bazie danych.
- Każdy post zawiera datę dodania.

### ✅ System polubień (Like)
- Użytkownik może polubić post.
- Jeden użytkownik może polubić post tylko raz.
- Liczba polubień będzie widoczna pod postem.

### ✅ Komentarze
- Użytkownik może dodać komentarz pod postem.
- Komentarze są zapisywane w bazie danych.
- Pod postem wyświetlana jest lista komentarzy.

---

## 3. Struktura bazy danych (MySQL)

### Tabela: users
- id
- username
- email
- password
- created_at

### Tabela: posts
- id
- user_id
- image
- description
- created_at

### Tabela: likes
- id
- user_id
- post_id

### Tabela: comments
- id
- user_id
- post_id
- comment
- created_at

Relacje:
- posts.user_id → users.id
- likes.user_id → users.id
- likes.post_id → posts.id
- comments.user_id → users.id
- comments.post_id → posts.id

---

## 4. Backend (PHP)

PHP będzie odpowiedzialne za:
- połączenie z bazą danych (PDO lub mysqli),
- rejestrację użytkowników,
- logowanie i sprawdzanie haseł,
- dodawanie postów,
- obsługę lajków,
- zapisywanie komentarzy,
- zarządzanie sesją użytkownika.

---

## 5. Frontend (HTML, CSS, JavaScript)

### HTML
- Struktura strony (formularze, posty, profil).

### CSS
- Styl podobny do Instagrama.
- Responsywny układ (Flexbox / Grid).
- Nowoczesny wygląd.

### JavaScript
- Obsługa przycisku Like bez przeładowania strony (fetch / AJAX).
- Dynamiczne dodawanie komentarzy.
- Interakcje użytkownika.

---

## 6. Struktura plików projektu

- index.php – strona główna (feed)
- register.php – rejestracja
- login.php – logowanie
- logout.php – wylogowanie
- profile.php – profil użytkownika
- add_post.php – dodawanie postów
- like.php – obsługa polubień
- comment.php – obsługa komentarzy
- db.php – połączenie z bazą danych
- style.css – wygląd strony
- script.js – logika JavaScript

---

## 7. Podsumowanie

Projekt będzie prostą wersją aplikacji typu Instagram, umożliwiającą:
- tworzenie kont,
- logowanie użytkowników,
- publikowanie zdjęć,
- lajkowanie postów,
- komentowanie treści.

Celem projektu jest stworzenie w pełni działającej aplikacji webowej z wykorzystaniem technologii frontendowych i backendowych.
