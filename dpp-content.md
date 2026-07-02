# Contenuto DPP — Bianchi T-Tronik C-Type Donna

> Questo file contiene TUTTI i dati da mostrare nel sito del Digital Product Passport (DPP).
> È la fonte di verità per i contenuti. La struttura segue lo schema DPP a 3 sezioni
> richiesto dal Regolamento ESPR e dagli standard GS1.
>
> **Legenda tag dato:**
> - `[REALE]` = informazione verificabile (schede tecniche / fornitori). Mostrare normalmente.
> - `[STIMA]` = valore simulato per il Proof of Concept. Nel sito pubblico va segnalato con un
>   piccolo badge discreto (es. "valore dimostrativo") oppure nascosto dietro un tooltip.
>   NON eliminare l'informazione del tag: serve a distinguere i due tipi di dato.

---

## Intestazione del passaporto

- **Prodotto:** Bianchi T-Tronik C-Type Donna
- **Tipologia:** E-bike urbana a pedalata assistita (city / trekking elettrica), categoria LMT (Light Means of Transport)
- **Posizione QR:** tubo obliquo (down tube) del telaio, vicino all'alloggiamento della batteria
- **Schema URL (GS1 Digital Link):** `https://dpp.quindi.ai/01/{GTIN}/21/{seriale}`
  - `/01/` = prefisso GS1 per il GTIN (codice prodotto)
  - `/21/` = prefisso GS1 per il numero di serie del singolo esemplare
- **Colori disponibili:** Bronzo Cangiante / Blu Pietra `[REALE]`

---

## SEZIONE 1 — Identificazione e anagrafica del prodotto

### 1.1 Codici univoci

| Codice | Valore | Tag | Note |
|---|---|---|---|
| GTIN | 08059XXXXXXXX | STIMA | Codice prodotto GS1, da assegnare via GS1 Italy |
| Numero di serie | TTC-2024-000427 | STIMA | Identifica il singolo esemplare |
| Numero di lotto | LOT-2024-11 | STIMA | Lotto / settimana di produzione |
| Codice modello Bianchi | T-Tronik C-Type Donna | REALE | Denominazione commerciale |

### 1.2 Scheda tecnica

| Caratteristica | Valore | Tag |
|---|---|---|
| Tipologia | E-bike urbana a pedalata assistita (25 km/h) | REALE |
| Telaio | Alluminio PG 6061, geometria step-through, taglie 43/47 | REALE |
| Ruote | 28" — ETRTO 622, cerchi e-bike a 32 fori | REALE |
| Livelli di assistenza | 3 livelli, fino a 25 km/h | REALE |
| Peso (indicativo) | ~27 kg | STIMA |
| Autonomia | Fino a 95 km | REALE |
| Colori | Bronzo Cangiante / Blu Pietra | REALE |

### 1.3 Distinta base (BOM) — componenti e fornitori

| Componente | Modello | Fornitore | Materiale prevalente | Tag |
|---|---|---|---|---|
| Motore | Shimano STEPS E6100 (250W, 60Nm) | Shimano | Alluminio / rame / magneti | REALE |
| Batteria | Phylion integrata 417Wh (36V) | Phylion | Celle Li-ion (NMC) | REALE |
| Display / cablaggio | Shimano SC-E6100 + cablaggio E-TUBE | Shimano | Plastica ABS / rame | REALE |
| Comandi cambio | SRAM X5, 9v | SRAM | Alluminio / acciaio | REALE |
| Cambio | SRAM X7, 9v (max 36T) | SRAM | Alluminio / acciaio | REALE |
| Guarnitura | FSA SMN e-bike + corona Shimano 38T | FSA / Shimano | Alluminio forgiato | REALE |
| Catena | KMC e9S | KMC | Acciaio | REALE |
| Freni | Promax DSK-925, dischi 160mm | Promax | Acciaio / alluminio | REALE |
| Forcella | Suntour NEX-E25 (63mm) | SR Suntour | Acciaio / alluminio | REALE |
| Pneumatici | Chaoyang E-Liner City 700x45C | Chaoyang (ZC-Rubber) | Gomma / tessuto | REALE |
| Cerchi / mozzi | Cerchi e-bike 28" + mozzi Shimano TX505 | Shimano | Alluminio | REALE |
| Manubrio / reggisella | Velomann | Velomann | Alluminio | REALE |
| Sella | Sella city comfort | Selle Royal (tipico) | Acciaio / schiuma / eco-pelle | STIMA |
| Portapacchi / ferramenta | Portapacchi posteriore (25 kg) + minuteria | Bianchi / OEM | Alluminio / acciaio inox | STIMA |

