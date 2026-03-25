# Project Overview — Enterprise RAG Assistant for Policies and Procedures

## 1. Contesto del progetto

I Large Language Models mostrano il loro valore massimo quando possono rispondere su una base documentale affidabile, aggiornata e verificabile. Nei contesti aziendali questo richiede spesso un approccio Retrieval-Augmented Generation (RAG), nel quale il modello non si limita a generare una risposta, ma recupera prima i contenuti più rilevanti da una knowledge base documentale.

Questo progetto nasce come esercizio pratico e progetto portfolio con l'obiettivo di costruire esperienza reale nella progettazione, implementazione e valutazione di un sistema RAG piccolo ma strutturato, sviluppato in Google Colab e organizzato in un repository GitHub.

L'obiettivo non è costruire un semplice chatbot sui documenti, ma un prototipo ragionato che dimostri competenze concrete su:

- preparazione del corpus documentale;
- definizione e gestione dei metadati;
- retrieval documentale con filtri;
- generazione di risposte grounded;
- citazioni e tracciabilità delle fonti;
- benchmark ed evaluation;
- analisi degli errori e dei limiti del sistema.

---

## 2. Razionale del progetto

Molte organizzazioni possiedono già grandi quantità di conoscenza distribuite in policy, procedure, FAQ, manuali, report e documentazione tecnica. Il problema non è soltanto l'esistenza dei documenti, ma la loro effettiva utilizzabilità: spesso l'informazione è frammentata, difficile da trovare, scarsamente strutturata e non immediatamente interrogabile in linguaggio naturale.

Questo progetto intende simulare un caso realistico di knowledge retrieval aziendale, nel quale un utente può porre una domanda in linguaggio naturale e ricevere una risposta supportata da riferimenti documentali espliciti.

Dal punto di vista formativo e portfolio, il valore del progetto sta nel mostrare non soltanto capacità di prompting o uso di API, ma anche capacità di:

- modellare un problema reale;
- organizzare un corpus eterogeneo;
- ragionare su retrieval e qualità della documentazione;
- misurare la bontà del sistema con benchmark ed eval;
- esplicitare limiti, rischi e failure modes.

---

## 3. Problema che il progetto vuole risolvere

In un contesto enterprise-like, un utente deve poter trovare rapidamente informazioni corrette all'interno di documenti eterogenei come policy, SOP, linee guida, manuali e note tecniche.

Il progetto vuole quindi costruire un assistente RAG capace di:

1. interrogare un corpus documentale multi-formato;
2. recuperare i contenuti rilevanti;
3. generare risposte in linguaggio naturale;
4. mostrare le fonti utilizzate;
5. rendere osservabile la qualità del retrieval e della risposta.

Il problema non è solo "rispondere", ma farlo in modo:

- affidabile;
- verificabile;
- trasparente;
- misurabile.

---

## 4. Obiettivi del progetto

### Obiettivo generale

Realizzare un prototipo RAG notebook-based, sviluppato in Google Colab, capace di rispondere a domande su un corpus di documenti enterprise-like con citazioni, metadati e valutazione strutturata della qualità.

### Obiettivi specifici

Il progetto dovrà:

- costruire una piccola knowledge base multi-formato;
- organizzare il corpus in modo coerente e riutilizzabile;
- definire uno schema metadati minimo ma significativo;
- indicizzare i documenti in un sistema di retrieval;
- supportare query in linguaggio naturale;
- restituire risposte grounded con riferimenti alle fonti;
- supportare filtri basati su metadati;
- creare un benchmark iniziale di domande;
- valutare retrieval e qualità delle risposte;
- produrre una demo semplice ma chiara;
- documentare il progetto in modo portfolio-ready.

---

## 5. Ambito del progetto

### In scope

Rientrano nel progetto:

- raccolta e organizzazione di un corpus pubblico enterprise-like;
- uso di documenti multi-formato;
- preparazione e pulizia dei file;
- assegnazione di metadati ai documenti;
- upload e indicizzazione dei file;
- retrieval documentale;
- risposta con citazioni;
- benchmark query;
- evaluation del sistema;
- demo tecnica minimale;
- documentazione del progetto.

### Out of scope

Non rientrano nella prima versione:

- deployment production-grade;
- autenticazione utenti;
- architettura multi-tenant;
- OCR avanzato su documenti complessi;
- orchestrazione multi-agent;
- MLOps completo;
- frontend dedicato separato dal notebook;
- gestione enterprise di sicurezza, audit e access control.

Questa delimitazione è intenzionale: il progetto deve essere abbastanza realistico da essere credibile, ma abbastanza contenuto da poter essere completato e spiegato bene.

