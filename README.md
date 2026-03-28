# 🏕️ Travel Agency Database – Dokumentacja projektu

Repozytorium zawiera kompletny projekt bazy danych dla systemu wspomagającego działalność biura turystycznego.  
Wszystkie elementy – schemat bazy danych, skrypty DDL, widoki, procedury, triggery, definicje uprawnień oraz przykładowe dane testowe – zostały zebrane w jednym pliku **`Database.pdf`**.

Dokument ten może stanowić gotową specyfikację dla deweloperów, administratorów baz danych lub analityków, którzy chcą zbudować aplikację opartą na tym modelu danych.

---

## 📋 Zakres projektu

Projekt obejmuje:

- **Opis funkcji systemu** – zestawienie głównych możliwości z podziałem na role użytkowników.
- **Schemat bazy danych** – diagram ERD oraz szczegółowy opis tabel (kolumny, typy, klucze, ograniczenia).
- **Skrypty DDL** – kod do tworzenia tabel, indeksów, kluczy obcych, wartości domyślnych i warunków CHECK.
- **Widoki, procedury, funkcje, triggery** – implementacja logiki biznesowej (rezerwacje, modyfikacje, walidacje) oraz ułatwień raportowania.
- **Zarządzanie uprawnieniami** – definicje ról i poziomów dostępu do obiektów bazy danych.

---

## 🎯 Dla kogo jest ten dokument?

- **Developerzy aplikacji** – znajdą w nim gotowy model danych i logikę biznesową, którą mogą wykorzystać jako warstwę danych w nowej aplikacji webowej lub desktopowej.
- **Administratorzy baz danych** – mogą wdrożyć opisany schemat jako produkcyjną bazę danych po ewentualnych dostosowaniach.
- **Analitycy biznesowi** – mogą korzystać z zaproponowanych widoków raportowych do analizy sprzedaży, obłożenia wycieczek i wpłat.

---

## 🚀 Jak wykorzystać ten projekt?

1. **Pobierz plik `Database.pdf`** – zawiera on wszystkie informacje niezbędne do wdrożenia bazy danych.
2. **Zapoznaj się z dokumentacją** – w szczególności ze schematem bazy danych, opisami tabel oraz skryptami DDL.
3. **Wdróż schemat** – korzystając z dołączonych skryptów SQL (zamieszczonych w dokumencie) utwórz bazę danych w środowisku Microsoft SQL Server.
4. **Rozwijaj aplikację** – na bazie przygotowanego modelu możesz tworzyć aplikację kliencką (np. w C#, Javie, Pythonie) korzystającą z tego schematu.

---

## 📌 Uwagi implementacyjne

- Baza została zaprojektowana z myślą o **Microsoft SQL Server** (wersja 2019 lub nowsza).
- Wszystkie reguły biznesowe (terminy rezerwacji, limity miejsc, automatyczne anulowania) są zaimplementowane po stronie bazy danych – dzięki temu aplikacja kliencka nie musi ich samodzielnie egzekwować.
- Widoki raportowe zostały tak przygotowane, aby dostarczać gotowych zestawień (dostępność wycieczek, lista uczestników, historia wpłat) bez konieczności tworzenia złożonych zapytań.

---

## 📄 Licencja

Projekt może być swobodnie wykorzystywany jako baza do dalszego rozwoju systemu zarządzania biurem turystycznym.

---

## 📬 Kontakt / uwagi

W przypadku pytań lub potrzeby dostosowania projektu do konkretnych wymagań prosimy o kontakt przez [mail/GitHub Issues].
