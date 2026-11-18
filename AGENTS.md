# Istruzioni per gli agenti di ScienceToSchool

ScienceToSchool raccoglie programmi annuali proposti per le scuole italiane. Chi lavora con un assistente AI usa queste istruzioni per curare i contenuti e conservarne la provenienza. Le procedure operative si trovano in [SKILLS.md](SKILLS.md).

## Cartella di lavoro

Per il lavoro locale di Tony, la copia operativa è `C:\Users\tonym\GitHub\Teaching\ScienceToSchool`. All'avvio verifica il percorso risolto, la radice Git, il branch, lo stato dei file e il remoto configurato. Imposta questa directory come `workdir` dei comandi e comunicala esplicitamente ai subagenti. Per un clone o un fork in un'altra posizione usa la cartella indicata dal suo proprietario.

La cartella `D:\Codex\ScienceToSchool` è la precedente area di preparazione. Dopo l'estrazione dello ZIP usa la copia operativa indicata sopra. Se i permessi della sessione impediscono l'accesso, segnala il percorso bloccato e chiedi di aprire la chat con quella cartella come workspace autorizzato. La directory di lavoro e i relativi permessi devono essere effettivi nell'ambiente.

## Lingua e voce

- Scrivi in italiano, compresi titoli, sommari, registro delle attività e messaggi di commit. Il messaggio iniziale del README principale è in inglese. Mantieni nella lingua originale i titoli delle fonti e le denominazioni tecniche quando tradurli ne altererebbe il senso.
- Usa la denominazione ufficiale di classi, materie, articolazioni e opzioni. Distingui il nome della classe di concorso da quello della disciplina. Introduci le sigle al primo uso.
- Il messaggio in prima persona nella home appartiene all’autore. Per modificarne esperienza, giudizi o tono occorre una sua indicazione. Per un fatto verificabile che vi è richiamato, colloca la fonte accanto al relativo passaggio.

## Dove intervenire

| Contenuto | Posizione e forma |
| --- | --- |
| Ricerche assistite dall’IA | Conserva i risultati tematici in `docs/ricerca-ai/`. Nel [rapporto sui titoli](docs/ricerca-ai/accesso-lm17.md) distingui requisiti di legge e titoli documentati per il singolo caso. La [nota sull’uso dell’IA](docs/ricerca-ai/uso-ai.md) raccoglie le fonti pertinenti per la scuola. |
| Indice | Tabella nel [README principale](README.md). Da ogni incrocio compilato si raggiunge il sotto-README pertinente. |
| Programma | `materie/<materia>/<scuola-o-indirizzo>/README.md` descrive il perimetro e collega ogni anno. `anno-01.md`, `anno-02.md` e così via seguono gli anni della scuola in cui si insegna la materia. Per un CPIA usa i periodi didattici previsti e spiegali nel sotto-README. |
| Interazioni e disclosure | Usa sempre [docs/interazioni-ai/registro.md](docs/interazioni-ai/registro.md). È l’unico registro Markdown cumulativo del progetto. La dichiarazione sintetica in apertura deriva dalle attività riportate nella tabella. |

Prima di modificare un’assegnazione, rileggi il rapporto, la riga dell’indice e il sotto-README. Quando scuole o indirizzi condividono una cartella, esplicita quali contenuti e anni condividono e quali varianti occorrono. Controlla gli orari nel quadro dell’articolazione interessata.

## Ruolo di archivista

1. Registra gli usi effettivi dell’IA che hanno prodotto un risultato o influito su una decisione. Riassumi in poche parole la richiesta e il contributo dell’autore, conservando il senso delle sue parole. Collega il risultato o la fonte. Non creare file per giorno, sessione o interazione e non trascrivere la chat.
2. Proteggi recapiti, certificati personali, dati degli alunni e testi riservati. Per contributi di terzi usa una breve sintesi e la fonte pubblica quando disponibile.
3. Distingui ciò che l’IA ha prodotto, ciò che una persona riferisce e ciò che è stato verificato indipendentemente. Indica chi ha verificato quale parte. Per l’impiego in una scuola o una pubblicazione verifica eventuali regole di disclosure su fonti pertinenti, distinguendo obblighi, raccomandazioni e opinioni.
4. Nella rilettura controlla risultati, rimandi e corrispondenza con le fonti. Cita il documento consultato con articolo, allegato, riga, nota o voce dell’indice quando disponibili.

## Provenienza dei commit

Quando proponi o crei un commit, anche di squash o merge, classifica l’origine delle modifiche effettive. Usa la grafia esatta e uno spazio dopo il prefisso. Il criterio vale anche quando l’autore copia il materiale o esegue personalmente il commit.

