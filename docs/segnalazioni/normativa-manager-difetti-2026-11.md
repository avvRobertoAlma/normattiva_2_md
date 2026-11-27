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
| 12 | Modifiche riportate da Normattiva solo in nota: in ricerca va il testo superato (art. 654 c.p.c. col «pretore», pene del c.p. in lire) | 139 articoli in 50 atti (127 già in ricerca) | — |

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

## Aggiornamento del 24/11/2026

### 12. Modifiche che Normattiva riporta solo in nota: testo «vigente» non aggiornato

**Il caso.** Un cliente ha segnalato due volte (ottobre e 23/11) un parere sull'art. 654 c.p.c. che cita come vigente il «decreto del conciliatore, del pretore o del presidente». Il testo viene così da Normattiva, ed è uguale in ogni formato: pagina del testo vigente, tutte le versioni dell'articolo nel tempo, esportazione Akoma Ntoso. L'art. 103 del d.lgs. 51/1998 ha sostituito «del giudice di pace, del pretore o del presidente» con «del giudice che ha pronunciato l'ingiunzione», ma il codice diceva «conciliatore»: le parole non coincidevano e Normattiva non ha applicato la modifica. La riporta solo nella nota «AGGIORNAMENTO (88)». Il manager toglie le note, quindi in ricerca va il testo superato, e la sintesi AI è scritta su quel testo. Anche `search_articles` della MCP restituisce oggi l'art. 654 col «pretore».

**Quanto è esteso.** Scansione del 24/11/2026 su tutte le 470 fonti del manager che hanno un URN (40.259 articoli, sola lettura da Normattiva, nessuna sintesi), poi verificata a mano: **139 articoli in 50 atti**. Di questi, 127 articoli in 44 atti sono già in ricerca; 12 articoli in 6 atti sono in «Da approvare» (i testi unici tributari del 2027). Nessuno è fra le fonti di contesto. Esempi:
- pene e sanzioni ancora in lire: codice penale (artt. 588 rissa, 625 furto aggravato, 628 rapina, 639 imbrattamento, 646 appropriazione indebita), l. 110/1975 sulle armi, codice della navigazione (21 articoli), d.P.R. 1124/1965, art. 52 d.lgs. 151/2001;
- d.P.R. 600/1973, art. 25: ritenuta d'acconto sui compensi dei professionisti al «15 per cento» (vigente: 20 per cento, l. 449/1997). Il modello di produzione, con quel testo, risponde 15%;
- codice civile: «patria potestà» (artt. 343, 348, 350, 356, 417), «figli naturali» (artt. 580, 594), art. 2465;
- art. 8 d.l. 138/2011: l'elenco delle materie escluse dalla contrattazione di prossimità senza i licenziamenti in gravidanza e per congedo;
- ministeri e uffici soppressi, accise dei tabacchi ferme ai valori originari (art. 39-octies d.lgs. 504/1995).

**Come si riconosce.** La nota è richiamata nel testo, per esempio «(88)», e contiene la formula fissa «le parole "X" sono sostituite dalle seguenti: "Y"» (anche al singolare, «la parola … è sostituita dalla seguente»), «sono soppresse» oppure «dopo le parole … sono inserite le seguenti …». La modifica non è applicata se il testo atteso non c'è. Tre cautele, emerse dalla verifica a mano:
1. **catene**: se una nota successiva cambia le parole introdotte da una precedente, le due modifiche si compongono. Nell'art. 6 d.lgs. 471/1997 il 2020 porta la sanzione al 90%, il 2024 al 70%, e nel testo c'è già «settanta»: nessun difetto. Nell'art. 628 c.p. il 2017 e il 2019 non sono applicati: vanno segnalati tutti e due;
2. **modifiche future**: non si segnala una modifica la cui nota, o una nota dello stesso atto, ha una data futura (art. 51 r.d. 12/1941, tribunale per le persone, i minorenni e le famiglie rinviato al 18/10/2027). La data va cercata fuori dalle parole sostituite: «31 dicembre 2028» nell'art. 8 d.lgs. 152/2006 è il nuovo termine, non la decorrenza;
3. **note di altri articoli**: si escludono le novelle che nominano un articolo diverso.

