---
marp: true
theme: default
paginate: true
header: "Zarządzanie projektami IT | Studia podyplomowe BIM"
footer: "© 2026 | Blok 1B – Przygotowanie"
style: |
  section {
    font-size: 1.05em;
  }
  h1 {
    color: #0078d4;
  }
  h2 {
    color: #106ebe;
  }
  code {
    background: #f0f6ff;
    border-radius: 4px;
    padding: 2px 6px;
  }
  pre {
    background: #1e1e1e;
    color: #d4d4d4;
  }
---

# Blok 1B – Przygotowanie

## Konfiguracja środowiska i Sprint Planning

**Studia podyplomowe BIM**

---

# Plan Bloku 1B

| Czas | Aktywność |
|---|---|
| 5 min | Podział na zespoły + losowanie gatunków |
| 15 min | Zakładanie kont Azure DevOps |
| 20 min | Konfiguracja projektu i backlogu |
| 20 min | Sprint Planning – PBI + Story Points |

---

# Krok 1 – Twój zespół i projekt

## Podział ról

| Rola | Zadanie teraz |
|---|---|
| **Product Owner** | Wymyśla PBI, prowadzi Sprint Planning |
| **Scrum Master** | Zakłada ADO, zaprasza, facylituje |
| **Developer(zy)** | Szacują PBI, planują swoje Taski |

## Gatunek powieści (losowanie!)

🔍 Kryminał | 👻 Horror | 💕 Romans | 🚀 Sci-fi | 🔫 Thriller

> Zdecydujcie: **tytuł roboczy** i **imię bohatera** *(2 min)*

---

# Krok 2 – Azure DevOps: Rejestracja

## Scrum Master wykonuje, pozostali obserwują

1. Wejdź na: **https://dev.azure.com**
2. Kliknij **„Start free"**
3. Zaloguj się kontem Microsoft (lub załóż Outlook.com)
4. Wpisz nazwę organizacji: `bim-[waszazespolu]`
5. Wybierz region: **West Europe**
6. Kliknij **„Continue"**

---

# Krok 2 – Zapraszanie członków

## Settings → Users → Add users

1. Kliknij ⚙️ → **Organization Settings**
2. W menu: **Users** → **Add users**
3. Wpisz e-maile wszystkich z zespołu
4. Access Level: **Basic**
5. Kliknij **Add**

## Każdy zaproszony:
- Sprawdź e-mail (i **SPAM**!)
- Kliknij link z zaproszenia
- Zaloguj się i potwierdź

---

# Krok 3 – Tworzenie projektu

## + New Project

| Pole | Wartość |
|---|---|
| Project name | *Tytuł waszej powieści* |
| Visibility | **Private** |
| Version control | **Git** |
| Work item process | **Scrum** ⬅️ WAŻNE! |

> Kliknij **„Create"**

---

# Krok 3 – Konfiguracja sprintu

## Boards → Backlogs → ⚙️ Team Configuration → Iterations

1. Kliknij **„+ New iteration"**
2. Nazwa: **Sprint 1**
3. Daty: **dzisiejszy dzień**
4. Kliknij **Save and close**
5. Zaznacz Sprint 1 → **Save**

✅ W Backlogs widoczna zakładka „Sprint 1"

---

# Hierarchia backlogu w ADO (Scrum)

```
Epic  (żółty)
 └── Feature  (fioletowy)
      └── Product Backlog Item  (niebieski) ← szacujemy!
           ├── Task  (żółty jasny)
           └── Bug  (czerwony)
```

| Typ | Przykład |
|---|---|
| Epic | „Napisanie powieści" |
| Feature | „Rozdział 1: Odkrycie zbrodni" |
| PBI | „Opis miejsca zbrodni (min. 200 słów)" |
| Task | „Wygeneruj tekst AI, przeredaguj" |

---

# Krok 3 – Utwórz Epic i Feature

## Product Owner tworzy strukturę w Backlogs

1. **+ New Work Item** → **Epic**
   - Tytuł: `Napisanie powieści [tytuł]`

2. Rozwiń Epica → **+ Add Feature**:
   - `Część I – Wprowadzenie i postacie`
   - `Część II – Akcja i punkt zwrotny`

---

# Krok 4 – Sprint Planning: Tworzenie PBI

## Product Owner tworzy PBI

Minimum **6 PBI** w backlogu:

**Przykład (Kryminał):**
- Opis miejsca zbrodni (≥ 200 słów)
- Profil detektywa (≥ 150 słów)
- Profil ofiary (≥ 100 słów)
- Rozdział 1 – Odkrycie ciała (≥ 300 słów)
- Rozdział 2 – Przesłuchanie (≥ 200 słów)
- Review i korekta Rozdziału 1

---

# Krok 4 – Story Points (Planning Poker)

## Skala szacowania

| SP | Co oznacza | Czas (~) |
|---|---|---|
| 1 | Trivialnie proste | 5 min |
| 2 | Proste | 10 min |
| 3 | Średnie | 15 min |
| 5 | Złożone | 20 min |
| 8 | Bardzo złożone | 30 min |

## Cel sprintu: **12–15 Story Points**

---

# Planning Poker – jak grać?

## Procedura dla każdego PBI

1. PO czyta tytuł i opis PBI
2. Każdy Developer **w tajemnicy** zapisuje ocenę
3. Na sygnał SM – **wszyscy jednocześnie** pokazują kartki
4. Rozbieżność? → krótka dyskusja (max 2 min)
5. SM wpisuje uzgodnioną wartość do ADO

> ✋ Dlaczego tajnie? Bo unikamy **anchoring bias** (wpływu na siebie nawzajem)

---

# Krok 4 – Wypełnianie Sprint Backlog

## Scrum Master + PO przeciągają PBI do Sprint 1

1. Boards → Backlogs → zakładka **Sprint 1**
2. Przeciągnij PBI z Backlogu do Sprint 1
3. Zacznij od **najwyższych priorytetów**
4. Dodawaj PBI aż suma SP = **12–15**

Dla każdego PBI w sprincie:
- **+ Add Task** → wpisz czynność
- Przypisz do konkretnego Developera

---

# Definition of Done – musisz zdefiniować PRZED sprintem!

## Overview → Wiki → „Definition of Done"

```markdown
## Dla rozdziału / sceny:
- [ ] Tekst ≥ 300 słów
- [ ] Imiona spójne w całym tekście
- [ ] Styl spójny z gatunkiem
- [ ] Tekst wklejony do dokumentu
- [ ] PBI = Done w ADO
- [ ] Review przez QA
```

---

# Lista kontrolna – czy jesteście gotowi na Sprint?

- [ ] Organizacja ADO założona, wszyscy mają dostęp
- [ ] Projekt Scrum z właściwą nazwą
- [ ] Sprint 1 skonfigurowany z datami
- [ ] Min. 6 PBI w backlogu z opisami
- [ ] Każde PBI ma Story Points
- [ ] Sprint Backlog: 12–15 SP
- [ ] Każde PBI ma Task przypisany do Developera
- [ ] Definition of Done w Wiki

---

# Gotowi? START SPRINT! 🚀

## Przejdź do: **Boards → Sprint 1 Board**

Kolumny: `To Do | In Progress | Review | Done`

Każdy Developer:
1. Bierze swój Task → przeciąga do **In Progress**
2. Pisze prompt dla AI → generuje tekst → redaguje
3. Po ukończeniu → przeciąga do **Review**
4. QA sprawdza DoD → **Done** lub wraca z komentarzem

> Następnie: [Blok 2A – Sprint](../../Blok2-Sprint-Podsumowanie/2A-Sprint/Slajdy.md)
