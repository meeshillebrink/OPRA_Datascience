# OPRA Datascience – RNA‑seq analyse (Periode C, 2025–2026)

Dit repository bevat de eindopdracht voor de RNA‑seq‑analyse binnen OPRA Periode C van het studiejaar 2025–2026.

## Inhoud van de repository

### 🔹 `rna_seq_analyse_2627.Rmd` — hoofdrapport  
Bevat de volledige RNA‑seq‑analyse, inclusief preprocessing, kwaliteitscontrole, normalisatie, clustering, PCA en differentiële expressie.

### 🔹 `geparametriseerd_2.Rmd` — geparametriseerde analyse  
Genereert automatisch een rapport voor elke combinatie van twee beschikbare weefsels.

Gebruik in RStudio:
1. Klik op Knit with Parameters  
2. Er verschijnt een parameterscherm met radiobuttons 
3. Selecteer twee weefsels  
4. Klik op Knit

Het gegenereerde document bevat uitsluitend figuren met onderschriften; alle inhoud past zich automatisch aan de gekozen weefsels aan.

### 🔹 `.gitignore`  
Bevat uitsluitingsregels voor grote databestanden (FASTQ, BAM, indexbestanden, QC‑output, tussenresultaten) en tijdelijke bestanden.  
Deze bestanden worden niet meegeversioneerd; de analyse laadt benodigde data automatisch vanaf de HU‑server.

### 🔹 `OPRA_Datascience.Rproj`  
RStudio‑projectbestand voor het openen van de volledige projectomgeving.

### 🔹 `README.md`  
Documentatie van het project en uitleg over de structuur van de repository.

---

## Repository clonen

### Via RStudio  
**New Project → Version Control → Git →** vul de HTTPS‑URL van deze repository in.

### Via de terminal  
```bash
git clone https://github.com/meeshillebrink/OPRA_Datascience.git
