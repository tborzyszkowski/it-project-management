# Jira – Pełny przykład: Sprint 1 w projekcie „Śmierć przychodzi o świcie"

> Dokument pokazuje **kompletny przebieg Sprintu 1** z perspektywy obsługi Jiry:  
> uruchomienie sprintu → praca na tablicy → impedimenty → review → zamknięcie.  
> Każdy krok jest ilustrowany konkretnymi danymi z przykładowego projektu.

---

## Dane projektu

| Element | Wartość |
|---|---|
| **Projekt w Jira** | `Śmierć przychodzi o świcie` (klucz: `SPC`) |
| **Site** | `bim-kryminal.atlassian.net` |
| **Sprint** | Sprint 1 – czas trwania 45 minut |
| **Cel sprintu** | „Napisać i zreviewować Rozdział 1 oraz profile postaci" |

### Skład zespołu

| Rola | Imię | Login w Jira |
|---|---|---|
| Product Owner | Karolina | karolina@example.com |
| Scrum Master | Marek | marek@example.com |
| Developer | Zofia | zofia@example.com |
| Developer | Piotr | piotr@example.com |
| Developer / QA | Natalia | natalia@example.com |

### Sprint Backlog – co zaplanowano na Sprint 1

| ID | Story | Story Points | Assignee |
|---|---|---|---|
| `SPC-5` | Profil komisarz Anny Wolskiej (min. 200 słów) | 2 | Zofia |
| `SPC-6` | Profil antagonisty – wstępny szkic | 3 | Piotr |
| `SPC-7` | Rozdział 1 – odkrycie ciała (min. 300 słów) | 5 | Zofia + Piotr |
| `SPC-8` | Opis miejsca akcji – Czerna w Beskidach (min. 150 słów) | 2 | Natalia |
| `SPC-9` | Review i korekta Rozdziału 1 | 2 | Natalia (QA) |

**Łącznie: 14 Story Points**

---

## Krok 1 – Marek (SM) uruchamia sprint

**Godzina: 10:00**

1. Marek otwiera Jirę: `bim-kryminal.atlassian.net`
2. Klika **„Backlog"** w lewym menu
3. W sekcji Sprint 1 widzi 5 Stories z przypisanymi SP
4. Klika **„Start sprint"**
5. Pojawia się okno:
   ```
   Sprint name: Sprint 1
   Duration: Custom
   Start date: 16 maja 2026, 10:00
   End date:   16 maja 2026, 10:45
   Sprint goal: Napisać i zreviewować Rozdział 1 oraz profile postaci
   ```
6. Klika **„Start"**

> ✅ Jira przełącza się na Board. Wszystkie Stories stoją w kolumnie **To Do**.

Marek głośno komunikuje: **„Sprint 1 – Start! Mamy 45 minut. Powodzenia!"**

Marek ustawia timer na **22 minuty** (Daily Scrum).

---

## Krok 2 – Developerzy biorą Stories (10:00–10:05)

### Zofia bierze SPC-5 (Profil komisarz Anny Wolskiej)

1. Zofia otwiera Board → widzi `SPC-5` w kolumnie **To Do**
2. Przeciąga kartę `SPC-5` do kolumny **In Progress**
3. Klika tytuł karty → otwiera panel boczny
4. Sprawdza pole **Assignee** → widzi swoje imię ✅
5. Zamyka panel i zaczyna pisać prompt

### Piotr bierze SPC-8 (Opis miejsca akcji)

> Choć `SPC-8` jest przypisane do Natalii, Piotr ma chwilę wcześniej wolne.  
> Piotr pyta Natalię: „Mogę wziąć opis Czernej, żebyś mogła zacząć od razu QA?"  
> Natalia zgadza się → Piotr przeciąga `SPC-8` do **In Progress** i zmienia Assignee na siebie.

**Jak zmienić Assignee:**
1. Kliknij kartę `SPC-8` na Board
2. W prawym panelu kliknij pole **„Assignee"**
3. Wybierz z listy: **Piotr**
4. Pole zapisuje się automatycznie

### Natalia zaczyna przygotowania do QA

Natalia otwiera `SPC-9` (Review Rozdziału 1) i widzi, że nie ma jeszcze co reviewować.  
Postanawia zamiast tego pomóc Zofii i bierze `SPC-6` (Profil antagonisty).

---

## Krok 3 – Praca podczas sprintu (10:05–10:22)

### Zofia pisze profil komisarz Wolskiej

Zofia korzysta z ChatGPT:
```
Jesteś autorem kryminału pisanym po polsku, styl Agathy Christie.

Kontekst: Górskie miasteczko Czerna w Beskidach. Jesień.
Zadanie: Stwórz profil postaci komisarz Anny Wolskiej.
Format: imię, wiek, wygląd, charakter, słabości, motywacja.
Długość: min. 200 słów.
```

Redaguje wynik, wkleja do Google Docs pod nagłówkiem „Bohaterowie".

**Aktualizacja Jiry:**
1. Zofia otwiera `SPC-5` na Board
2. Dodaje komentarz:
   ```
   Profil gotowy – 247 słów. Wklejony do Google Docs, sekcja "Bohaterowie". 
   Czeka na review.
   ```
3. Przeciąga kartę do kolumny **In Progress → Review**  
   *(lub zmienia status przyciskiem u góry panelu)*

### Piotr pisze opis Czernej

Piotr generuje opis z AI, redaguje, wkleja do dokumentu.

