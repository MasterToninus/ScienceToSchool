---
name: git-commit-push
description: Prepara e verifica commit e push di ScienceToSchool con messaggi estesi in italiano, provenienza documentata e aggiornamento del registro IA. Usa quando viene richiesto di registrare o pubblicare modifiche al progetto.
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
2. Controlla i collegamenti locali, gli anni collegati e i file aggiunti o spostati. Distingui questi controlli dalla revisione disciplinare umana; non presentare una verifica strutturale come convalida dei programmi o delle fonti.
3. Esamina ciò che era già in staging. Le modifiche estranee non devono entrare nel commit: preservale e usa, quando necessario, un indice separato o una selezione del commit che le escluda senza alterarle. Aggiungi esplicitamente i percorsi pertinenti. Per il primo snapshot richiesto dell'intero progetto includi il materiale previsto, le skill, la licenza e il registro; escludi temporanei e archivi di consegna secondo `.gitignore`.
4. Esamina `git diff --cached --check` e `git diff --cached`, oltre all'elenco dei file staged. Risolvi problemi pertinenti prima del commit. Non usare stash, reset distruttivi, amend o riscritture della storia come scorciatoie.

## Messaggio esteso in italiano

Usa un oggetto sintetico e descrittivo, una riga vuota e un corpo esteso quanto serve a capire il cambiamento senza leggere la chat. Il corpo documenta:

- scopo e motivazione del commit;
- modifiche effettive, organizzate per contenuto o funzione;
- controlli eseguiti e relativi risultati;
- limiti, verifiche ancora aperte e provenienza dei contributi quando rilevanti.

Usa i prefissi esatti `[Ai]` e `[Ai-human]` secondo AGENTS.md, prima dell'eventuale prefisso convenzionale. Una richiesta o approvazione non rende umano un testo prodotto dall'IA. Per uno snapshot misto con contributo umano sostanziale usa `[Ai-human]` e distingui nel corpo i materiali; per materiale prodotto dall'IA senza un contributo umano sostanziale usa `[Ai]`. Non inventare percentuali, risultati o verifiche.

Per esempio, l'oggetto di uno snapshot misto può essere `[Ai-human] docs: registra lo stato iniziale di ScienceToSchool`. Il corpo deve descrivere lo snapshot reale, non ripetere un modello generico.

Scrivi il messaggio in un file UTF-8 temporaneo escluso dalla versione e passa il file a `git commit --file`. Conserva paragrafi, accenti e testo letterale; evita di assemblare un messaggio multilinea nella riga di comando. Rileggi oggetto e corpo prima del commit e controllali anche nel commit creato.

## Commit, push e tracciabilità

- Dopo il commit verifica SHA completo, contenuto e stato locale. Esegui un normale push al remoto e branch autorizzati; imposta l'upstream quando necessario. Verifica che il riferimento remoto coincida con il commit locale: il solo messaggio di successo non sostituisce il controllo del risultato.
- Se un comando fallisce, controlla lo stato prima di ripeterlo. Non creare un commit duplicato se il primo è già riuscito e non trattare un rifiuto del push come un invito a usare force. Segnala limiti di rete o permessi con il punto concreto ancora da completare.
- Prima di un nuovo commit IA già necessario per altre modifiche, risolvi i `PENDING` delle attività precedenti già versionate: ricostruisci dalla storia il primo commit che incorpora gli effetti di ogni attività, controllane il contenuto e registra lo SHA completo nella stessa riga. Non assegnare automaticamente HEAD. Mantieni `non applicabile` per risultati solo esterni ai file versionati.
- Le attività incluse per la prima volta nel commit corrente restano `PENDING` fino al successivo commit IA utile. Non creare un secondo commit, un push aggiuntivo o un amend soltanto per inserire gli SHA o registrare l'esito del commit corrente. Riporta subito l'esito in chat e consolidalo nel registro al successivo intervento utile, senza aggiungere una nuova attività per la sola tracciabilità.
- Concludi indicando commit, branch, remoto, esito del push, controlli eseguiti e modifiche locali eventualmente rimaste. Non dichiarare pulita o sincronizzata una copia senza averla verificata.
