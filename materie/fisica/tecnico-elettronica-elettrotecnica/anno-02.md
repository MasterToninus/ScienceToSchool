# Segnali, logica e interfacce

![AI-GENERATED DRAFT. Versione Tentative generata tramite IA. Bozza da sottoporre a revisione docente.](../../../docs/assets/ai-generated-draft.png)

> **AI-GENERATED DRAFT — Versione Tentative generata tramite IA.** Bozza di programma da sottoporre a revisione docente; la scansione annuale è una proposta, non un programma ministeriale prescritto. [Registro dell’attività IA](../../../docs/interazioni-ai/registro.md#ai-0003) · [Ricerca autonoma delle fonti](../../../docs/interazioni-ai/registro.md#ai-0014).

Istituto tecnico, Elettronica ed elettrotecnica · Anno 2 · Proposta didattica

## Carico didattico

| Disciplina/perimetro | Coorte/ordinamento | Ore settimanali | Monte ore annuo | Fonte |
| --- | --- | --- | --- | --- |
| Fondamenti di elettrotecnica ed elettronica | Nuovo ordinamento; anno 2 dal 2027/28; annualità futura | 4 (media equivalente) | 132 ore | [D.M. 29/2026, allegato C6](https://www.istruzioneer.gov.it/2026/03/10/d-m-29-del-19-02-2026-riforma-istituti-tecnici-a-s-2026-27/?download=87104); [D.M. 71/2026, allegato 6](https://usrfvg.gov.it/export/sites/default/it/home/menu/uffici/Direzione/allegati-direzione/allegati-direzione-2026/All.-6-TECNOLOGICO-ELETTRONICA-ELETTROTECNICA-signed.pdf) |

Il D.L. 170/2026 conserva il monte biennale di 264 ore del dominio «Elementi di base dell’indirizzo» cui appartiene questa disciplina. È stato letto il quadro annuale specifico; queste ore sono distinte da quelle di Scienze sperimentali. L’orario concreto della scuola e gli eventuali aggiornamenti attuativi vanno comunque controllati.

I monti annui sono nominali ordinamentali. «Media equivalente» significa monte annuo ÷ 33; non descrive necessariamente l’orario settimanale reale né le ore effettivamente svolte. [Metodo, fonti e limiti della verifica al 18/11/2026](../../../docs/ricerca-ai/carico-didattico-fisica.md) · [Attività IA](../../../docs/interazioni-ai/registro.md#ai-0002).

## Programma proposto per nuclei tematici

**Ripartizione Tentative delle ore generata tramite IA.** Il budget di 132 ore usa la riga disciplinare del D.M. 29/2026, confermata nel D.M. 71/2026, per il dominio biennale rimasto invariato nel D.L. 170/2026. Le ore di ogni punto comprendono spiegazione, esempi ed eventuale laboratorio specifico; le attività indicate più avanti sono già comprese nei nuclei o nella riserva e non si sommano una seconda volta. I criteri di raccordo e le indicazioni metodologiche sono trasversali.

| Voce del budget | Ore |
| --- | ---: |
| Punti dei nuclei tematici | 108 |
| Riserva trasversale | 24 |
| **Totale programmato** | **132** |

Proposta per Fondamenti di elettrotecnica ed elettronica del nuovo ordinamento: prima dal 2026/27 e seconda dal 2027/28. Non sostituisce la componente fisica delle Scienze sperimentali.

**Prerequisiti e progressione.** Dalla prima: Ohm, Kirchhoff elementare, multimetro, potenza e schemi. Sinusoidi ed esponenziali sono introdotte come grafici nel nucleo pertinente; non si presume l’analisi matematica. Prima di sensori e logica, distinguere segnale analogico, soglia e livello elettrico. Arduino, amplificatori operazionali e fasori del manuale sono estensioni da programmare separatamente, non obiettivi impliciti delle 132 ore. Le eventuali lacune iniziali si trattano nella riserva o sostituendo un approfondimento, con nuova verifica della somma.

**Uso dei tempi e delle attività.** La disciplina degli Elementi di base è distinta dalle Scienze sperimentali: le ore non si sommano per finanziare due volte la stessa prova. Gli Orientamenti 2026 non fissano qui una lista annuale esaustiva; la scelta richiede curricolo d’istituto. Ogni montaggio e analisi è incluso nel punto relativo; il rapporto riusa i dati acquisiti. La riserva comprende valutazione con restituzione e recupero, non altre prove complete.

[Motivi della revisione critica e limiti](../../../docs/ricerca-ai/revisione-critica-fisica.md).

### Segnali nel tempo

**Subtotale del nucleo: 18 ore.**

- **5 ore.** Leggere periodo, frequenza, ampiezza e valore medio nei grafici di segnali continui, periodici e impulsivi.
- **5 ore.** Introdurre sinusoide e valore efficace mediante un grafico e dati forniti; l’analisi con fasori resta successiva.
- **4 ore.** Impostare base dei tempi e scala verticale dello strumento reale o simulato.
- **4 ore.** Confrontare due campionamenti e riconoscere limiti di visualizzazione, rumore e possibili ambiguità.


### Condensatori, induttori e transitori

**Subtotale del nucleo: 18 ore.**

- **5 ore.** Collegare carica, capacità, tensione ed energia di un condensatore.
- **6 ore.** Studiare carica/scarica RC con curve e stima della costante di tempo; introdurre l’esponenziale graficamente, senza equazioni differenziali.
- **4 ore.** Descrivere campo di una bobina, induzione ed energia immagazzinata; confrontare qualitativamente transitori capacitivi e induttivi.
- **3 ore.** Interpretare funzione di una bobina/relè e protezione del comando su uno schema già predisposto.


### Diodi e componenti non lineari

**Subtotale del nucleo: 18 ore.**

- **5 ore.** Confrontare caratteristica di resistore e diodo, polarità e limiti del modello a soglia.
- **5 ore.** Calcolare la resistenza di limitazione di un LED da dati nominali e tolleranze.
- **4 ore.** Verificare il circuito a bassissima tensione e confrontare due punti di funzionamento.
- **4 ore.** Usare un transistor come interruttore guidato per separare comando e carico; il dimensionamento completo è rinviato al triennio.


### Logica combinatoria

**Subtotale del nucleo: 22 ore.**

- **4 ore.** Introdurre rappresentazione binaria, bit e variabili logiche; distinguere numero codificato e stato elettrico.
- **6 ore.** Tradurre una richiesta in tavola di verità ed espressioni AND, OR e NOT.
- **6 ore.** Costruire una rete a due ingressi in simulazione e controllare tutte le combinazioni.
- **6 ore.** Confrontare livelli reali, soglie e risposta temporale con il modello logico ideale, senza affrontare una sintesi MSI completa.


### Sensori e interfacce

**Subtotale del nucleo: 16 ore.**

- **5 ore.** Collegare grandezza fisica e risposta del sensore con curva di taratura.
- **5 ore.** Interpretare un’interfaccia a soglia già predisposta e definire quando l’indicatore deve attivarsi.
- **6 ore.** Verificare rumore, saturazione e tempo di risposta, distinguendo valore analogico e stato logico.


### Prototipo e verifica

**Subtotale del nucleo: 16 ore.**

- **5 ore.** Integrare i moduli già verificati in un indicatore a due ingressi con schema e valori motivati.
- **5 ore.** Eseguire la tabella di prova completa e un caso limite, confrontando simulazione e misura.
- **6 ore.** Diagnosticare uno scarto con una misura mirata e redigere il rapporto conclusivo; la verifica individuale usa la riserva.

### Riserva per consolidamento e valutazione

**Subtotale della riserva: 24 ore.**

- **8 ore.** Esercitazioni trasversali e consolidamento: collegare i nuclei e discutere gli errori ricorrenti.
- **8 ore.** Verifiche, restituzione e autovalutazione, comprese le prove descritte nella sezione «Attività e verifica».
- **8 ore.** Recupero mirato e adattamento della progressione alle evidenze emerse in classe.

**Controllo del budget:** 108 ore nei punti + 24 ore di riserva = **132 ore**. Le ore perse per calendario o attività d’istituto richiedono una riprogrammazione; non sono già sottratte dal monte nominale.

## Attività e verifica

Progettare un indicatore luminoso comandato da due condizioni logiche. Documentare la risposta per tutte le combinazioni.

Verifica: schema, tabella di verità e confronto fra misura e simulazione in un caso limite.

## Libro consigliato

Fabrizio Cerri, Antonella Gallotti e Andrea Rondinelli, *Fondamenti di elettrotecnica ed elettronica*, Hoepli, **2026**, volume unico, ISBN **9788836022830**. [Scheda e indice pubblico dell’editore](https://www.hoeplieditore.it/hoepli-catalogo/articolo/default/default/3416). L’indice pubblica sezioni e argomenti, senza numerazione analitica o pagine: non si assegnano numeri di capitolo non visibili.

| Nucleo della scheda | Raccordo documentato | Stato |
| --- | --- | --- |
| Segnali nel tempo | Elettrotecnica generale: grandezze alternate; dettaglio temporale da verificare | Affinità; dettaglio aperto |
| Condensatori, induttori e transitori | Elettrotecnica generale: componenti capacitivi/induttivi; RC da verificare | Affinità; dettaglio aperto |
| Diodi e componenti non lineari | Elettronica di segnale: parte analogica | Indice |
| Logica combinatoria | Elettronica di segnale: parte digitale | Indice |
| Sensori e interfacce | Metrologia e Arduino: interfacciamento; sensore specifico da integrare | Affinità; dettaglio aperto |
| Prototipo e verifica | integrazione: prototipo e tabella di prova | Integrazione didattica |

**Integrazioni e scelta del materiale.** L’indice pubblico non consente di verificare singolarmente campionamento, costante RC, protezione del relè o tempo di risposta del sensore. Integrare curve e schede tecniche; la copertura generale non giustifica trasferire fasori, sintesi MSI o dimensionamento completo nella sequenza ridotta.

**Limite della verifica (18/11/2026).** Sono stati letti gli indici o i documenti indicati, non i manuali integrali né tutti gli esercizi. «Indice» attesta il tema nella precisa edizione; «affinità» non conferma il dettaglio del testo. Le prove, i dataset, le rubriche e il recupero della scheda sono integrazioni del docente, già comprese nel budget.

[Verifica delle edizioni, fonti e matrice delle 51 schede](../../../docs/ricerca-ai/verifica-manuali-fisica.md#tecnico-elettronica-elettrotecnica-2).

## Fonti consultate per questa proposta

- [MIM / USR Friuli Venezia Giulia — D.M. 71/2026, allegato 6 Elettronica ed elettrotecnica](https://usrfvg.gov.it/export/sites/default/it/home/menu/uffici/Direzione/allegati-direzione/allegati-direzione-2026/All.-6-TECNOLOGICO-ELETTRONICA-ELETTROTECNICA-signed.pdf) — Nuovo insegnamento del biennio.
- [MIM — Primi orientamenti per la progettazione curricolare degli istituti tecnici, 2026](https://www.buccarimarconi.edu.it/wp-content/uploads/2026/09/ORIENTAMENTI-ISTITUTI-TECNICI-2026.pdf) — Parte III: progettazione del biennio.
- [Hoepli — Cerri, Gallotti e Rondinelli, Fondamenti di elettrotecnica ed elettronica, 2026](https://www.hoeplieditore.it/hoepli-catalogo/articolo/default/default/3416) — Indice pubblico; selezione per il biennio.

La selezione e la distribuzione annuale sono una sintesi didattica del progetto. [Catalogo delle fonti di fisica: consultazione, perimetro e limiti](../../../docs/ricerca-ai/fonti-programmi/fisica.md).

[Quadro di riferimento e fonti del percorso](README.md)
