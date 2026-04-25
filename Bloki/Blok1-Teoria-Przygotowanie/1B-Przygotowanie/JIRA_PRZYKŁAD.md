# JIRA – Pełny przykład: powieść kryminalna „Śmierć przychodzi o świcie"

> Dokument pokazuje **kompletny przepływ pracy** w Scrum od zera:  
> tworzenie projektu w Jira → backlog → Sprint 1 → realizacja zadań.  
> Każdy krok jest ilustrowany konkretnymi danymi z przykładowego projektu.

---

## Dane projektu

| Element | Wartość |
|---|---|
| **Gatunek** | Kryminał |
| **Tytuł** | *Śmierć przychodzi o świcie* |
| **Główny bohater** | Komisarz Anna Wolska, 42 lata, detektyw z Krakowa |
| **Antagonista** | Nieznany sprawca ukryty wśród mieszkańców Czernej |
| **Miejsce akcji** | Górskie miasteczko Czerna w Beskidach, jesień |
| **Fabuła (1 zdanie)** | Komisarz Wolska przyjeżdża na urlop i nieoczekiwanie odkrywa ciało burmistrza — musi rozwiązać zagadkę, zanim sprawca ucieknie |

### Skład zespołu

| Rola | Imię | Specjalizacja w projekcie |
|---|---|---|
| Product Owner | Karolina | Wizja powieści, kryteria akceptacji |
| Scrum Master | Marek | Konfiguracja Jiry, prowadzenie ceremonii |
| Developer | Zofia | Pisanie scen i dialogów |
| Developer | Piotr | Research realiów (policja, Beskidy, prawo) |
| Developer | Natalia | Redakcja językowa i korekta |

---

## Część 1 – Tworzenie projektu w Jira

### Krok 1.1 – Rejestracja i konfiguracja (Scrum Master: Marek)

1. Wejdź na **https://www.atlassian.com/software/jira/free** → kliknij **„Get it free"**
2. Zarejestruj się e-mailem `marek@example.com` → potwierdź 6-cyfrowym kodem
3. **Site name**: wpisz `bim-kryminal`  
   → Twoja Jira będzie dostępna pod: `bim-kryminal.atlassian.net`
4. *„What kind of work?"* → wybierz **„Software development"** → **„Next"**
5. Szablon projektu → kliknij **„Scrum"** → **„Select"**
6. Typ projektu → **„Team-managed project"**
7. **Project name**: `Śmierć przychodzi o świcie`
8. Kliknij **„Create project"**

> ✅ Widoczny pusty Backlog — projekt gotowy.  
> Klucz projektu (automatyczny, np. `SPC`) będzie prefiksem każdego issue: `SPC-1`, `SPC-2` itd.

---

### Krok 1.2 – Zaproszenie zespołu (Scrum Master: Marek)

1. Lewe menu → **„Project settings"** (ikona koła zębatego, dół paska)
2. **„Access"** → **„Add people"**
3. Wpisz e-mail każdego członka zespołu i kliknij **„Send invite"**:

| Uczestnik | E-mail do wpisania | Rola w Jira |
|---|---|---|
| Karolina (PO) | karolina@example.com | Member |
| Zofia (Dev) | zofia@example.com | Member |
| Piotr (Dev) | piotr@example.com | Member |
| Natalia (Dev) | natalia@example.com | Member |

4. Każdy uczestnik kliknie **„Join project"** w e-mailu z zaproszenia

> ⚠️ Jeśli e-mail nie dotarł → sprawdź SPAM lub wyślij ponownie:  
> Project settings → Access → Pending invites → **Resend**

---

## Część 2 – Struktura backlogu: Epiki, Story, Sub-taski

### Epiki (Epics)

Epiki dzielą powieść na duże obszary fabularne. Nasz projekt ma 4 epiki:

| ID Epika | Nazwa | Zakres |
|---|---|---|
| **EPIC-1** | Część I – Prolog i wprowadzenie | Rozdziały 1–2 |
| **EPIC-2** | Część II – Śledztwo | Rozdziały 3–7 |
| **EPIC-3** | Część III – Przełom i finał | Rozdziały 8–10 |
| **EPIC-4** | Redakcja i spójność | Całość — review, korekta |

---

### Jak wpisać Epiki do Jiry

**Metoda: Timeline (Roadmap)**

