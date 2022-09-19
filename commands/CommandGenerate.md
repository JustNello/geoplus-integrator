## Generazione Masterdata/DepotKnowledge

### Sinopsi
```
python3 geoplus-generate [-source <path>] [-target <path>] [-r | --replace]
                         [--depots <list>] [--instances <number>] 
                         [--disable-arretramento] [--import]
```

### Descrizione
Utilizza i file [splittati](../etc/Glossary.md/#file-splittati) per generare i Masterdata ed i DepotKnowledge (maggiori dettagli [qui](../etc/Glossary.md/#file-masterdatadepotknowledge)).

### Opzioni
```
-source <path>
```
Indica la cartella dove sono stati generati i file splittati. Di fatto, è la cartella specificata dall'opzione __-target__ del comando [geoplus-split](CommandGeoplusSplit.md).

```
-target <path>
```
Indica la cartella di destinazione, cioè dove produrre i file. In base al numero di instanze, specificato con l'opzione __--instances__, i file sono partizionati. Per maggiori dettagli, si rimanda ad altri documenti in cui si fa riferimento alla famosa "formula di partizionamento", utilizzata anche da altri progetti (Indescritta, Gpl-Integration, T&T).

```
-r
--replace
```
Se NON specificato, l'esecuzione del comando si interromperà se ci sono file nella cartella specificata da __-target__

```
--depots <list>
```
Se specificato, solo i depositi elencati saranno processati. La lista deve contenere l'id dei depositi separati da una virgola e SENZA spazi, ad esempio:
```
--depots 12345,28421,35832
```

```
--instances <number>
```
Indica il numero di instanze di Logistic Planner e determina come i file generati devono essere partizionati, cioè distribuiti. Per maggiori dettagli, si rimanda ad altri documenti in cui si fa riferimento alla famosa "formula di partizionamento", utilizzata anche da altri progetti (Indescritta, Gpl-Integration, T&T).

```
--disable-arretramento
```
Se specificato, nessun deposito sarà abilitato all'arretramento.

```
--import
```
Se specificato, i file generati saranno subito importati in Logistic Planner. Altrimenti sarà possibile farlo in un secondo momento usando il comando [geoplus-logisticplanner](CommandLogisticPlanner.md).