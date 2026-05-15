# Jira – Tworzenie Task dla impedimentu podczas Daily Scrum

> Dokument uzupełniający do `Zadania.md` — zawiera dokładne opisy ekranów i przycisków.  
> Używaj gdy instrukcja w Zadaniach.md jest niewystarczająca lub coś wygląda inaczej.

---

## Co to jest impediment i po co go zapisywać?

**Impediment** (przeszkoda) to cokolwiek, co blokuje lub spowalnia pracę Developera.  
Scrum Master jest odpowiedzialny za ich usuwanie.  
Zapisanie impedimentu w Jira pozwala śledzić co blokowało sprint i jak szybko zostało usunięte.

---

## 1. Tworzenie Task – impediment (krok po kroku)

### 1.1 Otwórz okno tworzenia Issue

1. Upewnij się, że jesteś zalogowany do Jiry i masz otwarty swój projekt

2. Kliknij **„+ Create"** w górnym pasku nawigacyjnym  
   *(niebieski przycisk „Create" lub niebieskie „+" — zależnie od wersji interfejsu)*

3. Otwiera się okno **„Create issue"**

---

### 1.2 Uzupełnij formularz

Wypełnij pola w następującej kolejności:

**Project** *(pole u góry)*  
→ Wybierz swój projekt *(powinien być już zaznaczony automatycznie)*

**Issue type**  
→ Kliknij listę rozwijaną → wybierz **„Task"**  
*(nie „Story", nie „Bug" — „Task")*

**Summary** *(tytuł — pole obowiązkowe)*  
→ Wpisz krótki, konkretny opis impedimentu:

| ✅ Dobry tytuł | ❌ Zły tytuł |
|---|---|
| `IMPEDIMENT: DEV Zofia – brak dostępu do ChatGPT` | `problem` |
| `IMPEDIMENT: Cały zespół – wolny internet w sali` | `coś nie działa` |
| `IMPEDIMENT: DEV Piotr – niejasne kryterium DoD dla Rozdziału 1` | `pytanie` |

**Assignee**  
→ Kliknij pole → z listy wybierz **Scrum Master** *(osoba odpowiedzialna za usunięcie)*

**Labels** *(etykieta — pole może być ukryte)*  
→ Kliknij pole „Labels" *(lub rozwiń sekcję „More fields" jeśli nie widać)*  
→ Wpisz: `impediment` → naciśnij **Enter**  
→ Etykieta pojawia się jako tag

> ⚠️ Jeśli nie widzisz pola „Labels":  
> Kliknij **„Configure fields"** (link na dole formularza) → włącz „Labels" → gotowe.

**Description** *(opis — pole opcjonalne, ale zalecane)*  
→ Wpisz:
- Co dokładnie blokuje pracę?
- Kto zgłosił i kiedy?
- Jakie jest proponowane rozwiązanie?

---

### 1.3 Utwórz Issue

Kliknij niebieski przycisk **„Create"**

> ✅ Task pojawia się w Backlogu z etykietą `impediment`.  
> Numer Issue np. `SPC-15` — zanotuj, żeby szybko do niego wrócić.

---

## 2. Aktualizacja statusu impedimentu po usunięciu

Gdy Scrum Master usuwa przeszkodę:

1. Wejdź do Backloga lub wyszukaj Issue po numerze *(np. `SPC-15`)*

2. Kliknij tytuł → otwiera się panel boczny

3. Zmień status z **„To Do"** na **„In Progress"** gdy pracujesz nad rozwiązaniem

4. Zmień na **„Done"** gdy problem jest rozwiązany

5. Dodaj komentarz z opisem rozwiązania:
   ```
   Rozwiązanie: [co zrobiłeś/-aś].
   Czas rozwiązania: [ile minut].
   ```

---

## 3. Wyszukiwanie impedimentów po etykiecie

Jeśli chcesz zobaczyć wszystkie impedimenty z projektu:

1. W lewym menu kliknij **„Backlog"**

2. Znajdź pasek filtrów u góry widoku

3. Kliknij **„Label"** → wybierz `impediment` z listy

4. Backlog filtruje się do wyłącznie Issues z tą etykietą

> ℹ️ Alternatywnie: skorzystaj z wyszukiwarki Jiry (ikona lupy) → wpisz `label = impediment`

---

## 4. Przykładowe impedimenty i sposoby rozwiązania

| Impediment | Rozwiązanie SM |
|---|---|
| Brak dostępu do ChatGPT | Podaj link do Microsoft Copilot (bez logowania) |
| Wolny internet w sali | Przejdź na hotspot telefoniczny |
| Developer nie rozumie wymagań Story | SM organizuje 2-minutowe spotkanie z PO |
| Konflikt w Google Docs – dwoje edytuje jednocześnie | Podział dokumentu na sekcje z inicjałami autorów |
| Niejasne DoD – co znaczy „spójność postaci"? | SM + PO definiują wspólnie, zapisują w opisie Epica |
| QA nie dostępna – Natalia ma przerę | SM pełni tymczasowo rolę QA dla 1 Story |
