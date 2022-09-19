# Introduzione

## Motivazione
Lo script Python GEO+ NON è industrializzato e la mantenibilità del software è bassisima. Inoltre manca una corretta gestione degli errori; in altre parole, lo script è stato sviluppato assumendo che "tutto funzioni correttamente", ma sappiamo che il mondo reale si comporta all'opposto: errori e situazioni anomale sono all'ordine del giorno.

## Scopo documento
Lo scopo di questo documento è definire un piano di rinnovamento dello script. Questo documento si rivolge agli sviluppatori e NON va condiviso con altre figure, almeno fino a quando il piano non sarà completamente definito.

## Proposta
La proposta prende ispirazione da questo articolo: [CUPID Development](https://dannorth.net/2022/02/10/cupid-for-joyful-coding/)

Si propone di spezzettare lo script GEO+ in più parti, che siano più facilmente TESTABILI ed ESEGUIBILI.
Ogni parte avrà una singola funzionalità, così che sarà più facile capire se funziona oppure no. Invece, ad oggi esiste uno script unico ed è più difficile individuare cosa/dove/perché qualcosa ha smesso di funzionare.

Di fatto, lo script GEO+ sarà diviso in tanti piccoli script Python. Ogni script sarà TESTABILE, cioè ci saranno dei casi di test facili da verificare. Ogni script sarà facilmente ESEGUIBILE, cioè dalla macchina Linux sarà possibile eseguire il comando "python3 unzip /files_to_unzip_are_here" e poi "python3 archive /files_to_archive_are_here /archive" (i comandi precedenti sono solo degli esempi e non riflettono quello che sarà implementato!).

# Comandi

- [Opzioni comuni a tutti i comandi](./commands/CommandCommonOptions.md)
- [Lettura file GeoPlus](./commands/CommandGeoplusRead.md)
- [Generazione file intermedi](./commands/CommandGeoplusExtract.md)
- [Split file intermedi](./commands/CommandGeoplusSplit.md)
- [Generazione Masterdata/DepotKnowledge](./commands/CommandGenerate.md)
- [Import file in Logistic Planner](./commands/CommandLogisticPlanner.md)