# OPRA Datascience – RNA‑seq analyse (Periode C, 2025–2026)

Dit repository bevat de eindopdracht voor de RNA‑seq‑analyse binnen OPRA Periode C van het studiejaar 2025–2026.

## Inhoud van de repository

### 🔹 `rna_seq_analyse_2627.Rmd` — hoofdrapport  
Bevat de volledige RNA‑seq‑analyse, inclusief preprocessing, kwaliteitscontrole, normalisatie, clustering, PCA en differentiële expressie.

### 🔹 `geparametriseerd_2.Rmd` — geparametriseerde analyse  
Genereert automatisch een rapport voor elke combinatie van twee beschikbare weefsels.

Gebruik in RStudio:
1. Klik op **Knit with Parameters**  
2. Er verschijnt een parameterscherm met **radiobuttons**  
3. Selecteer twee weefsels  
4. Klik op **Knit**

Het gegenereerde document bevat uitsluitend figuren met onderschriften; alle inhoud past zich automatisch aan de gekozen weefsels aan.

### 🔹 `styles.css`  
CSS‑bestand dat gebruikt wordt voor de opmaak en lay‑out van het hoofdrapport (`rna_seq_analyse_2627.Rmd`).  
Het zorgt voor consistente styling van koppen, lettertypes, marges en figuurbijschriften.

### 🔹 `README.md`  
Documentatie van het project en uitleg over de structuur van de repository.

### 🔹 `.gitignore`  
Sluit grote databestanden (FASTQ, BAM, indexbestanden, QC‑output en tussenresultaten) en tijdelijke bestanden uit.  
Deze bestanden worden niet meegeversioneerd; de analyse laadt benodigde data automatisch vanaf de HU‑server.

---

## Repository clonen

### Via RStudio  
**New Project → Version Control → Git →** vul de HTTPS‑URL van deze repository in.

### Via de terminal  
```bash
git clone https://github.com/meeshillebrink/OPRA_Datascience.git
