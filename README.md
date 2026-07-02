# Pacchetto sito DPP — Bianchi T-Tronik C-Type Donna

Questo pacchetto contiene tutto ciò che serve a **Claude Code** per generare il sito del
Digital Product Passport (DPP).

## Contenuto della cartella

| File | Cosa contiene |
|---|---|
| `ISTRUZIONI.md` | Il brief per Claude Code: obiettivo, requisiti tecnici, struttura della pagina. **Punto di partenza.** |
| `dpp-content.md` | Tutti i dati e i testi del passaporto, organizzati nelle 3 sezioni DPP. La fonte di verità dei contenuti. |
| `brand.md` | Colori, font e regole d'uso del logo (identità quindi). |
| `assets/` | I file del logo quindi (versione chiara, scura, e solo simbolo). |

## Come usarlo con Claude Code

1. Copia questa cartella nel tuo computer (o scompatta lo zip).
2. Apri un terminale dentro la cartella.
3. Avvia Claude Code e dagli un'istruzione tipo:

   > Leggi ISTRUZIONI.md, dpp-content.md e brand.md in questa cartella.
   > Crea il sito statico del Digital Product Passport come descritto,
   > usando i dati di dpp-content.md e l'identità visiva di brand.md.
   > Voglio un sito mobile-first pubblicabile su GitHub Pages.

4. Rivedi il risultato, chiedi le modifiche che vuoi, poi pubblica su GitHub Pages/Netlify.

## Nota
I dati contrassegnati `[STIMA]` nel file dei contenuti sono valori dimostrativi per il PoC.
Vanno mostrati ma segnalati come tali (vedi ISTRUZIONI.md). Quando avrai i dati reali di
fabbrica, basterà sostituirli in `dpp-content.md` e rigenerare.
