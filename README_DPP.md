# Digital Product Passport — Bianchi T-Tronik C-Type Donna

Un sito web statico conforme a **ESPR (UE) 2024/1781** e **Batterie (UE) 2023/1542** che funziona da Passaporto Digitale Prodotto per una e-bike Bianchi.

## 📱 Caratteristiche

✅ **Mobile-first**: progettato e testato per smartphone (320px+)  
✅ **Statico**: nessun backend, nessun database — puro HTML + CSS  
✅ **Leggero**: zero dipendenze JavaScript, Google Fonts è l'unica risorsa esterna  
✅ **Responsive**: layout fluido su tablet, desktop e print  
✅ **Brand**: identità visiva quindi.ai (colori, font Hanken Grotesk, loghi)  
✅ **Accessibile**: semantica HTML5, contrasti WCAG AA  
✅ **Pubblicabile**: pronto per GitHub Pages, Netlify, o qualunque host statico

## 📂 Struttura

```
sito_fotonico/
├── index.html                 # Pagina principale (unico file HTML)
├── style.css                  # Stili mobile-first responsivi
├── assets/                    # Logo e risorse
│   ├── quindi-logo-white.png       # Logo testo bianco (sfondo scuro)
│   ├── quindi-logo-dark.png        # Logo testo scuro (sfondo chiaro)
│   └── quindi-mark.png             # Simbolo Q verde (favicon)
├── ISTRUZIONI.md              # Brief originale del progetto
├── dpp-content.md             # Contenuti e dati del DPP
├── brand.md                   # Identità visiva quindi
├── SETUP_GITHUB_PAGES.md      # Guida publicazione GitHub Pages
├── README_DPP.md              # Questo file
├── .gitignore                 # Per repository Git
└── dpp-site-package.zip       # Pacchetto originale (backup)
```

## 🚀 Quick Start

### Locale
```bash
cd C:\Users\HP\Desktop\sito_fotonico
python -m http.server 8000
# Apri http://localhost:8000
```

### GitHub Pages
Vedi **SETUP_GITHUB_PAGES.md** per la guida completa di pubblicazione.

## 📋 Contenuti

Il sito è organizzato in **3 sezioni ufficiali del DPP**:

### 1️⃣ Identificazione e anagrafica
- Codici univoci (GTIN, numero di serie, lotto)
- Scheda tecnica (tipo, telaio, ruote, peso, autonomia)
- **Distinta Base (BOM)**: 14 componenti con fornitori, modelli e materiali
- Dati di fabbricazione (produttore, data, anno modello)

### 2️⃣ Sostenibilità e impatto ambientale
- **Carbon footprint** (LCA): ~180 kg CO₂e totali, scomposto per componente
  - Batteria: 55 kg CO₂e
  - Telaio: 45 kg CO₂e
  - Motore + elettronica: 40 kg CO₂e
  - Componenti: 40 kg CO₂e
- Provenienza materiali (alluminio, acciaio, batterie, certificazioni)
- Consumo risorse (energia, acqua, scarti)
- Metodologia PEF / LCA per la trasparenza

### 3️⃣ Circolarità e fine vita
- **Link ufficiali di manutenzione** (Shimano, SRAM, SR Suntour, Bianchi)
- **Design for Disassembly**: 4 passi per smontare la bicicletta
- **Riciclabilità per componente** (batteria, motore, telaio, acciaio, pneumatici)
- **⚠ Avvertimento materiali pericolosi** (Li-ion)
- **🔋 Battery Passport** (obbligatorio dal 18.02.2027 per LMT)
  - Capacità: 417 Wh
  - SoH: ~60% dopo 1.000 cicli
  - Composizione: Li-ion NMC
  - Carbon footprint: ~55 kg CO₂e

### 📖 Governance e standard
- **ESPR** (Reg. UE 2024/1781) — obblighi DPP
- **Batterie** (Reg. UE 2023/1542) — Battery Passport
- **GS1 Digital Link** — schema URL e QR code
- **PEF / LCA** — metodologia carbon footprint (ISO 14040/44, ISO 14067)

## 🏷️ Badge [REALE] vs [STIMA]

Ogni dato è marcato nel sito per chiarire la provenienza:

- **[REALE]** (nessun badge visibile): da schede tecniche ufficiali, normative, fornitori certificati
- **[STIMA]** (badge grigio "Stima"): valori esemplificativi per il PoC, da popolare con quindi.ai in produzione

Nota finale nel sito spiega la differenza, così che lettori in mobilità capiscano immediatamente.

## 🎨 Design

- **Colore primario**: verde `#0BCE88` (accenti, bordi, badge)
- **Testo**: nero `#111111` su bianco
- **Header/Footer**: sfondo scuro `#0A0A0A` con logo bianco
- **Font**: Hanken Grotesk (Google Fonts) + fallback system sans-serif
- **Spazi**: generosi margini e padding per leggibilità mobile
- **Niente decorazioni**: pulito e professionale, senza linee inutili

### Responsive
- **Desktop** (1024px+): grid a 2-3 colonne, card affiancate
- **Tablet** (768px-1023px): grid a 2 colonne, adattamento spazi
- **Mobile** (< 768px): singola colonna, card impilate, testo leggibile

## 📄 Dati usati

Tutti i dati provengono da **dpp-content.md**:
- Specifiche Bianchi (telaio, ruote, peso, autonomia)
- Componenti Shimano, SRAM, Phylion, etc.
- Carbon footprint (metodologia PEF)
- Battery Passport (Phylion 417Wh)
- Link manutenzione ufficiali

**Non sono stati inventati dati**: il sito è una trasposizione fedele del file di contenuti.

## 🔗 URL e QR

Schema **GS1 Digital Link**:
```
https://dpp.quindi.ai/01/{GTIN}/21/{seriale}

Esempi:
https://dpp.quindi.ai/01/08059XXXXXXXX/21/TTC-2024-000427
```

Il QR code si applica sul tubo obliquo (down tube) del telaio, vicino all'alloggiamento batteria.

Nel PoC il sito è servito da un URL fisso; per il prodotto, il routing GS1 verrà gestito dall'infrastruttura quindi.ai.

## 📦 Pubblicazione

### GitHub Pages (consigliato)
1. Crea un repository su GitHub
2. Push di tutti i file (index.html, style.css, assets/)
3. Settings → Pages → Deploy from `main` branch
4. Il sito è live in ~5 minuti

### Netlify
1. Connetti il repo GitHub
2. Build command: (lasciare vuoto)
3. Publish directory: `/` (root)
4. Deploy

### Server statico custom
- Copia i file su un web server Apache, Nginx, o IIS
- Nessuna configurazione server-side richiesta

## ✔️ Checklist prima della produzione

- [ ] Aggiornare GTIN con un codice GS1 reale (attualmente STIMA)
- [ ] Aggiornare numero di serie / lotto con dati di fabbrica reali
- [ ] Popolare dati carbon footprint reali (da LCA certificato)
- [ ] Aggiungere link ufficiale Bianchi al DPP reale
- [ ] Configurare custom domain (`dpp.quindi.ai` o simile)
- [ ] Testare QR code con smartphone
- [ ] Verificare con screen reader (accessibilità)
- [ ] Print preview: controllare layout PDF

## 🛠️ Tecnologie

- **HTML5**: struttura semantica
- **CSS3**: Grid, Flexbox, Media Queries
- **Google Fonts**: Hanken Grotesk (font brand)
- **Zero JS**: nessuna dipendenza runtime

## 📜 Standard e normative

- **Regolamento ESPR** (UE) 2024/1781 — Ecodesign for Sustainable Products Regulation
- **Regolamento Batterie** (UE) 2023/1542 — Battery Passport (dal 18.02.2027 per LMT)
- **GS1**: standard internazionale per identificazione (GTIN, Digital Link)
- **PEF** (Product Environmental Footprint): metodologia EU per carbon footprint
- **LCA** (ISO 14040/44, ISO 14067): Life Cycle Assessment

## 👤 Contatti

- **Bianchi**: https://www.bianchi.com/
- **quindi.ai**: infrastruttura dati DPP (https://quindi.ai)
- **GS1**: https://gs1it.org/

---

**Sito statico quindi x Bianchi — DPP PoC v1.0**  
Creato: Luglio 2026  
Aggiornamenti: Vedi commit history nel repository Git
