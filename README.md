# Il verificatore

**L'IA dice. Le fonti decidono.**

Un laboratorio interattivo, gratuito e completamente autonomo nel browser per esercitarsi a **controllare le affermazioni prodotte dall'intelligenza artificiale** attraverso documenti di riferimento. È utilizzabile da singoli, gruppi di lavoro, formatori, biblioteche e organizzazioni che desiderano allenare il controllo delle fonti e il pensiero critico.


<img width="1231" height="785" alt="Screenshot 2026-10-22 alle 20 21 54" src="https://github.com/user-attachments/assets/ef321ac7-9a66-43b6-a9b5-575ce262c581" />


Il progetto è un sito statico: non richiede iscrizione, credenziali, API, servizi di IA o un server applicativo.

## In breve

- **3 fascicoli simulati**: contributi economici, segnalazioni di manutenzione stradale ed eventi culturali.
- **15 affermazioni** da verificare, una per una.
- Per ogni affermazione: **Confermata**, **Smentita** oppure **Non dimostrata**, più selezione della fonte decisiva.
- **Documenti con versioni differenti**, per esercitarsi a distinguere testi definitivi da bozze non approvate o superate.
- **Nota del revisore** e **debrief** con spiegazioni e possibile testo corretto.
- **Riepilogo finale** scaricabile in `.txt`.
- **Timer facoltativo** di 30 minuti, navigazione libera tra i fascicoli e interfaccia responsive.
- Nessuna dipendenza esterna; funziona **offline**.

## Avvio rapido

### Sul proprio computer

1. Scarica `index.html`.
2. Aprilo con un browser recente (Chrome, Firefox, Edge o Safari).
3. Premi **Inizia la verifica**.

Non serve installare nulla.

### Sul Github Pages

https://gigicogo.github.io/verificatore-pa/

## Come funziona

1. Seleziona un fascicolo.
2. Esamina le cinque frasi presenti nella bozza dell'assistente IA.
3. Sfoglia i documenti sulla destra (sugli schermi più piccoli, nella stessa schermata sotto le frasi).
4. Per ogni frase scegli un esito e indica il documento che lo sostiene o lo contraddice. Se le fonti non consentono di stabilire il punto, scegli **Non dimostrata** e **Nessuna fonte sufficiente**.
5. Aggiungi, se vuoi, una breve nota su come correggeresti il testo.
6. Premi **Verifica il fascicolo** per leggere le soluzioni commentate.
7. Nel riepilogo finale puoi scaricare un report locale in formato testo.

Puoi tornare alle risposte e cambiarle dopo il feedback. Il punteggio è **puramente orientativo**: un punto per l'esito e uno per la fonte di ogni affermazione. Non è un test certificativo.

## Cosa si impara

L'applicazione allena alcune abitudini utili quando si leggono contenuti generati dall'IA:

- separare una **frase plausibile** da una frase **supportata da una fonte**;
- controllare **date, versioni, soglie, importi e condizioni**;
- distinguere **presa in carico**, **valutazione** ed **esecuzione di un intervento**;
- non trasformare l'assenza di informazioni in una conclusione arbitraria;
- motivare una revisione prima di riutilizzare un contenuto.

## Documenti simulati: avvertenza importante

**Tutte le persone, gli enti, i procedimenti, le FAQ, gli avvisi e i documenti presenti nell'applicazione sono fittizi.** Il Comune di Vallechiara è inventato. Numeri, soglie economiche, scadenze e tempi hanno esclusivamente valore di esercitazione.

Non utilizzare i contenuti come indicazioni amministrative, regole reali, pareri legali o fonti normative. In situazioni reali consulta la documentazione ufficiale e le procedure applicabili.

## Privacy e funzionamento offline

- L'applicazione **non effettua chiamate di rete**, non utilizza analytics e non invia risposte a un server.
- Le scelte restano **nella memoria della pagina** e si perdono ricaricandola o chiudendola.
- Il report `.txt` viene creato **nel browser** e viene salvato soltanto se l'utente sceglie di scaricarlo.
- Le note inserite compaiono nel report esportato: **non inserirvi dati personali reali**.

## Personalizzazione

Tutti i materiali e la logica del gioco sono contenuti in `index.html`.

- **Contenuti:** modifica l'array JavaScript `DOSSIERS` (documenti, affermazioni, riscontri, testo corretto).
- **Aspetto:** modifica le variabili CSS in `:root`.
- **Durata:** la configurazione iniziale del timer si trova nella proprietà `timer.secs` (valore predefinito: `1800`, ossia 30 minuti).
- **Punteggio:** modifica la funzione `score()`.

Per ogni affermazione, `verdict` assume uno dei valori `yes`, `no`, `unknown`. La proprietà `source` contiene l'ID del documento di riferimento oppure `none` per l'assenza di una fonte sufficiente. Verifica che gli ID citati nelle risposte corrispondano a quelli dei documenti del fascicolo.

## Struttura del progetto

```text
il-verificatore/
├── index.html   # applicazione completa: HTML, CSS, JavaScript e dati simulati
└── README.md    # documentazione
```

## Accessibilità

La pagina utilizza pulsanti, etichette e controlli HTML standard; supporta la navigazione da tastiera, indicatori di focus visibili e layout adattabile. Se apporti modifiche, prova sempre l'interfaccia anche con tastiera e su schermi piccoli.

## Riutilizzo

Il progetto può essere riutilizzato da chiunque. Non reclamo nessun diritto

---

**Principio di fondo:** un testo sicuro da riutilizzare non è soltanto un testo ben scritto: è un testo le cui affermazioni rilevanti sono state controllate sulle fonti giuste.

## Risorse collegate
---
Se questi materiali ti sono utili, puoi seguire anche il resto del lavoro che faccio su AI generativa e divulgazione:

- **Newsletter** – https://gigicogo.substack.com - approfondimenti, casi d’uso e strumenti su AI generativa e content creation.  
- **Articoli** – https://webeconoscenza.gigicogo.it - guide e riflessioni su Medium / blog, con esempi pratici di utilizzo delle skill.  
- **Video e podcast** – https://www.youtube.com/@gigicogo - Guide, interviste e tutorial su IA Generativa.
