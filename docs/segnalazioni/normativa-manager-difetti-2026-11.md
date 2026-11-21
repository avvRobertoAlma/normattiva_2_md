# Normativa manager: atti rimasti in coda e difetti da correggere

Data: 16/11/2026. Verifica fatta sulla coda «Da approvare» di normativa.buddalaw.com (versione del codice `d6d36fc8af82`).

## In breve

Oggi sono stati approvati e pubblicati in ricerca 60 atti (6911 articoli). In «Da approvare» restano 23 atti:

- 21 non si possono approvare, perché il testo importato da Normattiva non è utilizzabile. Sono però gli atti più richiesti dagli utenti: insieme valgono circa 495 richieste.
- 2 sono importati bene e sono stati lasciati fuori solo per il costo.

Per sbloccare i 21 servono tre correzioni all'importazione. In più ci sono due problemi minori emersi durante i lavori.

| # | Problema | Atti colpiti | Richieste degli utenti |
|---|----------|--------------|------------------------|
| 1 | Atti abrogati importati con la sola riga di abrogazione | 4 | circa 150 |
| 2 | Leggi di bilancio a maxi-articolo tagliate in blocchi da 100 commi | 11 | 238 |
| 3 | Leggi finanziarie importate con i soli allegati | 6 | 106 |
| 4 | Connessioni al database esaurite durante le sintesi | 1 lavoro | — |
| 5 | Articoli pubblicati che il motore di ricerca non conferma | 1 atto | — |
| 6 | Inserimento a mano: articoli con numeri romani non riconosciuti | Costituzione (disp. trans. I–XVIII) | — |
| 7 | Inserimento a mano: una riga fra parentesi sotto «Art. N» diventa la rubrica | ogni atto a mano | — |
| 8 | «Atti mancanti» elenca come da inserire atti già in ricerca | Costituzione | 281 |
| 9 | La conferma della spesa è una finestra nativa del browser | approvazioni | — |
| 10 | «Approva gli atti spuntati» ha approvato tutti gli atti in coda, non solo quelli spuntati | approvazioni | — |
| 11 | Non c'è modo di togliere dalla ricerca una fonte pubblicata per errore | d.P.R. 43/1973 | — |

I tre atti che da soli sbloccano più domanda sono il d.lgs. 50/2016, la l. 160/2019 e la l. 296/2006: 259 richieste.

## Che cosa è stato fatto oggi

| Lotto | Lavori | Atti | Articoli in ricerca |
|-------|--------|------|---------------------|
| Primo | #22, #23 | 39 | 3813 |
| Secondo | #24, #25 | 6 | 1886 |
| Terzo | #26 | 15 | 1212 |
| Totale | | 60 | 6911 |

Per ogni atto sono stati verificati il testo degli articoli e il dominio prima dell'approvazione. Circa un quarto delle sintesi è marcato «parziale», perché gli articoli rinviano ad atti non ancora presenti: si potranno rifare quando quegli atti entrano.

## 1. Atti interamente abrogati (4 atti)

**Che cosa succede.** Per un atto abrogato per intero, Normattiva nella versione vigente restituisce per ogni articolo la sola riga «PROVVEDIMENTO ABROGATO DAL …». Il manager la importa come testo dell'articolo, conta l'articolo come vigente (0 abrogati) e mette come «in vigore dal» la data dell'abrogazione. Il preventivo propone una sintesi a pagamento per ogni riga.

| Fonte | Atto | Abrogato da | Dal | Richieste | Sintesi proposte |
|-------|------|-------------|-----|-----------|------------------|
| `/fonti/177/` | d.lgs. 50/2016, codice dei contratti pubblici | d.lgs. 36/2023 | 01/07/2023 | 132 | 222 |
| `/fonti/174/` | d.lgs. 163/2006, vecchio codice appalti | d.lgs. 50/2016 | 19/04/2016 | 13 | 274 |
| `/fonti/270/` | d.P.R. 43/1973, testo unico doganale | d.lgs. 141/2024 | 04/10/2024 | 3 | 371 |
| `/fonti/221/` | d.lgs. 626/1994, sicurezza sul lavoro | d.lgs. 81/2008 | 15/05/2008 | 2 o 3 | 173 |

