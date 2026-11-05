# Mappatura Nebrodi

Mappatura delle realtà produttive e delle risorse culturali nei 24 comuni del Parco dei Nebrodi, pensata per individuare possibili collaborazioni lungo la filiera della castagna: frutto, legno, buccia, riccio, foglie, corteccia, segatura e castagne non commerciabili.

- **261 realtà produttive**, divise in 10 macro-categorie.
- **58 risorse culturali** (macro-categoria 11): sagre, musei, monumenti, percorsi, tradizioni, associazioni e centri di educazione ambientale.

## Comuni mappati

**Messina:** Acquedolci, Alcara li Fusi, Capizzi, Caronia, Cesarò, Floresta, Galati Mamertino, Longi, Militello Rosmarino, Mistretta, Raccuja, Sant'Agata di Militello, Santa Domenica Vittoria, San Fratello, San Marco d'Alunzio, Santo Stefano di Camastra, San Teodoro, Tortorici, Ucria.

**Catania:** Bronte, Maniace, Randazzo.

**Enna:** Cerami, Troina.

## Contenuto del repository

| Percorso | Contenuto |
|---|---|
| `index.html` | L'applicativo: una scheda e un colore per ogni macro-categoria, legenda cliccabile, filtri per comune e disponibilità, campi da compilare, esportazione CSV e JSON |
| `data/produttive.json` | Le realtà produttive (macro-categorie 1–10) |
| `data/culturali.json` | Le risorse culturali (macro-categoria 11) |
| `download/mappatura_nebrodi.xlsx` | Excel completo: una scheda per macro-categoria, colori per categoria e legenda con i conteggi |
| `download/*.csv` | Gli stessi dati in CSV, con il punto e virgola come separatore |

## Pubblicare con GitHub Pages

1. Crea un nuovo repository su GitHub e carica tutti i file di questa cartella, compreso `.nojekyll`.
2. Vai in **Settings → Pages**.
3. In **Source** scegli **Deploy from a branch**, poi il branch `main` e la cartella `/ (root)`, e salva.
4. Dopo un minuto circa la pagina è online all'indirizzo `https://<utente>.github.io/<nome-repository>/`.

Ogni macro-categoria ha un link diretto: per esempio `#m7` apre l'artigianato artistico e `#m11` le risorse culturali.

Aprendo `index.html` con doppio clic il browser blocca la lettura dei file JSON. Per provarlo sul computer avvia un piccolo server nella cartella, per esempio con `python3 -m http.server`, e apri `http://localhost:8000`.

## Compilare e aggiornare i dati

Le colonne con la matita (Lavorazione, Materia prima, Possibile collaborazione, Disponibilità, Note e, nella scheda 11, Possibile collegamento) si compilano direttamente nella pagina. Le modifiche restano **solo nel browser di chi le fa**: GitHub Pages ospita pagine statiche e non ha un database.

Per renderle definitive e condividerle con il gruppo:

1. Nella pagina premi **Esporta dati (JSON)**: scarica `produttive.json` e `culturali.json` con le modifiche incluse.
2. Sostituisci i file nella cartella `data/` del repository e fai un commit.
3. Chi apre la pagina vede i dati aggiornati. **Ripristina dati originali** cancella le modifiche locali e ricarica i file del repository.

Ogni record ha un `id` stabile: aggiungendo nuove righe a mano, usa un `id` nuovo e lo stesso schema degli altri record.

## Fonti e limiti

- **Realtà produttive:** ricerche su Pagine Gialle per sottocategoria su ciascun comune, del 5 novembre 2026. Sono state tenute solo le attività con sede nei 24 comuni ed è stato scartato ciò che non era pertinente (negozi, imprese edili, sindacati e simili).
- **Risorse culturali:** schede dei comuni, centri visita e itinerari del sito del [Parco dei Nebrodi](https://www.parcodeinebrodi.it), più ricerche web. Ogni riga ha il link alla sua fonte.
- **Contatti e date:** sono quelli pubblicati online e vanno verificati prima di contattare le attività. Dove la fonte non indicava un dato (ad esempio l'organizzatore di una sagra) il campo dice "Da verificare".
- **Lacune note:** laboratori tessili, cosmetici e di biomateriali, aziende con castagneti, apicoltori, pro loco e fattorie didattiche sono poco presenti online e vanno integrati con altre fonti (Parco, GAL, consorzi, UNPLI).
