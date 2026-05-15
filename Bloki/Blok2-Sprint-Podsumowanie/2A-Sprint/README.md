# Część 2A – Sprint

> Czas: **45 minut** | Forma: laboratorium (praca zespołowa)  
> Zadania: [Zadania.md](./Zadania.md) | Slajdy: [Slajdy.md](./Slajdy.md)

---

## Cel dydaktyczny

Studenci doświadczają realistycznego sprintu scrumowego:  
biorą zadania z tablicy, pracują z AI, aktualizują statusy, weryfikują DoD.

---

## Przebieg sprintu

| Czas | Etap | Kto |
|---|---|---|
| 0:00–0:05 | Start sprintu – SM uruchamia sprint w Jira | Scrum Master |
| 0:05–0:22 | Praca – Developer bierze taski, pisze z AI | Developerzy |
| 0:22–0:30 | Daily Scrum (przejście do [2B](../2B-DailyScrum/README.md)) | Scrum Master |
| 0:30–0:45 | Kontynuacja pracy + QA review | Developerzy + QA |

---

## Workflow sprintu

```
SPRINT BACKLOG
      │
      ▼
[To Do] ──► [In Progress] ──► [Review] ──► [Done]
                 │                 │
            Developer           QA/PO
            pisze z AI        sprawdza DoD
```

---

## Role podczas sprintu

### Product Owner
- Dostępny dla pytań o wymagania
- Nie zmienia PBI w trakcie sprintu
- Śledzi postęp na tablicy

### Scrum Master
- Uruchamia sprint w Jira
- Usuwa przeszkody (impedimenty)
- Pilnuje WIP Limit (max 2 zadania In Progress na osobę)
- O 22. minucie: przerywa sprint na Daily Scrum

### Developer
- Bierze jeden Task naraz → In Progress
- Pisze prompt → generuje AI → redaguje → wkleja do dokumentu
- Po ukończeniu → Review, powiadamia QA

### QA
- Sprawdza DoD dla każdego ukończonego PBI
- Zatwierdza (→ Done) lub odsyła z komentarzem (→ In Progress)

---

## Obsługa Jira podczas sprintu

### Uruchomienie sprintu

1. Przejdź do **Backlog** w lewym menu
2. Kliknij **„Start sprint"** przy sekcji Sprint 1 → potwierdź daty
3. Przejdź do widoku **Board** (lewe menu) – widoczne kolumny: To Do / In Progress / Done

### Praca na tablicy

- Kliknij Story / Task → przeciągnij do kolumny `In Progress`
- Po ukończeniu → przeciągnij do `Review` lub `Done`
- QA otwiera Story → dodaje komentarz → przeciąga do `Done`

### Aktualizacja szacunku

- Otwórz Story/Task → zaktualizuj pole **„Story points"** lub dodaj komentarz z postępem

---

## Narzędzia AI – jak używać?

### Kiedy AI pomaga

- Generowanie tekstu na podstawie opisu
- Tworzenie profili postaci
- Pisanie dialogów
- Opis miejsc i atmosfery

### Kiedy AI nie wystarczy

- Spójność fabuły (AI nie pamięta poprzednich rozdziałów bez kontekstu)
- Unikatowy styl autora
- Decyzje fabularne i wartości artystyczne

### Wskazówka dotycząca promptów

Dobry prompt = **rola + kontekst + ograniczenia + format**

```
Jesteś autorem [gatunek] pisanym po polsku.
Kontekst: [opis dotychczasowej fabuły, imiona postaci, miejsce]
Zadanie: Napisz [co konkretnie], styl [mrocny/romantyczny/szybki].
Ograniczenia: max 300 słów, nie kończ sceny, zostaw napięcie.
```

---

## Impedimenty – jak zgłaszać?

Jeśli coś blokuje pracę:

1. Powiedz Scrum Masterowi
2. SM tworzy nowy **Task** w Jira z etykietą `impediment`:
   - **„+ Create"** → Task, tytuł: opis problemu, etykieta: `impediment`, Assigned To: SM
   - Opisuje problem i kto jest odpowiedzialny za usunięcie
3. SM próbuje usunąć przeszkodę lub eskaluje do prowadzącego

**Typowe impedimenty na zajęciach:**
- AI nie działa / brak dostępu → Microsoft Copilot bez logowania
- Nie można edytować w Jira → SM sprawdza Project settings → Access
- Nie ma wspólnego dokumentu → utwórz Google Docs i udostępnij

---

## Metryki do obserwowania podczas sprintu

| Metryka | Gdzie w Jira | Co pokazuje |
|---|---|---|
| **Burndown** | Reports → Burndown Chart | Czy praca idzie zgodnie z planem? |
| **Velocity** | Reports → Velocity Chart (po sprincie) | Ile SP ukończono? |
| **WIP** | Board – kolumna In Progress | Czy nie za dużo na raz? |
| **Story Points** | Story → pole Story points | Szacunek pracy na elemencie |
