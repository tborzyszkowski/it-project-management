# Zadania – Część 1B: Przygotowanie środowiska i Sprint Planning

> **Czas:** 60 minut | **Poziom:** podstawowy (bez programowania)  
> Wykonaj kroki w kolejności. Scrum Master prowadzi konfigurację, pozostali obserwują i powtarzają.

---

## Krok 1 – Podział na zespoły i wybór projektu

**Czas: 5 minut**

### Zadanie 1.1 – Podział na role

Zdecyduj, kto w waszym 4–5 osobowym zespole pełni jaką rolę:

| Rola | Imię osoby | E-mail |
|---|---|---|
| Product Owner | | |
| Scrum Master | | |
| Developer 1 | | |
| Developer 2 | | |
| Developer 3 (opcjonalnie) | | |

> **Wskazówka**: Scrum Master powinien być osobą, która lubi organizować i pilnować procesu. Product Owner – osobą z pomysłami i wizją.

### Zadanie 1.2 – Wylosuj gatunek

Wylosuj karteczkę z gatunkiem powieści i uzupełnij:

| Element | Twój wybór |
|---|---|
| **Gatunek** | *(np. Kryminał)* |
| **Tytuł roboczy** | *(np. „Zbrodnia w Zamku Blum")* |
| **Główny bohater** | *(np. „Komisarz Marek Starski, 48 lat")* |
| **Antagonista** | *(np. „Nieznany morderca z przeszłości komisarza")* |
| **Miejsce akcji** | *(np. „Małe miasteczko w Sudetach, zima")* |

---

## Krok 2 – Zakładanie kont Jira

**Czas: 15 minut | Wykonuje: każdy uczestnik samodzielnie, Scrum Master jako pierwszy**

> ✅ **Dlaczego Jira?**  
> Jira (plan Free) nie wymaga subskrypcji, karty płatniczej ani konta firmowego. Wystarczy dowolny adres e-mail. Bezpłatny plan obejmuje do **10 użytkowników** — w zupełności wystarczy na zajęcia.

---

### Zadanie 2.1 – Rejestracja konta Atlassian

> ✅ Masz już konto Atlassian (Jira, Trello, Confluence)? **Pomiń ten krok i przejdź do Zadania 2.2.**

**Wykonuje: każdy uczestnik (samodzielnie, zaczynając od Scrum Mastera)**

1. Otwórz przeglądarkę i wejdź na: **https://www.atlassian.com/software/jira/free**

2. Kliknij niebieski przycisk **„Get it free"**

3. Wpisz swój adres e-mail → kliknij **„Agree – Sign Up"**  
   *(Dowolny e-mail — nie wymaga konta Microsoft ani Google, nie pyta o adres zamieszkania)*

4. Sprawdź skrzynkę e-mail — Atlassian wysyła **6-cyfrowy kod weryfikacyjny**  
   *(Sprawdź też folder SPAM, jeśli nie ma po 2 minutach)*

5. Wpisz kod na stronie → kliknij **„Verify"**

6. Ustaw hasło (min. 8 znaków) → kliknij **„Continue"**

7. Wpisz imię i nazwisko → kliknij **„Continue"**

> ✅ Konto Atlassian gotowe. Zapamiętaj e-mail i hasło — będą potrzebne przy każdym logowaniu.

---

### Zadanie 2.2 – Tworzenie site i projektu

**Wykonuje: Scrum Master** *(pozostali dołączą przez zaproszenie w Zadaniu 2.3)*

1. Po rejestracji Jira pyta o nazwę **site** (Twoja przestrzeń robocza):
   - Wpisz: `bim-[nazwazespolu]`  
     *(np. `bim-kryminal`, `bim-horror`, `bim-romans`, `bim-fantastyka`)*  
     ⚠️ Tylko litery, cyfry i myślniki — **bez polskich znaków!**
   - Adres Twojej Jiry będzie: `bim-[nazwazespolu].atlassian.net`
   - Kliknij **„Continue"**

2. *„What kind of work does your team do?"* → wybierz **„Software development"** → **„Next"**

3. Pojawi się ekran wyboru szablonu projektu:
   - Kliknij kafelek **„Scrum"** ← **KRYTYCZNE! Nie wybieraj Kanban ani Basic!**
   - Kliknij **„Select"**
   - Typ projektu: wybierz **„Team-managed project"** *(prostszy dla początkujących)*
   - **Project name**: tytuł roboczy waszej powieści *(np. „Zbrodnia w Zamku Blum")*
   - Kliknij **„Create project"**

4. Jira tworzy projekt i otwiera widok **Backlog** — to jest Twój pulpit pracy.

> ✅ **Sprawdzenie**: widzisz stronę projektu z pustym Backlogiem i lewym menu z opcjami: Backlog, Board, Reports…

---

### Zadanie 2.3 – Zaproszenie członków zespołu

**Wykonuje: Scrum Master**

1. W lewym menu projektu (na samym dole) kliknij **„Project settings"**

2. Wybierz **„Access"** (lub **„People"** w zależności od wersji Jiry)

3. Kliknij **„Add people"** (prawy górny róg)

4. Wpisz adresy e-mail pozostałych członków zespołu  
   *(możesz wpisywać po jednym lub kilka oddzielonych przecinkami)*

5. Rola: zostaw **„Member"**

6. Kliknij **„Send invites"**

---

**Wykonuje: każdy zaproszony członek zespołu**

1. Sprawdź skrzynkę e-mail (i folder **SPAM / Oferty**)

2. Znajdź wiadomość od `no-reply@atlassian.com` z tytułem zawierającym *„invited you"*

3. Kliknij przycisk **„Join project"** w treści e-maila

4. Jeśli nie masz jeszcze konta Atlassian — zostaniesz przeprowadzony przez rejestrację (Zadanie 2.1)  
   Jeśli masz — zaloguj się i potwierdź dołączenie

5. Powinieneś zobaczyć projekt Scrum Mastera z Backlogiem

> ✅ **Sprawdzenie (Scrum Master)**: W **Project settings → Access** widoczni są wszyscy członkowie ze statusem aktywnym.

---

## Krok 3 – Konfiguracja projektu w Jira

**Czas: 20 minut | Wykonuje: Scrum Master + zespół**

### Zadanie 3.1 – Konfiguracja sprintu

1. W lewym menu kliknij **„Backlog"**

2. W widoku Backlog kliknij przycisk **„Create sprint"**  
   *(Pojawi się nowa sekcja „Sprint 1" u góry Backlogu)*

3. Kliknij **„···"** (trzy kropki) przy nagłówku sprintu → **„Edit sprint"**:
   - **Sprint name**: `Sprint 1`
   - **Start date**: dzisiejsza data
   - **End date**: dzisiejsza data *(sprint = 1 dzień zajęć)*
   - Kliknij **„Update"**

> ✅ **Sprawdzenie**: W Backlogu widoczna sekcja **„Sprint 1"** z datami oraz sekcja **„Backlog"** poniżej.

---

### Zadanie 3.2 – Poznaj hierarchię elementów w Jira Scrum

Zanim zaczniesz tworzyć elementy, zapamiętaj hierarchię w szablonie Scrum w Jira:

```
Epic  (duży obszar produktu)
 └── Story  (= PBI – główna jednostka, szacowana w Story Points)
      └── Sub-task  (konkretne działania)
 └── Bug  (błąd / niespójność – na tym samym poziomie co Story)
```

| Typ | Kolor | Odpowiednik Scrum | Użycie |
|---|---|---|---|
| **Epic** | Fioletowy | Epic | „Napisanie powieści" |
| **Story** | Zielony | PBI (Product Backlog Item) | Konkretne wymaganie, szacowane w SP |
| **Bug** | Czerwony | Bug | Błąd / niespójność do poprawy |
| **Sub-task** | Niebieski | Task | Działania techniczne w ramach Story |

> ℹ️ W Jira Free szablon Scrum nie ma osobnego poziomu „Feature" — **Epic** pełni rolę grupującą dla Stories.

---

### Zadanie 3.3 – Utwórz Epici

**Wykonuje: Product Owner**

1. W lewym menu kliknij **„Roadmap"** (lub **„Timeline"** w zależności od wersji Jiry)

2. Kliknij **„+ Create epic"** (lub przycisk **„+ Create"** w górnym menu → typ: **Epic**):
   - `Napisanie powieści – [tytuł]`
   - `Część I – Wprowadzenie i postacie`
   - `Część II – Akcja i punkt zwrotny`
   - `Część III – Zakończenie`

3. Kliknij **„Save"** lub **„Create"** po każdym Epicu

> ✅ **Sprawdzenie**: W widoku Roadmap widoczne są Epici jako poziome belki lub lista.

---

### Zadanie 3.4 – Utwórz pierwsze Stories w Backlogu

**Wykonuje: Product Owner**

1. W lewym menu kliknij **„Backlog"**

2. W sekcji „Backlog" (na dole widoku) kliknij **„+ Create issue"**

3. Upewnij się, że wybrany typ to **„Story"**

4. Wpisz tytuł Story → zatwierdź Enter lub kliknij **„Create"**

5. Otwórz Story (kliknij jej tytuł) i uzupełnij:
   - **Description**: treść wymagania + kryteria akceptacji
   - **Epic Link**: przypisz do odpowiedniego Epica *(prawy panel → pole „Epic Link")*
   - *(Story Points uzupełnisz w Kroku 4 – Sprint Planning)*

6. Powtórz dla kolejnych Stories

> ✅ **Sprawdzenie**: W sekcji **„Backlog"** widoczna lista Stories.

---

## Krok 4 – Sprint Planning

**Czas: 20 minut | Prowadzi: Product Owner + Scrum Master**

### Zadanie 4.1 – Tworzenie PBI (Product Backlog Items)

**Wykonuje: Product Owner**

Dla każdego gatunku powieści utwórz minimum **6 PBI**. Poniżej przykłady dla każdego gatunku:

---

#### 🔍 Kryminał

| # | Tytuł PBI | Opis / Kryterium akceptacji |
|---|---|---|
| 1 | Opis miejsca zbrodni | Mroczny, szczegółowy opis ≥ 200 słów. Czytelnik „widzi" miejsce. |
| 2 | Profil detektywa | Imię, wygląd, historia, motywacja, słabości ≥ 150 słów |
| 3 | Profil ofiary | Kim był? Co ukrywał? ≥ 100 słów |
| 4 | Rozdział 1 – Odkrycie ciała | Scena otwierająca ≥ 300 słów, napięcie, pierwsza wskazówka |
| 5 | Rozdział 2 – Pierwsze przesłuchanie | Dialog ≥ 200 słów, podejrzany bohater drugiego planu |
| 6 | Review i korekta Rozdziału 1 | Brak niespójności fabularnych, imiona spójne, DoD spełnione |
| 7 | Okładka – opis dla AI | Prompt do wygenerowania grafiki okładki |

---

#### 👻 Horror

| # | Tytuł PBI | Opis / Kryterium akceptacji |
|---|---|---|
| 1 | Opis opuszczonego miejsca | Klimat grozy, szczegóły sensoryczne ≥ 200 słów |
| 2 | Profil głównego bohatera | Zwykła osoba z przeszłością, podatna na strach ≥ 150 słów |
| 3 | Opis antagonisty / zła | Zjawa, potwór, psychopata – forma i motywacja ≥ 100 słów |
| 4 | Rozdział 1 – Przybycie | Bohater trafia do miejsca ≥ 300 słów, budowanie napięcia |
| 5 | Rozdział 2 – Pierwsze zdarzenie | Coś niemożliwego się dzieje ≥ 250 słów |
| 6 | Review Rozdziału 1 | DoD: klimat grozy, spójność, min. słów |
| 7 | Okładka – opis dla AI | Prompt do grafiki okładki |

---

#### 💕 Romans

| # | Tytuł PBI | Opis / Kryterium akceptacji |
|---|---|---|
| 1 | Profil bohaterki | Osobowość, wygląd, marzenia, słabości ≥ 150 słów |
| 2 | Profil bohatera | Osobowość, wygląd, historia ≥ 150 słów |
| 3 | Opis świata / miasta | Klimat, sezon, atmosfera ≥ 150 słów |
| 4 | Rozdział 1 – Pierwsze spotkanie | Chemia, napięcie, komizm ≥ 300 słów |
| 5 | Rozdział 2 – Komplikacja | Przeszkoda, nieporozumienie ≥ 250 słów |
| 6 | Review Rozdziału 1 | DoD: spójność postaci, emocje, min. słów |
| 7 | Okładka – opis dla AI | Prompt do grafiki okładki |

---

#### 🚀 Sci-fi

| # | Tytuł PBI | Opis / Kryterium akceptacji |
|---|---|---|
| 1 | Opis świata / universe | Zasady rządzące rzeczywistością ≥ 200 słów |
| 2 | Profil głównego bohatera | Rola w społeczeństwie przyszłości ≥ 150 słów |
| 3 | Opis technologii lub zjawiska | Centralna idea naukowa ≥ 150 słów |
| 4 | Rozdział 1 – Otwarcie | Bohater w swoim świecie, zawiązanie ≥ 300 słów |
| 5 | Rozdział 2 – Wyzwanie | Coś burzy porządek ≥ 250 słów |
| 6 | Review Rozdziału 1 | DoD: spójność świata, min. słów |
| 7 | Okładka – opis dla AI | Prompt do grafiki okładki |

---

#### 🔫 Thriller

| # | Tytuł PBI | Opis / Kryterium akceptacji |
|---|---|---|
| 1 | Opis sytuacji zagrożenia | Kontekst polityczny / kryminalny ≥ 200 słów |
| 2 | Profil bohatera | Agent, dziennikarz, cywil w tarapatach ≥ 150 słów |
| 3 | Profil antagonisty | Motywacja, zasoby, poziom zagrożenia ≥ 100 słów |
| 4 | Rozdział 1 – In medias res | Akcja od początku ≥ 300 słów, tempo, napięcie |
| 5 | Rozdział 2 – Punkt przełomowy | Bohater dowiaduje się za dużo ≥ 250 słów |
| 6 | Review Rozdziału 1 | DoD: tempo narracji, spójność, min. słów |
| 7 | Okładka – opis dla AI | Prompt do grafiki okładki |

---

### Zadanie 4.2 – Tworzenie Stories w Jira

**Wykonuje: Product Owner** (w Jira, widok Backlog)

Dla każdej Story z listy powyżej:

1. W widoku **Backlog** kliknij **„+ Create issue"** → typ: **„Story"**
2. Wpisz **tytuł** Story
3. Otwórz Story i w polu **„Description"** dodaj treść wymagania i kryteria akceptacji
4. Kliknij **„Save"**
5. Ustaw **kolejność** Stories przez przeciąganie w Backlogu (priorytet = kolejność od góry)

---

### Zadanie 4.3 – Szacowanie Story Points (Planning Poker)

**Prowadzi: Scrum Master**

#### Zasady szacowania

| Story Points | Co oznacza | Przykład |
|---|---|---|
| **1** | Trivialnie proste, 5 minut | Tytuł i jedno zdanie |
| **2** | Proste, ~10 minut | Krótki profil postaci (100 słów) |
| **3** | Średnie, ~15 minut | Dłuższy profil z backstory (150 słów) |
| **5** | Złożone, ~20 minut | Cały rozdział (300 słów + review) |
| **8** | Bardzo złożone, ~30 minut | Rozdział + kilka powiązanych zadań |

#### Procedura szacowania każdego PBI

1. PO czyta tytuł i opis PBI
2. Każdy Developer **w tajemnicy** zapisuje swoją ocenę (1/2/3/5/8) na kartce
3. Na sygnał SM – wszyscy jednocześnie pokazują kartki
4. Przy rozbieżności – krótka dyskusja (max 2 min), nowe głosowanie
5. Scrum Master wpisuje uzgodnioną wartość w Jira: otwórz Story → prawy panel → pole **„Story points"**

---

### Zadanie 4.4 – Wypełnij Sprint Backlog

**Prowadzi: Scrum Master + PO**

1. W widoku **Backlog** przeciągnij Story z sekcji „Backlog" do sekcji **„Sprint 1"**  
   *(lub kliknij Story prawym przyciskiem → „Move to sprint" → Sprint 1)*

2. Zacznij od najwyżej priorytetowych Stories

3. Dodawaj Stories dopóki suma Story Points ≤ **12–15 SP**

4. Dla każdej Story w Sprint 1 dodaj przynajmniej jeden **Sub-task**:
   - Otwórz Story → w sekcji „Child issues" kliknij **„Create child issue"** → typ: **Sub-task**
   - Przykład: `"Wygeneruj tekst z AI, przeredaguj do min. 300 słów"`
   - Przypisz Sub-task do konkretnego Developera

---

### Zadanie 4.5 – Wybierz sposób przechowywania wyników pracy

**Prowadzi: Scrum Master** (decyzja całego zespołu)

Zanim zaczniesz sprint, ustal gdzie zespół będzie zapisywał napisane teksty, opisy postaci i inne efekty pracy. Masz trzy opcje — wybierz jedną i trzymaj się jej przez cały sprint.

---

#### Opcja 1 — Jira Pages ✅ *(rekomendowana)*

Jira Pages to wbudowany edytor dokumentów (uproszczony wiki). Nie wymaga żadnych dodatkowych narzędzi.

1. W lewym menu projektu kliknij **„Pages"**  
   *(jeśli nie widać: kliknij „+ More" w lewym menu → „Pages")*

2. Kliknij **„Create page"**

3. Nadaj stronie tytuł zgodny z rozdziałem / elementem powieści  
   *(np. „Rozdział 1 – Odkrycie ciała")*

4. Napisz lub wklej tekst w edytorze — obsługuje nagłówki, listy, tabele, obrazy

5. Kliknij **„Publish"** — strona jest od razu widoczna dla całego zespołu

6. **Połącz stronę ze Story**: otwórz Story → prawy panel → **„Link a page"** → wybierz stronę

**Proponowana struktura stron:**
```
📄 [Tytuł powieści] — strona główna
  ├── 📄 Postacie i świat przedstawiony
  ├── 📄 Rozdział 1 – [tytuł]
  ├── 📄 Rozdział 2 – [tytuł]
  └── 📄 Notatki ze Sprintu
```

> ✅ Pages mają historię zmian — można wrócić do poprzedniej wersji

---

#### Opcja 2 — Opis i komentarze w Story

Dla krótkich fragmentów (opis postaci, krótka scena):

1. Otwórz Story w Backlogu
2. Kliknij pole **„Description"** — wpisz lub wklej tekst (obsługuje formatowanie rich text)
3. Aby dodać wersję do przeglądu przez SM/QA: kliknij **„Add a comment"** na dole Story

> ⚠️ Brak wersjonowania i trudniejsza nawigacja przy dłuższych tekstach — nie zalecane dla rozdziałów

---

#### Opcja 3 — Załączniki (pliki Word / PDF / txt)

Jeśli zespół woli pisać w zewnętrznym edytorze (Word, Google Docs, Notepad++):

1. Otwórz Story lub Epic
2. Kliknij ikonę spinacza **„Attach"** (prawy panel lub dolny pasek)
3. Przeciągnij plik lub kliknij **„Upload"** → wybierz plik z dysku
4. Plik jest widoczny przy Issue dla całego zespołu
5. Aby zaktualizować: wgraj nową wersję pod tą samą nazwą

> ⚠️ Brak edycji online — trzeba pobierać, edytować i wgrywać nową wersję

---

> ✅ **Sprawdzenie**: Cały zespół wie gdzie wklejać teksty i jak linkować wyniki do Stories w Jira.

---

### Zadanie 4.6 – Ustal Definition of Done

**Prowadzi: Scrum Master** (wszyscy ustalają razem)

Zapiszcie uzgodnione DoD w Jira:

1. W lewym menu projektu kliknij **„Pages"** (lub **„+ More"** → „Pages")
2. Kliknij **„Create page"**
3. Tytuł strony: `Definition of Done`
4. Wpisz uzgodnione kryteria i kliknij **„Publish"**

   > ℹ️ Jeśli opcja Pages nie jest widoczna — utwórz Story o tytule `[DoD] Definition of Done` i wpisz kryteria w polu Description.

```markdown
# Definition of Done – Sprint 1

## Dla rozdziału / sceny
- [ ] Tekst liczy minimum 300 słów
- [ ] Imiona postaci są spójne w całym tekście
- [ ] Styl narracji jest spójny z gatunkiem
- [ ] Tekst wklejony do wspólnego dokumentu
- [ ] Story zaktualizowana w Jira (status = Done)
- [ ] Review przeprowadzone przez QA (przynajmniej 1 osoba)
```

---

## Podsumowanie Kroku 4

Po zakończeniu Sprint Planning sprawdź listę kontrolną:

- [ ] Konto Jira (site) założone, wszyscy mają dostęp
- [ ] Projekt Scrum utworzony z właściwą nazwą
- [ ] Sprint 1 skonfigurowany z datami
- [ ] Minimum 6 PBI w backlogu z opisami
- [ ] Każde PBI ma Story Points
- [ ] Sprint Backlog zawiera 12–15 SP
- [ ] Każde PBI ma co najmniej 1 Task przypisany do Developera
- [ ] Ustalono sposób przechowywania wyników (Pages / Description / Załączniki)
- [ ] Definition of Done zapisane w Wiki
- [ ] Wszyscy znają swoje zadania na sprint

> ✅ Jeśli wszystko zaznaczone – jesteś gotowy/-a na **SPRINT!** → [Blok 2A](../../Blok2-Sprint-Podsumowanie/2A-Sprint/Zadania.md)
