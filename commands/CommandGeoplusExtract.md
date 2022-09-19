## Generazione file intermedi

### Sinopsi
```
python3 geoplus-extract [-source <path>] [-target <path>] [-r | --replace]
                        [--filter <expression>]
```

### Descrizione
Utilizza i file GEO+ [unzippati](../etc/Glossary.md/#file-unzippati) per generare i file [intermedi](../etc/Glossary.md/#file-intermedi). Per ottenere i file unzippati, si rimanda al comando [geoplus-read](CommandGeoplusRead.md).

### Opzioni
```
-source <path>
```
Indica la cartella di origine, cioè da dove leggere unzippati. Il comando darà errore se la cartella contiene almeno un file sconosciuto.

```
-target <path>
```
Indica la cartella di destinazione, cioè dove produrre i file intermedi.

```
-r
--replace
```
Se NON specificato, l'esecuzione del comando si interromperà se ci sono file nella cartella specificata da __-target__

```
--filter <expression>
```
Se specificata, solo i file che rispetteranno l'expression saranno processati. Alcuni filtri possono contenere delle condizioni che bloccano l'esecuzione del comando, in caso la condizione sia violata.