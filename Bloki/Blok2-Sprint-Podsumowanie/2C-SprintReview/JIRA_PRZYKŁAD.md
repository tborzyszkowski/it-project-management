# Jira – Pełny przykład: Sprint Review projektu „Śmierć przychodzi o świcie"

> Dokument pokazuje jak krok po kroku przeprowadzić Sprint Review z użyciem Jiry.  
> Karolina (PO) prezentuje, Marek (SM) przygotowuje dane, reszta obserwuje i komentuje.

---

## Dane projektu (kontynuacja z JIRA_PRZYKŁAD.md w 2A-Sprint)

| Element | Wartość |
|---|---|
| **Projekt** | `Śmierć przychodzi o świcie` (klucz: `SPC`) |
| **Site** | `bim-kryminal.atlassian.net` |
| **Sprint** | Sprint 1 (właśnie zakończony) |

---

## Stan Sprintu 1 po zakończeniu pracy

| ID | Story | SP | Status końcowy |
|---|---|---|---|
| `SPC-5` | Profil komisarz Anny Wolskiej | 2 | ✅ Done |
| `SPC-6` | Profil antagonisty | 3 | ✅ Done |
| `SPC-7` | Rozdział 1 – odkrycie ciała | 5 | ✅ Done |
| `SPC-8` | Opis miejsca akcji – Czerna | 2 | ✅ Done |
| `SPC-9` | Review i korekta Rozdziału 1 | 2 | ❌ Nie ukończone |

**Ukończone SP: 12 z 14 zaplanowanych**

---

## Krok 1 – Marek przygotowuje dane (przed Sprint Review)

**Godzina: 10:45 – tuż po zakończeniu sprintu**

Marek otwiera Jirę i sprawdza dane do prezentacji.

### 1.1 Weryfikacja tablicy

1. Marek klika **„Board"** → widzi:
   - Kolumna **Done**: `SPC-5`, `SPC-6`, `SPC-7`, `SPC-8` ✅
   - Kolumna **In Progress**: (pusta)
   - Kolumna **To Do**: `SPC-9` ← nie ukończone

2. Marek notuje: „4 z 5 Stories w Done, SPC-9 zostaje w Backlogu."

### 1.2 Otwieranie Burndown Chart

1. Marek klika **„Reports"** w lewym menu
2. Wybiera **„Burndown Chart"**
3. Widzi wykres:
   - Linia idealna: płynnie spada od 14 SP do 0 przez 45 minut
   - Linia rzeczywista: dość blisko idealnej, lekki zastój między godziną 10:15 a 10:22 (impediment Piotra + Daily Scrum)
   - Linia nie dochodzi do 0 — 2 SP nie ukończone (SPC-9)

4. Marek robi zdjęcie ekranu lub zostawia otwartą zakładkę

### 1.3 Obliczanie Velocity

Marek klika **„Reports"** → **„Velocity Chart"**:
- Widzi 1 słupek (Sprint 1)
- Szary słupek sięga 14 SP (planowane)
- Zielony słupek sięga 12 SP (ukończone)

**Velocity Sprint 1 = 12 SP**

---

## Krok 2 – Karolina (PO) otwiera Sprint Review

**Godzina: 10:50**

Karolina podchodzi do komputera z projektorem.

### 2.1 Widok Board – prezentacja ukończonych Stories

1. Karolina otwiera **„Board"**
2. Kolumna **Done** widoczna na ekranie – 4 karty
3. Karolina klika `SPC-7` (Rozdział 1) → otwiera panel boczny

   Panel pokazuje:
   ```
   SPC-7 · Story · Done
   Rozdział 1 – odkrycie ciała (min. 300 słów)
   Story Points: 5
   Assignee: Zofia, Piotr
   
   Comments:
   [Zofia] "Rozdział 1 gotowy – 412 słów. Link: docs.google.com/..."
   [Natalia] "QA: ⚠️ Prawie gotowe – akapit 3 za lekki. Zwracam."
   [Zofia] "Poprawiono akapit 3. Gotowe do review."
   [Natalia] "QA: ✅ Approved. Done."
   ```

4. Karolina komentuje:
   > „Widzicie historię pracy – QA zwróciła Story do poprawki, to dobra praktyka. Ostatecznie story spełniła DoD."

5. Karolina otwiera dokument Google Docs i czyta głośno kilka zdań z Rozdziału 1

### 2.2 Prezentacja pozostałych Stories