1. Lewe menu → kliknij **„Roadmap"** (lub **„Timeline"**)
2. W polu tekstowym u góry wpisz nazwę pierwszego Epika:  
   `Część I – Prolog i wprowadzenie`
3. Naciśnij **Enter** → Jira tworzy belkę Epika
4. Kliknij belkę → **„Open epic"** → uzupełnij opis:

```
Opis Epika EPIC-1:
Wprowadzenie w świat powieści. Odkrycie ciała burmistrza Czernej
przez komisarz Wolską. Przedstawienie głównych postaci i atmosfery
górskiego miasteczka.
```

5. Wybierz kolor Epika (np. czerwony dla napięcia) → zapisz
6. Powtórz dla pozostałych 3 epików (różne kolory dla czytelności)

> ✅ Na osi czasu widoczne 4 belki — możesz ustawić im orientacyjne daty

---

### Story (Product Backlog Items)

Każde Story = jeden rozdział lub kluczowa scena. Poniżej pełna lista wszystkich 14 Stories:

#### EPIC-1: Część I – Prolog i wprowadzenie

| ID | Tytuł Story | Opis / User Story | SP |
|---|---|---|---|
| SPC-1 | Prolog – odkrycie ciała | Jako czytelnik chcę przeczytać scenę odkrycia ciała, aby od pierwszej strony poczuć napięcie. **Akceptacja:** min. 400 słów, obecna Komisarz Wolska, znaleziono ciało burmistrza. | 5 |
| SPC-2 | Przedstawienie komisarz Wolskiej | Jako czytelnik chcę poznać główną bohaterkę, aby rozumieć jej motywacje. **Akceptacja:** wiek, wygląd, trauma z przeszłości, powód przyjazdu do Czernej. | 3 |
| SPC-3 | Opis miasteczka Czerna | Jako czytelnik chcę poczuć atmosferę miejsca akcji, aby zanurzyć się w świat powieści. **Akceptacja:** opis jesiennej scenerii, architektura, mieszkańcy jako tło. | 3 |

#### EPIC-2: Część II – Śledztwo

| ID | Tytuł Story | Opis / User Story | SP |
|---|---|---|---|
| SPC-4 | Pierwsza wizja lokalna | Jako czytelnik chcę zobaczyć Wolską na miejscu zbrodni, aby śledzić jej tok myślenia. **Akceptacja:** opis miejsca zbrodni, pierwsze poszlaki, rozmowa z lokalnym policjantem. | 5 |
| SPC-5 | Przesłuchanie świadków – runda I | Jako czytelnik chcę poznać zeznania 3 świadków, aby samodzielnie próbować rozwiązać zagadkę. **Akceptacja:** rozmowy z sekretarką, sąsiadką i barmanem. | 5 |
| SPC-6 | Fałszywy trop – podejrzany nr 1 | Jako czytelnik chcę wierzyć, że znalazłem sprawcę, aby zwrot akcji był zaskakujący. **Akceptacja:** dowody wskazujące na sekretarza Brzeskiego, jego alibi obalone i przywrócone. | 8 |
| SPC-7 | Odkrycie kluczowej poszlaki | Jako czytelnik chcę zobaczyć przełomowy moment śledztwa, aby fabuła nabrała tempa. **Akceptacja:** zaginiony zegarek burmistrza, analiza DNA lub odcisków palców. | 5 |
| SPC-8 | Przesłuchanie świadków – runda II | Jako czytelnik chcę zobaczyć, jak Wolska konfrontuje świadków z nowymi faktami, aby widzieć jej metodykę. **Akceptacja:** powrót do sekretarki i sąsiadki z nowymi pytaniami. | 3 |

#### EPIC-3: Część III – Przełom i finał

| ID | Tytuł Story | Opis / User Story | SP |
|---|---|---|---|
| SPC-9 | Zwrot akcji – prawdziwy sprawca | Jako czytelnik chcę być zaskoczony tożsamością sprawcy, aby powieść była satysfakcjonująca. **Akceptacja:** logiczne uzasadnienie, motyw ekonomiczny lub osobisty. | 8 |
| SPC-10 | Finałowe starcie | Jako czytelnik chcę przeżyć kulminację fabuły, aby odczuć katharsis. **Akceptacja:** konfrontacja Wolskiej ze sprawcą, element zagrożenia życia, rozwiązanie. | 8 |
| SPC-11 | Epilog i zamknięcie wątków | Jako czytelnik chcę wiedzieć, co stało się z postaciami, aby opuścić świat powieści z satysfakcją. **Akceptacja:** los sprawcy, Wolska wraca do Krakowa, otwarte zakończenie dla ewentualnego sequela. | 5 |

