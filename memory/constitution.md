# [PROJECT_NAME] Constitution
<!-- Esempio: Spec Constitution, TaskFlow Constitution, ecc. -->

## Principi Fondamentali

### [PRINCIPLE_1_NAME]
<!-- Esempio: I. Library-First -->
[PRINCIPLE_1_DESCRIPTION]
<!-- Esempio: Ogni funzionalità nasce come libreria standalone; Le librerie devono essere auto-contenute, testabili indipendentemente, documentate; Scopo chiaro richiesto - vietate librerie solo organizzative -->

### [PRINCIPLE_2_NAME]
<!-- Esempio: II. Interfaccia CLI -->
[PRINCIPLE_2_DESCRIPTION]
<!-- Esempio: Ogni libreria espone funzionalità via CLI; Protocollo testo in/out: stdin/args → stdout, errori → stderr; Supporto formati JSON + leggibile umano -->

### [PRINCIPLE_3_NAME]
<!-- Esempio: III. Test-First (NON NEGOZIABILE) -->
[PRINCIPLE_3_DESCRIPTION]
<!-- Esempio: TDD obbligatorio: Test scritti → Approvati dall'utente → I test falliscono → Poi si implementa; Ciclo Rosso-Verde-Refactor applicato rigorosamente -->

### [PRINCIPLE_4_NAME]
<!-- Esempio: IV. Test di Integrazione -->
[PRINCIPLE_4_DESCRIPTION]
<!-- Esempio: Aree di focus che richiedono test di integrazione: Nuovi contract test di libreria, Modifiche di contract, Comunicazione inter-servizio, Schemi condivisi -->

### [PRINCIPLE_5_NAME]
<!-- Esempio: V. Osservabilità, VI. Versioning & Breaking Changes, VII. Semplicità -->
[PRINCIPLE_5_DESCRIPTION]
<!-- Esempio: I/O testuale garantisce debuggabilità; Logging strutturato obbligatorio; Oppure: formato MAJOR.MINOR.BUILD; Oppure: Parti semplice, principi YAGNI -->

## [SECTION_2_NAME]
<!-- Esempio: Vincoli Aggiuntivi, Requisiti di Sicurezza, Standard di Prestazione, ecc. -->

[SECTION_2_CONTENT]
<!-- Esempio: Requisiti dello stack tecnologico, standard di conformità, policy di deployment, ecc. -->

## [SECTION_3_NAME]
<!-- Esempio: Workflow di Sviluppo, Processo di Revisione, Quality Gates, ecc. -->

[SECTION_3_CONTENT]
<!-- Esempio: Requisiti di code review, gate di testing, processo di approvazione al deployment, ecc. -->

## Governance
<!-- Esempio: La Constitution prevale su tutte le altre pratiche; Le modifiche richiedono documentazione, approvazione, piano di migrazione -->

[GOVERNANCE_RULES]
<!-- Esempio: Tutte le PR/revisioni devono verificare la conformità; La complessità deve essere giustificata; Usa [GUIDANCE_FILE] per la guida allo sviluppo runtime -->

**Versione**: [CONSTITUTION_VERSION] | **Ratificata**: [RATIFICATION_DATE] | **Ultima Modifica**: [LAST_AMENDED_DATE]
<!-- Esempio: Version: 2.1.1 | Ratified: 2025-06-13 | Last Amended: 2025-07-16 -->
