## Lettura file GeoPlus

### Sinopsi
```
python3 geoplus-read [-source <path>] [-target <path>] [-z | --unzip]
                     [-a | --archive] [-r | --replace] [--filter <expression>]
                     [--date <expression>]
```

### Descrizione
Può copiare ed unzippare i file GEO+. Il comando NON altera la struttura o il contenuto della cartella di origine, cioè quella specificata con l'opzione __-s__

### Opzioni
```
-source <path>
```
Indica la cartella di origine, cioè da dove leggere i file di GEO+. Si assume che la cartella contenga solo file con estensione ".zip".

```
-target <path>
```
Indica la cartella di destinazione, cioè dove produrre i file.

```
-z
--unzip
```
Se specificato, i file letti dalla cartella di origine saranno unzippati, altrimenti verrà fatto un mero copia-ed-incolla dei file dalla cartella specificata con l'opzione __-source__ a quella specificata con l'opzione __-target__

```
-a
--archive
```
Se specificato, i file letti dalla cartella di origine sono posizionati in una cartella "ARCHIVE" relativa al path specificato con l'opzione __-target__

```
-r
--replace
```
Se NON specificato, l'esecuzione del comando si interromperà se ci sono file nella cartella specificata da __-target__

```
--filter <expression>
```
Se specificata, solo i file che rispetteranno l'expression saranno processati. Alcuni filtri possono contenere delle condizioni che bloccano l'esecuzione del comando, in caso la condizione sia violata.

```
--date <expression>
```
Per convenzione, assumiamo che i file nella cartella specificata da __-source__ abbiano un prefisso nel nome. Il prefisso indica la data di validità di quei file GEO+. L'opzione __--date__ permette di specificare in che modo filtrare i file e quali prendere in considerazione, in base alla data. Può essere usato in congiunzione con l'opzione __--filter__