# Procedure di ricerca e manutenzione

Questo indice è utilizzabile sia da un docente sia da un assistente AI. Scegli la procedura in base alla decisione da prendere. Le schede complete nella cartella `.agents/skills/` contengono esempi, controlli ed esiti possibili. Nelle modifiche al repository si applicano anche le [istruzioni per gli agenti](AGENTS.md).

| Se vuoi sapere… | Procedura | Risultato |
| --- | --- | --- |
| Quale disposizione vale per questa classe, in questo anno scolastico? | [Verificare una modifica normativa](.agents/skills/verifica-normativa/SKILL.md) | Fonte primaria, decorrenza, prima coorte interessata e testo da aggiornare. |
| Quale parte di un libro sostiene questa unità? | [Incrociare programma e manuale](.agents/skills/mappa-manuale/SKILL.md) | Righe obiettivo, edizione, sezione, stato della verifica. |
| A quale scuola, insegnamento e anno porta una classe di concorso? | [Verificare un’assegnazione](.agents/skills/verifica-assegnazioni/SKILL.md) | Cella dell’indice documentata e collegamento al programma pertinente. |
| Come registrare e pubblicare uno stato del progetto? | [Creare un commit e fare push](.agents/skills/git-commit-push/SKILL.md) | SHA delle attività precedenti aggiornati nello stesso commit utile, messaggio esteso in italiano e verifica del push autorizzato. |

## Come eseguire le procedure

**Modifica normativa.** Parti dal testo in uso. Cerca gli atti successivi presso il Ministero dell’istruzione e del merito, la Gazzetta Ufficiale o Normattiva. Apri il testo e l’allegato. Annota l’oggetto modificato, il riferimento preciso, la data di pubblicazione, la decorrenza e le coorti. Se una riforma parte dalle prime, costruisci il prospetto delle classi coinvolte per ogni anno scolastico. Confrontalo con i file esistenti e conserva il precedente quadro finché vi sono classi che lo seguono.

**Programma e manuale.** Trasforma l’unità in un risultato osservabile. Identifica il libro con autore, titolo, volume, editore, edizione e ISBN quando disponibile. Controlla il sommario della stessa edizione. Collega al risultato una sezione effettivamente leggibile. Se hai soltanto la descrizione del volume, registra «affinità tematica» e lascia aperta la verifica di capitolo e pagine. Annota le attività che il docente deve integrare.

**Assegnazione.** Verifica prima il titolo e le note di accesso alla classe di concorso. Apri poi il quadro dell’ordine di scuola, dell’indirizzo, dell’articolazione e della coorte. Leggi insieme la riga della disciplina, gli anni con ore, gli altri codici ammessi e le relative note. Distingui accesso ordinario, salvaguardia di titolarità e compresenza. Nella home collega il sotto-README che documenta la riga. Nel sotto-README conserva la fonte e i limiti dell’assegnazione.

**Commit e push.** Applica la skill Git quando devi registrare o pubblicare modifiche. Prepara un messaggio esteso in italiano con oggetto sintetico, motivazioni, modifiche, verifiche, limiti e provenienza. Commit e push seguono le autorizzazioni effettivamente ricevute; una richiesta esplicita che include entrambi autorizza entrambi. Prima dello staging, risolvi nel registro gli SHA delle attività e delle fasi precedenti già versionate, verificandone il contenuto nella storia e conservando il primo commit storico. Includi il registro nello stesso commit utile; le fasi correnti restano `PENDING` fino al successivo intervento. Verifica il push autorizzato e comunica subito lo SHA corrente in chat, senza commit aggiuntivi o amend dedicati alla sola tracciabilità.

## Come registrare il risultato

Una verifica ripetibile conserva data della consultazione, URL pubblico, riferimento interno al documento e conclusione circoscritta. Registra anche una fonte contrastante quando cambia il quadro interpretativo. Etichetta come proposta le scelte dell’autore su ordine dei temi, tempi, esercizi e manuali consigliati. Registra ogni attività coerente svolta con l'IA in una riga del [registro delle attività](docs/interazioni-ai/registro.md), accorpando le correzioni della stessa attività. Consulta la [nota sull'uso dell'IA](docs/ricerca-ai/uso-ai.md) per i riferimenti di ricerca. Aggiorna la data della home e i collegamenti interessati secondo [AGENTS.md](AGENTS.md).