#### EPIC-4: Redakcja i spójność

| ID | Tytuł Story | Opis / User Story | SP |
|---|---|---|---|
| SPC-12 | Korekta spójności fabularnej | Jako Product Owner chcę mieć pewność, że fabuła nie ma sprzeczności, aby powieść była wiarygodna. **Akceptacja:** oś czasu wydarzeń bez luk, imiona postaci spójne w całości. | 5 |
| SPC-13 | Redakcja językowa całości | Jako czytelnik chcę czytać tekst wolny od błędów stylistycznych, aby lektura była przyjemna. **Akceptacja:** przejrzane wszystkie rozdziały, max. 2 błędy na stronę. | 8 |
| SPC-14 | Finalna wersja dokumentu | Jako PO chcę otrzymać gotowy plik do oddania, aby projekt mógł być zamknięty. **Akceptacja:** plik PDF/DOCX, spis treści, formatowanie nagłówków. | 2 |

---

### Jak wpisać Stories do Jiry

**Każdą Story wpisuje Person Odpowiedzialna (PO lub Dev), Scrum Master pilnuje kompletności**

**Dla każdej Story z powyższej tabeli:**

1. Lewe menu → **„Backlog"**
2. Kliknij **„+ Create issue"** na dole sekcji Backlog
3. Wpisz tytuł Story (np. `Prolog – odkrycie ciała`) → **Enter**
4. Kliknij tytuł Story — otwiera się panel szczegółów
5. Wypełnij pola zgodnie z tabelą:

| Pole w Jira | Co wpisać (przykład dla SPC-1) |
|---|---|
| **Summary** | `Prolog – odkrycie ciała` |
| **Description** | `Jako czytelnik chcę przeczytać scenę odkrycia ciała, aby od pierwszej strony poczuć napięcie. **Kryteria akceptacji:** min. 400 słów, obecna Komisarz Wolska, znaleziono ciało burmistrza.` |
| **Issue type** | Story |
| **Epic Link** | Wybierz `Część I – Prolog i wprowadzenie` |
| **Story point estimate** | `5` |
| **Priority** | High |
| **Assignee** | *(zostaw puste — przypisanie nastąpi na Sprint Planning)* |

6. Kliknij gdzie indziej — Jira zapisuje automatycznie
7. Powtórz dla wszystkich 14 Stories

> ✅ **Sprawdzenie po tym kroku:**  
> Backlog powinien zawierać 14 Stories z widocznymi numerami SPC-1 do SPC-14.  
> Każda Story ma badge z liczbą Story Points widoczny obok tytułu.

---

### Sub-taski (zadania wykonawcze)

Sub-taski rozbijają Story na konkretne czynności. Poniżej przykład dla **SPC-1** (Prolog):

**Story: `SPC-1 – Prolog – odkrycie ciała` (5 SP)**

| Sub-task | Opis | Szacowany czas |
|---|---|---|
| SPC-1a | Research: jak policja zabezpiecza miejsce zbrodni w Polsce | 30 min |
| SPC-1b | Napisanie pierwszego szkicu prologu (400+ słów) | 60 min |
| SPC-1c | Review szkicu przez PO i zespół | 20 min |
| SPC-1d | Poprawki po review | 20 min |
| SPC-1e | Finalna korekta językowa prologu | 15 min |

**Story: `SPC-2 – Przedstawienie komisarz Wolskiej` (3 SP)**

| Sub-task | Opis | Szacowany czas |
|---|---|---|
| SPC-2a | Opracowanie profilu psychologicznego bohaterki (bullet points) | 20 min |
| SPC-2b | Napisanie sceny charakteryzującej Wolską | 40 min |
| SPC-2c | Review i korekta | 15 min |

**Story: `SPC-3 – Opis miasteczka Czerna` (3 SP)**

| Sub-task | Opis | Szacowany czas |
|---|---|---|
| SPC-3a | Research: realia małego górskiego miasteczka w Polsce | 25 min |
| SPC-3b | Napisanie opisu miejsca (300+ słów) | 40 min |
| SPC-3c | Review i korekta | 15 min |