**Aktualizacja Jiry:**
1. Piotr otwiera `SPC-8`
2. Zmienia status na **„Done"** *(mały element, DoD spełnione bez formalnego QA)*
3. Dodaje komentarz:
   ```
   Opis gotowy – 189 słów. Wklejony do Google Docs, sekcja "Świat i miejsce akcji".
   ```

> ℹ️ SPC-8 miało tylko 2 SP i kryterium 150 słów – Piotr napisał 189. DoD spełnione.

---

## Krok 4 – Impediment (10:15)

Piotr zaczyna pracę nad `SPC-6` (profil antagonisty) i zgłasza problem Markowi:

> „Marek, nie mam pojęcia jak wygląda praca prokuratora w Polsce – chcę zrobić z niego prokuratora, ale nie chcę zmyślać szczegółów. Blokuje mnie to."

**Marek tworzy Task-impediment:**

1. Klika **„+ Create"** w górnym menu
2. Ustawia:
   ```
   Issue type: Task
   Summary: IMPEDIMENT: DEV Piotr – brak wiedzy o realiach prokuratury PL
   Assignee: Marek
   Labels: impediment
   Description: Piotr pisze profil prokuratora-antagonisty. Brak wiedzy o realiach.
                Proponowane rozwiązanie: wskazać zasoby do szybkiego researchu.
   ```
3. Klika **„Create"**

**Marek rozwiązuje impediment:**

Marek mówi do Piotra:
> „Skorzystaj z tego prompta i nie przejmuj się realiami – fikcja literacka ma pierwszeństwo. Napisz że jest prokuratorem okręgowym z Krakowa, który przyjechał na urlop."

Marek zamienia status Taska-impedimentu na **„Done"** i dodaje komentarz:
```
Rozwiązanie: zaproponowano podejście "fikcja literacka, nie dokument". 
Piotr odblokowuny. Czas rozwiązania: 3 min.
```

---

## Krok 5 – Daily Scrum (10:22)

Timer Marka dzwoni. Marek przerywa sprint.

> *[Daily Scrum opisany w Zadaniach 2B i JIRA_DETAILS.md katalogu 2B-DailyScrum]*

Po Daily Scrum (10:32) sprint wraca do pracy.

---

## Krok 6 – Kontynuacja i finalizacja (10:32–10:45)

### Zofia i Piotr piszą Rozdział 1 (SPC-7)

Wspólnie generują i redagują tekst. Zofia wkleja do dokumentu.

**Aktualizacja Jiry (SPC-7):**
1. Zofia otwiera `SPC-7` → dodaje komentarz:
   ```
   Rozdział 1 gotowy – 412 słów. Wklejony do Google Docs, sekcja "Rozdział 1: Odkrycie".
   Link do dokumentu: [https://docs.google.com/...]
   Czeka na review QA – Natalia.
   ```
2. Przeciąga kartę `SPC-7` do kolumny **Review**

### Natalia przeprowadza QA (SPC-5 i SPC-7)

**Sprawdzenie SPC-5 (profil komisarz Wolskiej):**

DoD checklist:
```
[✅] Tekst liczy min. 200 słów → 247 słów ✅
[✅] Postać ma imię, wiek, wygląd, charakter, słabości → ✅
[✅] Tekst wklejony do dokumentu Google Docs → ✅
[✅] Spójność z gatunkiem (kryminał) → ✅
```

Natalia otwiera `SPC-5` → zmienia status na **„Done"** → dodaje komentarz:
```
QA: DoD spełnione ✅ Profil zawiera wszystkie wymagane elementy, 247 słów. Approved.
```

**Sprawdzenie SPC-7 (Rozdział 1):**

DoD checklist:
```
[✅] Tekst liczy min. 300 słów → 412 słów ✅
[✅] Imiona postaci spójne z profilem → ✅ (Anna Wolska, prokurator bez imienia – do uzupełnienia)
[⚠️] Styl odpowiada gatunkowi → w 80% ✅, jeden akapit zbyt lekki tonem
[✅] Tekst wklejony do dokumentu → ✅
```

Natalia otwiera `SPC-7` → dodaje komentarz:
```
QA: ⚠️ Prawie gotowe – 412 słów ✅, ale akapit 3 ma zbyt lekki ton jak na kryminał.
Proszę przyciemnić klimat. Zwracam do In Progress.
```
Przeciąga `SPC-7` z powrotem do **In Progress**.

Piotr poprawia akapit 3 (5 minut), Zofia zatwierdza.

Zofia aktualizuje komentarz:
```
Poprawiono akapit 3 – klimat przyciemniony. Gotowe do ponownego review.
```

Natalia ponownie weryfikuje → zmienia status `SPC-7` na **Done**.

---

## Stan sprintu po 45 minutach

### Widok Board po zakończeniu

| Kolumna | Stories |
|---|---|
| **To Do** | (puste) |
| **In Progress** | (puste) |
| **Done** | SPC-5, SPC-6, SPC-7, SPC-8 |

> ⚠️ SPC-9 (Review dodatkowy) nie zostało wykonane – zostaje w Backlogu.

### Velocity Sprint 1

Ukończone Story Points:
- SPC-5: 2 SP ✅
- SPC-6: 3 SP ✅
- SPC-7: 5 SP ✅
- SPC-8: 2 SP ✅
- SPC-9: 2 SP ❌ (nie ukończone)

**Velocity = 12 SP** (z planowanych 14 SP)

Marek otwiera **Reports → Burndown Chart** i pokazuje wykres na projektorze przed Sprint Review.
