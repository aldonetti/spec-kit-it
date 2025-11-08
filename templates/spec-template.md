# Specifiche della Funzionalità: [FEATURE NAME]

**Branch della Feature**: `[###-feature-name]`  
**Creato**: [DATE]  
**Stato**: Bozza  
**Input**: Descrizione utente: "$ARGUMENTS"

## Scenari Utente e Test *(obbligatorio)*

<!--
  IMPORTANTE: Le user story devono essere PRIORITIZZATE come percorsi utente in ordine di importanza.
  Ogni user story/percorso deve essere TESTABILE INDIPENDENTEMENTE - cioè, implementandone anche SOLO UNA,
  si deve ottenere comunque un MVP (Minimum Viable Product) che generi valore.
  
  Assegna priorità (P1, P2, P3, ecc.) a ciascuna story, dove P1 è la più critica.
  Considera ogni story come una fetta di funzionalità indipendente che può essere:
  - Sviluppata indipendentemente
  - Testata indipendentemente
  - Deployata indipendentemente
  - Dimostrata agli utenti indipendentemente
-->

### User Story 1 - [Brief Title] (Priorità: P1)

[Descrivi questo percorso utente in linguaggio semplice]

**Perché questa priorità**: [Spiega il valore e il motivo di questo livello di priorità]

**Test Indipendente**: [Descrivi come può essere testata indipendentemente - es.: "Può essere testata completamente tramite [azione specifica] e fornisce [valore specifico]"]

**Casi di Accettazione**:

1. **Dato** [initial state], **Quando** [action], **Allora** [expected outcome]
2. **Dato** [initial state], **Quando** [action], **Allora** [expected outcome]

---

### User Story 2 - [Brief Title] (Priorità: P2)

[Descrivi questo percorso utente in linguaggio semplice]

**Perché questa priorità**: [Spiega il valore e il motivo di questo livello di priorità]

**Test Indipendente**: [Descrivi come può essere testata indipendentemente]

**Casi di Accettazione**:

1. **Dato** [initial state], **Quando** [action], **Allora** [expected outcome]

---

### User Story 3 - [Brief Title] (Priorità: P3)

[Descrivi questo percorso utente in linguaggio semplice]

**Perché questa priorità**: [Spiega il valore e il motivo di questo livello di priorità]

**Test Indipendente**: [Descrivi come può essere testata indipendentemente]

**Casi di Accettazione**:

1. **Dato** [initial state], **Quando** [action], **Allora** [expected outcome]

---

[Aggiungi altre user story secondo necessità, ciascuna con una priorità assegnata]

### Casi Limite

<!--
  AZIONE RICHIESTA: Il contenuto di questa sezione rappresenta segnaposto.
  Sostituiscili con i corretti casi limite.
-->

- Cosa succede quando [boundary condition]?
- Come gestisce il sistema [error scenario]?

## Requisiti *(obbligatorio)*

<!--
  AZIONE RICHIESTA: Il contenuto di questa sezione rappresenta segnaposto.
  Sostituiscili con i corretti requisiti funzionali.
-->

### Requisiti Funzionali

- **FR-001**: Il sistema DEVE [specific capability, e.g., "allow users to create accounts"]
- **FR-002**: Il sistema DEVE [specific capability, e.g., "validate email addresses"]  
- **FR-003**: Gli utenti DEVONO poter [key interaction, e.g., "reset their password"]
- **FR-004**: Il sistema DEVE [data requirement, e.g., "persist user preferences"]
- **FR-005**: Il sistema DEVE [behavior, e.g., "log all security events"]

*Esempio di come marcare requisiti poco chiari:*

- **FR-006**: Il sistema DEVE autenticare gli utenti tramite [NEEDS CLARIFICATION: auth method not specified - email/password, SSO, OAuth?]
- **FR-007**: Il sistema DEVE conservare i dati utente per [NEEDS CLARIFICATION: retention period not specified]

### Entità Chiave *(includere se la funzionalità coinvolge dati)*

- **[Entity 1]**: [What it represents, key attributes without implementation]
- **[Entity 2]**: [What it represents, relationships to other entities]

## Criteri di Successo *(obbligatorio)*

<!--
  AZIONE RICHIESTA: Definisci criteri di successo misurabili.
  Devono essere agnostici rispetto alla tecnologia e misurabili.
-->

### Risultati Misurabili

- **SC-001**: [Measurable metric, e.g., "Users can complete account creation in under 2 minutes"]
- **SC-002**: [Measurable metric, e.g., "System handles 1000 concurrent users without degradation"]
- **SC-003**: [User satisfaction metric, e.g., "90% of users successfully complete primary task on first attempt"]
- **SC-004**: [Business metric, e.g., "Reduce support tickets related to [X] by 50%"]
