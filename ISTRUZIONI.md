# Istruzioni per Claude Code — Sito Digital Product Passport (DPP)

## Obiettivo
Creare un sito web statico che funga da **Digital Product Passport** per una bicicletta
Bianchi T-Tronik C-Type Donna. Il sito è il contenuto a cui punta un QR code applicato sul
telaio. È un Proof of Concept (PoC) da pubblicare come sito statico.

## Fonte dei contenuti
Tutti i testi e i dati sono in **`dpp-content.md`**. Non inventare dati: usa solo quelli del file.
Il documento è organizzato nelle 3 sezioni ufficiali del DPP:
1. Identificazione e anagrafica
2. Sostenibilità e impatto ambientale
3. Circolarità e fine vita

## Requisiti tecnici
- **Sito statico**, pubblicabile su **GitHub Pages** (o Netlify). Nessun backend, nessun database.
- HTML + CSS (+ minimo JS se serve). Semplice e manutenibile. Va bene anche un solo file `index.html`,
  ma è preferibile separare `index.html`, `style.css` e mettere le immagini in `assets/`.
- **Mobile-first**: la pagina viene aperta soprattutto da smartphone dopo la scansione del QR.
  Deve essere leggibile e ordinata su schermo piccolo.
- Nessuna dipendenza pesante: niente framework obbligatori. Se vuoi usare qualcosa, resta leggero.

## Struttura URL (GS1 Digital Link)
Rispetta lo schema descritto in `dpp-content.md`:
`https://dpp.quindi.ai/01/{GTIN}/21/{seriale}`
Per il PoC va bene una pagina singola servita a un URL fisso; se implementi il routing,
segui questo schema (prefisso `/01/` per il GTIN, `/21/` per il seriale).

## Gestione dei tag dato `[REALE]` / `[STIMA]`
Nel file dei contenuti ogni dato è marcato `REALE` o `STIMA`.
- I dati `REALE` si mostrano normalmente.
- I dati `STIMA` sono valori dimostrativi: mostrali comunque, ma con un **badge piccolo e discreto**
  (es. una pillola grigia "valore dimostrativo" o un asterisco con nota a piè pagina).
- NON rimuovere i dati `STIMA`: servono a rendere il PoC completo.
- In fondo alla pagina, aggiungi una breve nota che spiega la differenza tra dato reale e stima.

## Identità visiva (quindi)
Vedi **`brand.md`** per colori, font e uso del logo. In sintesi:
- Colore primario verde `#0BCE88`; sfondo chiaro per i contenuti, header/footer scuri se serve contrasto.
- Logo in `assets/` (versione chiara per sfondo scuro, versione scura per sfondo chiaro, più il solo simbolo).
- Look pulito, professionale, poco decorato. Niente barre colorate decorative o linee accento sotto i titoli.

## Struttura della pagina (suggerita)
1. **Header**: logo quindi + nome prodotto "Bianchi T-Tronik C-Type Donna" + una riga che dice cos'è (Digital Product Passport).
2. **Sezione 1 — Identificazione**: codici, scheda tecnica, distinta base (BOM) con fornitori. La BOM è una tabella importante: rendila leggibile su mobile (card impilate o tabella scrollabile).
3. **Sezione 2 — Sostenibilità**: carbon footprint (idealmente con una piccola visualizzazione della scomposizione per componente), provenienza materiali, consumo risorse. Includi la nota metodologica PEF.
4. **Sezione 3 — Circolarità e fine vita**: link manutenzione (bottoni/link ufficiali), passi di smontaggio, tabella riciclo, e il riquadro Battery Passport (mettilo in evidenza: è il punto forte).
5. **Footer**: governance/standard (ESPR, GS1, PEF), la frase di sintesi sul valore per Bianchi, e la nota sui dati dimostrativi.

## Note utili
- I link della sezione 3.1 sono URL ufficiali reali: rendili cliccabili (aprono in nuova scheda).
- Il Battery Passport (sezione 3.4) è il contenuto più distintivo perché è una e-bike: dagli risalto visivo.
- Puoi generare tu un QR code di esempio che punta all'URL del sito (per la demo), ma è opzionale.
