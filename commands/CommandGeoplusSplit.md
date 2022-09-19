## Split file intermedi

### Sinopsi
```
python3 geoplus-split [-source <path>] [-target <path>] [-r | --replace]
                      [--filter <expression>] [--depots <list>]
```

### Descrizione
[Splitta](../etc/Glossary.md/#file-splittati) i file [intermedi](../etc/Glossary.md/#file-intermedi) generati con il comando [geoplus-extract](CommandGeoplusExtract.md).
Nella cartella specificata da __-target__ saranno create altre cartelle, ognuna avrà il nome di un deposito e conterrà i suoi file splittati.

### Opzioni
```
-source <path>
```
Indica la cartella di origine, cioè da dove leggere intermedi.

```
-target <path>
```
Indica la cartella di destinazione, cioè dove produrre i file splittati.

```
-r
--replace
```
Se NON specificato, l'esecuzione del comando si interromperà se esiste già un file splittato.

```
--filter <expression>
```
Se specificata, solo i file intermedi che rispetteranno l'expression saranno processati. Alcuni filtri possono contenere delle condizioni che bloccano l'esecuzione del comando, in caso la condizione sia violata.

```
--depots <list>
```
Se specificato, solo i depositi elencati saranno processati. La lista deve contenere l'id dei depositi separati da una virgola e SENZA spazi, ad esempio:
```
--depots 12345,28421,35832
```