---

### Jak wpisać Sub-taski do Jiry

1. W Backlogu kliknij tytuł Story (np. `SPC-1 – Prolog – odkrycie ciała`)
2. W oknie szczegółów Story przewiń w dół do sekcji **„Child issues"**
3. Kliknij **„+ Create child issue"**
4. W polu typu upewnij się, że wybrany jest **„Subtask"**
5. Wpisz tytuł sub-taska (np. `Research: jak policja zabezpiecza miejsce zbrodni`) → **Enter**
6. Kliknij sub-task → uzupełnij:
   - **Description**: co dokładnie trzeba zrobić, źródła do sprawdzenia
   - **Assignee**: osoba wykonująca (przypisz już teraz lub podczas Sprint Planning)
7. Powtórz dla każdego sub-taska z powyższej tabeli

> ℹ️ Sub-taski dziedziczą przynależność do Sprintu od swojej Story-rodzica.  
> Sub-taski **nie mają** Story Points — szacujemy zawsze na poziomie Story.

---

## Część 3 – Organizacja Sprintu 1

### Sprint Goal (Cel Sprintu 1)

> **„Dostarczyć gotową Część I powieści: prolog, wprowadzenie bohaterki  
> i opis miasteczka — zaakceptowane przez PO i zredagowane przez Natalię."**

Sprint 1 obejmuje Stories: **SPC-1, SPC-2, SPC-3** (łącznie **11 Story Points**)

---

### Krok 3.1 – Tworzenie Sprintu w Jira

1. Lewe menu → **„Backlog"**
2. Kliknij **„Create sprint"** (u góry sekcji Backlog)  
   → Pojawia się sekcja „Sprint 1" powyżej listy Backlog
3. Kliknij **„···"** przy nagłówku Sprint 1 → **„Edit sprint"**
4. Uzupełnij dane:

| Pole | Wartość dla Sprint 1 |
|---|---|
| **Sprint name** | `Sprint 1 – Część I Prologu` |
| **Start date** | *(dzisiejsza data, np. 25 kwi 2026)* |
| **End date** | *(data + 2 tygodnie, np. 9 maj 2026)* |
| **Sprint goal** | `Dostarczyć gotową Część I: prolog, bohaterka, miasteczko` |

5. Kliknij **„Update"**

---

### Krok 3.2 – Sprint Backlog: przeniesienie Stories

**Kto wykonuje: Scrum Master (Marek), podczas Sprint Planning**

1. W widoku Backlog przeciągnij Story **SPC-1** z sekcji „Backlog" do sekcji „Sprint 1"
2. Powtórz dla **SPC-2** i **SPC-3**
3. Alternatywnie: kliknij prawym przyciskiem na Story → **„Move to Sprint"** → wybierz `Sprint 1 – Część I Prologu`

> ✅ Sprint Backlog powinien teraz wyglądać tak:

```
Sprint 1 – Część I Prologu  [Start sprint]
 ├── SPC-1  Prolog – odkrycie ciała                  [5 SP]
 ├── SPC-2  Przedstawienie komisarz Wolskiej          [3 SP]
 └── SPC-3  Opis miasteczka Czerna                   [3 SP]
                                            RAZEM: 11 SP

Backlog
 ├── SPC-4  Pierwsza wizja lokalna                   [5 SP]
 ├── SPC-5  Przesłuchanie świadków – runda I         [5 SP]
 ... (pozostałe 9 Stories)
```

---

### Krok 3.3 – Estymacja Story Points (Planning Poker)

**Kto: cały zespół (Karolina, Marek, Zofia, Piotr, Natalia)**  
**Forma: każdy głosuje jednocześnie, Marek wpisuje wynik do Jiry**

Skala Fibonacci używana w projekcie:

| Punkty | Interpretacja dla pisania powieści |
|---|---|
| 1 | Krótka scena, < 200 słów, bez research |
| 2 | Prosta scena, 200–300 słów, minimalne research |
| 3 | Scena ze strukturą, 300–500 słów lub 2h pracy |
| 5 | Złożona scena, wiele wątków, research wymagany |
| 8 | Trudna scena, kluczowa dla fabuły, wiele przeróbek |
| 13 | Za duże — podziel Story na dwie mniejsze! |

**Przebieg głosowania dla SPC-1 (Prolog):**

