## Import file in Logistic Planner

### Sinopsi
```
python3 geoplus-logisticplanner [-source <path>] [--depots <list>]
```

### Descrizione
Invia i file a Logisitc Planner.

### Opzioni
```
-source <path>
```
Indica il path che contiene le cartelle partizionate per ogni instanza.

```
--depots <list>
```
Se specificato, solo i depositi elencati saranno processati. La lista deve contenere l'id dei depositi separati da una virgola e SENZA spazi, ad esempio:
```
--depots 12345,28421,35832
```