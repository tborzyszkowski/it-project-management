# Jira – Szczegółowe kroki podczas Sprint Review

> Dokument uzupełniający do `Zadania.md` — zawiera dokładne opisy ekranów i przycisków.  
> Używaj go gdy instrukcja w Zadaniach.md jest niewystarczająca lub coś wygląda inaczej.

---

## 1. Wyświetlenie ukończonych Stories (Board – kolumna Done)

Przed prezentacją Product Owner przygotowuje widok tablicy.

1. W lewym menu kliknij **„Board"**

2. Upewnij się, że widzisz kolumny: **To Do | In Progress | Done**

3. Kolumna **„Done"** pokazuje wszystkie Stories ukończone w aktywnym sprincie

4. Kliknij dowolną kartę w kolumnie Done → otwiera się panel boczny z detalami

5. W panelu możesz pokazać:
   - Tytuł Story i jej opis
   - Historia zmian statusów (sekcja „Activity" → „History")
   - Komentarze QA potwierdzające DoD

> 💡 **Wskazówka dla PO**: przed prezentacją zwiększ zoom przeglądarki (Ctrl + +) do 125–150%, żeby karty były czytelne z daleka.

---

## 2. Zliczenie ukończonych Story Points (Backlog)

Scrum Master sumuje Story Points ukończonych Stories, żeby obliczyć Velocity.

1. W lewym menu kliknij **„Backlog"**

2. Na górze widoku wybierz zakładkę **„Sprint 1"** *(jeśli sprint jest jeszcze aktywny, Stories są w sekcji Sprint)*

3. Znajdź wszystkie Stories ze statusem **„Done"** *(oznaczone zielonym paskiem lub checkmarkiem)*

4. Odczytaj ich Story Points *(liczba w prawym rogu każdej karty Story)*

5. Zsumuj — to jest **Velocity Sprint 1**

> ✅ Alternatywnie: skorzystaj z raportu Velocity Chart (patrz punkt 4).

---

## 3. Burndown Chart – jak go odczytać i pokazać

### 3.1 Nawigacja do Burndown Chart

1. W lewym menu kliknij **„Reports"**

2. Z listy dostępnych raportów wybierz **„Burndown Chart"**

3. Upewnij się, że w górnym menu dropdown wybrany jest właściwy sprint:  
   *(np. „Sprint 1 – Śmierć przychodzi o świcie")*

4. Wykres ładuje się automatycznie

### 3.2 Co pokazuje Burndown Chart?

| Element | Co oznacza |
|---|---|
| **Oś X** | Czas (dni / godziny sprintu) |
| **Oś Y** | Pozostałe Story Points do ukończenia |
| **Linia szara / przerywana** | Idealny postęp — liniowy spadek od sumy SP do zera |
| **Linia niebieska / kolorowa** | Rzeczywisty postęp zespołu |

### 3.3 Interpretacja kształtu wykresu

| Kształt linii rzeczywistej | Interpretacja |
|---|---|
| Przebiega poniżej idealnej | Zespół pracuje szybciej niż planowano 🚀 |
| Przebiega powyżej idealnej | Ryzyko nieukończenia sprintu ⚠️ |
| Płaski odcinek | Brak postępu w tym czasie (impedimenty, przerwy) |
| Gwałtowny spadek na końcu | Praca „na ostatnią chwilę" |
| Linia nie dochodzi do zera | Nie wszystkie SP zostały ukończone |

### 3.4 Pytania do dyskusji przy wykresie

- Czy linia rzeczywista biegła zgodnie z idealną?
- W którym momencie pojawił się „zastój" – co go spowodowało?
- Co zrobilibyśmy inaczej, żeby wykres był bardziej liniowy?

---

## 4. Velocity Chart – gdzie go znaleźć

1. W lewym menu kliknij **„Reports"**

2. Wybierz **„Velocity Chart"** z listy raportów

3. Wykres pokazuje słupki dla każdego sprintu:
   - **Szary słupek**: Story Points zaplanowane (w Sprint Backlogu)
   - **Zielony / niebieski słupek**: Story Points ukończone

4. Na pierwszym sprincie widoczny jest tylko **1 słupek** — to normalne

5. Odczytaj: **Velocity = wysokość zielonego słupka**

> ℹ️ Velocity jest podstawą do planowania pojemności Sprint 2:  
> Jeśli Sprint 1 Velocity = 12 SP, to Sprint 2 planujemy też na ok. 12 SP.

---

## 5. Dodanie feedbacku stakeholderów do Jiry

Po wysłuchaniu prezentacji każdego zespołu, Product Owner może zapisać feedback w Jira.

### 5.1 Jako komentarz do Epica

1. W lewym menu kliknij **„Backlog"** lub **„Roadmap"**

2. Znajdź główny Epic *(np. „Napisanie powieści")*

3. Kliknij tytuł Epica → otwiera się panel lub pełna strona Issue

4. Przewiń do sekcji **„Activity"** → zakładka **„Comments"**

5. Kliknij **„Add a comment"** → wpisz feedback → **„Save"**

### 5.2 Jako nowa Story w Backlogu (nowe wymaganie)

Jeśli feedback stakeholdera to nowe wymaganie:

1. Kliknij **„+ Create"**
2. Issue type: **Story**
3. Tytuł: np. `„Dodać epilog z perspektywy innego bohatera"` *(sugestia ze Sprint Review)*
4. Opis: kto zaproponował, podczas jakiego Review
5. Pozostaw w Backlogu *(nie przypisuj do sprintu)*
6. PO ustali priorytet przy Sprint Planning 2

---

## 6. Częste problemy podczas Sprint Review

| Problem | Możliwa przyczyna | Rozwiązanie |
|---|---|---|
| Board jest pusty | Sprint się zakończył (auto-zamknięcie) | Reports → Velocity Chart — dane są zachowane |
| Burndown Chart nie ładuje się | Sprint nie był aktywny lub brak danych | Sprawdź, czy sprint był wystartowany przed pracą |
| Story widoczna w Done, ale nie zalicza SP | Story nie miała Story Points | Otwórz Story → dodaj Story Points → wykres się odświeży |
| Nie mogę otworzyć Epica | Nie masz dostępu do projektu | Project settings → Access — sprawdź uprawnienia |
