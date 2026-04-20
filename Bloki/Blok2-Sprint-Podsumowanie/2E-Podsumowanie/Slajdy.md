---
marp: true
theme: default
paginate: true
header: "Zarządzanie projektami IT | Studia podyplomowe BIM"
footer: "© 2026 | Blok 2E – Podsumowanie"
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
  blockquote {
    border-left: 4px solid #0078d4;
    background: #dbeafe;
    padding: 0.5em 1em;
    font-style: italic;
  }
  .lesson-number {
    font-size: 3em;
    font-weight: bold;
    color: #e8e8e8;
    position: absolute;
    right: 60px;
    top: 40px;
  }
---

# Blok 2E – Podsumowanie

## 5 Kluczowych lekcji z zarządzania projektami IT

**Studia podyplomowe BIM | Kwiecień 2026**

---

# Co przeszliśmy dziś?

| Blok | Aktywność | Narzędzie |
|---|---|---|
| 1A | Teoria: metodyki, role, narzędzia | Wykład |
| 1B | Konfiguracja ADO + Sprint Planning | Azure DevOps |
| 2A | Sprint z AI (45 min) | ADO + ChatGPT/Copilot |
| 2B | Daily Scrum | ADO Boards |
| 2C | Sprint Review + Velocity | ADO Analytics |
| 2D | Retrospektywa Start/Stop/Continue | ADO Wiki |

---

# Lekcja 1: Backlog > Plan Gantta

## Dlaczego?

> „Plan to nic, planowanie to wszystko."
> — Dwight D. Eisenhower

| Plan Gantta | Backlog |
|---|---|
| Stałe wymagania | Dynamiczne wymagania |
| Zmiany = przeplanowanie | Zmiany = repriorytyzacja |
| Skupia się na **czasie** | Skupia się na **wartości** |
| Aktualizowany rzadko | Żywy dokument |

---

# Lekcja 1: Kiedy co stosować?

## Gantt jest lepszy gdy:
- Wymagania są **stałe i znane z góry**
- Projekt ma zewnętrzne zobowiązania terminowe
- Regulacje narzucają sekwencyjność prac
- *(np. projekt budowlany, BIM w fazie wykonawczej)*

## Backlog jest lepszy gdy:
- Wymagania **zmieniają się w trakcie**
- Klient odkrywa potrzeby podczas pracy
- Priorytetyzacja wartości biznesowej jest kluczowa
- *(np. aplikacja, oprogramowanie, produkt cyfrowy)*

---

# Lekcja 2: Product Owner – rola dla każdego z Was

## PO **nie musi** programować

> „Product Owner to głos klienta i strażnik wartości produktu."

**Co robi PO:**
- Definiuje **co** budujemy (nie **jak**)
- Priorytetyzuje backlog wg wartości biznesowej
- Akceptuje lub odrzuca przyrosty
- Reprezentuje interesariuszy w zespole

---

# Lekcja 2: BIM Manager jako Product Owner

## Analogia

| Rola w IT | Odpowiednik w BIM |
|---|---|
| Product Owner | BIM Manager |
| Product Backlog | Lista wymagań BIM |
| Sprint | Faza projektu (koncepcja, PW, przetarg) |
| Increment | Dostarczona dokumentacja BIM |
| Stakeholder | Inwestor, projektant, wykonawca |

> BIM Manager łączy architekturę, konstrukcję i instalacje  
> — tak jak PO łączy biznes z technologią.

---

# Lekcja 3: Definition of Done

## Bez DoD każdy ma inne rozumienie słowa „gotowe"

### Przykład:

| Osoba | Co znaczy „gotowe" |
|---|---|
| Developer | „Napisałem tekst" |
| QA | „Brak błędów fabularnych" |
| PO | „Spełnia oczekiwania czytelnika" |
| Stakeholder | „Jest na stronie / do pobrania" |

---

# Lekcja 3: DoD w praktyce

## Dobry Definition of Done to kontrakt wewnętrzny

```
Definition of Done – Rozdział powieści:
✅ Tekst ≥ 300 słów
✅ Imiona postaci spójne
✅ Styl odpowiada gatunkowi
✅ Wklejony do dokumentu
✅ Review przez QA
✅ PBI = Done w ADO
```

