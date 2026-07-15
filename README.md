# Ombre e Percorsi

Archivio fotografico personale, organizzato per album. Sito statico Jekyll, pubblicato con GitHub Pages.

## Come aggiungere un nuovo album

1. **Crea la cartella delle foto** dentro `assets/images/albums/`, con un nome breve senza spazi (es. `sofia-bulgaria`), e mettici dentro le foto.
   - Consiglio: rinomina i file con un numero davanti (`01-piazza.jpg`, `02-mercato.jpg`, ...) così compaiono in quell'ordine nell'album.

2. **Crea il file dell'album** dentro `_albums/`, chiamandolo ad esempio `sofia-bulgaria.md`, con questo contenuto:

```yaml
   ---
   title: "Sofia, Bulgaria"
   date: 2026-04-02
   location: "Sofia, Bulgaria"
   description: "Una breve descrizione dell'album, visibile anche in home."
   folder: "sofia-bulgaria"      # deve combaciare col nome della cartella foto
   cover: "01-piazza.jpg"        # il file usato come copertina in home
   captions:
     01-piazza.jpg: "Didascalia opzionale solo per questa foto."
     05-museo.jpg: "Le didascalia sono facoltative: aggiungile solo dove vuoi."
   ---
```

3. Fatto: tutte le foto presenti nella cartella dell'album vengono mostrate automaticamente nella pagina dell'album, in ordine alfabetico/numerico. Non serve elencarle una per una — solo `cover` e le eventuali `captions` vanno indicate a mano.

4. L'album comparirà in home ordinato per `date` (più recenti prima).

## Sviluppo locale

```
bundle install
bundle exec jekyll serve
```