| Prefisso | Quando usarlo | Esempio di oggetto |
| --- | --- | --- |
| `[Ai]` | L’IA ha prodotto il materiale. Una richiesta, la scelta fra due bozze, l’accettazione o la copia da parte dell’autore sono compatibili con questa attribuzione. | `[Ai] docs: aggiunge le proposte annuali di fisica` |
| `[Ai-human]` | Una persona ha fornito contenuto sostanziale che l’IA ha riorganizzato, tradotto o integrato, oppure ha rielaborato in modo sostanziale una bozza dell’IA. | `[Ai-human] docs: organizza le motivazioni dettate dall’autore` |
| Senza prefisso | Il contenuto è attribuibile interamente a lavoro umano. | `Corregge a mano un esempio di cinematica` |

Il tag precede l’eventuale prefisso convenzionale come `docs:`. Per un commit che comprende contributi distinti, descrivili nel registro per materiale. Se li consegni insieme e il contributo umano al contenuto è sostanziale, usa `[Ai-human]`. Se l’origine è incerta, registra il dubbio e chiedi solo il dato necessario prima di proporre l’attribuzione definitiva. Applica la convenzione ai nuovi messaggi. L’autorizzazione a eseguire le operazioni Git segue le regole sotto.

La revisione è un’informazione separata. Una persona che controlla e accetta una scheda generata dall’IA può averla verificata senza averne scritto il contenuto. Annota nel registro il controllo effettivo e il suo perimetro.

## Manutenzione del registro di disclosure

1. Cerca nel [registro](docs/interazioni-ai/registro.md) l’attività con lo stesso scopo e risultato. Accorpa lì richieste successive, tentativi e correzioni. Apri una nuova riga per un’attività distinta, anche se viene svolta nella stessa giornata. Includi un risultato scartato o rimasto in chat se ha orientato una scelta.
2. Assegna un ID progressivo stabile `AI-0001`, `AI-0002`, ecc. e indica la data di registrazione in formato ISO, fuso di Roma. Se ricostruisci un’attività precedente, qualifica la sua data effettiva come nota, riferita o sconosciuta. Registra persona e contributo, strumento, modello e sforzo di ragionamento quando effettivamente disponibili, attività e materiale, evidenza ed esito, verifiche e limiti, primo commit. Conserva modello e sforzo nella colonna «Modello», distinguendo le fasi quando cambiano; per i valori non esposti scrivi «n.r.» senza dedurli dal nome dello strumento o da altre sessioni. Nella descrizione usa il livello 0 per amministrazione, 1 per stesura, 2 per verifiche su fonti o calcoli, 3 per una proposta originale.
3. Quando una persona comunica un controllo, una correzione, l’adozione o il rifiuto di un risultato, aggiorna la stessa riga con data, ambito ed esito. Distingui i controlli automatici dalla verifica umana. Rivedi la dichiarazione sintetica quando cambia la portata dell’uso documentato.
4. Usa `PENDING` quando lo SHA del primo commit pertinente non è ancora registrato, anche per le attività che entrano nel commit corrente. Nel successivo commit IA già necessario per altre modifiche, risolvi i `PENDING` delle attività precedenti: individua nella storia il primo commit che ne incorpora effettivamente gli effetti, controllane il contenuto e registra lo SHA completo. Non assegnare automaticamente HEAD. Non creare commit o push aggiuntivi soltanto per compilare gli SHA e non riscrivere la storia Git. Per uno storico irricostruibile usa `UNKNOWN` con il motivo; per lavoro soltanto in chat o estraneo ai file versionati indica «non applicabile».

## Data, commit e consegna

- Una modifica a ricerca, programmi, istruzioni o indice aggiorna la data «Ultimo aggiornamento» nella home alla data effettiva in `Europe/Rome`. Conserva le date delle singole verifiche. L’aggiornamento di una sola scheda non certifica una nuova verifica delle altre.
- Lavora sui file locali secondo la richiesta. Il commit è un passo distinto, da eseguire quando autorizzato. Prima del commit rileggi il diff, controlla i link interni e verifica che gli anni collegati esistano. Controlla anche il contenuto già in staging, per lasciare al proprietario le modifiche estranee alla richiesta.
- Seleziona esplicitamente i percorsi pertinenti. Controlla i dati staged con `git diff --cached --check` e `git diff --cached`. Crea un commit coerente per argomento con un messaggio esteso in italiano: oggetto sintetico con il prefisso corrispondente alla provenienza e corpo che descrive scopo, modifiche, verifiche e limiti. Applica la [skill Git commit e push](.agents/skills/git-commit-push/SKILL.md). Nel resoconto indica quali controlli hai eseguito.
- Creazione del repository remoto, push, apertura di una pull request e merge richiedono un’indicazione esplicita per l’azione corrispondente. Chi riceve una richiesta limitata alla copia locale conclude consegnando i file locali.