**Che cosa serve.**

- Riconoscere l'atto abrogato per intero (tutti gli articoli con la stessa riga di abrogazione) e scaricare da Normattiva il testo vigente al giorno precedente l'abrogazione.
- Marcare la fonte e gli articoli come abrogati, con data e atto abrogante, in modo che la ricerca li trovi ma li mostri come non più in vigore.
- Non proporre sintesi per gli articoli il cui testo è la sola riga di abrogazione.

**Perché conta.** Il d.lgs. 50/2016 è l'atto più richiesto di tutta la coda: si applica ancora alle gare bandite prima del 1° luglio 2023.

**Nota.** Dove sono abrogati solo singoli articoli il manager si comporta bene: li marca «abrogato» e li esclude dal preventivo.

## 2. Leggi di bilancio a maxi-articolo (11 atti)

**Che cosa succede.** L'articolo 1 (centinaia o più di mille commi) viene tagliato in blocchi da 100 commi. Ogni blocco si chiama «art. 1», non ha rubrica e pesa da 60 a 150 mila caratteri. Una sintesi e un vettore per blocco non permettono di trovare un comma.

Esempio, `/fonti/216/` (l. 160/2019): 9 blocchi «Art. 1», che iniziano ai commi 1, 101, 201 … 801, da 58 a 98 mila caratteri l'uno. Seguono gli articoli da 2 in poi, che sono gli stati di previsione dei ministeri.

| Fonte | Atto | Richieste | Blocchi oggi |
|-------|------|-----------|--------------|
| `/fonti/216/` | l. 160/2019, bilancio 2020 | 65 | 27 |
| `/fonti/176/` | l. 296/2006, finanziaria 2007 | 62 | 14 |
| `/fonti/229/` | l. 145/2018, bilancio 2019 | 29 | 30 |
| `/fonti/223/` | l. 205/2017, bilancio 2018 | 27 | 30 |
| `/fonti/243/` | l. 197/2022, bilancio 2023 | 15 | 29 |
| `/fonti/211/` | l. 178/2020, bilancio 2021 | 9 | 31 |
| `/fonti/193/` | l. 662/1996, collegato alla finanziaria 1997 | 9 | 5 |
| `/fonti/198/` | l. 232/2016, bilancio 2017 | 6 | 25 |
| `/fonti/186/` | l. 244/2007, finanziaria 2008 | 6 | 12 |
| `/fonti/209/` | l. 234/2021, bilancio 2022 | 5 | 32 |
| `/fonti/207/` | l. 266/2005, finanziaria 2006 | 5 | 7 |

Nella l. 662/1996 il difetto riguarda anche gli articoli 2 e 3 (fino a 159 mila caratteri).

**Che cosa serve.**

- Dividere per comma quando un articolo supera una soglia di lunghezza, oppure per gruppi di pochi commi, con il numero del comma nell'identificativo e nel titolo («art. 1, comma 345»).
- Conservare il rinvio al comma nei collegamenti in entrata: gli altri atti citano «articolo 1, comma N».
- Valutare se escludere dalle sintesi gli articoli sugli stati di previsione dei ministeri, che non hanno contenuto utile alla ricerca giuridica.

**Nota.** Lo stesso limite, in piccolo, tocca gli atti già approvati: circa 35 articoli molto lunghi (oltre 30 mila caratteri) in finanziarie e decreti omnibus hanno una sintesi sola. Esempi: art. 119 del d.l. 34/2020, art. 59 della l. 449/1997, art. 17 della l. 127/1997. Con la divisione per comma andrebbero rifatti.

## 3. Leggi finanziarie importate con i soli allegati (6 atti)

