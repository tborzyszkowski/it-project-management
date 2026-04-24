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

**Czas: 15 minut | Wykonuje: Scrum Master (wszyscy obserwują i powtarzają na swoich komputerach)**

> ⚠️ **Przed startem**: każdy uczestnik potrzebuje adresu e-mail dostępnego na swoim komputerze (do odebrania zaproszenia). Konto Microsoft zakłada **Scrum Master** — reszta dołącza przez zaproszenie.

---

### Zadanie 2.1 – Założenie konta Microsoft (jeśli nie masz)

> ✅ Masz już konto Outlook.com / Hotmail / Live / konto Microsoft 365 (służbowe lub szkolne)? **Pomiń ten krok i przejdź do Zadania 2.2.**

1. Otwórz przeglądarkę i wejdź na: **https://signup.live.com**

2. W polu **„Utwórz adres e-mail"** wpisz wybraną nazwę użytkownika, np. `jan.kowalski.bim`  
   → domena: `@outlook.com`  
   → kliknij **„Dalej"**

3. Ustaw hasło (min. 8 znaków, wielka litera + cyfra) → kliknij **„Dalej"**

4. Podaj imię i nazwisko → kliknij **„Dalej"**

5. Wybierz kraj **(Polska)** i datę urodzenia → kliknij **„Dalej"**

6. Rozwiąż captcha (puzzle graficzne) → kliknij **„Dalej"**

7. Konto jest gotowe. Zapamiętaj lub zapisz:
   - **Login**: `jan.kowalski.bim@outlook.com`
   - **Hasło**: *(zapisz w bezpiecznym miejscu)*

---

### Zadanie 2.2 – Logowanie do Azure DevOps i tworzenie organizacji

**Wykonuje: Scrum Master**

> ⛔ **Ważna uwaga – NIE zakładamy konta Azure!**  
> Azure DevOps (narzędzie do zarządzania projektem) to **osobna, darmowa usługa** — nie wymaga subskrypcji Azure ani podawania adresu zamieszkania czy danych karty płatniczej.  
> Jeśli widzisz stronę *„Tworzenie bezpłatnego konta platformy Azure"* z pytaniami o adres lub kartę — **zatrzymaj się i wróć do kroku 1 poniżej**.

1. Otwórz przeglądarkę i wejdź **bezpośrednio** na adres rejestracji Azure DevOps:  
   **https://aex.dev.azure.com/signup**  
   *(Ten adres pomija stronę marketingową i trafia od razu do właściwego kreatora.)*

2. Pojawi się ekran logowania Microsoft — **zaloguj się kontem Outlook.com / Hotmail / Live**:
   - Wpisz adres e-mail → kliknij **„Dalej"**
   - Wpisz hasło → kliknij **„Zaloguj się"**
   - Jeśli pojawi się pytanie *„Pozostać zalogowanym?"* → kliknij **„Tak"**

   > ⚠️ Jeśli po zalogowaniu nadal widzisz ekran z pytaniem o adres zamieszkania lub kartę płatniczą — zamknij tę kartę przeglądarki i wróć do linka z kroku 1. Możliwe, że przeglądarka zapamiętała poprzednią sesję i przekierowała na złą stronę. Spróbuj otworzyć okno prywatne (Ctrl+Shift+N).

3. Przy pierwszym logowaniu Azure DevOps wyświetli pytania powitalne — **nie ma tu pól adresowych**:
   - *„What is your name?"* → wpisz imię i nazwisko
   - *„What do you want to work on?"* → wybierz dowolnie (np. **„Software development"**)
   - Kliknij **„Continue"**

4. Pojawi się ekran **„Create new organization"**:
   - **Organization name**: wpisz `bim-[nazwazespolu]`  
     *(np. `bim-kryminal`, `bim-horror`, `bim-romans`, `bim-fantastyka`)*  
     ⚠️ Tylko litery, cyfry i myślniki — **bez polskich znaków!**
   - **We'll host your projects in**: wybierz **West Europe**
   - Rozwiąż captcha, jeśli się pojawi
   - Kliknij **„Continue"**

5. Pojawi się kreator nowego projektu — **NIE twórz jeszcze projektu**, zamknij lub pomiń (kliknij „X" lub „Skip"). Projekt utworzymy w Kroku 3.

