# Część 1B – Przygotowanie do pracy

> Czas: **60 minut** | Forma: laboratorium + warsztat  
> Zadania: [Zadania.md](./Zadania.md) | Slajdy: [Slajdy.md](./Slajdy.md)

---

## Cel dydaktyczny

Student zakłada konto w Jira (plan Free), konfiguruje projekt Scrum,  
tworzy backlog dla projektu „Powieść pisana z AI" i przeprowadza Sprint Planning.

---

## Harmonogram

| Czas | Aktywność | Kto | Czas trwania |
|---|---|---|---|
| 1:00–1:05 | Podział na zespoły, losowanie gatunków | Wykładowca | 5 min |
| 1:05–1:20 | Zakładanie kont Jira, tworzenie site i projektu | Scrum Master + wszyscy | 15 min |
| 1:20–1:40 | Konfiguracja projektu, backlogu i sprintu | Scrum Master + zespół | 20 min |
| 1:40–2:00 | Sprint Planning – PBI, szacowanie SP | PO + SM + Dev | 20 min |

---

## Krok 1 – Podział na zespoły (5 min)

**Rozmiar zespołów:** 4–5 osób

**Przypisanie ról:**

| Rola | Ile osób | Zadanie teraz |
|---|---|---|
| Product Owner | 1 | Zakłada wizję produktu, prowadzi Sprint Planning |
| Scrum Master | 1 | Zakłada konto Jira, tworzy site i projekt, zaprasza zespół, ułatwia |
| Developer | 2–3 | Uczestniczy w Sprint Planning, szacuje PBI |

**Losowanie gatunków powieści:**

Każdy zespół losuje kartkę z gatunkiem:
- 🔍 Kryminał
- 👻 Horror
- 💕 Romans
- 🚀 Sci-fi
- 🔫 Thriller

Następnie zespół ustala **tytuł roboczy** i **imię głównego bohatera** (2 min).

---

## Krok 2 – Zakładanie kont Jira (15 min)

Szczegółowe kroki: [Zadania.md – Krok 2](./Zadania.md#krok-2)

**Każdy uczestnik (samodzielnie):**
1. Wchodzi na [atlassian.com/software/jira/free](https://www.atlassian.com/software/jira/free)
2. Klika „Get it free" i rejestruje się dowolnym e-mailem
3. Potwierdza adres 6-cyfrowym kodem z e-maila

**Scrum Master (jako pierwszy):**
1. Po rejestracji tworzy site: `bim-[nazwazespolu].atlassian.net`
2. Wybiera szablon **Scrum** i tworzy projekt (nazwa = tytuł powieści)
3. Zaprasza pozostałych przez Project settings → Access → Add people

**Pozostali członkowie:**
1. Otrzymują e-mail od `no-reply@atlassian.com`
2. Klikają „Join project" i rejestrują własne konto Atlassian
3. Potwierdzają dołączenie do projektu

**Najczęstsze problemy:**
- Nie przychodzi e-mail z zaproszeniem → sprawdź folder SPAM / Oferty
- Strona po rejestracji pyta o dane do subskrypcji → to błędna ścieżka, wróć na link z e-maila
- Ktoś trafił na kreator Azure zamiast Jiry → to inna usługa, wróć do [atlassian.com/software/jira/free](https://www.atlassian.com/software/jira/free)

---

## Krok 3 – Konfiguracja projektu w Jira (20 min)

Szczegółowe kroki: [Zadania.md – Krok 3](./Zadania.md#krok-3)

**Wynik na końcu kroku 3:**
- ✅ Projekt Scrum utworzony (nazwa = tytuł powieści)
- ✅ Sprint 1 skonfigurowany (daty = dzisiejsze zajęcia)
- ✅ Hierarchia backlogu widoczna (Epic → Story → Sub-task)
- ✅ Wszyscy członkowie mają dostęp do projektu

---

## Krok 4 – Sprint Planning (20 min)

Szczegółowe kroki: [Zadania.md – Krok 4](./Zadania.md#krok-4)

**Product Owner:**
- Tworzy minimum **6 Stories** w backlogu
- Opisuje każdą Story (tytuł + opis + kryteria akceptacji)
- Ustawia priorytety (kolejność w backlogu)

**Scrum Master:**
- Facylituje sesję szacowania (Planning Poker uproszczony)
- Pyta o impedimenty
- Monitoruje pojemność sprintu

**Developerzy:**
- Szacują każdą Story w Story Points: **1 / 2 / 3 / 5 / 8**
- Dyskutują przy rozbieżnościach

**Cel:** Sprint Backlog ze Story Points sumującymi się do **12–15 SP**.

---

## Definition of Done – ustalamy przed sprintem!

Każdy zespół przed startem sprintu **musi uzgodnić DoD** dla PBI:

```
Definition of Done dla rozdziału powieści:
☐ Tekst liczy minimum 300 słów
☐ Imiona postaci są spójne z profilem
☐ Tekst przeszedł review przez QA
☐ Tekst jest wklejony do wspólnego dokumentu Google Docs / Word Online
☐ Story zaktualizowana w Jira (status = Done)
```

DoD jest zapisywane w Jira Pages lub jako opis dedykowanej Story `[DoD] Definition of Done`.

---

## Wskazówki dla prowadzącego

- Krąż po sali podczas konfiguracji Jiry – najczęstszy problem to zaproszenia lądujące w SPAM.
- Zachęcaj zespoły do ustalenia **tytułu powieści** – to angażuje grupę.
- Sprint Planning może się przeciągać – pilnuj czasu, ale nie skracaj na siłę.
- Jeśli ktoś ma problem z rejestracją – może obserwować u kolegi lub użyć tego samego konta Atlassian co kolega (każdy ma osobne konto, ale rejestracja trwa ~2 min).
- Sprawdź przed zajęciami, czy Jira działa (status: [status.atlassian.com](https://status.atlassian.com)).
