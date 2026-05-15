# Jira – Szczegółowe kroki podczas Sprintu

> Dokument uzupełniający do `Zadania.md` — zawiera dokładne opisy ekranów i przycisków.  
> Używaj go gdy instrukcja w Zadaniach.md jest niewystarczająca lub coś wygląda inaczej.

---

## 1. Uruchomienie Sprintu

### 1.1 Start Sprintu – widok Backlog

1. W lewym menu kliknij **„Backlog"**

2. Znajdź sekcję **„Sprint 1"** — powinna być widoczna powyżej sekcji „Backlog"

3. Upewnij się, że Sprint 1 zawiera co najmniej kilka Stories z przypisanymi Story Points

4. Kliknij niebieski przycisk **„Start sprint"** widoczny w nagłówku sekcji Sprint 1

5. Pojawi się okno potwierdzające daty:
   - **Sprint name**: `Sprint 1`
   - **Duration**: możesz zostawić domyślne lub ustawić ręcznie
   - **Start date** / **End date**: sprawdź, czy są poprawne
   - Kliknij **„Start"**

6. Jira automatycznie przełącza widok do tablicy **Board**

> ✅ Widzisz tablicę z kolumnami: **To Do | In Progress | Done**

> ⚠️ Jeśli przycisk „Start sprint" jest nieaktywny — upewnij się, że Sprint 1 zawiera przynajmniej **1 Story z Story Points**.

---

### 1.2 Przełączanie między widokami Jiry

| Widok | Lokalizacja w lewym menu | Kiedy używać |
|---|---|---|
| **Board** | „Board" | Praca podczas sprintu — przeciąganie zadań |
| **Backlog** | „Backlog" | Planowanie, wgląd w Sprint Backlog |
| **Reports** | „Reports" | Sprawdzanie Burndown Chart, Velocity |
| **Roadmap** | „Roadmap" / „Timeline" | Widok Epiców na osi czasu |

---

## 2. Praca na tablicy (Board)

### 2.1 Przeciąganie Task / Story między kolumnami

1. W lewym menu kliknij **„Board"**

2. Znajdź swoją Story lub Task w kolumnie **„To Do"**

3. Kliknij kartę i **przytrzymaj** → przeciągnij do kolumny **„In Progress"**

4. **Puść** — karta zmienia kolumnę, status aktualizuje się automatycznie

> ℹ️ Jeśli przeciąganie nie działa — sprawdź, czy masz uprawnienia **Member** (nie Viewer):  
> Project settings → Access → odszukaj swoje konto.

### 2.2 Zmiana statusu bez przeciągania (alternatywnie)

1. Kliknij tytuł Story/Task na tablicy — otwiera się panel boczny