### 1.4 Dati di fabbricazione

| Voce | Valore | Tag |
|---|---|---|
| Produttore | F.I.V. Edoardo Bianchi S.p.A. — Treviglio (BG), Italia | REALE |
| Stabilimento di assemblaggio | Da specificare per lotto | STIMA |
| Data di produzione | Novembre 2024 (esempio) | STIMA |
| Anno modello | 2024 | REALE |

---

## SEZIONE 2 — Sostenibilità e impatto ambientale

> **Nota metodologica:** i valori di carbon footprint si calcolano con la metodologia europea
> PEF (Product Environmental Footprint), su base LCA (ISO 14040/44 e 14067), espressi in
> kg CO₂e. Per la T-Tronik questi dati non sono pubblici: nel PoC sono STIME. Servono a mostrare
> perché è necessaria un'infrastruttura dati (quindi.ai) per popolarli con valori reali e
> verificati da terza parte.

### 2.1 Carbon footprint (LCA)

| Voce | Valore | Metodo | Tag |
|---|---|---|---|
| Impronta totale bici | ~180 kg CO₂e | LCA cradle-to-gate | STIMA |
| di cui telaio alluminio | ~45 kg CO₂e | PEF materiali | STIMA |
| di cui batteria 417Wh | ~55 kg CO₂e | PEF batterie (Art. 7 Reg. 2023/1542) | STIMA |
| di cui motore + elettronica | ~40 kg CO₂e | PEF componenti | STIMA |
| di cui altri componenti | ~40 kg CO₂e | PEF componenti | STIMA |

### 2.2 Provenienza dei materiali

- **Alluminio telaio (PG 6061):** percentuale di riciclato ~30% `[STIMA]` — da certificare con il fornitore del telaio.
- **Acciaio (catena, minuteria, dischi):** riciclabile al 100%, quota di riciclato in ingresso da dichiarare `[STIMA]`.
- **Celle batteria (Li-ion NMC):** materiali critici — litio, nichel, cobalto, grafite; tracciabilità richiesta dal Reg. Batterie `[REALE]`.
- **Certificazioni:** per il ciclo (metallo/gomma) NON si applicano FSC/GOTS (tipiche di legno e tessile); rilevano le dichiarazioni ambientali di prodotto (EPD) e la conformità REACH/RoHS per l'elettronica `[REALE]`.

### 2.3 Consumo di risorse (produzione)

| Risorsa | Valore | Tag |
|---|---|---|
| Energia di assemblaggio | ~25 kWh per unità | STIMA |
| Acqua (verniciatura / trattamenti) | ~120 litri per unità | STIMA |
| Scarti di produzione | % da rilevare in linea (dato quindi.ai) | STIMA |

---

## SEZIONE 3 — Circolarità e fine vita

### 3.1 Istruzioni di utilizzo e manutenzione (link ufficiali)

- Sistema Shimano STEPS E6100 (uso, ricarica, display) — https://www.shimano-steps.com/e-bikes/europe/en/product-information/city-trekking/e6100 `[REALE]`
- FAQ e manutenzione batteria/motore Shimano — https://bike.shimano.com/support-and-service/faq/STP0A.html `[REALE]`
- Manuali e service trasmissione SRAM — https://www.sram.com/en/service/manuals--documents `[REALE]`
- Manuale forcella SR Suntour NEX — https://www.srsuntour.com/support/product-support/owners-manuals/ `[REALE]`
- Pagina modello Bianchi — https://www.bianchi.com/it/t-tronik-c-type/ `[REALE]`