---

## 6. Visione funzionale del sistema

Il sistema finale dovrà consentire a un utente di inserire una domanda in linguaggio naturale e ottenere:

- una risposta sintetica e chiara;
- uno o più riferimenti alle fonti consultate;
- la possibilità di applicare filtri semplici sui documenti;
- una base di osservabilità minima sul comportamento del retrieval.

Dal punto di vista dell'utente, l'interazione dovrà sembrare quella con un assistente documentale.

Dal punto di vista del progettista, il sistema dovrà restare leggibile, spiegabile e misurabile.

---

## 7. Deliverable attesi

Al termine del progetto ci si aspetta di avere:

1. un repository GitHub ordinato e navigabile;
2. una struttura di notebook chiara e riutilizzabile;
3. un corpus documentale preparato e documentato;
4. uno schema metadati definito;
5. un prototipo RAG funzionante;
6. un benchmark di query;
7. un set iniziale di metriche e risultati;
8. una demo semplice;
9. documentazione tecnica e descrittiva del progetto;
10. una sezione esplicita sui limiti e sulle evoluzioni future.

---

## 8. Architettura logica di alto livello

Il progetto seguirà una pipeline logica composta da cinque blocchi principali:

### 1. Corpus layer
Raccolta, pulizia e organizzazione dei documenti.

### 2. Metadata layer
Classificazione dei documenti tramite attributi coerenti.

### 3. Retrieval layer
Indicizzazione e recupero dei contenuti rilevanti.

### 4. Answer layer
Generazione della risposta con grounding e citazioni.

### 5. Evaluation layer
Misurazione della qualità del retrieval e della risposta.

Questa separazione è utile perché consente di capire con precisione dove il sistema funziona e dove invece fallisce.

---

## 9. Workflow di riferimento del progetto

Questo workflow rappresenta la traccia ufficiale di sviluppo del progetto.

### Fase 1 — Definizione del caso d'uso

In questa fase si chiarisce:

- quale dominio documentale verrà usato;
- quale tipo di domande il sistema dovrà gestire;
- quale valore pratico si intende dimostrare;
- quali funzionalità minime rientrano nell'MVP.

**Output atteso:**
- definizione del dominio;
- definizione del perimetro;
- obiettivi MVP;
- criteri iniziali di successo.

### Fase 2 — Preparazione del corpus

In questa fase si raccolgono e organizzano i documenti.

Le attività principali includono:

- selezione del corpus iniziale;
- normalizzazione dei nomi file;
- verifica dei formati;
- rimozione di duplicati, file corrotti o irrilevanti;
- organizzazione in cartelle coerenti.

**Output atteso:**
- corpus pulito e utilizzabile;
- elenco documenti inclusi;
- struttura dati iniziale.

### Fase 3 — Definizione dei metadati

In questa fase si costruisce lo schema metadati da associare ai documenti.

Metadati minimi previsti:

- domain;
- doc_type;
- region;
- version;
- status;
- owner;
- language.

**Output atteso:**
- schema metadati definito;
- tabella metadati coerente per tutti i documenti.

### Fase 4 — Ingestion e indexing

In questa fase i documenti vengono caricati e resi interrogabili nel sistema di retrieval.

Le attività includono:

- creazione dello store o indice;
- upload dei file;
- associazione dei metadati;
- verifica della corretta indicizzazione;
- test iniziale di recupero.

**Output atteso:**
- knowledge base interrogabile;
- primo test funzionale del retrieval.

### Fase 5 — Querying e risposta grounded

In questa fase si costruisce la logica di interrogazione del corpus e di generazione della risposta.

Le attività includono:

- esecuzione di query di prova;
- analisi dei contenuti recuperati;
- costruzione di risposte con citazioni;
- verifica del comportamento con e senza filtri.

**Output atteso:**
- prime risposte affidabili;
- esempi di citazione;
- verifica della leggibilità della risposta.

### Fase 6 — Benchmark ed evaluation

In questa fase si misura la qualità del sistema in modo strutturato.

Le attività includono:

- creazione di un set di domande benchmark;
- classificazione delle query per difficoltà;
- esecuzione sistematica dei test;
- raccolta delle metriche;
- analisi dei failure modes.

**Output atteso:**
- benchmark iniziale;
- risultati misurabili;
- elenco errori ricorrenti e limiti osservati.

### Fase 7 — Demo e packaging portfolio

In questa fase il progetto viene rifinito e reso presentabile.

Le attività includono:

- costruzione della demo;
- pulizia dei notebook;
- organizzazione finale del repository;
- stesura del README;
- raccolta di screenshot, esempi e risultati.

