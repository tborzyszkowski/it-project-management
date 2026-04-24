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
| 15 min | Zakładanie kont Jira |
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

# Krok 2 – Jira: Rejestracja konta

## Każdy uczestnik samodzielnie (Scrum Master zaczyna)

1. Wejdź na: **https://www.atlassian.com/software/jira/free**
2. Kliknij **„Get it free"**
3. Wpisz dowolny e-mail → **„Agree – Sign Up"**
4. Wpisz 6-cyfrowy **kod z e-maila** → ustaw hasło → wpisz imię
5. *(Scrum Master)* Wpisz nazwę site: `bim-[waszazespolu]`
6. Wybierz **„Software development"** → **„Next"**

---

# Krok 2 – Jira: Zapraszanie członków

## Project settings → Access → Add people

1. Lewe menu: **Project settings** → **Access**
2. Kliknij **„Add people"**
3. Wpisz e-maile wszystkich z zespołu
4. Rola: **Member**
5. Kliknij **„Send invites"**

## Każdy zaproszony:
- Sprawdź e-mail od `no-reply@atlassian.com` (i **SPAM**!)
- Kliknij **„Join project"**
- Utwórz konto Atlassian lub zaloguj się

---

# Krok 3 – Jira: Tworzenie projektu

## Get it free → Scrum → Team-managed

| Pole | Wartość |
|---|---|
| Site name | `bim-[waszazespolu]` |
| Template | **Scrum** ⬅️ WAŻNE! |
| Project type | **Team-managed** |
| Project name | *Tytuł waszej powieści* |

> Kliknij **„Create project"**

---

# Krok 3 – Jira: Konfiguracja sprintu

## Backlog → Create sprint → Edit sprint

1. Lewe menu: **Backlog**
2. Kliknij **„Create sprint"**
3. Kliknij **„···"** → **„Edit sprint"**
4. Nazwa: **Sprint 1**, daty: **dzisiejszy dzień**
5. Kliknij **„Update"**

✅ W Backlogu widoczna sekcja „Sprint 1"

---

# Hierarchia elementów w Jira Scrum

```
Epic  (fioletowy)
 └── Story  (zielony) ← szacujemy! (= PBI)
      └── Sub-task  (niebieski)
 └── Bug  (czerwony)
```

| Typ | Przykład |
|---|---|
| Epic | „Napisanie powieści" |
| Story | „Opis miejsca zbrodni (min. 200 słów)" |
| Sub-task | „Wygeneruj tekst AI, przeredaguj" |
| Bug | „Imię bohatera jest niespójne" |

---

# Krok 3 – Utwórz Epici i Stories

## Product Owner tworzy strukturę w Jira

1. **Roadmap** → **„+ Create epic"**:
   - `Napisanie powieści [tytuł]`
   - `Część I – Wprowadzenie i postacie`
   - `Część II – Akcja i punkt zwrotny`

2. **Backlog** → **„+ Create issue"** → typ: **Story**

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
5. SM wpisuje uzgodnioną wartość w Jira (pole „Story points")

> ✋ Dlaczego tajnie? Bo unikamy **anchoring bias** (wpływu na siebie nawzajem)

---

# Krok 4 – Wypełnianie Sprint Backlog

## Scrum Master + PO przeciągają Stories do Sprint 1

1. Backlog → sekcja **Sprint 1**
2. Przeciągnij Story z Backlogu do Sprint 1
3. Zacznij od **najwyższych priorytetów**
4. Dodawaj Stories aż suma SP = **12–15**

Dla każdej Story w sprincie:
- Otwórz Story → **„Create child issue"** → Sub-task
- Przypisz do konkretnego Developera

---

# Definition of Done – musisz zdefiniować PRZED sprintem!

## Pages → „Definition of Done"

```markdown
## Dla rozdziału / sceny:
- [ ] Tekst ≥ 300 słów
- [ ] Imiona spójne w całym tekście
- [ ] Styl spójny z gatunkiem
- [ ] Tekst wklejony do dokumentu
- [ ] Story = Done w Jira
- [ ] Review przez QA
```

---

# Lista kontrolna – czy jesteście gotowi na Sprint?

- [ ] Konto Jira (site) założone, wszyscy mają dostęp
- [ ] Projekt Scrum z właściwą nazwą
- [ ] Sprint 1 skonfigurowany z datami
- [ ] Min. 6 PBI w backlogu z opisami
- [ ] Każde PBI ma Story Points
- [ ] Sprint Backlog: 12–15 SP
- [ ] Każde PBI ma Task przypisany do Developera
- [ ] Definition of Done w Wiki

---

# Gotowi? START SPRINT! 🚀

## Przejdź do: **Board** (lewe menu)

Kolumny: `To Do | In Progress | Done`

Każdy Developer:
1. Bierze swój Sub-task → przeciąga do **In Progress**
2. Pisze prompt dla AI → generuje tekst → redaguje
3. Po ukończeniu → przeciąga do **Done**
4. QA sprawdza DoD → Story → **Done** lub wraca z komentarzem

> Następnie: [Blok 2A – Sprint](../../Blok2-Sprint-Podsumowanie/2A-Sprint/Slajdy.md)