```
Marek (SM): "Czytam Story SPC-1: Prolog – odkrycie ciała. 
             Kryteria: min. 400 słów, scena Wolskiej, ciało burmistrza.
             Wszyscy gotowi? Trzy, dwa, jeden — karty!"

Zofia  → pokazuje: 5
Piotr  → pokazuje: 8
Natalia → pokazuje: 5
Karolina → pokazuje: 5

Marek: "Piotr, dlaczego 8?"
Piotr: "Research policyjny zajmie dużo czasu — chcę to dobrze zrobić."
Zofia: "Mogę przejąć research — mam już notatki. To obniży złożoność."
Marek: "Głosujemy ponownie..."

Zofia  → 5 | Piotr → 5 | Natalia → 5 | Karolina → 5

Marek wpisuje do Jiry: Story point estimate = 5 ✅
```

**Wyniki estymacji Sprint 1:**

| Story | Głosy | Ustalona wartość | Uwagi |
|---|---|---|---|
| SPC-1 Prolog | 5,8,5,5 → ponowne: 5,5,5,5 | **5 SP** | Piotr przekazuje research Zofii |
| SPC-2 Bohaterka | 3,3,2,3 | **3 SP** | Consensus od razu |
| SPC-3 Miasteczko | 3,5,3,3 → ponowne: 3,3,3,3 | **3 SP** | Piotr wyjaśnia, że research jest krótki |
| **SUMA** | | **11 SP** | Velocity dla Sprint 1 |

---

### Krok 3.4 – Przypisanie zadań do członków zespołu

**Kto wykonuje: PO (Karolina) i SM (Marek) razem z zespołem**

**Zasada przypisania:** na poziomie Sub-tasków (nie Story), aby każdy wiedział, co konkretnie robi.

#### Przydział dla Sprint 1:

| Sub-task | Assignee | Uzasadnienie |
|---|---|---|
| SPC-1a: Research policyjny | **Piotr** | Specjalizacja: research realiów |
| SPC-1b: Szkic prologu | **Zofia** | Specjalizacja: pisanie narracyjne |
| SPC-1c: Review prologu | **Karolina** | PO ocenia zgodność z wizją |
| SPC-1d: Poprawki prologu | **Zofia** | Autorka poprawia po review |
| SPC-1e: Korekta językowa prologu | **Natalia** | Specjalizacja: redakcja |
| SPC-2a: Profil psychologiczny bohaterki | **Karolina** | PO zna wizję postaci |
| SPC-2b: Scena charakteryzująca Wolską | **Zofia** | Pisanie |
| SPC-2c: Review i korekta | **Natalia** | Redakcja |
| SPC-3a: Research miasteczko | **Piotr** | Research |
| SPC-3b: Opis miasteczka | **Zofia** | Pisanie |
| SPC-3c: Review i korekta | **Natalia** | Redakcja |

#### Jak przypisać w Jira:

1. W Backlogu kliknij tytuł Story (np. `SPC-1`)
2. Przewiń do sekcji **„Child issues"**
3. Kliknij sub-task (np. `SPC-1a: Research policyjny`)
4. W prawym panelu kliknij pole **„Assignee"** → wybierz `Piotr` z listy
5. Powtórz dla każdego sub-taska

> ✅ Na tablicy Board każdy dev widzi tylko swoje zadania filtrując widok:  
> Board → kliknij awatar osoby w górnym pasku → widok filtrowany

---

### Krok 3.5 – Start Sprintu

1. Lewe menu → **„Backlog"**
2. Upewnij się, że w Sprint 1 są 3 Stories z SP i przypisanymi Assignee
3. Kliknij **„Start sprint"** (niebieski przycisk w nagłówku Sprint 1)
4. Pojawi się okno potwierdzenia z datami — kliknij **„Start"**
5. Jira automatycznie otwiera tablicę **„Board"**

> ✅ Na tablicy widoczne 3 Stories + 11 Sub-tasków w kolumnie **„To Do"**

---

## Część 4 – Realizacja zadań przez zespół

### Dzień 1 – Kick-off (pierwsze 30 min)

**Daily Scrum #1** (choć to dzień 1 — traktuj go jako sesję startową):

