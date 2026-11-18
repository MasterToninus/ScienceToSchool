---
name: git-commit-push
description: Prepara e verifica commit e push di ScienceToSchool con messaggi estesi in italiano, provenienza documentata e aggiornamento degli SHA precedenti nel registro IA dentro lo stesso commit utile. Usa quando viene richiesto di registrare o pubblicare modifiche al progetto.
---

# Creare un commit e fare push

Registra uno stato verificabile del progetto e pubblicalo sul remoto indicato, nei limiti della richiesta. Segui le [istruzioni del progetto](../../../AGENTS.md) per directory operativa, provenienza, date e autorizzazioni.

## Perimetro e stato Git

- Distingui le azioni autorizzate: preparazione, commit, push. La richiesta esplicita di commit e push autorizza entrambi; non richiedere una seconda conferma per le stesse azioni. L'esistenza della skill non autorizza operazioni future.
- Imposta la directory operativa come `workdir` di ogni comando e comunicala ai subagenti. Verifica directory risolta, radice Git, branch, stato, staging e URL del remoto prima di intervenire.
- Una repository senza commit è uno stato valido: controlla il contenuto effettivo dei file non tracciati e dello staging, senza dare per esistente `HEAD`.
- Prima del push controlla i riferimenti remoti. Per aggiornare un branch remoto esistente, acquisisci i riferimenti e verifica che l'aggiornamento sia fast-forward. Se manca il remoto o incontri una storia divergente, fermati su quel passaggio e descrivi il problema concreto; non creare repository, forzare il push o riscrivere la storia senza una richiesta specifica.

## Preparare il contenuto

1. Rileggi i file coinvolti e il [registro cumulativo](../../../docs/interazioni-ai/registro.md). Accorpa la nuova evidenza nella riga pertinente; apri una riga solo per un'attività distinta. Aggiorna la data della home quando previsto da AGENTS.md.
2. **Prima dello staging, aggiorna gli SHA delle attività e delle fasi precedenti** secondo la procedura sotto. Questo passaggio fa parte di ogni nuovo commit IA utile già autorizzato per altre modifiche, anche se l'autore non lo ripete nella richiesta.
3. Controlla i collegamenti locali, gli anni collegati e i file aggiunti o spostati. Distingui questi controlli dalla revisione disciplinare umana; non presentare una verifica strutturale come convalida dei programmi o delle fonti.
4. Esamina ciò che era già in staging. Le modifiche estranee non devono entrare nel commit: preservale e usa, quando necessario, un indice separato o una selezione del commit che le escluda senza alterarle. Aggiungi esplicitamente i percorsi pertinenti, **compreso il registro aggiornato** nello stesso commit. Per il primo snapshot richiesto dell'intero progetto includi il materiale previsto, le skill, la licenza e il registro; escludi temporanei e archivi di consegna secondo `.gitignore`.
5. Esamina `git diff --cached --check` e `git diff --cached`, oltre all'elenco dei file staged. Controlla in particolare il diff staged del registro: SHA completi riscontrati, primi commit conservati, fasi correnti ancora `PENDING` e motivazione dei riferimenti rimasti aperti. Risolvi problemi pertinenti prima del commit. Non usare stash, reset distruttivi, amend o riscritture della storia come scorciatoie.

## Aggiornare gli SHA precedenti