**Che cosa succede.** Per sei leggi il manager ha solo allegati, tabelle ed elenchi. Il testo degli articoli manca del tutto. Gli allegati sono numerati come articoli, e allegati ed elenchi con lo stesso numero si sovrappongono (due «Art. 1», due «Art. 2»).

| Fonte | Atto | Richieste | Che cosa c'è oggi |
|-------|------|-----------|-------------------|
| `/fonti/220/` | l. 147/2013, stabilità 2014 | 43 | 5 allegati, 2 elenchi |
| `/fonti/191/` | l. 190/2014, stabilità 2015 | 26 | 10 allegati, 1 tabella |
| `/fonti/241/` | l. 311/2004, finanziaria 2005 | 14 | 7 allegati |
| `/fonti/187/` | l. 208/2015, stabilità 2016 | 13 | 7 allegati, 3 elenchi |
| `/fonti/250/` | l. 350/2003, finanziaria 2004 | 5 | 2 allegati, 1 tabella |
| `/fonti/264/` | l. 549/1995, collegato alla finanziaria 1996 | 5 | 1 allegato |

**Che cosa serve.**

- Capire perché lo scaricamento ha perso l'articolato e riscaricare le sei leggi.
- Distinguere allegati, tabelle ed elenchi dagli articoli, con un identificativo proprio.
- Non mandare alla sintesi gli allegati il cui testo è solo «Parte di provvedimento in formato grafico».
- Una volta riscaricate, queste leggi ricadono nel problema 2 (maxi-articolo).

**Perché non approvarle così.** Chi cerca un comma troverebbe l'atto, ma solo con le tabelle: peggio che non averlo.

## 4. Connessioni al database esaurite

Nel lavoro #22 (39 atti, 3813 sintesi) 38 sintesi del r.d. 773/1931 sono fallite con:

```
connection failed: connection to server at "172.18.0.2", port 5432 failed: FATAL: sorry, too many clients already
```

