# MisuraLab

Web app per preparare studenti della prima classe del liceo scientifico a una verifica sulle misure e le grandezze.

## Contenuti

| Attività | Numero |
| --- | ---: |
| Scelta multipla, con cinque alternative | 60 |
| Risposte aperte, con soluzione modello e rubrica | 40 |
| Esercizi di calcolo, con spiegazione | 80 |
| Totale | 180 |

Argomenti: materia e livelli di indagine, Sistema Internazionale, proprietà intensive ed estensive, equivalenze, notazione scientifica, strumenti ed errori di misura, cifre significative, volume e capacità, massa e peso, temperatura e calore, densità e peso specifico.

La banca è composta da esercizi originali basati sugli argomenti del materiale didattico fornito. Il PDF di riferimento non è distribuito nel repository.

## Uso

Aprire [MisuraLab online](https://mich090909.github.io/misuralab/), oppure aprire `index.html` nel browser. Non sono richiesti installazione, compilazione o account degli studenti. L'app funziona anche offline.

- Filtri per argomento, tipologia, livello e attività da ripassare.
- Correzioni delle scelte multiple e dei risultati numerici.
- Controllo delle cifre significative, dei decimali e della notazione scientifica nei quesiti che lo richiedono.
- Soluzioni modello e quattro criteri di autovalutazione per ogni domanda aperta.
- Simulazione: 20 quesiti (8 a scelta multipla, 8 calcoli, 4 aperti), 40 minuti, correzioni dopo la consegna.
- Formulario, segnalibri, salvataggio locale dei progressi ed esportazione JSON.
- Stampa delle attività filtrate, con o senza soluzioni.

## Criteri di correzione

Le risposte aperte **non vengono valutate automaticamente**: lo studente confronta la propria risposta con il modello e applica una rubrica di autovalutazione, fino a 10 punti. Formulazioni equivalenti, se corrette, sono valide. I punteggi hanno finalità di allenamento e non sostituiscono il giudizio del docente.

Nei calcoli, l'unità richiesta è indicata accanto alla casella e non va digitata. Sono accettate la virgola e il punto decimale, oltre a forme come `2,5e-3` e `2,5 × 10^-3`. Il confronto numerico usa una tolleranza relativa di 10^-10 per gestire le approssimazioni del calcolo informatico. Dove richiesto, il valore corretto deve anche rispettare il numero di cifre significative o di decimali indicato.

Per le serie di misure, l'errore assoluto è calcolato come semidispersione, secondo il metodo del capitolo di riferimento; questa convenzione non vale automaticamente per ogni misurazione.

## Dati e privacy

L'app non richiede nomi o indirizzi e-mail e non contiene servizi di analisi, librerie esterne o richieste di rete. Risposte e progressi restano nel browser del dispositivo, se il salvataggio locale è consentito. Il gestore del servizio di hosting può trattare i normali dati tecnici di accesso al sito. Il PDF del libro e dati reali degli studenti non sono presenti nei file distribuiti.

## Verifiche effettuate

- Conteggio e identificatori univoci delle 180 attività.
- Cinque alternative distinte e una sola chiave per ciascuna scelta multipla.
- Distribuzione delle risposte corrette: 12 in ciascuna delle cinque posizioni.
- Ricalcolo indipendente di tutti gli 80 risultati numerici.
- Test di correzione, parser numerico, arrotondamenti, autovalutazione, filtri, salvataggio e simulazione, incluso il timeout.

L'app pubblicata è stata collaudata anche nel browser Chrome: caricamento e interfaccia desktop, correzione della scelta multipla, controllo di 7,7 rispetto a 7,70, salvataggio dell'autovalutazione e avvio/consegna della simulazione. I test completi della logica sono stati eseguiti con un ambiente DOM simulato. La visualizzazione su smartphone non è stata collaudata direttamente.

## Struttura

- `index.html`: app completa, con stile, codice e banca incorporati.
- `.nojekyll`: file vuoto per la pubblicazione statica.
- `README.md`: descrizione e criteri di utilizzo.

La pubblicazione di questo pacchetto rende leggibile anche il codice incorporato e la banca di soluzioni. L'app è uno strumento di preparazione, non una piattaforma per somministrare prove riservate.
