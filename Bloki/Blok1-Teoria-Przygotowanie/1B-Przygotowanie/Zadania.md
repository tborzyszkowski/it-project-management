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

## Krok 2 – Zakładanie kont Azure DevOps

**Czas: 15 minut | Wykonuje: Scrum Master (wszyscy obserwują)**

### Zadanie 2.1 – Rejestracja i tworzenie organizacji

1. Otwórz przeglądarkę i przejdź na: **https://dev.azure.com**

2. Kliknij przycisk **„Start free"** (niebieski przycisk na środku strony).

3. Zaloguj się:
   - ✅ Masz konto Microsoft (Outlook, Hotmail, Live)? → Zaloguj się.
   - ❌ Nie masz konta? → Kliknij „Create one!" i załóż konto Outlook.com.

4. Po zalogowaniu zostaniesz przekierowany do kreatora organizacji:
   - Wpisz nazwę organizacji: `bim-[waszazespolu]`  
     *(np. `bim-kryminal`, `bim-horror`, `bim-romans`)*
   - Wybierz region: **West Europe**
   - Kliknij **„Continue"**

5. Pojawi się kreator nowego projektu – **NIE twórz jeszcze projektu**, przejdź do Zadania 2.2.

---

### Zadanie 2.2 – Zaproszenie członków zespołu

**Wykonuje: Scrum Master**

1. Kliknij ikonę koła zębatego ⚙️ (prawy dolny róg, przy nazwie organizacji) → **„Organization Settings"**

2. W lewym menu wybierz **„Users"**

3. Kliknij **„Add users"**

4. Wprowadź adresy e-mail pozostałych członków zespołu (jeden po drugim lub wszystkie na raz, oddzielone przecinkami)

5. Ustaw Access Level: **Basic**

6. Kliknij **„Add"**

**Wykonuje: każdy zaproszony członek**

1. Sprawdź skrzynkę e-mail (i folder SPAM!)
2. Kliknij link w e-mailu z zaproszeniem
3. Zaloguj się na swoje konto Microsoft
4. Potwierdź dołączenie do organizacji

> ✅ **Sprawdzenie**: wszyscy członkowie widoczni na liście Users w ustawieniach organizacji.

---

## Krok 3 – Konfiguracja projektu w Azure DevOps

**Czas: 20 minut | Wykonuje: Scrum Master + zespół**

### Zadanie 3.1 – Tworzenie projektu

1. Wróć do strony głównej organizacji (kliknij logo ADO lub nazwę organizacji)

2. Kliknij **„+ New project"** (prawy górny róg)