Tutte le altre sono riuscite e il rilancio (lavoro #23) ha chiuso le 38 mancanti in un minuto. Nei lavori successivi, lanciati uno alla volta, l'errore non si è ripetuto. Serve un limite alle connessioni contemporanee dei worker, o un pool, e un nuovo tentativo automatico su questo errore.

## 5. Articoli pubblicati che il motore di ricerca non conferma

Nel lavoro #26 il d.lgs. 181/2000 (`/fonti/247/`) risulta pubblicato, ma il confronto finale dice: «il motore di ricerca ne ha 0, il manager ne ha pubblicati 2». Gli articoli sono l'1-bis e il 4-bis, gli unici in vigore (gli altri cinque sono abrogati). La scheda della fonte la dà comunque «in ricerca».

Un tentativo di rilanciare «Pubblica in ricerca» dalla scheda non ha creato alcun lavoro. Da verificare se i due documenti sono davvero assenti dall'indice e perché la ripubblicazione non parte.

## Atti importati bene e lasciati fuori (2 atti)

| Fonte | Atto | Richieste | Sintesi |
|-------|------|-----------|---------|
| `/fonti/225/` | d.lgs. 66/2010, codice dell'ordinamento militare | 13 | 2337 |
| `/fonti/280/` | r.d. 1775/1933, testo unico acque e impianti elettrici | 1 | 230 |

Si possono approvare in qualsiasi momento: è solo una questione di spesa rispetto alla domanda.

## Aggiornamento del 20/11/2026

Oggi sono entrati in ricerca altri 43 atti (lavoro #36, 2134 articoli, tutto in pari). Sono emersi quattro difetti nuovi.

### 6. Numeri romani non riconosciuti nell'inserimento a mano

Il riconoscimento degli articoli accetta solo numeri arabi, anche con «-bis». «Art. I», «Art. XIII», «Disposizione I» non vengono riconosciuti, e il loro testo finisce in coda all'articolo precedente. Per questo la Costituzione (`/fonti/294/`) ha i 139 articoli ma non le **disposizioni transitorie e finali I–XVIII**: la XII (divieto di ricostituire il partito fascista) e la XIII (Casa Savoia) sono citate.

**Che cosa serve.** Accettare i numeri romani come identificativo dell'articolo (per la Costituzione con un identificativo distinto, es. «disp. trans. XIII»), poi reinserire le 18 disposizioni.

### 7. Riga fra parentesi letta come rubrica

Nell'inserimento a mano una riga fra parentesi subito sotto «Art. N» diventa la rubrica. Per un articolo abrogato scritto «(Articolo abrogato dalla legge costituzionale …)» la rubrica si prende tutto il testo e l'articolo risulta vuoto. Va almeno detto nella guida della pagina; meglio riconoscere come rubrica solo una riga breve.

### 8. «Atti mancanti» non vede la Costituzione già in ricerca

La Costituzione è in ricerca dal 16/11 (`/fonti/294/`, `urn:nir:stato:costituzione:1947-12-27;const`), ma «Atti mancanti» la elenca ancora come «da controllare a mano» con 281 richieste, in cima a tutte. Probabilmente le richieste degli utenti non vengono abbinate alla fonte inserita a mano.

**Nota (non del manager).** Le 281 richieste hanno anche un'altra causa: la ricerca MCP rifiutava i domini `constitutional`, `administrative` ed `eu_law`. È corretto nel backend con la PR #1273.

### 9. Conferma della spesa in una finestra nativa

«Approva gli atti spuntati» chiede conferma con una finestra nativa del browser (`confirm`). Quando la pagina è pilotata da un'automazione, la finestra si chiude da sola e l'approvazione non parte, senza nessun messaggio. Una conferma dentro la pagina (un riquadro con il preventivo e il bottone «Conferma») sarebbe più chiara anche per le persone e mostrerebbe il numero di sintesi.

### 10. L'approvazione ha preso tutti gli atti in coda

Il 20/11 alle 14:55 erano spuntati 40 atti (2299 sintesi), ma il clic su «Approva gli atti spuntati» ha avviato il lavoro #43 «Approvazione (69 atti)», cioè tutto ciò che c'era in «Da approvare»: anche gli atti abrogati del problema 1, le leggi di bilancio dei problemi 2 e 3 e il d.lgs. 66/2010 (2337 sintesi). Il lavoro è stato fermato a mano dopo 849 sintesi; tra queste le 371 del d.P.R. 43/1973, abrogato. Il d.P.R. 495/1992 è rimasto a metà (253 sintesi su 406, nessuna pubblicata). Una causa possibile è che le spunte si siano perse ricaricando la pagina e che una richiesta senza fonti selezionate venga letta come «tutte»; non l'abbiamo verificato. La ripetizione con 36 atti spuntati (lavoro #44) ha preso solo quelli. Servirebbe: (a) con nessuna fonte selezionata, rifiutare la richiesta invece di approvare tutto; (b) mostrare nella conferma il numero di atti e di sintesi effettivamente inviati.

### 11. Nessun modo di togliere una fonte dalla ricerca

Nella pagina della fonte ci sono solo «Riprendi il testo», «Scrivi le sintesi mancanti» e «Pubblica in ricerca». Il d.P.R. 43/1973 (fonte 270), abrogato, ora è in ricerca con 371 articoli «PROVVEDIMENTO ABROGATO»; serve un'azione «Togli dalla ricerca» (cancellazione dei documenti da OpenSearch), utile anche per gli altri abrogati.

## Ordine suggerito

1. Problema 1, a partire dal d.lgs. 50/2016.
2. Problema 2, a partire dalle leggi 160/2019 e 296/2006.
3. Problema 3, a partire dalla l. 147/2013.
4. Problemi 4 e 5.
5. Problemi 10 e 11, subito: il 10 ha già fatto spendere sintesi inutili.
6. Problemi 6 e 8 (Costituzione), poi 7 e 9.

Dopo ogni correzione gli atti vanno riscaricati e ricontrollati prima dell'approvazione, perché il numero di sintesi cambierà.
