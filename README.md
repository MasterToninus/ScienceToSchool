> This repository is written in Italian for people preparing to teach in Italian schools. Start with the table below to find a subject, a school pathway and a year-by-year teaching plan.

# ScienceToSchool

![AI-GENERATED DRAFT. Versione Tentative generata tramite IA. Bozza da sottoporre a revisione docente.](docs/assets/ai-generated-draft.png)

> **AI-GENERATED DRAFT — Versione Tentative generata tramite IA.**
>
> **Esperimento preparatorio al passaggio all’insegnamento.** I programmi sono bozze da sottoporre a revisione docente. [Registro della progettazione IA](docs/interazioni-ai/registro.md#ai-0003) · [Ricerca autonoma delle fonti](docs/interazioni-ai/registro.md#ai-0014).

**Ultimo aggiornamento: 18/11/2026 · Anno scolastico di riferimento: 2026/27**

ScienceToSchool raccoglie **196 programmi Tentative in 54 percorsi**, organizzati per materia, scuola e anno, a partire dagli sbocchi della laurea magistrale in Fisica (LM-17). Ogni scheda propone argomenti, attività, verifiche e libri, con fonti consultabili.[^ricerca-ia]

Dalla tabella si raggiungono i percorsi annuali. [Fonti](docs/ricerca-ai/fonti-programmi/README.md), [carico didattico](docs/ricerca-ai/carico-didattico.md), [revisione critica](docs/ricerca-ai/revisione-critica-programmi.md) e [verifica dei manuali](docs/ricerca-ai/verifica-manuali.md) documentano riferimenti, orari, correzioni e limiti.

## Dall’autore


Come molti altri ricercatori precari, sono stato messo alla porta dall’accademia. Due anni fa vedevo ancora altri lavori verso cui avrei potuto orientarmi in caso di necessità. Oggi, per come ho vissuto la ricerca di lavoro, l’AI si è presa anche quelle possibilità. L’unica porta che vedo ancora aperta è l’insegnamento, e temo che lo resterà ancora per poco [>tagli!<](https://pagellapolitica.it/articoli/tagli-scuola-legge-di-bilancio).

**Il mio passaggio all’insegnamento non è ancora avvenuto, ma lo ritengo probabile al 99%.** Questa raccolta è un esperimento per prepararmi a quel passaggio.

*Tony*

## Classi di concorso e scuole

L’accesso è riferito alla **LM-17 conseguita nel 2015**; i requisiti personali restano da documentare.[^titolo] Il punto «·» indica un abbinamento non censito.

| Classe di concorso | Accesso con il titolo del 2015[^procedure] | Medie e adulti[^medie-adulti] | Licei | Istruzione tecnica[^ordinamenti] | Istruzione professionale[^ordinamenti] |
| --- | --- | --- | --- | --- | --- |
| **A-20 · Fisica** | Diretto[^diretto] | · | [Scientifico ordinario](materie/fisica/liceo-scientifico/README.md), [scienze applicate](materie/fisica/liceo-scientifico-scienze-applicate/README.md), [sportivo](materie/fisica/liceo-scientifico-sportivo/README.md), anni 1-5 | Componente fisica delle scienze nei settori [economico](materie/fisica/tecnico-economico/README.md) e [tecnologico](materie/fisica/tecnico-tecnologico/README.md). [Fisica ambientale e altri insegnamenti di indirizzo](materie/fisica/README.md) | [Scienze integrate](materie/fisica/professionale/README.md), [Ottica e ottica applicata](materie/fisica/professionale-ottico/README.md) |
| **A-26 · Matematica** | 30 CFU MAT[^a26] | · | [Scientifico, comprese le sue opzioni e sezioni](materie/matematica/liceo-scientifico/README.md), [Made in Italy](materie/matematica/liceo-made-in-italy/README.md). [Classico, linguistico, scienze umane](materie/matematica/licei-classico-linguistico-scienze-umane/README.md)[^a-esaurimento] e [opzione economico-sociale](materie/matematica/liceo-economico-sociale/README.md)[^a-esaurimento] | [Economico](materie/matematica/tecnico-economico/README.md), [tecnologico](materie/matematica/tecnico-tecnologico/README.md), [Complementi](materie/matematica/tecnico-complementi/README.md) dove previsti | [Matematica, tutti gli indirizzi](materie/matematica/professionale/README.md) |
| **A-27 · Matematica e fisica** | Salvaguardato[^titolo-salvaguardato] | · | [Matematica](materie/matematica/README.md) dal primo anno. [Fisica](materie/fisica/README.md) dal primo negli scientifici e dal terzo negli altri licei elencati, incluso il Made in Italy | [Matematica](materie/matematica/tecnico-tecnologico/README.md), [Complementi](materie/matematica/tecnico-complementi/README.md) e, per le coorti previgenti, fisica negli indirizzi ammessi dalla tabella ministeriale | [Matematica, tutti gli indirizzi](materie/matematica/professionale/README.md) |
| **A-28 · Matematica e scienze** | Salvaguardato[^titolo-salvaguardato] | [Scuola media, anni 1-3](materie/matematica-e-scienze/secondaria-di-primo-grado/README.md). [CPIA, primo livello](materie/matematica-e-scienze/cpia-primo-livello/README.md) | · | · | · |
| **A-33 · Scienze e tecnologie aeronautiche** | Requisito aeronautico[^a33] | · | · | [Conduzione del mezzo aereo](materie/navigazione/tecnico-conduzione-aerea/README.md), [Trasporti e logistica](materie/trasporti-e-logistica/tecnico-trasporti-e-logistica/README.md) | · |
| **A-35 · Scienze e tecnologie della calzatura e della moda** | Diploma specifico[^a35-a44] | · | · | Sistema moda: [calzatura](materie/tecnologie-della-calzatura/tecnico-sistema-moda/README.md) e [laboratorio del biennio comune](materie/tecnologie-tessili/tecnico-sistema-moda/README.md)[^moda] | · |
| **A-40 · Scienze e tecnologie elettriche ed elettroniche** | Diretto[^diretto] | · | [Informatica nello scientifico scienze applicate](materie/informatica/liceo-scientifico-scienze-applicate/README.md), anni 1-5 | [Elettronica ed elettrotecnica, meccatronica, trasporti, telecomunicazioni](materie/elettronica/README.md) e [TIC](materie/informatica/tecnico-tecnologico-tic/README.md) secondo l’indirizzo | [Manutenzione](materie/elettronica/professionale-manutenzione/README.md), [Industria e artigianato](materie/elettronica/professionale-industria-artigianato/README.md), [Gestione delle acque](materie/elettronica/professionale-gestione-acque/README.md). [TIC](materie/informatica/professionale-tic/README.md)[^tic-titolarita] |
| **A-41 · Scienze e tecnologie informatiche** | Diretto[^diretto] | · | [Scientifico, scienze applicate](materie/informatica/liceo-scientifico-scienze-applicate/README.md) | [Informatica e telecomunicazioni](materie/informatica/tecnico-informatica-telecomunicazioni/README.md), [economico](materie/informatica/tecnico-economico/README.md), [TIC e altri indirizzi](materie/informatica/README.md), [specializzazione Enotecnico](materie/informatica/tecnico-agrario/anno-06.md) | [TIC](materie/informatica/professionale-tic/README.md), [Servizi commerciali](materie/informatica/professionale-servizi-commerciali/README.md) |
| **A-43 · Scienze e tecnologie nautiche** | Requisito nautico[^a43] | · | · | [Conduzione del mezzo navale](materie/navigazione/tecnico-conduzione-navale/README.md), [Trasporti e logistica](materie/trasporti-e-logistica/tecnico-trasporti-e-logistica/README.md) | [Pesca commerciale e produzioni ittiche, anni 3-5](materie/navigazione/professionale-pesca/README.md) |
| **A-44 · Scienze e tecnologie tessili, dell’abbigliamento e della moda** | Diploma specifico[^a35-a44] | · | · | Sistema moda: [tessile e abbigliamento](materie/tecnologie-tessili/tecnico-sistema-moda/README.md), [calzatura](materie/tecnologie-della-calzatura/tecnico-sistema-moda/README.md) | [Industria e artigianato, declinazione tessile](materie/tecnologie-tessili/professionale-industria-e-artigianato/README.md) |
| **A-47 · Scienze matematiche applicate** | Diretto[^diretto] | · | [Scientifico, scienze applicate](materie/matematica/liceo-scientifico/README.md)[^a-esaurimento] | [Economico](materie/matematica/tecnico-economico/README.md). Nel nuovo ordinamento anche [matematica comune agli indirizzi tecnologici](materie/matematica/tecnico-tecnologico/README.md) | [Matematica, tutti gli indirizzi](materie/matematica/professionale/README.md) |
| **A-61 · Tecnologie e tecniche delle comunicazioni multimediali** | Titoli professionali[^a61] | · | [Artistico, audiovisivo e multimediale](materie/comunicazione-multimediale/liceo-artistico-audiovisivo/README.md) | [Grafica e comunicazione](materie/comunicazione-multimediale/tecnico-grafica-e-comunicazione/README.md) | [Servizi culturali e dello spettacolo](materie/comunicazione-multimediale/professionale-servizi-culturali/README.md), [Industria e artigianato](materie/comunicazione-multimediale/professionale-industria-artigianato/README.md) |

Le condizioni e le fonti sono raccolte nelle note e nel [rapporto sui titoli di accesso](docs/ricerca-ai/accesso-lm17.md).

## Collaborare

Mi auguro che questo esperimento venga **forkato e adattato ad altre materie**. Accolgo pull request che aggiungano percorsi, correggano errori nei programmi o colleghino un argomento alla sezione verificabile di un manuale. È particolarmente utile spiegare per quale scuola, anno ed edizione del libro vale una correzione. Per partecipare o contattarmi: [sito di Antonio Michele Miti](https://www.antoniomiti.it/).

## AI-Friendly

Per lavorare con un assistente IA, leggere [AGENTS.md](AGENTS.md) e scegliere la procedura in [SKILLS.md](SKILLS.md). I due file definiscono istruzioni e verifiche riutilizzabili. [Formato AGENTS.md](https://agents.md/) · [Agent Skills](https://agentskills.io/)

L’unico [registro IA](docs/interazioni-ai/registro.md) documenta contributi, strumenti e verifiche. I nuovi commit usano `[AI]` o `[AI-Human]` secondo la provenienza; i messaggi storici restano invariati. [Uso dell’IA e verifica delle fonti](docs/ricerca-ai/uso-ai.md)

## Licenza

Salvo diversa indicazione, i materiali didattici e la documentazione originali di ScienceToSchool sono distribuiti con licenza [Creative Commons Attribuzione-NonCommerciale 4.0 Internazionale](https://creativecommons.org/licenses/by-nc/4.0/deed.it). Le opere di terzi citate o riprodotte conservano le rispettive condizioni di utilizzo. [Testo integrale della licenza](LICENSE)

[^ricerca-ia]: Non ho chiesto all’IA di inventare programmi mediante generazione stocastica, ma di eseguire una ricerca ad albero delle risorse online disponibili e di sintetizzarle in file organizzati secondo la tabella sottostante. La responsabilità umana resta piena su tutto il lavoro, dalla scelta delle fonti alla verifica dei contenuti e al loro utilizzo.
[^titolo]: Nove classi citano la LM-17; A-35, A-44 e A-61 ammettono qualsiasi laurea magistrale con requisiti ulteriori. Il dottorato in matematica non sostituisce i CFU richiesti: occorre il certificato degli esami con i settori scientifico-disciplinari. [Verifica per classe](docs/ricerca-ai/accesso-lm17.md).
[^procedure]: Abilitazione, graduatorie, concorsi e disponibilità di cattedre seguono le condizioni della rispettiva procedura.
[^diretto]: La tabella dei titoli ammette la LM-17 senza ulteriori CFU disciplinari.
[^titolo-salvaguardato]: Restano utilizzabili i requisiti già soddisfatti secondo la disciplina precedente, nei limiti della salvaguardia applicabile.
[^a26]: Occorre documentare almeno 30 CFU nei settori MAT previsti dalla tabella applicabile.
[^a33]: Occorrono 12 CFU in FIS/06 oppure 12 in GEO/12, o il titolo aeronautico alternativo previsto.
[^a35-a44]: Oltre alla laurea magistrale serve uno degli specifici diplomi tessili previsti per la classe.
[^a43]: Occorre l’abilitazione a ufficiale di coperta oppure lo specifico status militare previsto.
[^a61]: Oltre alla laurea magistrale servono titoli professionali accertati dall’Ufficio scolastico regionale.
[^a-esaurimento]: L’assegnazione indicata riguarda soltanto il personale già titolare interessato dalla clausola.
[^tic-titolarita]: Per A-40, verificare le clausole sulla titolarità riportate nel [percorso TIC professionale](materie/informatica/professionale-tic/README.md).
[^moda]: Nel triennio l’assegnazione dipende dall’articolazione: calzatura oppure tessile e abbigliamento.
[^medie-adulti]: Tempo ordinario, prolungato e indirizzo musicale condividono il [percorso triennale](materie/matematica-e-scienze/secondaria-di-primo-grado/README.md), con orari distinti. I [CPIA](materie/matematica-e-scienze/cpia-primo-livello/README.md) sono organizzati per periodi didattici.
[^ordinamenti]: Dal 1° ottobre 2026 il [DL 170/2026, art. 9](https://www.gazzettaufficiale.it/eli/id/2026/09/30/26G00190/sg) introduce le denominazioni «licei tecnologici» e «licei professionali»; per i tecnici modifica anche i monte ore per area. Al 18/11/2026 la conversione è in corso. La riforma dei tecnici quinquennali parte dalle prime 2026/27: scegliere la scheda per coorte e articolazione. Le ore disciplinari del [DM 71/2026](https://www.ufficioscolasticoregionalelazio.it/2026/06/08/decreto-ministeriale-n-71-del-29-aprile-2026/) vanno lette con i nuovi vincoli: [quadro e limiti](docs/ricerca-ai/carico-didattico.md).
