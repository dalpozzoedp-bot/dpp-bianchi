# Pubblicazione su GitHub Pages

Questo Digital Product Passport è un sito statico pronto per la pubblicazione su GitHub Pages.

## Passi per pubblicare

### 1. Preparazione del repository GitHub

Se non hai ancora un repository:

```bash
git init
git add .
git commit -m "Initial commit: DPP Bianchi T-Tronik"
git branch -M main
git remote add origin https://github.com/TUO_USERNAME/DPP_REPOSITORY.git
git push -u origin main
```

Sostituisci `TUO_USERNAME` e `DPP_REPOSITORY` con i tuoi dati GitHub.

### 2. Attiva GitHub Pages

1. Vai al repository su GitHub
2. Clicca su **Settings** → **Pages**
3. Seleziona:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main`
   - **Folder:** `/ (root)`
4. Clicca **Save**

GitHub Pages pubblicherà automaticamente il sito all'URL:
```
https://TUO_USERNAME.github.io/DPP_REPOSITORY/
```

### 3. Configurazione opzionale: custom domain

Se hai un dominio personalizzato (es. `dpp.quindi.ai`):

1. Nello stesso pannello **Settings → Pages**, aggiungi il dominio in **Custom domain**
2. Aggiorna i DNS del tuo dominio per puntare a GitHub Pages
3. Abilita **Enforce HTTPS**

## Struttura del progetto

```
sito_fotonico/
├── index.html              # Pagina principale (unico file HTML)
├── style.css               # Stili mobile-first
├── assets/
│   ├── quindi-logo-white.png    # Logo per sfondo scuro
│   ├── quindi-logo-dark.png     # Logo per sfondo chiaro
│   └── quindi-mark.png          # Simbolo della Q per favicon
├── SETUP_GITHUB_PAGES.md   # Questa guida
└── ISTRUZIONI.md           # Specifiche del progetto
```

## Test locale

Per testare il sito prima di pubblicarlo:

### Opzione 1: Python (Python 3.x)
```bash
cd C:\Users\HP\Desktop\sito_fotonico
python -m http.server 8000
```
Apri il browser su `http://localhost:8000`

### Opzione 2: Node.js
```bash
npx http-server
```

### Opzione 3: VS Code Live Server
Installa l'estensione "Live Server" di Ritchie Zelazny, clicca destro su `index.html` e seleziona "Open with Live Server".

## Note sulla compatibilità

- ✅ Mobile-first: testato su viewport da 320px fino a 1200px+
- ✅ Modern browsers: Chrome, Firefox, Safari, Edge (ultimi 2 anni)
- ✅ Nessuna dipendenza esterna (solo Google Fonts)
- ✅ CSS Grid e Flexbox per layout responsive
- ✅ Accessibilità: contrasti WCAG AA, semantica HTML5

## Badge e dati dimostrativi

I dati marcati con **[STIMA]** nel file `dpp-content.md` sono mostrati con un piccolo badge grigio "Stima" nel sito, per chiarire che sono valori esemplificativi per il Proof of Concept.

I dati **[REALE]** da documenti ufficiali (schede tecniche, fornitori, normative) non hanno badge.

## Aggiornamento contenuti

Per aggiornare i dati del DPP:

1. Modifica `index.html` direttamente (è auto-contenuto)
2. Commit e push su GitHub
3. GitHub Pages si aggiornerà automaticamente entro pochi minuti

Non serve compilare, buildare, né install dipendenze.

## Troubleshooting

### Il sito non appare su GitHub Pages
- Verifica che il branch sia impostato correttamente in Settings → Pages
- Controlla i GitHub Actions per eventuali errori di build
- Aspetta 5 minuti dopo il push (a volte ci vuole tempo)

### Le immagini (logo) non si caricano
- Verifica che la cartella `assets/` sia nel repository
- I path nel HTML usano `assets/` (relativo): questo funziona sia in locale che su GitHub Pages

### Styling non carica
- Pulisci cache del browser: Ctrl+Shift+Del
- Verifica che `style.css` sia nella root directory (stesso livello di `index.html`)

## QR Code per il sito

Puoi generare un QR code che punta all'URL del sito pubblicato usando:
- https://www.qr-code-generator.com/
- https://qr.io/

QR da scansionare sul telaio della bicicletta 🚲

---

**Creato con:** HTML5 + CSS3 mobile-first  
**Font:** Hanken Grotesk (Google Fonts)  
**Brand:** quindi.ai identity  
**Standard:** ESPR (UE) 2024/1781 + GS1 Digital Link