**Consiglio d'uso chiave (dai manuali reali):** per prolungare la vita della batteria Shimano E6100,
conservarla a ~70% di carica se inutilizzata a lungo ed evitare ricariche ripetute tra 80% e 100%.
Dopo 1.000 cicli di ricarica la cella mantiene circa il 60% della capacità originaria (dato utile per
lo stato di salute nel Battery Passport). `[REALE]`

### 3.2 Smontabilità (Design for Disassembly)

1. **Estrarre la batteria** — sgancio rapido sulla parte superiore del tubo obliquo (nessun utensile).
2. **Rimuovere motore ed elettronica** — motore al movimento centrale, display e cablaggio E-TUBE; avviano il flusso RAEE.
3. **Separare i gruppi meccanici** — trasmissione, freni, forcella, ruote (acciaio / alluminio).
4. **Telaio nudo** — alluminio PG 6061 avviato al riciclo dedicato, massimizzando la purezza del materiale.

### 3.3 Riciclabilità e smaltimento per componente

| Componente | Flusso di fine vita | Note | Tag |
|---|---|---|---|
| Batteria Li-ion | Raccolta batterie dedicata | Reg. UE 2023/1542 — no indifferenziato | REALE |
| Motore / display / cablaggio | RAEE (elettronica) | Dir. RAEE 2012/19/UE | REALE |
| Telaio alluminio | Riciclo metalli | Riciclabile ~100% | REALE |
| Acciaio (catena, dischi, minuteria) | Riciclo metalli | Riciclabile ~100% | REALE |
| Pneumatici / camere d'aria | Riciclo gomma | Filiera dedicata gomma | STIMA |
| Sella / plastiche | Recupero plastiche | Da verificare per materiale | STIMA |

**Materiali pericolosi:** le celle Li-ion vanno gestite come rifiuto pericoloso; nessun contenuto di
mercurio/cadmio/piombo oltre le soglie del Reg. Batterie. `[REALE]`

### 3.4 Battery Passport

> Essendo una e-bike, la batteria attiva il Battery Passport, obbligatorio dal 18 febbraio 2027
> per le batterie LMT (Reg. UE 2023/1542). È il primo pilastro del DPP, non una normativa separata:
> lo stesso QR sul telaio dà accesso anche a questi dati.

| Dato | Valore | Fonte | Tag |
|---|---|---|---|
| Capacità nominale | 417 Wh (36V) | Scheda tecnica Phylion | REALE |
| Stato di salute (SoH) | ~60% dopo 1.000 cicli | FAQ Shimano E6100 | REALE |
| N° cicli di carica | Contatore da sistema (E-TUBE) | Telemetria motore | STIMA |
| Composizione celle | Li-ion NMC (litio, nichel, cobalto, grafite) | Fornitore cella | STIMA |
| Carbon footprint batteria | ~55 kg CO₂e (da dichiarare/verificare) | PEF, Art. 7 Reg. Batterie | STIMA |
| % materiali recuperati | Obbligo dal 2028 | Reg. Batterie | REALE |

---

## Governance dei dati e standard

- **Quadro normativo:** Regolamento ESPR (UE) 2024/1781 per il DPP; Regolamento Batterie (UE) 2023/1542 per il Battery Passport. `[REALE]`
- **Standard operativi:** GS1 — GTIN e GS1 Digital Link per identificazione e vettore dati (QR). Rif.: https://gs1it.org/migliorare-processi/supply-chain-sostenibile/passaporto-digitale-prodotto/ `[REALE]`
- **Metodologia ambientale:** PEF / LCA (ISO 14040/44, ISO 14067) per il carbon footprint. `[REALE]`
- **Accesso differenziato:** pubblico, autorità, operatori di fine vita — con permessi di lettura diversi sugli stessi dati. `[REALE]`

**Valore per Bianchi (frase di sintesi):** con un solo QR sul telaio, Bianchi copre due obblighi normativi
(Battery Passport 2027 + ESPR 2029-30) e trasforma un adempimento in trasparenza verso il cliente.
quindi.ai è il motore che genera i dati affidabili del passaporto: raccoglie dalla fabbrica materiali,
distinta base, consumi e impronta di carbonio, e li integra con l'ERP per alimentare il DPP in tempo reale.
