# Część 1A – Teoria zarządzania projektami IT

> Czas: **60 minut** | Forma: wykład z elementami dyskusji  
> Slajdy: [Slajdy.md](./Slajdy.md)

---

## Cel dydaktyczny

Student rozumie czym jest projekt IT, jakie metodyki zarządzania są stosowane,  
jakie role pełnią poszczególne osoby w zespole i jakich narzędzi się używa.

---

## Tematy i minutaż

### 1. Wprowadzenie – czym różni się projekt IT od innych? (10 min)

**Kluczowe pytanie do otwarcia dyskusji:**  
> „Czym różni się budowanie domu od tworzenia aplikacji mobilnej?"

**Omawiane zagadnienia:**

- Specyfika projektów IT:
  - niematerialny produkt (trudno ocenić „gotowość"),
  - zmieniające się wymagania (klient nie wie czego chce, dopóki nie zobaczy),
  - wysoka złożoność i zależności między komponentami,
  - szybkie tempo zmian technologicznych.

- **Chaos Report (Standish Group)** – kluczowe dane:
  - tylko ~30% projektów IT kończy się sukcesem (na czas, budżet, zakres),
  - najczęstsze przyczyny niepowodzeń: niejasne wymagania, brak komunikacji, rozszerzanie zakresu projektu.

- **Trójkąt projektowy** (Iron Triangle):
  - trzy wierzchołki: Zakres – Czas – Budżet,
  - w klasycznych projektach: stały zakres, elastyczny budżet/czas,
  - w IT (Agile): stały czas i budżet, **elastyczny zakres**.

---

### 2. Metodyki zarządzania projektami IT (25 min)

#### Waterfall – model kaskadowy (7 min)

Fazy sekwencyjne: **Wymagania → Projektowanie → Implementacja → Testowanie → Wdrożenie**

| Zalety | Wady |
|---|---|
| Przewidywalność harmonogramu | Zmiana wymagań = restart lub katastrofa |
| Dobra dokumentacja | Długi czas do pierwszego działającego produktu |
| Jasne kamienie milowe | Klient widzi produkt dopiero na końcu |
| Prosta struktura zarządzania | Nie nadaje się do projektów innowacyjnych |

**Kiedy stosować:**  
- projekty o stałych, dobrze znanych wymaganiach,  
- systemy embedded (np. sterowniki maszyn),  
- projekty regulowane (medycyna, lotnictwo),  
- **analogia BIM**: projekt wykonawczy w BIM (wymagania znane z góry, zmiany kosztowne).

**Pytanie do dyskusji:** *Czy Waterfall pasuje do projektu BIM? Kiedy tak, kiedy nie?*

---

#### Agile – manifest i wartości (5 min)

**Manifest Agile (2001) – 4 wartości:**

| Bardziej cenimy *(lewa strona)* | Niż *(prawa strona)* |
|---|---|
| **Ludzie i interakcje** | Procesy i narzędzia |
| **Działające oprogramowanie** | Obszerna dokumentacja |
| **Współpraca z klientem** | Negocjowanie umów |
| **Reagowanie na zmiany** | Podążanie za planem |

> „Cenimy rzeczy po prawej stronie *(procesy, dokumentację, umowy, plan)*, ale bardziej cenimy te po lewej *(ludzi, oprogramowanie, współpracę, zmiany)*."

**Kluczowe pojęcia:**
- **Iteracja** – krótki cykl pracy zakończony działającym produktem,
- **Przyrost (Increment)** – wartość dostarczona w każdej iteracji,
- **Empiryzm** – uczymy się przez robienie, nie przez planowanie.

---

#### Scrum (8 min)

Scrum to **framework** (nie metodologia!) oparty na Agile.

**Trzy filary Scrum:**
- **Przejrzystość** (Transparency) – wszyscy widzą to samo
- **Inspekcja** (Inspection) – regularnie sprawdzamy postęp
- **Adaptacja** (Adaptation) – zmieniamy plan gdy trzeba

**Artefakty Scrum:**

| Artefakt | Opis | W projekcie powieści |
|---|---|---|
| **Product Backlog** | Lista wszystkich wymagań (PBI) | Lista rozdziałów, scen, postaci |
| **Sprint Backlog** | PBI zaplanowane na bieżący sprint | Zadania na dziś (45 min) |
| **Increment** | Gotowy, działający przyrost produktu | Ukończone i sprawdzone rozdziały |

**Zdarzenia Scrum:**

| Zdarzenie | Cel | Czas dziś |
|---|---|---|
| **Sprint Planning** | Zaplanuj sprint, wybierz PBI | ~20 min (koniec Bloku 1) |
| **Daily Scrum** | Synchronizacja, impedimenty | ~10 min (środek sprintu) |
| **Sprint Review** | Pokaż przyrost stakeholderom | ~15 min (Blok 2) |
| **Retrospektywa** | Poprawa procesu | ~15 min (Blok 2) |

**Cykl iteracji Scrum (jeden Sprint):**

![Cykl iteracji Scrum](./scrum-iteracja.png)

**Sprint na dzisiejszych zajęciach = 45 minut** ← jedna iteracja!

---

#### Kanban (5 min)

Kanban to **system zarządzania przepływem pracy** – nie ma sprintów, jest ciągły przepływ.

**Tablica Kanban:**
```
| To Do          | In Progress    | Review         | Done           |
|----------------|----------------|----------------|----------------|
| Zadanie A      | Zadanie B      | Zadanie C      |                |
| Zadanie D      |                |                |                |
```

**Kluczowa zasada: WIP Limit (Work in Progress)**  
- Ograniczamy liczbę zadań „w toku" (np. max 2 w kolumnie In Progress),  
- Cel: szybsze kończenie zadań zamiast zaczynania nowych.

**Scrum vs Kanban:**

| | Scrum | Kanban |
|---|---|---|
| Iteracje | Tak (sprint 1–4 tyg.) | Nie (ciągły przepływ) |
| Role | PO, SM, Dev | Opcjonalne |
| Zmiany w trakcie | Nie (w sprincie) | Tak (zawsze) |
| Dobre dla | Nowych produktów | Wsparcia, utrzymania |

---

### 3. Role w projekcie IT (15 min)

#### Opis ról

| Rola | Odpowiedzialność | W projekcie powieści |
|---|---|---|
| **Product Owner** | Wizja, backlog, priorytety, głos klienta | Wydawca / Redaktor naczelny |
| **Scrum Master** | Facylitacja, impedimenty, stróż procesu | Coach / Kierownik projektu |
| **Developer** | Tworzenie przyrostów, szacowanie | Pisarz / Autor |
| **QA / Tester** | Jakość, defekty, kryteria DoD | Korektor / Beta-czytelnik |
| **Stakeholder** | Odbiorca, źródło wymagań | Czytelnik docelowy |

> W małych zespołach role można łączyć. **PO i SM nie powinny być tą samą osobą** – to konflikt interesów (biznes vs. proces).

#### Ćwiczenie (5 min): „Czyja to odpowiedzialność?"

Prowadzący czyta scenariusze, studenci wskazują rolę:

1. „Klient chce zmienić priorytet zadania w trakcie sprintu." → *PO (decyzja o backlogu), SM (ochrona sprintu)*
2. „Nikt nie wie, jak skonfigurować narzędzie." → *SM (impediment)*
3. „Testowanie wykazało, że postać ma dwa różne imiona w rozdziale 2." → *QA (bug)*
4. „Ile czasu zajmie napisanie rozdziału 3?" → *Developer (szacowanie)*
5. „Czy powieść jest gotowa do publikacji?" → *PO (akceptacja) + QA (DoD)*

---

### 4. Narzędzia w projektach IT (10 min)

#### Jira – plan bezpłatny (Free)

| Moduł | Funkcje | Używamy dziś |
|---|---|---|
| **Backlog** | Product Backlog, Sprint Backlog, priorytety | ✅ Tak |
| **Board** | Tablica Scrum / Kanban, przepływ zadań | ✅ Tak |
| **Roadmap** | Epici i harmonogram | ✅ Tak |
| **Reports** | Burndown, Velocity, Cumulative Flow | Poglądowo |
| **Pages** | Wiki, Definition of Done | ✅ Tak |

**Ograniczenia planu Free:**
- Max **10 użytkowników** na projekt,
- Brak zaawansowanych raportów i Time Tracking,
- Nieograniczone projekty i tablice w ramach limitu użytkowników.

#### Azure DevOps (ADO) – plan bezpłatny (Basic)

| Moduł | Funkcje | Odpowiednik Jira |
|---|---|---|
| **Boards** | Backlog, Kanban, Sprint Board | Backlog + Board |
| **Repos** | Repozytoria Git | *(brak w Jira Free)* |
| **Pipelines** | CI/CD automatyzacja | *(brak w Jira Free)* |
| **Wiki** | Dokumentacja zespołu | Pages |

**Ograniczenia planu Basic:**
- Tworzenie organizacji wymaga **konta służbowego / szkolnego Microsoft 365** lub subskrypcji Azure — osobiste konta Outlook.com nie wystarczą (zmiana polityki Microsoft od 2023 r.),
- Max 5 użytkowników na bezpłatnym planie Basic (powyżej — płatny),
- Natywna integracja z Microsoft 365 i GitHub.

#### Porównanie – Jira Free vs Azure DevOps Free

| Cecha | Jira Free | Azure DevOps Basic |
|---|---|---|
| Rejestracja | Dowolny e-mail | Wymaga konta M365 / subskrypcji Azure |
| Maks. użytkownicy | 10 | 5 |
| Scrum Boards | ✅ | ✅ |
| Kanban | ✅ | ✅ |
| Repozytoria Git | ❌ | ✅ |
| CI/CD | ❌ | ✅ |
| Edukacja / szkolenia | Intuicyjny UI | Rozbudowany, bardziej korporacyjny |

#### Dlaczego Jira na tych zajęciach?

- Rejestracja **bez karty płatniczej i bez konta Microsoft** — wystarczy dowolny e-mail,
- Plan Free obsługuje do **10 użytkowników** — wystarczy na cały zespół,
- Najpopularniejsze narzędzie Agile/Scrum na rynku (Atlassian Jira używa ponad 300 000 firm),
- Intuicyjny interfejs backlogu — łatwy do opanowania w trakcie jednych zajęć.

---

## Pytania kontrolne po części 1A

1. Czym różni się Scrum od Kanban?
2. Kto odpowiada za priorytety w backlogu?
3. Co to jest Definition of Done?
4. Dlaczego Waterfall nie sprawdza się w projektach o zmiennych wymaganiach?
5. Jakie są trzy artefakty Scrum?