6. Powinieneś znaleźć się na stronie głównej swojej organizacji:  
   `https://dev.azure.com/bim-[nazwazespolu]`

> ✅ **Sprawdzenie**: w prawym górnym rogu widać ikonę konta (inicjały lub awatar) i nazwę organizacji na górze strony. Nie było żadnych pytań o adres ani kartę płatniczą.

---

### Zadanie 2.3 – Zaproszenie członków zespołu

**Wykonuje: Scrum Master**

1. W lewym dolnym rogu strony kliknij ikonę koła zębatego ⚙️ → **„Organization settings"**  
   *(Alternatywna ścieżka: `https://dev.azure.com/bim-[nazwazespolu]/_settings/`)*

2. W lewym menu (sekcja **„General"**) kliknij **„Users"**

3. Kliknij niebieski przycisk **„Add users"** (prawy górny róg tabeli)

4. Wypełnij formularz:
   - **Users**: wpisz adresy e-mail wszystkich członków zespołu  
     *(możesz wpisywać po jednym i naciskać Enter, lub wkleić kilka naraz oddzielonych przecinkami)*
   - **Access level**: wybierz **Basic**
   - **Add to projects**: zostaw puste (projekt dodamy później)
   - **Azure DevOps Groups**: zostaw domyślne (`Project Contributors`)

5. Kliknij **„Add"**

6. Na ekranie pojawi się potwierdzenie: *„X user(s) added successfully"*  
   Na adresy e-mail uczestników zostaną wysłane zaproszenia.

---

**Wykonuje: każdy zaproszony członek zespołu**

1. Otwórz skrzynkę e-mail (sprawdź też folder **SPAM / Oferty**)

2. Znajdź wiadomość od `azure@microsoft.com` z tytułem:  
   *„[Scrum Master imię] has invited you to join Azure DevOps"*

3. Kliknij niebieski przycisk **„Join now"** w treści e-maila

4. Zostaniesz przekierowany do przeglądarki — zaloguj się swoim kontem Microsoft  
   *(tak samo jak w Zadaniu 2.2, krok 3)*

5. Potwierdź dołączenie klikając **„Continue"**

6. Powinieneś zobaczyć stronę organizacji Scrum Mastera:  
   `https://dev.azure.com/bim-[nazwazespolu]`

> ✅ **Sprawdzenie (Scrum Master)**: wróć do **Organization Settings → Users** — wszyscy zaproszeni powinni mieć status **„Active"** (nie „Pending"). Jeśli ktoś ma „Pending" — e-mail jeszcze nie otworzył lub trafił do SPAM.

---

## Krok 3 – Tworzenie i konfiguracja projektu

**Czas: 20 minut | Wykonuje: Scrum Master + zespół**

### Zadanie 3.1 – Tworzenie projektu

1. Przejdź na stronę główną organizacji: `https://dev.azure.com/bim-[nazwazespolu]`

2. Kliknij niebieski przycisk **„+ New project"** (prawy górny róg strony)

3. Wypełnij formularz:

   | Pole | Wartość |
   |---|---|
   | **Project name** | Tytuł roboczy powieści *(np. „Zbrodnia w Zamku Blum")* |
   | **Description** | Gatunek + 1 zdanie o fabule |
   | **Visibility** | **Private** ← ważne! |
   | **Version control** | Git |
   | **Work item process** | **Scrum** ← **KRYTYCZNE! Nie wybieraj innego!** |

4. Kliknij **„Create"**

5. Azure DevOps przez kilka sekund tworzy projekt, następnie automatycznie otwiera jego stronę główną (Overview → Summary).

6. **Dodaj uczestników do projektu** (poza organizacją to oddzielny krok):
   - Kliknij **„Project settings"** (lewy dolny róg) → **„Teams"** → kliknij nazwę domyślnego zespołu *(np. „Zbrodnia w Zamku Blum Team")*
   - Kliknij **„Add"**
   - Wpisz adresy e-mail (lub wyszukaj po nazwie — pojawią się osoby dodane w kroku 2.3)
   - Kliknij **„Save"**

> ✅ **Sprawdzenie**: W **Project Settings → Teams → [nazwa zespołu]** widoczni są wszyscy członkowie zespołu.

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
