---

description: "Template elenco task per implementazione funzionalità"
---

# Task: [FEATURE NAME]

**Input**: Documenti di design da `/specs/[###-feature-name]/`
**Prerequisiti**: plan.md (obbligatorio), spec.md (obbligatorio per user story), research.md, data-model.md, contracts/

**Test**: Gli esempi sotto includono task di test. I test sono OPZIONALI - includerli solo se richiesti esplicitamente nella specifica della funzionalità.

**Organizzazione**: I task sono raggruppati per user story per consentire implementazione e test indipendenti di ogni story.

## Formato: `[ID] [P?] [Story] Descrizione`

- **[P]**: Può essere eseguito in parallelo (file diversi, nessuna dipendenza)
- **[Story]**: A quale user story appartiene il task (es.: US1, US2, US3)
- Includere percorsi file esatti nelle descrizioni

## Convenzioni Percorsi

- **Single project**: `src/`, `tests/` alla radice del repository
- **Web app**: `backend/src/`, `frontend/src/`
- **Mobile**: `api/src/`, `ios/src/` o `android/src/`
- I percorsi sotto assumono single project - adattare in base alla struttura di plan.md

<!-- 
  ============================================================================
  IMPORTANT: The tasks below are SAMPLE TASKS for illustration purposes only.
  
  The /speckit.tasks command MUST replace these with actual tasks based on:
  - User stories from spec.md (with their priorities P1, P2, P3...)
  - Feature requirements from plan.md
  - Entities from data-model.md
  - Endpoints from contracts/
  
  Tasks MUST be organized by user story so each story can be:
  - Implemented independently
  - Tested independently
  - Delivered as an MVP increment
  
  DO NOT keep these sample tasks in the generated tasks.md file.
  ============================================================================
-->

## Fase 1: Setup (Infrastruttura Condivisa)

**Scopo**: Inizializzazione progetto e struttura base

- [ ] T001 Create project structure per implementation plan
- [ ] T002 Initialize [language] project with [framework] dependencies
- [ ] T003 [P] Configure linting and formatting tools

---

## Fase 2: Fondazionale (Prerequisiti Bloccanti)

**Scopo**: Infrastruttura core che DEVE essere completa prima che QUALSIASI user story possa essere implementata

**⚠️ CRITICO**: Nessuna user story può iniziare prima che questa fase sia completa

Esempi di task fondazionali (adattare in base al progetto):

- [ ] T004 Setup database schema and migrations framework
- [ ] T005 [P] Implement authentication/authorization framework
- [ ] T006 [P] Setup API routing and middleware structure
- [ ] T007 Create base models/entities that all stories depend on
- [ ] T008 Configure error handling and logging infrastructure
- [ ] T009 Setup environment configuration management

**Checkpoint**: Foundation pronta - l'implementazione delle user story può iniziare in parallelo

---

## Fase 3: User Story 1 - [Title] (Priorità: P1) 🎯 MVP

**Obiettivo**: [Breve descrizione di ciò che questa story fornisce]

**Test Indipendente**: [Come verificare che la story funzioni da sola]

### Test per User Story 1 (OPZIONALE - solo se richiesti) ⚠️

> **NOTA: Scrivere prima questi test e assicurarsi che FALLISCANO prima dell'implementazione**

- [ ] T010 [P] [US1] Contract test for [endpoint] in tests/contract/test_[name].py
- [ ] T011 [P] [US1] Integration test for [user journey] in tests/integration/test_[name].py

### Implementazione per User Story 1

- [ ] T012 [P] [US1] Create [Entity1] model in src/models/[entity1].py
- [ ] T013 [P] [US1] Create [Entity2] model in src/models/[entity2].py
- [ ] T014 [US1] Implement [Service] in src/services/[service].py (depends on T012, T013)
- [ ] T015 [US1] Implement [endpoint/feature] in src/[location]/[file].py
- [ ] T016 [US1] Add validation and error handling
- [ ] T017 [US1] Add logging for user story 1 operations

**Checkpoint**: A questo punto, la User Story 1 dovrebbe essere completamente funzionale e testabile indipendentemente

---

## Fase 4: User Story 2 - [Title] (Priorità: P2)

**Obiettivo**: [Breve descrizione di ciò che questa story fornisce]

**Test Indipendente**: [Come verificare che la story funzioni da sola]

### Test per User Story 2 (OPZIONALE - solo se richiesti) ⚠️

- [ ] T018 [P] [US2] Contract test for [endpoint] in tests/contract/test_[name].py
- [ ] T019 [P] [US2] Integration test for [user journey] in tests/integration/test_[name].py

### Implementazione per User Story 2

- [ ] T020 [P] [US2] Create [Entity] model in src/models/[entity].py
- [ ] T021 [US2] Implement [Service] in src/services/[service].py
- [ ] T022 [US2] Implement [endpoint/feature] in src/[location]/[file].py
- [ ] T023 [US2] Integrate with User Story 1 components (if needed)

**Checkpoint**: A questo punto, le User Story 1 E 2 dovrebbero funzionare indipendentemente

---

## Fase 5: User Story 3 - [Title] (Priorità: P3)