3. Uzupełnij formularz:
   - **Project name**: wpisz tytuł roboczy waszej powieści  
     *(np. „Zbrodnia w Zamku Blum")*
   - **Description**: gatunek + jedno zdanie o fabule
   - **Visibility**: **Private**
   - **Version control**: **Git**
   - **Work item process**: **Scrum** ← **WAŻNE! Nie zmieniaj!**

4. Kliknij **„Create"**

---

### Zadanie 3.2 – Konfiguracja sprintu

1. W lewym menu kliknij **„Boards"** → **„Backlogs"**

2. Kliknij ikonę koła zębatego ⚙️ przy nazwie zespołu (prawy górny róg widoku Boards)

3. Wybierz **„Team configuration"**

4. Przejdź do zakładki **„Iterations"**

5. Kliknij **„+ New iteration"**:
   - Nazwa: **Sprint 1**
   - Data początkowa: *dzisiejsza data*
   - Data końcowa: *dzisiejsza data* (sprint = 1 dzień zajęć)
   - Kliknij **„Save and close"**

6. Zaznacz checkbox przy **Sprint 1** → kliknij **„Save"**

> ✅ **Sprawdzenie**: W widoku Backlogs widoczna jest zakładka „Sprint 1".

---

### Zadanie 3.3 – Poznaj hierarchię backlogu

Zanim zaczniesz tworzyć elementy, zapamiętaj hierarchię w szablonie Scrum:

```
Epic
 └── Feature
      └── Product Backlog Item (PBI)  ← główna jednostka
           └── Task                   ← konkretne działania
           └── Bug                    ← defekty
```

| Typ | Kolor w ADO | Użycie |
|---|---|---|
| Epic | Żółty | „Napisanie powieści" |
| Feature | Fioletowy | „Rozdział 1", „Profil postaci" |
| **PBI** | Niebieski | Konkretne wymagania, szacowane w SP |
| Task | Żółty jasny | Działania techniczne w ramach PBI |
| Bug | Czerwony | Błędy do naprawy |

### Zadanie 3.4 – Utwórz Epic i Feature

**Wykonuje: Product Owner**

1. W widoku **Boards → Backlogs** upewnij się, że jesteś w widoku „Backlog" (nie Sprint 1)

2. Kliknij **„+ New Work Item"** → wybierz **Epic**:
   - Tytuł: `Napisanie powieści [tytuł]`
   - Kliknij **„Save"**

3. Rozwiń Epica i kliknij **„+ Add Feature"**:
   - `Część I – Wprowadzenie i postacie`
   - `Część II – Akcja i punkt zwrotny`
   - `Część III – Zakończenie`

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

### Zadanie 4.2 – Tworzenie PBI w ADO

**Wykonuje: Product Owner** (w ADO, widok Boards → Backlogs)

Dla każdego PBI z listy powyżej:

1. Kliknij **„+ New Work Item"** → **„Product Backlog Item"**
2. Wpisz **tytuł** PBI
3. W opisie dodaj **kryteria akceptacji** (pole „Acceptance Criteria" w ADO)
4. Zapisz PBI (przycisk „Save")
5. Ustaw **kolejność** PBI przez przeciąganie (priorytet = kolejność od góry)

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
5. Scrum Master wpisuje uzgodnioną wartość do pola **„Story Points"** w ADO

---

### Zadanie 4.4 – Wypełnij Sprint Backlog

**Prowadzi: Scrum Master + PO**

1. W widoku **Boards → Backlogs** przejdź na zakładkę **„Sprint 1"**

2. Przeciągnij PBI z Backlogu do Sprint 1 (lub kliknij prawym przyciskiem → „Move to Sprint 1")

3. Zacznij od najwyżej priorytetowych PBI

4. Dodawaj PBI dopóki suma Story Points ≤ **12–15 SP**

5. Dla każdego PBI w Sprint 1 dodaj przynajmniej jeden **Task**:
   - Kliknij PBI → kliknij „+ Add Task"
   - Przykład: `"Wygeneruj tekst z AI, przeredaguj do min. 300 słów"`
   - Przypisz Task do konkretnego Developera

---

### Zadanie 4.5 – Ustal Definition of Done

**Prowadzi: Scrum Master** (wszyscy ustalają razem)

Odpiszcie uzgodnione DoD w ADO:

1. Przejdź do **Overview → Wiki**
2. Kliknij **„Create Wiki"** (lub „Add page")
3. Utwórz stronę `Definition of Done`
4. Wpisz uzgodnione kryteria (minimum 3):

```markdown
# Definition of Done – Sprint 1

## Dla rozdziału / sceny
- [ ] Tekst liczy minimum 300 słów
- [ ] Imiona postaci są spójne w całym tekście
- [ ] Styl narracji jest spójny z gatunkiem
- [ ] Tekst wklejony do wspólnego dokumentu
- [ ] PBI zaktualizowane w ADO (status = Done)
- [ ] Review przeprowadzone przez QA (przynajmniej 1 osoba)
```

---

## Podsumowanie Kroku 4

Po zakończeniu Sprint Planning sprawdź listę kontrolną:

- [ ] Organizacja ADO założona, wszyscy mają dostęp
- [ ] Projekt Scrum utworzony z właściwą nazwą
- [ ] Sprint 1 skonfigurowany z datami
- [ ] Minimum 6 PBI w backlogu z opisami
- [ ] Każde PBI ma Story Points
- [ ] Sprint Backlog zawiera 12–15 SP
- [ ] Każde PBI ma co najmniej 1 Task przypisany do Developera
- [ ] Definition of Done zapisane w Wiki
- [ ] Wszyscy znają swoje zadania na sprint

> ✅ Jeśli wszystko zaznaczone – jesteś gotowy/-a na **SPRINT!** → [Blok 2A](../../Blok2-Sprint-Podsumowanie/2A-Sprint/Zadania.md)
