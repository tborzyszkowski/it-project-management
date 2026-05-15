# Jira – Zapisanie wyników Retrospektywy jako Task

> Dokument uzupełniający do `Zadania.md` — zawiera dokładne opisy ekranów i przycisków.  
> Używaj gdy instrukcja w Zadaniach.md jest niewystarczająca lub coś wygląda inaczej.

---

## Po co zapisywać Retrospektywę w Jira?

Task z wynikami Retrospektywy to **archiwum procesu** — nie element pracy do wykonania.  
Dzięki niemu można po zakończeniu kursu sprawdzić co zmieniało się między sprintami.  
Task nie musi mieć przypisanego sprintu ani Story Points.

---

## 1. Tworzenie Task – wyniki Retrospektywy (krok po kroku)

### 1.1 Otwórz okno tworzenia Issue

1. Upewnij się, że jesteś zalogowany do Jiry i masz otwarty swój projekt

2. Kliknij **„+ Create"** w górnym pasku nawigacyjnym

3. Otwiera się okno **„Create issue"**

---

### 1.2 Uzupełnij pola formularza

**Issue type**  
→ Kliknij listę → wybierz **„Task"**

**Summary** *(tytuł)*  
→ Wpisz dokładnie:
```
Retrospektywa Sprint 1
```

**Labels** *(etykieta — pole może być ukryte)*  
→ Kliknij pole „Labels" *(lub „More fields")*  
→ Wpisz: `retrospektywa` → naciśnij **Enter**

> ⚠️ Jeśli nie widzisz pola „Labels":  
> Kliknij **„Configure fields"** na dole formularza → włącz „Labels"

**Description** *(najważniejsze pole)*  
→ Skopiuj szablon poniżej i uzupełnij po retrospektywie:

```markdown
# Retrospektywa Sprint 1

**Data:** [data zajęć]
**Zespół:** [imiona uczestników]
**Gatunek powieści:** [wybrany gatunek]

## Start (co zaczynamy w Sprint 2)
- [odpowiedź 1]
- [odpowiedź 2]

## Stop (co kończymy)
- [odpowiedź 1]
- [odpowiedź 2]

## Continue (co kontynuujemy)
- [odpowiedź 1]
- [odpowiedź 2]

## Action Item – co wdrażamy w Sprint 2
**[Wybrany Action Item — ten z największą liczbą głosów]**
Osoba odpowiedzialna: [imię]
```

> 💡 Formatowanie markdown działa w opisie Jiry — nagłówki, listy i pogrubienia będą widoczne po zapisaniu.

**Story Points** *(nie ustawiaj)*  
→ Pozostaw puste — to nie jest task do wyceny

**Assignee**  
→ Przypisz do **Scrum Master** *(jako autor wpisu)*

**Sprint**  
→ **Nie przypisuj do sprintu** — Task jest archiwem, nie zadaniem

---

### 1.3 Zapisz Task

Kliknij niebieski przycisk **„Create"**

> ✅ Task pojawia się w Backlogu z tytułem „Retrospektywa Sprint 1".  
> Numer Issues: np. `SPC-12`.

---

## 2. Edytowanie Taska jeśli popełnisz błąd

1. W lewym menu kliknij **„Backlog"**

2. Znajdź Task „Retrospektywa Sprint 1" *(lub wyszukaj po numerze)*

3. Kliknij tytuł → otwiera się panel boczny lub pełna strona Issue

4. Kliknij dowolne pole *(tytuł, opis, etykieta)* → możesz je edytować bezpośrednio

5. Zmiany zapisują się automatycznie po kliknięciu poza pole

---

## 3. Statusy Taska Retrospektywy

| Status | Kiedy ustawić |
|---|---|
| **To Do** | Task właśnie stworzony, opis jeszcze nie uzupełniony |
| **In Progress** | SM uzupełnia opis podczas Retrospektywy |
| **Done** | Opis kompletny, Retrospektywa zakończona |

> ℹ️ Możesz zmienić status klikając przycisk statusu na górze panelu Issue *(np. „To Do ▼")*.

---

## 4. Różnica między Task-impediment a Task-retrospektywa

| Cecha | Task – impediment | Task – retrospektywa |
|---|---|---|
| **Cel** | Śledzenie blokady i jej usunięcia | Archiwum wyników spotkania |
| **Etykieta** | `impediment` | `retrospektywa` |
| **Tworzony przez** | SM podczas Daily Scrum | SM podczas Retrospektywy |
| **Assignee** | SM (usuwa blokadę) | SM (autor wpisu) |
| **Sprint** | Aktywny sprint (opcjonalnie) | Brak sprintu |
| **Story Points** | Brak | Brak |
| **Status Done** | Po usunięciu blokady | Po zakończeniu Retrospektywy |