Falso allarme noto: art. 573 c.c., già riscritto in altro modo. La regola è nel backend (PR avvRobertoAlma/buddalaw-backend#1354, `unapplied_amendments` in `api/components/normattiva_fetcher.py`): il manager può usare la stessa.

**Che cosa servirebbe nel manager.**
1. All'importazione e a ogni aggiornamento, segnare l'articolo come «testo non aggiornato», con la nota.
2. Dare al modello che scrive la sintesi anche la nota, con l'istruzione di applicare la modifica. In alternativa, mettere l'articolo in una coda «da correggere a mano» dove si scrive il testo corretto, controllato sulla Gazzetta Ufficiale (l'inserimento a mano esiste già).
3. Nell'indice, pubblicare il testo corretto, o almeno l'avviso in testa al testo, così lo vedono anche la MCP e la v3, che sceglie le fonti dalla sintesi.
4. Rifare le sintesi dei 127 articoli già in ricerca (spesa piccola) e controllare i 12 in «Da approvare» prima dell'approvazione.
5. Farlo prima che il codice penale entri in ricerca (PR backend #1097): altrimenti la ricerca darà come vigenti pene in lire.

Il controllo delle modifiche di Normattiva non segnalerà mai questi articoli, perché per Normattiva la modifica è già registrata.

**Elenco completo** (fonte nel manager, stato, numero di articoli, articoli):

| Fonte | Stato | N. | Articoli |
|---|---|---|---|
| `/fonti/245/` Regio Decreto 327/1942 | in ricerca | 21 | 1162, 1163, 1164, 1169, 1170, 1171, 1178, 1179, 1180, 1193, 1196, 1198, 1199, 1200, 1201, 1204, 1207, 1208, 1209, 1211, 1213 |
| `/fonti/18/` Codice Civile | in ricerca | 12 | 252, 343, 348, 350, 356, 401, 417, 468, 573, 580, 594, 2465 |
| `/fonti/49/` Decreto Legislativo 152/2006 | in ricerca | 10 | 3, 8, 13, 32-bis, 224, 252, 275, 279, 281, 298 |
| `/fonti/263/` Decreto del Presidente della Repubblica 309/1990 | in ricerca | 7 | 31, 35, 41, 46, 47, 54, 70 |
| `/fonti/297/` Decreto Legislativo 173/2024 | da approvare | 6 | 30, 31, 33, 36, 37, 67 |
| `/fonti/432/` Legge 110/1975 | in ricerca | 6 | 4, 10, 15, 19, 22, 23 |
| `/fonti/372/` Decreto del Presidente della Repubblica 495/1992 | in ricerca | 5 | 10, 11, 12, 13, 16 |
| `/fonti/17/` Codice Penale | in ricerca | 5 | 588, 625, 628, 639, 646 |
| `/fonti/14/` Codice di Procedura Civile | in ricerca | 5 | 67, 118, 137, 654, 769 |
| `/fonti/48/` Decreto Legislativo 58/1998 | in ricerca | 4 | 83-sexies, 147-ter, 190, 194-bis |
| `/fonti/52/` Decreto Legislativo 81/2008 | in ricerca | 4 | 26, 137, 222, 232 |
| `/fonti/214/` Decreto del Presidente della Repubblica 1124/1965 | in ricerca | 3 | 139, 175, 246 |
| `/fonti/21/` Decreto del Presidente della Repubblica 380/2001 | in ricerca | 3 | 44, 46, 48 |
| `/fonti/55/` Decreto Legislativo 285/1992 | in ricerca | 3 | 95, 107, 123 |
| `/fonti/8/` Decreto del Presidente della Repubblica 600/1973 | in ricerca | 2 | 23, 25 |
| `/fonti/6/` Decreto del Presidente della Repubblica 602/1973 | in ricerca | 2 | 19, 43-ter |
| `/fonti/4/` Decreto del Presidente della Repubblica 917/1986 | in ricerca | 2 | 10, 47 |
| `/fonti/227/` Decreto Legge 138/2011 | in ricerca | 2 | 1, 8 |
| `/fonti/199/` Decreto Legge 98/2011 | in ricerca | 2 | 12, 21 |
| `/fonti/234/` Decreto Legislativo 471/1997 | in ricerca | 2 | 9, 11 |
| `/fonti/30/` Decreto Legislativo 36/2023 | in ricerca | 2 | 67, 202 |
| `/fonti/300/` Decreto Legislativo 123/2025 | da approvare | 2 | 110, 112 |
| `/fonti/200/` Regio Decreto 773/1931 | in ricerca | 2 | 28, 109 |
| `/fonti/196/` Decreto Legge 78/2010 | in ricerca | 1 | 47 |
| `/fonti/206/` Decreto Legge 95/2012 | in ricerca | 1 | 16-bis |
| `/fonti/24/` Decreto Legge 77/2021 | in ricerca | 1 | 46 |
| `/fonti/365/` Decreto Legge 21/2022 | in ricerca | 1 | 17 |
| `/fonti/342/` Decreto Legislativo 504/1995 | in ricerca | 1 | 39-octies |
| `/fonti/67/` Decreto Legislativo 286/1998 | in ricerca | 1 | 10 |
| `/fonti/62/` Decreto Legislativo 151/2001 | in ricerca | 1 | 52 |
| `/fonti/44/` Decreto Legislativo 165/2001 | in ricerca | 1 | 34-bis |
| `/fonti/82/` Decreto Legislativo 276/2003 | in ricerca | 1 | 14 |
| `/fonti/2/` Decreto Legislativo 196/2003 | in ricerca | 1 | 79 |
| `/fonti/142/` Decreto Legislativo 170/2004 | in ricerca | 1 | 1 |
| `/fonti/47/` Decreto Legislativo 209/2005 | in ricerca | 1 | 283 |
| `/fonti/225/` Decreto Legislativo 66/2010 | da approvare | 1 | 1008 |
| `/fonti/72/` Decreto Legislativo 81/2015 | in ricerca | 1 | 2 |
| `/fonti/50/` Decreto Legislativo 14/2019 | in ricerca | 1 | 25-sexies |
| `/fonti/287/` Decreto Legislativo 175/2024 | in ricerca | 1 | 102 |
| `/fonti/352/` Decreto Legislativo 141/2026 | da approvare | 1 | 94 |
| `/fonti/105/` Legge 59/1997 | in ricerca | 1 | 11 |
| `/fonti/236/` Legge 289/2002 | in ricerca | 1 | 22 |
| `/fonti/97/` Legge 3/2012 | in ricerca | 1 | 13 |
| `/fonti/220/` Legge 147/2013 | da approvare | 1 | 1 |
| `/fonti/211/` Legge 178/2020 | da approvare | 1 | 1 |
| `/fonti/87/` Legge 193/2024 | in ricerca | 1 | 23 |
| `/fonti/12/` Decreto Ministeriale 44/2011 | in ricerca | 1 | 13 |
| `/fonti/373/` Regio Decreto 12/1941 | in ricerca | 1 | 109 |
| `/fonti/173/` Regio Decreto 267/1942 | in ricerca | 1 | 34 |
| `/fonti/288/` Regio Decreto 318/1942 | in ricerca | 1 | 38 |


## Ordine suggerito

1. Problema 1, a partire dal d.lgs. 50/2016.
2. Problema 2, a partire dalle leggi 160/2019 e 296/2006.
3. Problema 3, a partire dalla l. 147/2013.
4. Problemi 4 e 5.
5. Problemi 10 e 11, subito: il 10 ha già fatto spendere sintesi inutili.
6. Problemi 6 e 8 (Costituzione), poi 7 e 9.
7. Problema 12 prima che il codice penale entri in ricerca; per gli atti già in ricerca, intanto, partire da c.p.c. 654, c.p. e c.c.

Dopo ogni correzione gli atti vanno riscaricati e ricontrollati prima dell'approvazione, perché il numero di sintesi cambierà.
