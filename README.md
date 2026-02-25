# OPRA_Datascience RNA-seq analyse

Dit repository bevat de eindopdracht voor de RNA‑seq analyse binnen OPRA Periode C.
De volledige analyse staat in het bestand:

- rnaseq_opdracht.Rmd

Grote databestanden (FASTQ, BAM, indexbestanden, QC-output en tussenresultaten) zijn uitgesloten via .gitignore omdat deze te groot zijn en niet nodig zijn voor beoordeling.

INHOUD VAN DE REPOSITORY
rnaseq_opdracht.Rmd   – hoofdrapport met analyses en interpretaties
.gitignore            – uitgesloten bestanden en mappen
README.md             – documentatie van het project

REPO CLONEN (RSTUDIO SERVER / TERMINAL)
Optie 1 – Via RStudio:
New Project → Version Control → Git → vul de HTTPS-URL in.

Optie 2 – Via de terminal:
git clone https://github.com/meeshillebrink/OPRA_Datascience.git

Git vraagt dan om:
- Username: jouw GitHub-gebruikersnaam
- Password: jouw Personal Access Token (classic)

Let op:
Fine-grained tokens werken NIET voor repositories waar je collaborator bent.
Gebruik daarom een classic token met ‘repo’-rechten.

GITHUB AUTHENTICATIE (TOKEN + CREDENTIALS)

1. Classic token aanmaken:
GitHub → Settings → Developer settings →
Personal access tokens → Tokens (classic) → Generate new token (classic)

Vink aan:
- repo

2. Credentials instellen (optioneel maar handig):
git config --global user.name "jouw_gebruikersnaam"
git config --global user.email "jouw_email"
git config --global credential.helper store

Zonder credential.helper store moet je bij elke push opnieuw je token invoeren.

PUSHEN EN PULLEN

Pushen:
git add .
git commit -m "Beschrijving van je wijziging"
git push

Pullen:
git pull


DATA KOPIËREN VAN DE SERVER (FASTQ / INDEX / BAM)

De grote databestanden staan op de gedeelde HU-server en worden niet meegeversioneerd.
Je kunt ze zelf kopiëren naar je projectmap.

Paden naar de data:
- Indexbestanden (hg38): /home/data/opra4v/hg38_index/
- FASTQ-bestanden:       /home/data/opra4v/fastq/


BESTANDEN KOPIËREN VIA R (file.copy)

Voorbeeld: FASTQ-bestanden kopiëren naar je eigen projectmap:

dir.create("fastq", showWarnings = FALSE)
file.copy(
  from = list.files("/home/data/opra4v/fastq/", full.names = TRUE),
  to   = "fastq",
  recursive = TRUE
)

Voorbeeld: indexbestanden kopiëren:

dir.create("hg38_index", showWarnings = FALSE)
file.copy(
  from = list.files("/home/data/opra4v/hg38_index/", full.names = TRUE),
  to   = "hg38_index",
  recursive = TRUE
)


BESTANDEN KOPIËREN VIA DE TERMINAL

FASTQ-bestanden:
cp /home/data/opra4v/fastq/* ./fastq/

Indexbestanden:
cp /home/data/opra4v/hg38_index/* ./hg38_index/

Let op:
Gebruik eerst mkdir fastq of mkdir hg38_index als de map nog niet bestaat.


RAPPORT OPENEN

1. Clone of download deze repository.
2. Open rnaseq_opdracht.Rmd in RStudio.
3. Klik ‘Knit’ om het volledige rapport te genereren.

PROJECTGROEP

Arjan Peters
Chelaysiah Steba
Kerem Şentürk
Mees Hillebrink
Shinda Mohammed
