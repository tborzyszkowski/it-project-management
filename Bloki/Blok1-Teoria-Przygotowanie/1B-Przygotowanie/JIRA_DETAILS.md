# Jira Free – Szczegółowe kroki

> Dokument uzupełniający do `Zadania.md` — zawiera dokładne opisy ekranów i przycisków.  
> Używaj go gdy instrukcja w Zadaniach.md jest niewystarczająca lub coś wygląda inaczej.

---

## 1. Założenie konta darmowego i zaproszenie współpracowników

### 1.1 Rejestracja konta Atlassian

1. Otwórz: **https://www.atlassian.com/software/jira/free**

2. Kliknij niebieski przycisk **„Get it free"**

3. Wybierz sposób rejestracji:
   - **E-mail** → wpisz adres → kliknij **„Agree – Sign Up"**  
   - Lub zaloguj się przez **Google / Apple / Microsoft** — rejestracja jest szybsza

4. Sprawdź skrzynkę — Atlassian wysyła **6-cyfrowy kod weryfikacyjny**  
   *(Sprawdź folder SPAM / Oferty jeśli nie ma po 2 minutach)*

5. Wpisz kod → kliknij **„Verify"**

6. Ustaw hasło (min. 8 znaków, musi zawierać cyfrę lub znak specjalny) → **„Continue"**

7. Wpisz imię i nazwisko → **„Continue"**

8. Jira pyta o **nazwę site** (Twojej przestrzeni Atlassian):
   - Wpisz: `bim-[nazwazespolu]` *(np. `bim-kryminal`)*
   - Tylko litery, cyfry i myślniki. Bez polskich znaków!
   - Adres Twojej Jiry: `bim-[nazwazespolu].atlassian.net`
   - Kliknij **„Continue"**

9. *„What kind of work does your team do?"* → **„Software development"** → **„Next"**

10. Wybierz szablon projektu → kliknij **„Scrum"** → **„Select"**

11. Typ projektu → **„Team-managed project"** *(prostszy; company-managed ma więcej opcji konfiguracji)*

12. **Project name** → tytuł waszej powieści *(np. „Zbrodnia w Zamku Blum")*

13. Kliknij **„Create project"** — Jira otwiera widok **Backlog**

> ✅ Widzisz pusty Backlog z lewym menu: Backlog, Board, Reports, Project settings — konto gotowe.

---

### 1.2 Zaproszenie współpracowników do projektu

**Wykonuje: Scrum Master (właściciel projektu)**

1. W lewym menu kliknij **„Project settings"** (ikona koła zębatego, na samym dole paska)

2. Kliknij **„Access"** w lewym podmenu

3. Kliknij przycisk **„Add people"** (prawy górny róg)

4. W polu wyszukiwania wpisz adres e-mail zapraszanej osoby

5. Rola: **„Member"** *(Member może tworzyć i edytować zadania; Viewer — tylko czyta)*

6. Kliknij **„Send invite"**

7. Powtórz dla kolejnych osób

**Co widzi zaproszony uczestnik:**

1. Otrzymuje e-mail od `no-reply@atlassian.com` z tytułem *„[imię] invited you to…"*

2. Klika **„Join project"** w e-mailu

3. Jeśli nie ma konta Atlassian → przechodzi przez rejestrację (kroki 1–7 powyżej)  
   Jeśli ma konto → loguje się i widzi projekt

4. Po zalogowaniu projekt Scrum Mastera jest widoczny na liście projektów

> ⚠️ **Częste problemy:**
> - E-mail z zaproszeniem w folderze SPAM — sprawdź!
> - Uczestnik musi kliknąć link z właściwego konta e-mail, z którego był zapraszany
> - Jeśli link wygasł (24h) — Scrum Master wysyła zaproszenie ponownie (Project settings → Access → Pending invites → Resend)

---

## 2. Dodanie Epic / Story / Sub-task

### 2.1 Tworzenie Epica

Epic to duży obszar funkcjonalności grupujący wiele Stories (PBI).

**Metoda A — przez Roadmap (Timeline):**

1. W lewym menu kliknij **„Roadmap"** (lub **„Timeline"**)

2. W polu tekstowym na górze wpisz nazwę Epica

3. Naciśnij **Enter** — Epic pojawia się jako pozioma belka na osi czasu

4. Kliknij belkę Epica → **„Open epic"** → uzupełnij opis i daty

**Metoda B — przez przycisk Create:**

1. Kliknij **„+ Create"** w górnym menu (niebieskie „+" lub przycisk)

2. W polu **„Issue type"** wybierz **„Epic"**