2. U góry panelu znajduje się przycisk ze statusem *(np. „To Do")*

3. Kliknij ten przycisk → z listy wybierz nowy status: **„In Progress"** lub **„Done"**

4. Karta automatycznie wędruje do właściwej kolumny

### 2.3 Otwieranie i edytowanie Story/Task

Kliknij tytuł karty na tablicy, by otworzyć panel boczny z detalami:

| Pole / Akcja | Lokalizacja w panelu | Co zrobić |
|---|---|---|
| Zmiana statusu | Przycisk u góry *(np. „To Do")* | Kliknij → wybierz status z listy |
| Dodanie komentarza | Sekcja „Activity" → zakładka „Comments" | Kliknij „Add a comment" → wpisz → „Save" |
| Zmiana Assignee | Prawy panel → „Assignee" | Kliknij → wybierz osobę z listy |
| Story Points | Prawy panel → „Story point estimate" | Kliknij → wpisz liczbę → Enter |
| Edycja opisu | Sekcja „Description" | Kliknij tekst → edytuj → zapisz |
| Otwórz pełny widok | Ikona „↗" obok tytułu | Kliknij — otwiera osobną stronę Issue |

---

## 3. Tworzenie Task – impediment

Jeśli coś blokuje pracę zespołu, Scrum Master tworzy Task z etykietą `impediment`.

1. Kliknij **„+ Create"** w górnym pasku nawigacyjnym *(niebieskie „+" lub przycisk „Create")*

2. W oknie tworzenia Issue ustaw:

   | Pole | Wartość |
   |---|---|
   | **Project** | Twój projekt *(powinien być wybrany automatycznie)* |
   | **Issue type** | **Task** |
   | **Summary** | Krótki opis problemu, np. `"DEV: brak dostępu do narzędzi AI"` |
   | **Assignee** | Scrum Master |

3. Dodaj etykietę `impediment`:
   - W oknie tworzenia kliknij **„Labels"** *(lub znajdź pole Labels w formularzu)*
   - Wpisz: `impediment` → naciśnij **Enter**

4. Opcjonalnie — w polu **„Description"** opisz: co blokuje, kto zgłosił, kiedy

5. Kliknij **„Create"**

> ✅ Task pojawia się w Backlogu z etykietą `impediment`.

> ⚠️ Jeśli nie widzisz pola „Labels" — kliknij **„Configure fields"** w oknie tworzenia i włącz pole „Labels".

---

## 4. Dodawanie komentarza do Story/Task

Po ukończeniu pracy Developer dodaje komentarz informujący QA.

1. Na tablicy Board kliknij tytuł swojej Story/Task

2. W panelu bocznym przewiń do sekcji **„Activity"**

3. Kliknij zakładkę **„Comments"** → **„Add a comment"**

4. Wpisz komentarz (obsługiwany jest Markdown: `**pogrubienie**`, listy `-`)

5. Kliknij **„Save"**

**Gotowe komentarze do skopiowania:**

```
Tekst gotowy – wklejony do dokumentu Google Docs. Czeka na review QA.
```

```
QA: DoD spełnione ✅ Tekst ma [X] słów, imiona spójne, styl odpowiada gatunkowi. Zatwierdzam → Done.
```

```
QA: ❌ Tekst ma [X] słów (wymagane 300). Proszę uzupełnić przed zamknięciem → zwracam do In Progress.
```

---

## 5. Sprawdzanie postępu sprintu

### 5.1 Burndown Chart

1. W lewym menu kliknij **„Reports"**

2. Z listy raportów wybierz **„Burndown Chart"**

3. Upewnij się, że w górnym menu dropdown wybrany jest właściwy sprint *(Sprint 1)*

4. Odczytaj wykres:

| Element wykresu | Znaczenie |
|---|---|
| **Linia szara / przerywana** | Idealny postęp (liniowy spadek do zera) |
| **Linia niebieska / ciągła** | Rzeczywisty postęp zespołu |
| Linia spada szybciej niż idealna | Zespół pracuje szybciej niż planowano 🚀 |
| Linia powyżej idealnej | Ryzyko nieukończenia sprintu ⚠️ |
| Płaski odcinek | Brak postępu – prawdopodobny impediment |

### 5.2 Velocity Chart

1. W lewym menu kliknij **„Reports"**

2. Wybierz **„Velocity Chart"**

3. Wykres pokazuje Story Points z poprzednich sprintów  
   *(Na pierwszym sprincie pojawia się tylko 1 słupek — to normalne)*

4. Odczytaj: **ile Story Points zostało ukończonych** w Sprint 1

---

## 6. Częste problemy i rozwiązania

| Problem | Możliwa przyczyna | Rozwiązanie |
|---|---|---|
| Nie widzę Board | Sprint nie jest wystartowany | Backlog → „Start sprint" |
| Nie mogę przeciągać kart | Rola Viewer (brak uprawnień) | Project settings → Access → zmień rolę na Member |
| Nie widzę cudzych zadań | Nie jesteś w projekcie | Sprawdź e-mail z zaproszeniem (też folder SPAM) |
| Reports jest puste | Sprint nie jest aktywny | Backlog → „Start sprint" |
| Brak pola Labels | Pole ukryte w formularzu | Create → „Configure fields" → włącz „Labels" |
| Story nie ma Story Points | Nie ustawiono podczas planowania | Otwórz Story → „Story point estimate" → wpisz |
| Board nie pokazuje wszystkich kart | Widok filtrowany | Sprawdź filtry w górnym pasku Board (usuń wszystkie) |
