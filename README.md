# 🏕️ Travel Agency Database – Projekt i dokumentacja

Kompletny projekt bazy danych dla systemu wspomagającego działalność biura turystycznego.  
Zawiera on szczegółowy schemat bazy danych, definicje obiektów (tabele, widoki, procedury, triggery), reguły integralności, uprawnienia oraz przykładowe dane testowe.

Celem projektu jest dostarczenie gotowego do wdrożenia modelu danych, który może stanowić bazę dla docelowej aplikacji obsługującej sprzedaż wycieczek, rezerwacje oraz raportowanie.

---

## 📋 Zakres projektu

Projekt obejmuje:

- **Opis funkcji systemu** – zestawienie głównych możliwości z podziałem na role użytkowników.
- **Schemat bazy danych** – diagram ERD oraz szczegółowy opis tabel (kolumny, typy, klucze, ograniczenia).
- **Skrypty DDL** – kod do tworzenia tabel, indeksów, kluczy obcych, wartości domyślnych i warunków CHECK.
- **Widoki, procedury, funkcje, triggery** – implementacja logiki biznesowej (rezerwacje, modyfikacje, walidacje) oraz ułatwień raportowania.
- **Dane testowe** – skrypt generujący realistyczny zestaw danych do testowania i prezentacji.
- **Zarządzanie uprawnieniami** – definicje ról i poziomów dostępu do obiektów bazy danych.

---

## 🎯 Dla kogo jest ten projekt?

Projekt jest przeznaczony dla:

- **Developerów aplikacji** – mogą wykorzystać gotowy schemat i logikę bazy danych jako warstwę danych w nowej aplikacji webowej lub desktopowej.
- **Administratorów baz danych** – mogą wdrożyć go jako produkcyjną bazę danych po ewentualnych dostosowaniach.
- **Analityków biznesowych** – mogą korzystać z widoków raportowych do analizy sprzedaży, obłożenia wycieczek i wpłat.

---

## 🧱 Zawartość repozytorium

| Plik | Opis |
|------|------|
| `docs/functionality.md` | Opis funkcji systemu i macierz uprawnień |
| `docs/erd.png` | Diagram bazy danych |
| `sql/schema.sql` | Skrypt DDL – tworzenie tabel, kluczy, ograniczeń |
| `sql/views.sql` | Definicje widoków raportowych |
| `sql/procedures.sql` | Procedury składowane (rezerwacje, modyfikacje, płatności) |
| `sql/triggers.sql` | Triggers realizujące automatyczne sprawdzanie terminów i spójności |
| `sql/test_data.sql` | Skrypt wypełniający bazę przykładowymi danymi |
| `sql/roles.sql` | Definicje ról i nadanie uprawnień |

---

## 🚀 Jak wykorzystać ten projekt?

1. **Przegląd dokumentacji** – zacznij od zapoznania się z opisem funkcji i schematem bazy danych w folderze `docs`.
2. **Wdrożenie schematu** – wykonaj skrypty w odpowiedniej kolejności:
   - `schema.sql` – struktura bazy danych
   - `views.sql`
   - `procedures.sql`
   - `triggers.sql`
   - `roles.sql`
3. **Załadowanie danych testowych** – opcjonalnie uruchom `test_data.sql`, aby uzyskać przykładowe dane.
4. **Rozwijaj aplikację** – na bazie przygotowanego modelu możesz tworzyć aplikację kliencką (np. w C#, Javie, Pythonie) korzystającą z tego schematu.

---

## 📌 Uwagi implementacyjne

- Baza została zaprojektowana z myślą o **Microsoft SQL Server** (wersja 2019 lub nowsza).
- Wszystkie reguły biznesowe (terminy rezerwacji, limity miejsc, automatyczne anulowania) są zaimplementowane po stronie bazy danych – dzięki temu aplikacja kliencka nie musi ich samodzielnie egzekwować.
- Widoki raportowe zostały tak przygotowane, aby dostarczać gotowych zestawień (dostępność wycieczek, lista uczestników, historia wpłat) bez konieczności tworzenia złożonych zapytań.

---

## 📊 Przykładowe dane testowe

Skrypt `test_data.sql` generuje dane dla:

- 10 wycieczek w różnych terminach i miejscach
- 5–10 usług dodatkowych dla każdej wycieczki
- 50 klientów (firmy i osoby prywatne)
- 150 rezerwacji w różnych stanach (nowe, potwierdzone, anulowane, zakończone)
- Imiennych uczestników dla każdej rezerwacji
- Historii wpłat (częściowe i pełne)

Dzięki temu można od razu testować działanie procedur, widoków i raportów.

---

## 📄 Licencja i autor

Projekt został wykonany jako zadanie zaliczeniowe z przedmiotu [nazwa przedmiotu].  
Może być swobodnie wykorzystywany jako baza do dalszego rozwoju systemu zarządzania biurem turystycznym.

---

## 📬 Kontakt / uwagi

W przypadku pytań lub potrzeby dostosowania projektu do konkretnych wymagań prosimy o kontakt przez [mail/GitHub Issues].
