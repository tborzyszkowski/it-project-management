# Plan zajęć – Zarządzanie projektami IT (4 godziny)

> **Studia podyplomowe BIM** | Zajęcia laboratoryjne  
> Czas trwania: 2 bloki × 2 godziny  
> Wymagania: brak umiejętności programowania

---

## Cele zajęć

Po zajęciach student będzie potrafił:

- wyjaśnić różnice między kluczowymi metodykami zarządzania projektami IT (Waterfall, Scrum, Kanban),
- opisać role projektowe i ich odpowiedzialności,
- założyć i skonfigurować projekt w narzędziu Azure DevOps (plan bezpłatny),
- pracować w zespole posługując się backlogiem, tablicą Kanban i przebiegiem sprintu,
- przeprowadzić retrospektywę i wyciągnąć wnioski z realizacji sprintu.

---

## Projekt edukacyjny – „Powieść pisana z AI"

Przez całe zajęcia zespoły realizują **jeden wspólny projekt symulacyjny**: napisanie krótkiej powieści (np. kryminału, horroru lub romansu) z pomocą narzędzi AI (ChatGPT, Copilot itp.).

Projekt celowo **nie wymaga umiejętności technicznych** – pozwala za to skupić się na procesie, rolach i narzędziach, które są identyczne w prawdziwych projektach IT (aplikacja = powieść, funkcja = rozdział, bug = błąd stylistyczny/fabularny).

### Analogia IT ↔ Powieść

| Świat IT | Projekt powieści |
|---|---|
| Produkt końcowy | Gotowa powieść (PDF / dokument) |
| Feature / User Story | Rozdział, scena, postać |
| Bug / Defect | Błąd fabularny, niespójność postaci |
| Definition of Done | Rozdział ma min. 300 słów, przeszedł review |
| Release | Opublikowany plik do pobrania |

---

## BLOK 1 – Teoria i przygotowanie (120 minut)

### Część 1A – Teoria zarządzania projektami IT (60 min)

#### 1. Wprowadzenie – czym różni się projekt IT od innych? (10 min)

- Specyfika projektów IT: zmieniające się wymagania, niematerialny produkt, wysoka złożoność.
- Częste przyczyny niepowodzeń (Chaos Report): niejasne wymagania, brak komunikacji, brak priorytetyzacji.
- Trójkąt projektowy: zakres – czas – budżet. W IT zwykle „zakres jest elastyczny".

#### 2. Metodyki zarządzania projektami IT (25 min)

##### Waterfall (model kaskadowy)
- Fazy: Wymagania → Projektowanie → Implementacja → Testowanie → Wdrożenie.
- Zalety: przewidywalność, dobra dokumentacja.
- Wady: zmiana wymagań = katastrofa, długi czas do pierwszego rezultatu.
- Kiedy stosować: projekty o stałych wymaganiach (np. systemy embedded, projekty budowlane z BIM).

##### Agile – manifest i wartości
- 4 wartości i 12 zasad Manifestu Agile.
- Kluczowe pojęcie: **iteracja** – małe, mierzalne przyrosty wartości.

##### Scrum (framework Agile)
- **Artefakty**: Product Backlog, Sprint Backlog, Increment.
- **Zdarzenia**: Sprint Planning, Daily Scrum, Sprint Review, Retrospektywa.
- **Sprint**: timeboxed (1–4 tygodnie), na zajęciach = 45 minut.

##### Kanban
- Tablica z kolumnami: `To Do | In Progress | Done`.
- Ograniczenie WIP (Work in Progress) – dlaczego to ważne?
- Różnica Scrum vs Kanban: iteracje vs ciągły przepływ.

#### 3. Role w projekcie IT (15 min)