3. Wypełnij:
   - **Summary** (tytuł): *(np. „Część I – Wprowadzenie i postacie")*
   - **Description**: szczegóły zakresu Epica
   - **Epic Color**: opcjonalnie wybierz kolor dla czytelności

4. Kliknij **„Create"**

---

### 2.2 Tworzenie Story (PBI)

Story = Product Backlog Item — główna jednostka pracy szacowana w Story Points.

1. W lewym menu kliknij **„Backlog"**

2. W sekcji **„Backlog"** kliknij **„+ Create issue"** (na dole sekcji)  
   *(lub kliknij **„+ Create"** w górnym menu i wybierz typ **„Story"**)*

3. Wpisz tytuł Story → potwierdź **Enter**

4. Kliknij tytuł Story, by otworzyć jej szczegóły — uzupełnij:

   | Pole | Wartość | Uwagi |
   |---|---|---|
   | **Summary** | Tytuł PBI | Zwięzły, np. „Opis miejsca zbrodni" |
   | **Description** | Treść wymagania | Kryteria akceptacji, format: „Jako [rola] chcę [cel] aby [korzyść]" |
   | **Epic Link** | Przypisanie do Epica | Prawy panel → pole „Epic Link" → wybierz z listy |
   | **Story Points** | Liczba (1, 2, 3, 5, 8…) | Prawy panel → pole „Story point estimate" |
   | **Assignee** | Osoba odpowiedzialna | Prawy panel → „Assignee" → wybierz z listy |
   | **Priority** | Medium / High / Low | Prawy panel → „Priority" |

5. Kliknij **„Save"** lub po prostu zamknij — zmiany zapisują się automatycznie

> ✅ Story widoczna w sekcji **„Backlog"** z numerem (np. `BIM-1`)

---

### 2.3 Tworzenie Sub-task

Sub-task = konkretne działanie techniczne w ramach Story.

1. Otwórz Story (kliknij jej tytuł w Backlogu)

2. Przewiń w dół do sekcji **„Child issues"**

3. Kliknij **„+ Create child issue"**

4. Wpisz tytuł Sub-task → **Enter**

5. Kliknij Sub-task, by uzupełnić:
   - **Assignee**: kto wykonuje to konkretne działanie
   - **Description**: co dokładnie trzeba zrobić
   - *(Sub-taski nie mają Story Points — szacuje się Story na poziomie wyżej)*

> **Przykład rozbicia Story na Sub-taski:**
> 
> Story: *„Opis miejsca zbrodni"*
> - Sub-task 1: Napisanie pierwszego szkicu opisu (200 słów)
> - Sub-task 2: Review i korekta językowa
> - Sub-task 3: Dodanie do dokumentu Confluence/Pages

---

## 3. Utworzenie i estymacja Sprintu

### 3.1 Tworzenie Sprintu

1. W lewym menu kliknij **„Backlog"**

2. Kliknij przycisk **„Create sprint"** (u góry widoku Backlog)  
   *(Jeśli przycisk nie jest widoczny — upewnij się, że projekt jest **Scrum**, nie Kanban)*

3. Pojawia się sekcja **„Sprint 1"** ponad sekcją „Backlog"

4. Kliknij **„···"** (trzy kropki / More) przy nagłówku Sprint 1 → **„Edit sprint"**:

   | Pole | Wartość |
   |---|---|
   | **Sprint name** | `Sprint 1` *(lub np. „Sprint 1 – Rozdział 1")* |
   | **Start date** | Data rozpoczęcia *(np. dzisiaj)* |
   | **End date** | Data zakończenia *(np. dzisiaj + 45 min na zajęcia)* |
   | **Sprint goal** | Krótki cel, np. *„Napisać i zreviewować Rozdział 1"* |

5. Kliknij **„Update"**

---

### 3.2 Przenoszenie Stories do Sprintu (Sprint Backlog)

1. W widoku Backlog przeciągnij Story z sekcji **„Backlog"** do sekcji **„Sprint 1"**  
   *(lub: kliknij prawym przyciskiem na Story → **„Move to Sprint"** → wybierz Sprint 1)*

2. Powtórz dla wszystkich Stories zaplanowanych na ten sprint

> ✅ Sekcja Sprint 1 zawiera wybrane Stories — to jest Sprint Backlog

---

### 3.3 Estymacja Story Points (Planning Poker)

**Każda Story musi mieć oszacowanie przed wystartowaniem Sprintu.**

1. Kliknij tytuł Story w Backlogu

2. W prawym panelu znajdź pole **„Story point estimate"**  
   *(W starszych wersjach Jiry: „Story Points")*

3. Kliknij pole i wpisz liczbę wg skali Fibonacci: **1, 2, 3, 5, 8, 13**

   | Punkty | Oznaczenie |
   |---|---|
   | 1 | Bardzo proste, <30 min pracy |
   | 2 | Proste, ok. 1h pracy |
   | 3 | Średnie, kilka godzin |
   | 5 | Złożone, pół dnia |
   | 8 | Duże, cały dzień |
   | 13 | Zbyt duże — rozbuduj na mniejsze Stories! |

4. Naciśnij **Enter** — liczba pojawia się jako badge przy tytule Story

> **Planning Poker na zajęciach:**  
> Każdy członek zespołu pokazuje swoją kartę jednocześnie. Jeśli różnice są duże (np. 2 vs 8) — osoba z najniższą i najwyższą oceną tłumaczy swój wybór. Głosujcie ponownie do osiągnięcia konsensusu. **Scrum Master wpisuje uzgodnioną liczbę do Jiry.**

---

## 4. Wystartowanie Sprintu

### 4.1 Start Sprintu

> ⚠️ Sprint można wystartować tylko jeśli w sekcji Sprint są co najmniej **1 issue** i mają ustawione Story Points.

1. W widoku **„Backlog"** upewnij się, że:
   - Sprint ma nazwę i daty
   - Co najmniej jedna Story jest przeniesiona do sekcji Sprint
   - Stories mają Story Points

2. Kliknij przycisk **„Start sprint"** (niebieski, widoczny w nagłówku sekcji Sprint)

3. Pojawi się potwierdzenie z datami i liczbą sprintów — kliknij **„Start"**

4. Jira automatycznie przełącza widok do tablicy **„Board"**  
   *(lub możesz kliknąć „Board" w lewym menu)*

### 4.2 Widok tablicy (Board)

Po wystartowaniu sprintu tablica pokazuje kolumny:

| Kolumna | Znaczenie |
|---|---|
| **To Do** | Stories/Sub-taski jeszcze nierozpoczęte |
| **In Progress** | Zadania aktualnie wykonywane |
| **Done** | Ukończone zadania |

> ℹ️ Liczba kolumn i ich nazwy można dostosować: **Project settings → Board → Columns**

---

## 5. Raportowanie wykonania zadań podczas Sprintu

### 5.1 Przenoszenie zadań między statusami (Daily Scrum)

Podczas pracy każdy członek zespołu aktualizuje swoje zadania:

**Opcja A — Tablica (Board):**

1. W lewym menu kliknij **„Board"**

2. Znajdź swoją Story lub Sub-task w kolumnie **„To Do"**

3. Przeciągnij ją do kolumny **„In Progress"** gdy zaczynasz pracę

4. Przeciągnij do **„Done"** gdy skończysz i spełnione są kryteria DoD

**Opcja B — Bezpośrednio w Issue:**

1. Otwórz Story lub Sub-task (kliknij tytuł)

2. Kliknij przycisk ze statusem u góry *(np. „To Do")*

3. Wybierz nowy status z listy: **„In Progress"** lub **„Done"**

> ✅ Każda zmiana statusu jest rejestrowana w historii Issue (sekcja „Activity" na dole)

---

### 5.2 Logowanie czasu (opcjonalnie)

Jira Free nie ma zaawansowanego time-trackingu, ale można rejestrować czas:

1. Otwórz Issue

2. Kliknij **„Log work"** (sekcja „Time tracking" w prawym panelu)

3. Wpisz czas: `1h 30m` lub `90m`

4. Kliknij **„Save"**

---

### 5.3 Burndown Chart — śledzenie postępu Sprintu

Burndown Chart pokazuje czy sprint idzie zgodnie z planem.

1. W lewym menu kliknij **„Reports"**

2. Wybierz **„Burndown Chart"**

3. Wykres pokazuje:
   - **Oś Y** — pozostałe Story Points
   - **Oś X** — czas (dni sprintu)
   - **Linia szara** — idealny postęp (równomierne kończenie)
   - **Linia niebieska/czerwona** — rzeczywisty postęp

   | Sytuacja | Interpretacja |
   |---|---|
   | Linia realna **powyżej** idealnej | Sprint za wolno — ryzyko niedowiezienia |
   | Linia realna **poniżej** idealnej | Sprint szybko — można wziąć dodatkowe Stories |
   | Linia realna **skacze w górę** | Dodano nowe Stories w trakcie sprintu |

---

### 5.4 Zamknięcie Sprintu

Po zakończeniu sprintu (Sprint Review + Retrospektywa):

1. W lewym menu kliknij **„Backlog"** lub **„Board"**

2. Kliknij **„Complete sprint"** (przycisk widoczny na tablicy lub w Backlogu)

3. Jira pyta co zrobić z niezakończonymi Issues:
   - **„Move to [nowy sprint]"** — przenosi do kolejnego sprintu
   - **„Move to Backlog"** — wraca do Backlogu (nie wchodzą do następnego sprintu automatycznie)

4. Kliknij **„Complete"**

5. Jira generuje **Sprint Report** — podsumowanie:
   - Ukończone Stories i ich SP
   - Niedokończone Stories
   - Velocity (suma SP ukończonych)

> ✅ Sprint Report jest widoczny w **Reports → Sprint Report** — wybierz sprint z listy rozwijanej

---

## Skróty i wskazówki

| Akcja | Skrót / Wskazówka |
|---|---|
| Szybkie tworzenie Issue | Naciśnij **`C`** będąc na dowolnej stronie projektu |
| Wyszukiwanie Issues | Naciśnij **`/`** → wyszukiwarka Issues |
| Filtrowanie tablicy | Board → „Group by Assignee" — widać kto co robi |
| Kopiowanie linku do Issue | Otwórz Issue → skopiuj URL (np. `bim-kryminal.atlassian.net/browse/BIM-5`) |
| Obserwowanie Issue | Otwórz Issue → **„Watch"** → dostaniesz e-mail przy każdej zmianie |
| Status Jiry | https://status.atlassian.com — sprawdź czy Jira działa |
