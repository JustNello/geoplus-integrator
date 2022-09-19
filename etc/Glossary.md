# Glossary

In varie parti di questo documento si fa riferimento a questi file:
- File sorgente GEO+
- File unzippati
- File intermedi
- File splittati
- File Masterdata/DepotKnowledge

### File sorgente GEO+
Sono prodotti dai sistemi GEO+ e sono file __zippati__, cioè con estensione ".zip".

### File unzippati
Sono file sorgente GEO+ unzippati.

### File intermedi
Sono una transformazione dei file unzippati. Ogni file intermedio contiene i dati per TUTTI i depositi.

### File splittati
Un singolo file intermedio può essere "splittato" (cioè spezzetato/diviso) in più file, uno per singolo deposito.

### File Masterdata/DepotKnowledge
Sono dei file con estensione ".json" da importare in Logistic Planner.

## Flusso di esempio
```
"file_geoplus.zip"
    --> "file_geoplus_unzippato"
        --> "file_intermedio" --> "file_splittato_1_per_deposito_X"
                              --> "file_splittato_2_per_deposito_Y"
                                --> "file_masterdata_per_deposito_X.json"
                                --> "file_masterdata_per_deposito_Y.json
                                --> "file_depotknowledge_per_deposito_X.json"
                                --> "file_depotknowledge_per_deposito_Y.json
```