| Rola | Odpowiedzialność | Odpowiednik w projekcie powieści |
|---|---|---|
| **Product Owner (PO)** | Wizja produktu, priorytetyzacja backlogu, głos klienta | Wydawca / Redaktor naczelny |
| **Scrum Master (SM)** | Facylitacja, usuwanie przeszkód, stróż procesu | Kierownik projektu / Coach |
| **Developer** | Tworzenie przyrostów, szacowanie, wykonanie | Pisarz / Autor |
| **QA / Tester** | Weryfikacja jakości, zgłaszanie defektów | Korektor / Beta-czytelnik |
| **Stakeholder** | Odbiorca produktu, źródło wymagań | Czytelnik docelowy |

> **Ważne**: W małych zespołach role można łączyć – Developer może być QA, ale PO i SM nie powinny być tą samą osobą.

#### 4. Narzędzia w projektach IT (10 min)

##### Azure DevOps (ADO) – plan bezpłatny (Basic)
- Do 5 użytkowników bezpłatnie, nieograniczone repozytoria Git, Boards, Pipelines (ograniczone).
- Kluczowe moduły na dziś: **Boards** (backlog, tablica Kanban, sprinty).

##### Jira – plan bezpłatny
- Do 10 użytkowników, funkcje Scrum i Kanban, raporty.
- Ograniczenia: brak zaawansowanych raportów i integracji.

> Na zajęciach używamy **Azure DevOps** (łatwiejsze zakładanie kont bez karty płatniczej).

---

### Część 1B – Przygotowanie do pracy (60 min)

#### Krok 1 – Podział na zespoły (5 min)

- Grupy 4–5 osób.
- Każda grupa losuje gatunek powieści: **kryminał / horror / romans / sci-fi / thriller**.
- Każda grupa wybiera tytuł roboczy i głównego bohatera.

**Przypisanie ról w zespole:**

| Rola | Ile osób |
|---|---|
| Product Owner | 1 |
| Scrum Master | 1 |
| Developer | 2–3 |

> W projekcie 4-osobowym: 1 PO, 1 SM, 2 Developerów (jeden z nich pełni też rolę QA).

---

#### Krok 2 – Zakładanie kont Azure DevOps (15 min)

**Instrukcja krok po kroku:**

