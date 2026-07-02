# Identità visiva quindi — token per il sito DPP

## Colori

| Ruolo | HEX | Uso |
|---|---|---|
| Verde primario | `#0BCE88` | accenti, badge, elementi attivi, bordi |
| Verde scuro | `#07A86E` | testo su verde chiaro, hover, kicker |
| Verde tint | `#EEF6F1` | sfondo dei riquadri/callout in evidenza |
| Nero/inchiostro | `#111111` | testo principale, header/footer scuri |
| Nero pieno | `#0A0A0A` | sfondi scuri (title/footer) |
| Grigio | `#6B7280` | testo secondario, didascalie |
| Grigio chiaro | `#9AA0A8` | testo tenue, note |
| Bordo | `#E3E6EA` | bordi tabelle e card |
| Off-white | `#F5F7F8` | sfondo alternato righe tabella, card neutre |
| Bianco | `#FFFFFF` | sfondo principale dei contenuti |

**Regola di dominanza:** il verde `#0BCE88` è l'accento, non il colore dominante.
Sfondo dei contenuti bianco, testo scuro. Header e footer possono essere scuri (`#0A0A0A`)
per fare da "sandwich" attorno ai contenuti chiari.

## Tipografia
- Font di brand: **Hanken Grotesk** (Google Fonts, gratuito). Importalo da Google Fonts.
- Fallback: `-apple-system, "Segoe UI", Roboto, Arial, sans-serif`.
- Titoli in peso semibold/bold; corpo in regular. Buon contrasto e interlinea generosa.

Esempio import:
```css
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@400;500;600;700&display=swap');
:root { --font: 'Hanken Grotesk', -apple-system, 'Segoe UI', Roboto, Arial, sans-serif; }
```

## Logo (in `assets/`)
- `quindi-logo-white.png` — logo con testo bianco: usare **su sfondo scuro** (header/footer scuri).
- `quindi-logo-dark.png` — logo con testo scuro: usare **su sfondo chiaro**.
- `quindi-mark.png` — solo il simbolo (la "Q" verde): per favicon o spazi piccoli.

Mantieni un margine di rispetto attorno al logo; non deformarlo (conserva le proporzioni ~4.5:1 per i loghi con testo).

## Da evitare (coerenza con lo stile quindi)
- Niente linee/accento decorative sotto i titoli.
- Niente barre colorate a tutta larghezza come decorazione.
- Niente sfondi crema/beige: usare bianco o i colori del brand.
- Non dare a tutti i colori lo stesso peso: il verde è accento, non riempimento.