**Output atteso:**
- repository portfolio-ready;
- demo funzionante;
- documentazione completa.

---

## 10. Workflow operativo sintetico

Il workflow complessivo può essere riassunto così:

1. Definire il problema e l'MVP.
2. Selezionare il corpus.
3. Preparare i documenti.
4. Assegnare i metadati.
5. Caricare e indicizzare i file.
6. Interrogare il sistema.
7. Generare risposte con fonti.
8. Eseguire benchmark ed eval.
9. Migliorare corpus, metadati e logica di risposta.
10. Preparare demo e documentazione finale.

Questo è il workflow che guiderà la realizzazione del progetto.

---

## 11. Strategia di valutazione

Il progetto non verrà valutato solo in base all'impressione soggettiva che le risposte "sembrino buone". La qualità dovrà essere giudicata in modo più disciplinato.

Le dimensioni principali di valutazione saranno:

- qualità del retrieval;
- groundedness della risposta;
- qualità delle citazioni;
- utilità dei metadati;
- trasparenza nei casi di fallimento;
- chiarezza della documentazione prodotta.

### Domande guida per la valutazione

- Il sistema recupera davvero documenti utili?
- La risposta è coerente con le fonti recuperate?
- Le citazioni aiutano a verificare la risposta?
- I filtri metadati migliorano il retrieval?
- Il sistema evita di inventare quando il corpus non basta?
- I limiti sono documentati in modo onesto?

---

## 12. Criteri di successo

Il progetto sarà considerato riuscito se, al termine dell'MVP, saranno soddisfatte queste condizioni:

- il corpus è organizzato e documentato;
- i metadati sono coerenti e applicati;
- il sistema risponde ad almeno un set base di query in modo grounded;
- le risposte mostrano riferimenti alle fonti;
- esiste un benchmark di valutazione;
- i risultati sono leggibili e spiegabili;
- il repository è abbastanza pulito da essere mostrato in portfolio.

Il successo del progetto non dipenderà dalla perfezione, ma dalla qualità del metodo e dalla trasparenza nell'analisi dei risultati.

---

## 13. Rischi e vincoli

### Vincoli principali

Il progetto sarà sviluppato in Google Colab per semplificare setup e sperimentazione. Questa scelta accelera lo sviluppo, ma introduce alcuni limiti:

- runtime temporanei;
- ambiente non persistente;
- dipendenze da reinstallare;
- variabilità dell'infrastruttura disponibile;
- minore controllo rispetto a un ambiente locale o cloud dedicato.

### Rischi principali

- corpus troppo piccolo o poco rappresentativo;
- metadati incoerenti;
- retrieval rumoroso;
- benchmark troppo debole;
- demo funzionante ma poco informativa;
- eccessiva dispersione su aspetti non essenziali.

### Strategia di mitigazione

Per ridurre questi rischi il progetto dovrà:

- partire con un MVP ristretto;
- fissare uno schema metadati semplice;
- usare un benchmark piccolo ma curato;
- migliorare una componente per volta;
- documentare sempre errori e limiti.

---

## 14. Valore formativo e di portfolio

Questo progetto ha valore non perché usa un LLM, ma perché obbliga a ragionare in modo strutturato su problemi reali di knowledge retrieval.

Le competenze che mira a rendere visibili sono:

- capacità di definire un problema applicativo concreto;
- capacità di progettare un corpus documentale utile;
- capacità di ragionare sui metadati e sul retrieval;
- capacità di costruire eval e benchmark;
- capacità di esplicitare i limiti del sistema;
- capacità di documentare un progetto in modo chiaro e professionale.

In questo senso il progetto deve essere letto non come una demo isolata, ma come una piccola esercitazione di engineering su un problema realistico.

---

## 15. Passi immediati successivi

A partire da questo documento, i prossimi passi operativi saranno:

1. definire in modo definitivo il dominio documentale dell'MVP;
2. creare la struttura iniziale del repository;
3. definire lo schema metadati;
4. raccogliere il primo corpus;
5. predisporre i notebook di setup e corpus preparation.

Questi passi rappresentano l'avvio concreto del lavoro.

---

## 16. Stato del documento

Questo documento costituisce la base descrittiva e metodologica del progetto.

Il suo ruolo è:

- fissare l'intento del progetto;
- definire il workflow di riferimento;
- chiarire scope, obiettivi e deliverable;
- guidare in modo coerente le prime fasi di sviluppo.

Non sostituisce il README tecnico del repository, ma lo precede e lo orienta.

In altre parole, questo documento definisce **che cosa si intende costruire, perché lo si vuole costruire e come si intende procedere**.

