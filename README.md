# Pizza Tools

Una piccola applicazione web per calcolare ingredienti e tempi di preparazione degli impasti per pizza.

Il progetto comprende due calcolatori:

- **Pizza napoletana al 65% di idratazione**, con gestione di panetti baby e standard;
- **Pizza in teglia al 72% di idratazione**, con dosi totali e quantità per singola teglia.

## Funzionalità

- calcolo automatico di farina, acqua, sale, lievito e, per la teglia, olio EVO;
- pianificazione a ritroso a partire dalla data e dall'ora di cottura;
- stima del lievito fresco in base ai tempi di maturazione e fermentazione;
- suddivisione dell'acqua tra autolisi e impasto finale;
- margine extra configurabile;
- avvisi operativi e riepilogo stampabile;
- interfaccia adatta anche a smartphone;
- disponibilità offline dopo il primo caricamento, tramite service worker.

## Utilizzo

Apri **[Pizza Tools](https://alvarochi.github.io/pizza-calc/)** nel browser e scegli il calcolatore desiderato. Modificando i valori di input, ricetta e calendario operativo vengono aggiornati automaticamente.

Le quantità e le tempistiche ottenute sono indicazioni pratiche: temperatura, farina, lievito e condizioni ambientali possono influire sul risultato. È quindi consigliabile adattarle alla propria esperienza e al proprio impasto.

## Esecuzione in locale

Non sono richieste dipendenze né una procedura di compilazione. È sufficiente servire la cartella con un qualsiasi server HTTP statico, per esempio con Python:

```bash
python -m http.server 8000
```

Poi visita `http://localhost:8000`.

> Il service worker non funziona aprendo direttamente i file con il protocollo `file://`; per provare la modalità offline occorre usare `localhost` o HTTPS.

## Struttura del progetto

| File | Descrizione |
| --- | --- |
| `index.html` | Pagina iniziale e selezione del calcolatore |
| `calcolatore-napoletana.html` | Calcolatore per pizza napoletana al 65% |
| `calcolatore-teglia.html` | Calcolatore per pizza in teglia al 72% |
| `manifest.json` | Configurazione della Progressive Web App |
| `service-worker.js` | Cache dei file per l'utilizzo offline |
| `icons/` | Risorse per le icone dell'app |

## Tecnologie

Il progetto usa soltanto HTML, CSS e JavaScript, senza framework o dipendenze esterne.

## Contributi

Segnalazioni di problemi e proposte di miglioramento sono benvenute tramite le issue e le pull request del repository.
