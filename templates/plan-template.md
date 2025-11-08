# Piano di Implementazione: [FEATURE]

**Branch**: `[###-feature-name]` | **Data**: [DATE] | **Spec**: [link]
**Input**: Specifica della funzionalità da `/specs/[###-feature-name]/spec.md`

**Nota**: Questo template viene compilato dal comando `/speckit.plan`. Vedi `.specify/templates/commands/plan.md` per il flusso di esecuzione.

## Riepilogo

[Estratto dalla specifica: requisito primario + approccio tecnico da analisi]

## Contesto Tecnico

<!--
  ACTION REQUIRED: Replace the content in this section with the technical details
  for the project. The structure here is presented in advisory capacity to guide
  the iteration process.
-->

**Linguaggio/Versione**: [e.g., Python 3.11, Swift 5.9, Rust 1.75 or NEEDS CLARIFICATION]  
**Dipendenze Primarie**: [e.g., FastAPI, UIKit, LLVM or NEEDS CLARIFICATION]  
**Storage**: [se applicabile, e.g., PostgreSQL, CoreData, files or N/A]  
**Testing**: [e.g., pytest, XCTest, cargo test or NEEDS CLARIFICATION]  
**Piattaforma Target**: [e.g., Linux server, iOS 15+, WASM or NEEDS CLARIFICATION]
**Tipo Progetto**: [single/web/mobile - determina la struttura sorgente]  
**Obiettivi di Performance**: [domain-specific, e.g., 1000 req/s, 10k lines/sec, 60 fps or NEEDS CLARIFICATION]  
**Vincoli**: [domain-specific, e.g., <200ms p95, <100MB memory, offline-capable or NEEDS CLARIFICATION]  
**Scala/Ambito**: [domain-specific, e.g., 10k users, 1M LOC, 50 screens or NEEDS CLARIFICATION]

## Constitution Check

*GATE: Deve passare prima della ricerca Fase 0. Rieseguire dopo la progettazione Fase 1.*

[Gate determinati in base al file constitution]

## Struttura del Progetto

### Documentazione (questa funzionalità)

```text
specs/[###-feature]/
├── plan.md              # This file (/speckit.plan command output)
├── research.md          # Phase 0 output (/speckit.plan command)
├── data-model.md        # Phase 1 output (/speckit.plan command)
├── quickstart.md        # Phase 1 output (/speckit.plan command)
├── contracts/           # Phase 1 output (/speckit.plan command)
└── tasks.md             # Phase 2 output (/speckit.tasks command - NOT created by /speckit.plan)
```

### Codice Sorgente (radice repository)
<!--
  ACTION REQUIRED: Replace the placeholder tree below with the concrete layout
  for this feature. Delete unused options and expand the chosen structure with
  real paths (e.g., apps/admin, packages/something). The delivered plan must
  not include Option labels.
-->

```text
# [REMOVE IF UNUSED] Option 1: Single project (DEFAULT)
src/
├── models/
├── services/
├── cli/
└── lib/

tests/
├── contract/
├── integration/
└── unit/

# [REMOVE IF UNUSED] Option 2: Web application (when "frontend" + "backend" detected)
backend/
├── src/
│   ├── models/
│   ├── services/
│   └── api/
└── tests/

frontend/
├── src/
│   ├── components/
│   ├── pages/
│   └── services/
└── tests/

# [REMOVE IF UNUSED] Option 3: Mobile + API (when "iOS/Android" detected)
api/
└── [same as backend above]

ios/ or android/
└── [platform-specific structure: feature modules, UI flows, platform tests]
```

**Decisione Struttura**: [Documentare la struttura selezionata e fare riferimento
alle directory reali catturate sopra]

## Monitoraggio Complessità

> **Compilare SOLO se il Constitution Check ha violazioni che devono essere giustificate**

| Violazione | Perché Necessaria | Alternativa Semplice Respinta Perché |
|------------|------------------|--------------------------------------|
| [e.g., 4th project] | [current need] | [why 3 projects insufficient] |
| [e.g., Repository pattern] | [specific problem] | [why direct DB access insufficient] |