**Obiettivo**: [Breve descrizione di ciò che questa story fornisce]

**Test Indipendente**: [Come verificare che la story funzioni da sola]

### Test per User Story 3 (OPZIONALE - solo se richiesti) ⚠️

- [ ] T024 [P] [US3] Contract test for [endpoint] in tests/contract/test_[name].py
- [ ] T025 [P] [US3] Integration test for [user journey] in tests/integration/test_[name].py

### Implementazione per User Story 3

- [ ] T026 [P] [US3] Create [Entity] model in src/models/[entity].py
- [ ] T027 [US3] Implement [Service] in src/services/[service].py
- [ ] T028 [US3] Implement [endpoint/feature] in src/[location]/[file].py

**Checkpoint**: Tutte le user story dovrebbero ora essere funzionali indipendentemente

---

[Add more user story phases as needed, following the same pattern]

---

## Fase N: Rifiniture & Aspetti Trasversali

**Scopo**: Miglioramenti che impattano multiple user story

- [ ] TXXX [P] Documentation updates in docs/
- [ ] TXXX Code cleanup and refactoring
- [ ] TXXX Performance optimization across all stories
- [ ] TXXX [P] Additional unit tests (if requested) in tests/unit/
- [ ] TXXX Security hardening
- [ ] TXXX Run quickstart.md validation

---

## Dipendenze & Ordine di Esecuzione

### Dipendenze tra Fasi

- **Setup (Fase 1)**: Nessuna dipendenza - può iniziare subito
- **Fondazionale (Fase 2)**: Dipende dal completamento Setup - BLOCCA tutte le user story
- **User Story (Fase 3+)**: Tutte dipendono dal completamento Fondazionale
  - Le user story possono procedere in parallelo (se c'è capacità)
  - Oppure in ordine di priorità (P1 → P2 → P3)
- **Rifiniture (Fase Finale)**: Dipende dal completamento delle user story desiderate

### Dipendenze tra User Story

- **User Story 1 (P1)**: Può iniziare dopo Fondazionale (Fase 2) - Nessuna dipendenza
- **User Story 2 (P2)**: Può iniziare dopo Fondazionale (Fase 2) - Può integrare US1 ma deve essere testabile indipendentemente
- **User Story 3 (P3)**: Può iniziare dopo Fondazionale (Fase 2) - Può integrare US1/US2 ma deve essere testabile indipendentemente

### All'interno di ogni User Story

- I test (se inclusi) DEVONO essere scritti e FALLIRE prima dell'implementazione
- Modelli prima dei servizi
- Servizi prima degli endpoint
- Implementazione core prima dell'integrazione
- Story completa prima di passare alla priorità successiva

### Opportunità di Parallelismo

- Tutti i task di Setup marcati [P] possono girare in parallelo
- Tutti i task Fondazionali marcati [P] possono girare in parallelo (entro Fase 2)
- Una volta completata la fase Fondazionale, tutte le user story possono partire in parallelo (se c'è capacità)
- Tutti i test di una user story marcati [P] possono girare in parallelo
- I modelli di una story marcati [P] possono girare in parallelo
- User story diverse possono essere sviluppate in parallelo da membri diversi

---

## Esempio Parallelismo: User Story 1

```bash
# Launch all tests for User Story 1 together (if tests requested):
Task: "Contract test for [endpoint] in tests/contract/test_[name].py"
Task: "Integration test for [user journey] in tests/integration/test_[name].py"

# Launch all models for User Story 1 together:
Task: "Create [Entity1] model in src/models/[entity1].py"
Task: "Create [Entity2] model in src/models/[entity2].py"
```

---

## Strategia di Implementazione

### Prima MVP (Solo User Story 1)

1. Completa Fase 1: Setup
2. Completa Fase 2: Fondazionale (CRITICA - blocca tutte le story)
3. Completa Fase 3: User Story 1
4. **STOP e VALIDARE**: Testare la User Story 1 indipendentemente
5. Deploy/demo se pronta

### Consegna Incrementale

1. Completa Setup + Fondazionale → Foundation pronta
2. Aggiungi User Story 1 → Test indipendente → Deploy/Demo (MVP!)
3. Aggiungi User Story 2 → Test indipendente → Deploy/Demo
4. Aggiungi User Story 3 → Test indipendente → Deploy/Demo
5. Ogni story aggiunge valore senza rompere le precedenti

### Strategia Team in Parallel

With multiple developers:

1. Il team completa Setup + Fondazionale insieme
2. Una volta completata la Fondazionale:
  - Dev A: User Story 1
  - Dev B: User Story 2
  - Dev C: User Story 3
3. Le story si completano e si integrano indipendentemente

---

## Note

- Task [P] = file diversi, nessuna dipendenza
- Etichetta [Story] collega il task alla specifica user story per tracciabilità
- Ogni user story deve essere completabile e testabile indipendentemente
- Verificare che i test falliscano prima di implementare
- Commit dopo ogni task o gruppo logico
- Fermarsi a ogni checkpoint per validare la story indipendentemente
- Evitare: task vaghi, conflitti sullo stesso file, dipendenze trasversali che rompono l'indipendenza