1. Przejdź na stronę [https://dev.azure.com](https://dev.azure.com).
2. Kliknij **„Start free"**.
3. Zaloguj się kontem Microsoft (Outlook, Hotmail) lub utwórz nowe konto.
4. Po zalogowaniu kliknij **„Create new organization"**.
5. Podaj nazwę organizacji: `bim-[nazwazespolu]` (np. `bim-kryminał`).
6. Wybierz region: **West Europe**.
7. Kliknij **„Continue"**.

> **Uwaga**: Scrum Master zakłada organizację i **zaprasza pozostałych członków** przez Settings → Users → Add users (podając ich adresy e-mail).

---

#### Krok 3 – Konfiguracja projektu w ADO (20 min)

**Tworzenie projektu:**

1. Na stronie organizacji kliknij **„New project"**.
2. Nazwa projektu: tytuł roboczy powieści.
3. Widoczność: **Private**.
4. Version control: **Git**.
5. Work item process: **Scrum** ← ważne!
6. Kliknij **„Create"**.

**Konfiguracja Boards:**

1. Przejdź do **Boards → Backlogs**.
2. Skonfiguruj sprint: kliknij ikonę koła zębatego (Project Settings → Boards → Team Configuration → Iterations).
3. Utwórz sprint o nazwie `Sprint 1` z datami odpowiadającymi blokowi 2.

**Typy elementów w backlogu (Scrum template):**

| Typ | Opis | Przykład |
|---|---|---|
| **Epic** | Duży obszar produktu | „Napisanie powieści" |
| **Feature** | Część Epika | „Rozdział 1: Zbrodnia" |
| **Product Backlog Item (PBI)** | Konkretna funkcjonalność | „Opis miejsca zbrodni (min. 200 słów)" |
| **Task** | Działanie techniczne | „Wygeneruj opis z AI, przeredaguj" |
| **Bug** | Defekt | „Postać ma dwa różne imiona" |

---

#### Krok 4 – Sprint Planning (20 min)

**Product Owner prowadzi sesję planowania:**

1. PO tworzy w backlogu co najmniej **6 PBI** dla projektu powieści, np.:
   - Napisanie opisu świata przedstawionego (min. 150 słów)
   - Stworzenie profilu głównego bohatera
   - Stworzenie profilu antagonisty
   - Napisanie Rozdziału 1 (scena otwierająca)
   - Napisanie Rozdziału 2 (punkt zwrotny)
   - Review i korekta Rozdziału 1
   - Przygotowanie okładki (opis / prompt dla AI)

2. Scrum Master prowadzi **szacowanie** (Planning Poker uproszczony):
   - Każdy developer ocenia PBI w skali Story Points: 1 / 2 / 3 / 5 / 8.
   - Dyskusja przy rozbieżnościach.
   - Docelowa pojemność sprintu: **12–15 Story Points** (ok. 45 min pracy).

3. PBI z najwyższym priorytetem trafiają do **Sprint 1 Backlog**.

---

## BLOK 2 – Sprint i podsumowanie (120 minut)

### Część 2A – Sprint (45 minut aktywnej pracy)

**Scrum Master uruchamia sprint w ADO:**

1. Boards → Backlogs → Sprint 1 → kliknij **„Start sprint"** (lub ustaw daty).
2. Przełącz widok na **Boards → Sprint Board** (kolumny: To Do / In Progress / Done).

**Zasady pracy podczas sprintu:**

- Każdy Developer bierze **jeden Task** naraz i przeciąga go do `In Progress`.
- Korzysta z AI (ChatGPT/Copilot) do generowania treści, następnie **redaguje i poprawia**.
- Po ukończeniu przeciąga do `Done` i aktualizuje opis PBI.
- QA weryfikuje Definition of Done (min. słów, spójność fabuły) i oznacza PBI jako `Done` lub odsyła z komentarzem.

**Przykładowy workflow dla jednego PBI:**

```
[To Do] "Napisanie Rozdziału 1"
   ↓ Developer bierze task
[In Progress] → pisze prompt do AI → redaguje tekst → wkleja do dokumentu
   ↓ po ukończeniu
[Review] → QA sprawdza: czy ma 300+ słów? czy imiona są spójne?
   ↓ po akceptacji
[Done] → PBI zamknięte, PO powiadamiany
```

**Rola AI w projekcie:**

- AI jest narzędziem wspomagającym (jak GitHub Copilot dla programistów), nie autorem.
- Prompt engineering = odpowiednik konfiguracji narzędzia deweloperskiego.
- Przykładowe prompty do zademonstrowania:
  - `"Napisz mroczny opis opuszczonej willi w stylu horroru gotycko-angielskiego, max 200 słów, po polsku."`
  - `"Stwórz profil postaci: detektyw, 45 lat, cyniczny, z przeszłością w policji kryminalnej. Imię, wygląd, motywacja, słabości. Max 150 słów."`

---

### Część 2B – Daily Scrum (symulacja, 10 minut)

W połowie sprintu Scrum Master zatrzymuje pracę i prowadzi **Daily Scrum** (max 15 min):

Każdy Developer odpowiada na 3 pytania:
1. Co zrobiłem od ostatniego spotkania?
2. Co zamierzam zrobić do następnego?
3. Czy coś mi przeszkadza? (impedimenty)

Scrum Master notuje impedimenty w ADO jako `Impediment` work item i stara się je usunąć.

---

### Część 2C – Sprint Review (15 minut)

Każdy zespół **prezentuje przyrost** (to, co zostało ukończone):

- Odczytuje napisane fragmenty powieści.
- PO ocenia: czy produkt spełnia oczekiwania?
- Pozostałe zespoły (stakeholders) mogą zadawać pytania i zgłaszać uwagi.

Metryki do omówienia w ADO:
- Velocity (ile Story Points ukończono?)
- Burndown Chart (Boards → Analytics → Burndown)
- Ile PBI zostało w backlogu?

---

### Część 2D – Retrospektywa (15 minut)

Scrum Master prowadzi retrospektywę metodą **„Start / Stop / Continue"**:

| Kategoria | Pytanie | Przykłady odpowiedzi |
|---|---|---|
| **Start** | Co powinniśmy zacząć robić? | „Ustalać Definition of Done przed sprintem" |
| **Stop** | Co powinniśmy przestać robić? | „Zmieniać PBI w trakcie sprintu" |
| **Continue** | Co działa i powinniśmy kontynuować? | „Codzienne aktualizowanie tablicy" |

Wyniki retrospektywy wpisywane są jako **Wiki** w ADO (Overview → Wiki → Create page).

---

### Część 2E – Podsumowanie i dyskusja (35 minut)

#### Omówienie kluczowych lekcji (20 min)

**1. Dlaczego backlog jest ważniejszy niż plan Gantta?**
- Plan Gantta zakłada stałe wymagania → w IT wymagania zmieniają się co sprint.
- Backlog jest żywy: można dodawać, usuwać, zmieniać priorytety bez przepisywania całego harmonogramu.

**2. Rola Product Ownera jako pomostu biznes–technika**
- PO nie musi programować, musi rozumieć wartość biznesową.
- Priorytetyzacja backlogu = strategiczna decyzja biznesowa.
- Analogia BIM: BIM Manager jako PO – łączy architekturę, konstrukcję i instalacje.

**3. Definition of Done – dlaczego „skończone" musi być zdefiniowane?**
- Bez DoD każdy ma inne rozumienie „gotowe".
- DoD eliminuje dług techniczny (w powieści: niespójności, błędy, braki).

**4. Velocity i planowanie capacity**
- Velocity = ile pracy (SP) zespół realnie wykonuje w jednym sprincie.
- Podstawa realistycznego planowania kolejnych sprintów.

**5. Jira vs Azure DevOps – porównanie bezpłatnych planów**

| Cecha | Azure DevOps Free | Jira Free |
|---|---|---|
| Użytkownicy | 5 | 10 |
| Projekty | Nieograniczone | Nieograniczone |
| Repozytoria Git | Nieograniczone | Nieograniczone |
| Scrum boards | Tak | Tak |
| Kanban boards | Tak | Tak |
| Raporty / Analytics | Podstawowe | Podstawowe |
| CI/CD | 1800 min/miesiąc | Nie (Jira Software tylko) |
| Integracja z Microsoft 365 | Natywna | Przez plugin |
| Rekomendacja dla | Środowisk Microsoft, BIM | Startupów, firm zwinnych |

#### Pytania do dyskusji (15 min)

1. Jak metodyki Agile mogą zastosować się do projektu BIM? Co byłby backlogiem? Co sprintem?
2. Jaką rolę najchętniej wybralibyście w prawdziwym projekcie IT i dlaczego?
3. Co było największym wyzwaniem podczas pracy zespołowej dziś?
4. Jakie narzędzie (ADO / Jira) wydaje się bardziej intuicyjne i dlaczego?

---

## Harmonogram zajęć – widok godzinowy

### Blok 1 (120 min)

| Czas | Aktywność | Forma |
|---|---|---|
| 0:00 – 0:10 | Wprowadzenie – specyfika projektów IT | Wykład |
| 0:10 – 0:35 | Metodyki: Waterfall, Agile, Scrum, Kanban | Wykład + dyskusja |
| 0:35 – 0:50 | Role w projekcie IT | Wykład + ćwiczenie: przypisz rolę do scenariusza |
| 0:50 – 1:00 | Narzędzia: ADO vs Jira, omówienie planów | Wykład |
| 1:00 – 1:05 | Podział na zespoły, losowanie gatunku powieści | Organizacyjne |
| 1:05 – 1:20 | Zakładanie kont i organizacji w Azure DevOps | Laboratorium |
| 1:20 – 1:40 | Konfiguracja projektu, backlogu i sprintu | Laboratorium |
| 1:40 – 2:00 | Sprint Planning – PBI + szacowanie Story Points | Warsztat |

### Blok 2 (120 min)

| Czas | Aktywność | Forma |
|---|---|---|
| 0:00 – 0:45 | Sprint – praca w zespołach nad powieścią z AI | Laboratorium |
| 0:45 – 0:55 | Daily Scrum (symulacja) | Warsztat |
| 0:55 – 1:10 | Sprint Review – prezentacja przyrostów | Prezentacje |
| 1:10 – 1:25 | Retrospektywa – Start/Stop/Continue | Warsztat |
| 1:25 – 1:45 | Omówienie lekcji i kluczowych pojęć | Wykład + dyskusja |
| 1:45 – 2:00 | Pytania, wnioski, zakończenie | Dyskusja |

---

## Materiały i wymagania

### Wymagania sprzętowe i dostępowe

- Sala laboratoryjna z komputerami z dostępem do Internetu.
- Każdy student potrzebuje adresu e-mail (najlepiej Microsoft / Outlook).
- Opcjonalnie: smartfony do szybkiego logowania i weryfikacji.

### Zasoby do przygotowania przez prowadzącego

- [ ] Slajdy z teorią (metodyki, role, narzędzia).
- [ ] Kartki z losowaniem gatunków powieści.
- [ ] Wydruk kart Planning Poker (1, 2, 3, 5, 8, 13, ?) lub wersja cyfrowa.
- [ ] Przykładowy backlog w ADO (demo, do pokazania studentom).
- [ ] Lista przykładowych promptów AI dla każdego gatunku.

### Narzędzia używane na zajęciach

| Narzędzie | Link | Plan | Uwagi |
|---|---|---|---|
| Azure DevOps | [dev.azure.com](https://dev.azure.com) | Basic (free) | Max 5 użytkowników/org |
| ChatGPT | [chat.openai.com](https://chat.openai.com) | Free (GPT-4o mini) | Lub Microsoft Copilot |
| Microsoft Copilot | [copilot.microsoft.com](https://copilot.microsoft.com) | Free | Bez logowania |
| Google Docs / Word Online | – | Free | Wspólny dokument powieści |

---

## Słownik pojęć (dla studentów)

| Pojęcie | Definicja |
|---|---|
| **Backlog** | Lista wszystkich wymagań i zadań projektu, posortowana priorytetowo |
| **Sprint** | Krótki, ograniczony czasowo okres pracy (1–4 tygodnie), kończący się działającym przyrostem |
| **User Story** | Wymaganie opisane z perspektywy użytkownika: „Jako [rola] chcę [funkcja] aby [korzyść]" |
| **Story Points** | Względna miara złożoności zadania, nie czasu |
| **Velocity** | Średnia liczba Story Points ukończonych przez zespół w jednym sprincie |
| **Definition of Done** | Uzgodnione kryteria uznania zadania za ukończone |
| **Impediment** | Przeszkoda blokująca postęp pracy |
| **WIP Limit** | Maksymalna liczba zadań „w toku" w danym momencie |
| **Increment** | Działający, gotowy fragment produktu dostarczony po sprincie |
| **Kanban** | Metodyka zarządzania przepływem pracy przez wizualizację na tablicy |

---

## Przykładowe User Stories dla projektu powieści

```
Jako czytelnik kryminału
Chcę poznać tajemnicze tło zbrodni w pierwszym rozdziale
Aby wciągnąć się w fabułę od pierwszych stron.

Acceptance Criteria:
- Scena zawiera opis miejsca zbrodni (min. 200 słów)
- Pojawiają się co najmniej 2 wskazówki dla czytelnika
- Styl jest spójny z gatunkiem (mroczny, napięty)
```

```
Jako czytelnik romansu
Chcę poczuć chemię między głównymi bohaterami w pierwszym spotkaniu
Aby chcieć czytać dalej i kibicować ich związkowi.

Acceptance Criteria:
- Scena pierwszego spotkania liczy min. 300 słów
- Oboje bohaterowie są opisani fizycznie i charakterologicznie
- Pojawia się element napięcia lub komizmu sytuacyjnego
```

---

*Plan zajęć opracowany na potrzeby studiów podyplomowych BIM | Zarządzanie projektami IT | Kwiecień 2026*