1. Cerca i riferimenti da risolvere **nell'intero registro**: colonna «Primo commit», descrizioni delle fasi, verifiche e nota iniziale «SHA e versioni». Una riga con il primo SHA già compilato può contenere un ampliamento successivo ancora `PENDING`. Distingui le fasi già versionate da quelle presenti soltanto nelle modifiche locali correnti.
2. Per ogni attività o fase precedente da risolvere, individua i file e le modifiche che ne costituiscono l'esito. Esamina la storia dei percorsi, per esempio con `git log --reverse --format="%H %s" -- <percorso>`, e il contenuto dei commit candidati con `git show <sha> -- <percorso>` o `git show <sha>:<percorso>`. Se necessario segui le rinomine o cerca il testo distintivo nella storia. Registra lo **SHA completo del primo commit che incorpora effettivamente quell'esito**. La presenza del solo ID nel registro, il titolo del commit o la data non bastano; non assegnare automaticamente `HEAD`.
3. Mantieni il significato della colonna «Primo commit»: identifica la prima versione degli effetti dell'attività. Conserva gli SHA già corretti; per un ampliamento o una revisione successiva annota **fase, data e relativo SHA nella stessa riga**, senza sostituire il primo commit storico. Aggiorna coerentemente anche i richiami iniziali e le formulazioni provvisorie; evita sostituzioni globali indistinte dei `PENDING` e nuove righe per la sola tracciabilità.
4. Lascia `PENDING` per le attività e le fasi che entrano per la prima volta nel commit in preparazione, anche quando la riga possiede già uno SHA storico. In una repository senza commit non tentare di leggere `HEAD`: i primi riferimenti restano `PENDING`. Se manca temporaneamente la storia necessaria, conserva il riferimento aperto spiegando il limite; usa `UNKNOWN` con motivo solo per uno storico irricostruibile. Mantieni «non applicabile» per risultati solo esterni ai file versionati.
5. Distingui **commit identificato** e **pubblicazione verificata**. Puoi risolvere uno SHA locale senza dichiararlo pubblicato. Per registrare un precedente push, usa l'evidenza disponibile o verifica che il commit appartenga alla storia del branch remoto dopo l'aggiornamento dei riferimenti previsto per il push autorizzato; non esigere che un vecchio commit coincida ancora con la punta remota. Se la pubblicazione non è verificabile, dichiaralo senza inventare l'esito.

**Esempio:** un'attività ha come primo commit `A`; una sua revisione è stata incorporata nel commit già esistente `B`, ma il registro riporta ancora `PENDING` per quella fase. Durante la preparazione del successivo commit utile `C`, conserva `A` nella colonna «Primo commit», annota lo SHA completo di `B` nella descrizione della revisione e lascia `PENDING` per eventuali effetti nuovi che entreranno in `C`. `A`, `B` e `C` sono simboli dell'esempio, non valori da scrivere nel registro.

Il commit corrente non può contenere il proprio SHA definitivo. Dopo averlo creato, comunica SHA ed esito in chat e consolidali nel registro al successivo intervento IA utile. **Non creare un secondo commit, un push aggiuntivo o un amend soltanto per compilare il log.**

## Messaggio esteso in italiano

Usa un oggetto sintetico e descrittivo, una riga vuota e un corpo esteso quanto serve a capire il cambiamento senza leggere la chat. Il corpo documenta:

- scopo e motivazione del commit;
- modifiche effettive, organizzate per contenuto o funzione;
- controlli eseguiti e relativi risultati;
- limiti, verifiche ancora aperte e provenienza dei contributi quando rilevanti.

Usa i prefissi esatti `[AI]` e `[AI-Human]` secondo AGENTS.md, prima dell'eventuale prefisso convenzionale. Una richiesta o approvazione non rende umano un testo prodotto dall'IA. Per uno snapshot misto con contributo umano sostanziale usa `[AI-Human]` e distingui nel corpo i materiali; per materiale prodotto dall'IA senza un contributo umano sostanziale usa `[AI]`. Non inventare percentuali, risultati o verifiche. Queste grafie si applicano ai nuovi messaggi; conserva i prefissi dei commit e delle registrazioni storiche.

Per esempio, l'oggetto di uno snapshot misto può essere `[AI-Human] docs: registra lo stato iniziale di ScienceToSchool`. Il corpo deve descrivere lo snapshot reale, non ripetere un modello generico.

Scrivi il messaggio in un file UTF-8 temporaneo escluso dalla versione e passa il file a `git commit --file`. Conserva paragrafi, accenti e testo letterale; evita di assemblare un messaggio multilinea nella riga di comando. Rileggi oggetto e corpo prima del commit e controllali anche nel commit creato.

## Commit, push e tracciabilità

- Dopo il commit verifica SHA completo, contenuto e stato locale. Esegui un normale push al remoto e branch autorizzati; imposta l'upstream quando necessario. Verifica che il riferimento remoto coincida con il commit locale: il solo messaggio di successo non sostituisce il controllo del risultato.
- Se un comando fallisce, controlla lo stato prima di ripeterlo. Non creare un commit duplicato se il primo è già riuscito e non trattare un rifiuto del push come un invito a usare force. Segnala limiti di rete o permessi con il punto concreto ancora da completare.
- Concludi indicando commit, branch, remoto, esito del push, controlli eseguiti, riferimenti precedenti risolti e quelli ancora aperti con motivo, oltre alle modifiche locali eventualmente rimaste. Applica la regola sopra per lo SHA corrente, senza un secondo commit per il log. Non dichiarare pulita o sincronizzata una copia senza averla verificata.
