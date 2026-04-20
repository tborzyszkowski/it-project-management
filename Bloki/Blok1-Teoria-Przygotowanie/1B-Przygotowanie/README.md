# Część 1B – Przygotowanie do pracy

> Czas: **60 minut** | Forma: laboratorium + warsztat  
> Zadania: [Zadania.md](./Zadania.md) | Slajdy: [Slajdy.md](./Slajdy.md)

---

## Cel dydaktyczny

Student zakłada konto w Azure DevOps, konfiguruje projekt Scrum,  
tworzy backlog dla projektu „Powieść pisana z AI" i przeprowadza Sprint Planning.

---

## Harmonogram

| Czas | Aktywność | Kto | Czas trwania |
|---|---|---|---|
| 1:00–1:05 | Podział na zespoły, losowanie gatunków | Wykładowca | 5 min |
| 1:05–1:20 | Zakładanie kont ADO, tworzenie organizacji | Scrum Master | 15 min |
| 1:20–1:40 | Konfiguracja projektu, backlogu i sprintu | Scrum Master + zespół | 20 min |
| 1:40–2:00 | Sprint Planning – PBI, szacowanie SP | PO + SM + Dev | 20 min |

---

## Krok 1 – Podział na zespoły (5 min)

**Rozmiar zespołów:** 4–5 osób

**Przypisanie ról:**

| Rola | Ile osób | Zadanie teraz |
|---|---|---|
| Product Owner | 1 | Zakłada wizję produktu, prowadzi Sprint Planning |
| Scrum Master | 1 | Zakłada konto ADO, zaprasza zespół, facylituje |
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

## Krok 2 – Zakładanie kont Azure DevOps (15 min)

Szczegółowe kroki: [Zadania.md – Krok 2](./Zadania.md#krok-2)

**Scrum Master:**
1. Zakłada konto na [dev.azure.com](https://dev.azure.com)
2. Tworzy organizację `bim-[nazwazespolu]`
3. Zaprasza pozostałych członków przez Settings → Users

**Pozostali członkowie:**
1. Otrzymują e-mail z zaproszeniem
2. Logują się do organizacji
3. Potwierdzają uczestnictwo

**Najczęstsze problemy:**
- Brak konta Microsoft → konto Outlook.com (1 min do założenia)
- Nie przychodzi e-mail z zaproszeniem → sprawdź spam / wyślij ponownie
- Zły region → usuń organizację i załóż ponownie (West Europe)

---

## Krok 3 – Konfiguracja projektu w ADO (20 min)

Szczegółowe kroki: [Zadania.md – Krok 3](./Zadania.md#krok-3)

**Wynik na końcu kroku 3:**
- ✅ Projekt Scrum utworzony (nazwa = tytuł powieści)
- ✅ Sprint 1 skonfigurowany (daty = dzisiejsze zajęcia)
- ✅ Hierarchia backlogu widoczna (Epic → Feature → PBI → Task)
- ✅ Wszyscy członkowie mają dostęp do projektu

---

## Krok 4 – Sprint Planning (20 min)

Szczegółowe kroki: [Zadania.md – Krok 4](./Zadania.md#krok-4)

**Product Owner:**
- Tworzy minimum **6 PBI** w backlogu
- Opisuje każde PBI (tytuł + opis + kryteria akceptacji)
- Ustawia priorytety (kolejność w backlogu)

**Scrum Master:**
- Facylituje sesję szacowania (Planning Poker uproszczony)
- Pyta o impedimenty
- Monitoruje pojemność sprintu

**Developerzy:**
- Szacują każde PBI w Story Points: **1 / 2 / 3 / 5 / 8**
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
☐ PBI zaktualizowane w ADO (status = Done)
```

DoD jest zapisywane w ADO Wiki lub jako komentarz do sprintu.

---

## Wskazówki dla prowadzącego

- Krąż po sali podczas konfiguracji ADO – najczęstszy problem to zaproszenia.
- Zachęcaj zespoły do ustalenia **tytułu powieści** – to angażuje grupę.
- Sprint Planning może się przeciągać – pilnuj czasu, ale nie skracaj na siłę.
- Jeśli ktoś nie ma konta Microsoft – może obserwować u kolegi lub założyć konto Outlook na miejscu.
- Sprawdź przed zajęciami, czy ADO działa (status: [status.dev.azure.com](https://status.dev.azure.com)).