> DoD **eliminuje dług techniczny**.  
> W budownictwie: protokół odbioru = DoD.

---

# Lekcja 4: Velocity – jedyne wiarygodne narzędzie

## Co to jest Velocity?

**Velocity** = liczba Story Points ukończona przez zespół w jednym sprincie

## Dlaczego to ważne?

```
Sprint 1: Velocity = 10 SP
Sprint 2: Velocity = 12 SP
Sprint 3: Velocity = 11 SP

Średnia: ~11 SP/sprint

Backlog: 88 SP pozostało
Prognoza: 88 ÷ 11 = 8 sprintów
```

---

# Lekcja 4: Story Points ≠ godziny

## Dlaczego nie szacujemy w godzinach?

| Szacowanie w godzinach | Story Points |
|---|---|
| Pressure – „8 godzin to 8 godzin" | Bez presji – względna skala |
| Senior: 2h, Junior: 8h – różne osoby | Zespołowe szacowanie |
| Uwzględnia optymizm | Empiryczne, oparte na historii |
| Tworzysz zobowiązanie | Tworzysz prognozę |

---

# Lekcja 5: ADO vs Jira – co wybrać?

| Cecha | Azure DevOps Free | Jira Free |
|---|---|---|
| Użytkownicy | **5** | 10 |
| Scrum / Kanban | ✅ | ✅ |
| CI/CD | 1800 min/mies. | ❌ |
| MS 365 | Natywna ✅ | Plugin |
| Karty płatniczej | ❌ nie trzeba | ❌ nie trzeba |

## Wniosek:

> Koncepcje są **identyczne**. Narzędzie dobierz do ekosystemu firmy.

---

# Scrum w jednym slajdzie

```
Product Backlog  →  Sprint Planning  →  Sprint (1–4 tygodnie)
                                              │
                                     Daily Scrum (codziennie)
                                              │
                                       Sprint Review
                                       (pokaz przyrostu)
                                              │
                                     Retrospektywa
                                     (usprawnienie procesu)
                                              │
                              ←──────────────┘
                           (następny sprint)
```

---

# Pytania do dyskusji

## Refleksja po zajęciach

1. Jak Agile może się zastosować do projektu BIM?  
   *(Co byłby backlogiem? Co sprintem? Kto byłby PO?)*

2. Jaką rolę wybralibyście w prawdziwym projekcie IT?

3. Co było największym wyzwaniem podczas pracy zespołowej dziś?

4. Co zrobilibyście inaczej w **Sprint 2**?

5. ADO vs Jira – które narzędzie wydaje się bardziej intuicyjne?

---

# Najważniejsze pojęcia – ściągawka

| Pojęcie | Definicja |
|---|---|
| **Backlog** | Priorytetowa lista wymagań projektu |
| **Sprint** | Timeboxed iteracja (1–4 tygodnie) |
| **Story Points** | Względna miara złożoności zadania |
| **Velocity** | SP ukończone w jednym sprincie |
| **DoD** | Uzgodnione kryteria „gotowości" |
| **Impediment** | Przeszkoda blokująca pracę |
| **WIP Limit** | Max zadań „w toku" naraz |
| **Increment** | Gotowy przyrost po sprincie |

---

# Dziękuję za udział w zajęciach!

## Co zabrać ze sobą

- ✅ Konto Azure DevOps (zostaje)
- ✅ Projekt powieści (macie link do dokumentu)
- ✅ Doświadczenie jednego pełnego sprintu Scrum
- ✅ Wiedza o rolach, metodykach i narzędziach

## Materiały do zajęć

Wszystkie pliki: **Bloki/** w repozytorium GitHub  
Plan zajęć: **Dokumentacja/PlanZajec.md**

---

# Backlog kolejnych zajęć?

## Jeśli mielibyśmy więcej czasu...

- Sprint 2 – dokończenie powieści
- Kanban Board – praca bez sprintów
- CI/CD – automatyczne „wydawanie" rozdziałów
- Raporty i dashboardy w ADO
- Skalowanie Agile – SAFe, LeSS
- Agile w projektach BIM – case study

> „Reagowanie na zmiany ponad podążanie za planem" — Manifest Agile
