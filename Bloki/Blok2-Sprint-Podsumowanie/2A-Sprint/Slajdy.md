---
marp: true
theme: default
paginate: true
header: "Zarządzanie projektami IT | Studia podyplomowe BIM"
footer: "© 2026 | Blok 2A – Sprint"
style: |
  section {
    font-size: 1.05em;
  }
  h1 {
    color: #0078d4;
  }
  h2 {
    color: #107c10;
  }
  pre {
    background: #1e1e1e;
    color: #d4d4d4;
    font-size: 0.85em;
  }
  .timer {
    font-size: 2em;
    font-weight: bold;
    color: #d83b01;
  }
---

# Blok 2A – Sprint!

## 45 minut aktywnej pracy

**Boards → Sprint 1 Board**
`To Do | In Progress | Review | Done`

---

# Zasady sprintu

## Co robimy teraz?

1. **Developer**: bierze Task → `In Progress` → pisze z AI → redaguje
2. **QA**: sprawdza ukończone PBI wg DoD → zatwierdza lub odsyła
3. **PO**: dostępny na pytania, **nie zmienia PBI!**
4. **SM**: usuwa przeszkody, pilnuje WIP Limit, moderuje tablicę

---

# Workflow – krok po kroku

```
Sprint Backlog (To Do)
       │
       ▼  Developer bierze Task
  In Progress
       │  pisze prompt → generuje AI → redaguje → wkleja
       ▼
    Review
       │  QA sprawdza DoD
       ├── ✅ DoD OK → Done
       └── ❌ Brak → z powrotem In Progress + komentarz
```

---

# Jak pisać z AI?

## Szablon dobrego promptu

```
Jesteś autorem [GATUNEK] pisanym po polsku.

Bohaterowie: [IMIONA I KRÓTKI OPIS]
Miejsce: [OPIS]
Fabuła dotąd: [CO JUŻ SIĘ WYDARZYŁO]

Zadanie: Napisz [CO KONKRETNIE].
Styl: [MROCZ NY / ROMANTYCZNY / SZYBKI].
Długość: min. [ILE] słów.
```

> AI = narzędzie (jak Copilot dla programistów). **Ty** jesteś autorem!

---

# Przykładowy prompt – Kryminał

```
Jesteś autorem kryminału pisanym po polsku.
Styl: Agatha Christie, atmosferyczny.

Bohater: Komisarz Marek Starski, 48 lat, cyniczny.
Miejsce: Opuszczona willa, późna jesień, wieczór.

Zadanie: Napisz opis miejsca zbrodni – szczegółowy,
z detalami sensorycznymi (zapach, zimno, cisza).
Długość: min. 200 słów.
Dodaj jedną wskazówkę dla czytelnika.
```

---

# Przykładowy prompt – Horror

```
Jesteś autorem horroru psychologicznego pisanym po polsku.

Bohaterka: Anna, 32 lata, architektka, racjonalistka.
Miejsce: Stary dworek na Mazurach, noc.

Zadanie: Napisz scenę, w której Anna słyszy coś
niemożliwego po raz pierwszy.
Styl: Narastające napięcie, unikaj dosłowności.
Długość: min. 250 słów.
Zakończ na decyzji bohaterki.
```

---

# Przykładowy prompt – Romans

```
Jesteś autorem romansu współczesnego pisanym po polsku.

Bohaterowie:
- Zofia (30 lat, weterynarka, niezależna)
- Piotr (35 lat, kucharz, charyzmatyczny)

Miejsce: Targ na Kazimierzu w Krakowie, lato.

Zadanie: Napisz scenę pierwszego spotkania.
Styl: Lekki, ciepły, z dialogiem i humorem.
Długość: min. 300 słów.
```

---

# QA – Definition of Done Checklist

## Sprawdź każde PBI przed zatwierdzeniem

```
[ ] Tekst liczy min. 300 słów
[ ] Imiona postaci spójne z profilem
[ ] Styl odpowiada gatunkowi
[ ] Tekst wklejony do dokumentu
[ ] Brak oczywistych błędów logicznych
[ ] PBI zaktualizowane w ADO
```

**Zatwierdź** → przeciągnij do `Done`
**Odrzuć** → wróć do `In Progress` + komentarz z opisem problemu

---

# Impedimenty

## Coś blokuje pracę?

1. Powiedz **Scrum Masterowi**
2. SM tworzy: `Boards → New Work Item → Impediment`

## Najczęstsze problemy i rozwiązania

| Problem | Rozwiązanie |
|---|---|
| AI nie działa | Microsoft Copilot (bez logowania) |
| Brak dostępu w ADO | SM sprawdza Settings → Users |
| Brak wspólnego dokumentu | SM tworzy Google Docs |
| Nie wiem co pisać | Zapytaj PO o wymagania |

---

# Timer – Daily Scrum za 22 minuty!

## Scrum Master: ustaw timer ⏱️

Po **22 minutach** zatrzymaj pracę  
i przeprowadź **Daily Scrum** → [Blok 2B](../2B-DailyScrum/Slajdy.md)

---

# Metryki sprintu

## Gdzie je znaleźć?

| Metryka | Lokalizacja w ADO |
|---|---|
| **Burndown** | Boards → Analytics → Burndown |
| **Velocity** | Po zakończeniu sprintu |
| **WIP** | Tablica – kolumna In Progress |
| **Remaining Work** | Task → pole Remaining Work |

---

# Po 45 minutach – co powinniście mieć?

## Minimum sukcesu sprintu

- ✅ 2+ PBI w statusie **Done**
- ✅ 1+ rozdziały w dokumencie
- ✅ Profile postaci gotowe
- ✅ ADO zaktualizowane
- ✅ Burndown Chart widoczny

> Następnie: **Sprint Review** → prezentujecie przyrost!