| Pytanie | Zofia | Piotr | Natalia |
|---|---|---|---|
| Co zrobiłam wczoraj? | *(sprint startuje)* | *(sprint startuje)* | *(sprint startuje)* |
| Co zrobię dziś? | Szkic prologu (SPC-1b) | Research policyjny (SPC-1a) + research miasteczko (SPC-3a) | Przeglądam wytyczne stylistyczne |
| Czy mam blokery? | Potrzebuję wyników researchu od Piotra | Nie | Nie |

**Akcja Marka (SM):** Odnotowuje bloker Zofii → ustala z Piotrem, że research (SPC-1a) ma priorytet.

---

### Jak aktualizować zadania w Jira (codziennie)

**Opcja A – Tablica (Board) — przeciąganie:**

1. Lewe menu → **„Board"**
2. Piotr zaczyna `SPC-1a: Research policyjny` → przeciąga kartę z **„To Do"** do **„In Progress"**
3. Po skończeniu → przeciąga do **„Done"**

**Opcja B – Bezpośrednio w Issue:**

1. Kliknij tytuł Sub-taska (np. `SPC-1a`)
2. Kliknij status **„To Do"** u góry ekranu
3. Wybierz **„In Progress"** z menu → zapisuje się automatycznie

> ✅ Każda zmiana statusu pojawia się w historii Issue (sekcja „Activity") z datą i godziną.

---

### Przykładowy przepływ dnia 2–3

**Piotr kończy SPC-1a (Research policyjny):**

1. Otwiera SPC-1a w Jira
2. Zmienia status na **„Done"**
3. Dodaje komentarz w polu „Activity":
   ```
   Research gotowy. Kluczowe fakty:
   - Zabezpieczenie miejsca zbrodni: taśma policyjna + protokół
   - Czas dotarcia policji w terenie górskim: 25-40 min
   - Podstawa prawna przeszukania: art. 219 KPK
   Materiały w Google Docs: [link]
   ```
4. Zofia dostaje powiadomienie → może zacząć SPC-1b (szkic prologu)

**Zofia pisze SPC-1b (Szkic prologu):**

1. Otwiera SPC-1b → zmienia status na **„In Progress"**
2. Po skończeniu (60 min): zmienia status na **„Done"**, dodaje link do szkicu w komentarzu
3. `SPC-1` (Story-rodzic) automatycznie pokazuje postęp: 2/5 sub-tasków Done

---

### Śledzenie postępu – Burndown Chart

Po 3–4 dniach Sprintu Marek (SM) sprawdza postęp:

1. Lewe menu → **„Reports"** → **„Burndown Chart"**
2. Oś X = dni Sprintu | Oś Y = pozostałe Story Points
3. Idealna linia (szara przerywana) vs linia rzeczywista (niebieska)

**Interpretacja dla Sprint 1:**

```
Dzień 1:  11 SP (nic nie Done — normalnie)
Dzień 3:   8 SP (SPC-3 ukończona — 3 SP odpadają)
Dzień 5:   5 SP (SPC-2 ukończona — 3 SP odpadają)
Dzień 10:  0 SP (SPC-1 ukończona — 5 SP odpadają) ← ideał
```

> ⚠️ **Jeśli linia rzeczywista jest powyżej idealnej** po 5 dniach:  
> SM organizuje dodatkowe spotkanie → identyfikacja blokerów → ewentualne usunięcie Story ze Sprintu

---

### Definition of Done (DoD) dla projektu

Story jest **„Done"** gdy spełnione są WSZYSTKIE warunki:

- [ ] Tekst ma minimalną liczbę słów określoną w Kryteriach Akceptacji
- [ ] Wszystkie sub-taski mają status „Done" w Jira
- [ ] PO (Karolina) zaakceptowała Story podczas review
- [ ] Natalia wykonała korektę językową
- [ ] Tekst jest wklejony do wspólnego dokumentu (Google Docs / Confluence Pages)
- [ ] Brak otwartych komentarzy „do poprawy" od zespołu

---

### Sprint Review (ostatni dzień Sprintu 1)

**Kto prowadzi: PO (Karolina)**  
**Uczestnicy: cały zespół**

1. Lewe menu → **„Board"** → sprawdź, że wszystkie 3 Stories są w kolumnie **„Done"**
2. Karolina czyta po kolei każdą Story i ocenia spełnienie Kryteriów Akceptacji:

| Story | Kryterium | Spełnione? |
|---|---|---|
| SPC-1 | Min. 400 słów | ✅ (napisano 520 słów) |
| SPC-1 | Obecna Komisarz Wolska | ✅ |
| SPC-1 | Znaleziono ciało burmistrza | ✅ |
| SPC-2 | Wiek, wygląd, trauma | ✅ |
| SPC-3 | Opis jesiennej scenerii | ✅ |

3. Karolina klika Story → zmienia status na **„Done"** (jeśli jeszcze nie zmieniony)
4. Zespół decyduje, czy SPC-1–3 mogą wejść do **Increment** (gotowej wersji Części I)

**Wynik Sprint Review:**

> *„Sprint 1 zakończony sukcesem. Dostarczono 11 SP = Część I powieści  
> (prolog, bohaterka, miasteczko) zaakceptowana przez PO.  
> Velocity Sprint 1 = 11 SP — podstawa do planowania Sprint 2."*

---

### Sprint Retrospektywa (po Review)

**Kto prowadzi: SM (Marek)**  
**Czas: 15 minut**  
**Format: Start / Stop / Continue**

| Kategoria | Co powiedzieli |
|---|---|
| **Start** | „Zacząć dzielić research i pisanie równolegle, nie sekwencyjnie" |
| **Stop** | „Przestać czekać na review PO dłużej niż 24h — ustalamy timebox 4h" |
| **Continue** | „Kontynuować wstawianie komentarzy z linkami do materiałów w Jira" |

**Marek tworzy action items w Jira:**

1. Kliknij **„+ Create"** → Issue type: **Task** (nie Story)
2. Tytuł: `RETRO: Ustalić równoległy harmonogram research+pisanie`
3. Assignee: Marek (SM) | Sprint: Sprint 2

---

### Sprint 2 – Planowanie (podgląd)

Po zamknięciu Sprint 1:

1. Lewe menu → **„Backlog"** → kliknij **„Create sprint"** → Sprint 2
2. Cel: `„Dostarczyć Rozdziały 3–4: wizja lokalna + pierwsze przesłuchania"`
3. Do Sprint 2 przesuwamy: **SPC-4** (5 SP) + **SPC-5** (5 SP) = 10 SP
4. Velocity Sprint 1 = 11 SP → Sprint 2 planujemy na ~10–11 SP (bezpieczna pojemność)

---

## Podsumowanie – Mapa całego projektu

```
PROJEKT: Śmierć przychodzi o świcie
│
├── EPIC-1: Część I – Prolog i wprowadzenie
│   ├── SPC-1: Prolog – odkrycie ciała              [5 SP] ← Sprint 1
│   ├── SPC-2: Przedstawienie komisarz Wolskiej      [3 SP] ← Sprint 1
│   └── SPC-3: Opis miasteczka Czerna               [3 SP] ← Sprint 1
│
├── EPIC-2: Część II – Śledztwo
│   ├── SPC-4: Pierwsza wizja lokalna               [5 SP] ← Sprint 2
│   ├── SPC-5: Przesłuchania – runda I              [5 SP] ← Sprint 2
│   ├── SPC-6: Fałszywy trop                        [8 SP] ← Sprint 3
│   ├── SPC-7: Kluczowa poszlaka                    [5 SP] ← Sprint 3
│   └── SPC-8: Przesłuchania – runda II             [3 SP] ← Sprint 3
│
├── EPIC-3: Część III – Przełom i finał
│   ├── SPC-9:  Zwrot akcji – prawdziwy sprawca     [8 SP] ← Sprint 4
│   ├── SPC-10: Finałowe starcie                    [8 SP] ← Sprint 4
│   └── SPC-11: Epilog                              [5 SP] ← Sprint 4
│
└── EPIC-4: Redakcja i spójność
    ├── SPC-12: Korekta spójności fabularnej        [5 SP] ← Sprint 5
    ├── SPC-13: Redakcja językowa całości           [8 SP] ← Sprint 5
    └── SPC-14: Finalna wersja dokumentu            [2 SP] ← Sprint 5

SUMA: 14 Stories | 73 Story Points | 5 Sprintów
```

---

> **Wskazówka dla wykładowcy:** Ten plik służy jako wzorzec demonstracyjny.  
> Studenci powtarzają identyczną procedurę dla swojego wylosowanego gatunku i tytułu.  
> Liczba Stories na Sprint powinna odpowiadać dostępnemu czasowi: na 45-minutowe zajęcia  
> wystarczy 2–3 Stories w Sprint 1 z łączną liczbą SP 8–13.
