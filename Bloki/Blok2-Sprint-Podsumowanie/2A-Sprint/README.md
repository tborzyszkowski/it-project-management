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
| 0:00–0:05 | Start sprintu – SM uruchamia sprint w ADO | Scrum Master |
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
- Uruchamia sprint w ADO
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

## Obsługa ADO podczas sprintu

### Uruchomienie sprintu

1. Boards → Backlogs → Sprint 1
2. Kliknij **„Set dates"** lub po prostu przełącz na widok Sprint Board
3. Przejdź do: **Boards → Boards** (Sprint Board)

### Praca na tablicy

- Kliknij Task → przeciągnij kolumnę `In Progress`
- Po ukończeniu → przeciągnij do `Review`
- QA otwiera PBI → dodaje komentarz → przeciąga do `Done`

### Aktualizacja Remaining Work

- Otwórz Task → w polu **„Remaining Work"** wpisz pozostały czas w godzinach
- Aktualizuj po każdej sesji pracy

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
2. SM tworzy Work Item typu **Impediment** w ADO:
   - Boards → New Work Item → Impediment
   - Opisuje problem i kto jest odpowiedzialny za usunięcie
3. SM próbuje usunąć przeszkodę lub eskaluje do prowadzącego

**Typowe impedimenty na zajęciach:**
- AI nie działa / brak dostępu → Microsoft Copilot bez logowania
- Nie można edytować w ADO → sprawdź uprawnienia w Settings
- Nie ma wspólnego dokumentu → utwórz Google Docs i udostępnij

---

## Metryki do obserwowania podczas sprintu

| Metryka | Gdzie w ADO | Co pokazuje |
|---|---|---|
| **Burndown** | Boards → Analytics → Burndown | Czy praca idzie zgodnie z planem? |
| **Velocity** | Sprint Review (po sprincie) | Ile SP ukończono? |
| **WIP** | Tablica – kolumna In Progress | Czy nie za dużo na raz? |
| **Remaining Work** | Task → Remaining Work | Ile pracy zostało |