Karolina podobnie otwiera `SPC-5` (profil komisarz) i `SPC-8` (opis Czernej):
- Każdą krótko komentuje
- Pokazuje komentarze QA lub autorów
- Odczytuje fragment tekstu

---

## Krok 3 – Dyskusja nad niespełnionymi Stories

`SPC-9` (Review i korekta Rozdziału 1) — nie ukończone.

Marek tłumaczy:
> „SPC-9 nie zostało ukończone, bo Natalia skupiła się na review inline w ramach SPC-7. To była dobra decyzja w trakcie sprintu — ale task formalnie nie został zamknięty."

Karolina (PO) decyduje:
> „SPC-9 przenosimy do Backlogu Sprint 2. Ale dostosujemy opis — review rozdziału 2, nie 1."

**Marek aktualizuje w Jira:**

1. Otwiera `SPC-9`
2. Zmienia tytuł na: `Review i korekta Rozdziału 2`
3. Dodaje komentarz:
   ```
   Sprint 1: Story nie ukończona – review odbyło się inline w SPC-7. 
   Przenoszona do Sprint 2 z nowym zakresem (Rozdział 2).
   ```
4. Story pozostaje w Backlogu (poza sprintem)

---

## Krok 4 – Marek prezentuje Burndown Chart

1. Marek klika **„Reports"** → **„Burndown Chart"**
2. Wyświetla na projektorze

**Opis wykresu dla zespołu:**

> „Szara przerywana linia to co byłoby idealnie. Nasza niebieska linia jest blisko — to dobry znak. Widać zastój między 10:15 a 10:32 — to czas impedimentu Piotra i Daily Scrum. Nie dotarliśmy do 0 — zostały 2 SP, czyli SPC-9."

Zofia pyta: „Czy to znaczy, że sprint się nie udał?"

Karolina odpowiada:
> „Nie — 85% planowanych SP w pierwszym sprincie to bardzo dobry wynik. Velocity 12 SP będzie bazą do planowania Sprint 2."

---

## Krok 5 – Karolina zapisuje feedback w Jira

Po przesłuchaniu prezentacji Karolina zbiera feedbak od obserwatorów (wykładowcy, inne zespoły).

**Feedback 1: „Świetny klimat Rozdziału 1 – Beskidy dają ciekawe tło"**

1. Karolina wchodzi do **Backloga** → znajduje Epic `SPC-1` (np. „Napisanie powieści kryminalnej")
2. Klika Epic → otwiera panel
3. W sekcji **„Activity" → „Comments"** klika **„Add a comment"**
4. Wpisuje:
   ```
   Sprint Review: Feedback zewnętrzny ✅
   
   Od: dr Kowalski (wykładowca)
   "Świetny klimat Rozdziału 1. Beskidy to ciekawe i nieoczywiste tło."
   
   Decyzja PO: Zachowujemy lokalizację. Można rozwinąć w kolejnych rozdziałach.
   ```
5. Klika **„Save"**

**Feedback 2: „Warto dodać więcej dialogów"**

Karolina tworzy nową Story:
1. Klika **„+ Create"**
2. Issue type: **Story**
3. Summary: `Wzbogacić Rozdział 1 o 2-3 dialogi między postaciami`
4. Description:
   ```
   Feedback ze Sprint Review (dr Kowalski):
   Aktualny Rozdział 1 jest opisowy. Dialogi zwiększyłyby dynamikę.
   
   DoD: Dodane min. 2 dialogi (po 3–5 wypowiedzi każdy).
   ```
5. Story Points: 2
6. **Nie przypisuje do sprintu** — zostaje w Backlogu
7. Klika **„Create"**

> ✅ Nowa Story pojawia się w Backlogu jako `SPC-10`. PO nada jej priorytet przed Sprint 2.

---

## Podsumowanie Sprint Review w Jira

| Akcja | Kto | Gdzie w Jira |
|---|---|---|
| Pokazanie Done Stories | Karolina (PO) | Board → kolumna Done |
| Prezentacja Burndown | Marek (SM) | Reports → Burndown Chart |
| Odczytanie Velocity | Marek (SM) | Reports → Velocity Chart |
| Zapisanie feedbacku | Karolina (PO) | Epic → Comments |
| Nowe wymaganie do Backlogu | Karolina (PO) | + Create → Story → Backlog |
| Aktualizacja nieskończonej Story | Marek (SM) | SPC-9 → zmiana tytułu + komentarz |
