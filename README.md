# OPRA Datascience – RNA‑seq analyse
Dit repository bevat de eindopdracht voor de RNA‑seq analyse binnen OPRA Periode C.

De volledige analyse staat in:
* rnaseq_opdracht.Rmd

Grote databestanden (FASTQ, BAM, indexbestanden, QC‑output en tussenresultaten) worden niet meegeversioneerd en zijn uitgesloten via .gitignore.

De analyse laadt deze bestanden automatisch vanaf de HU‑server; handmatig kopiëren is niet nodig.

## Inhoud van de repository
- rnaseq_opdracht.Rmd – hoofdrapport met analyses en interpretaties
- README.md – documentatie van het project
- .gitignore – uitsluiting van grote databestanden en tijdelijke output

## Repository clonen (RStudio Server / Terminal)
Optie 1 – via RStudio
New Project → Version Control → Git → vul de HTTPS‑URL van de repository in.

Optie 2 – via de terminal
git clone https://github.com/meeshillebrink/OPRA_Datascience.git

Git vraagt vervolgens om:
Username: je GitHub‑gebruikersnaam
Password: je Personal Access Token (classic)

Let op: fine‑grained tokens werken niet voor repositories waar je collaborator bent.
Gebruik daarom een classic token met minimaal de scope "repo".

GitHub‑authenticatie (token en credentials)
Personal Access Token (classic) aanmaken
GitHub → Settings → Developer settings →
Personal access tokens → Tokens (classic) → Generate new token
Selecteer minimaal: repo

## Credentials instellen (optioneel)
git config --global user.name  "jouw_gebruikersnaam"
git config --global user.email "jouw_email"
git config --global credential.helper store

Met credential.helper store hoef je je token niet bij elke push opnieuw in te voeren.

## Werken met Git
### Pushen:
git add .
git commit -m "Beschrijving van je wijziging"
git push

### Pullen:
git pull

## Rapport openen
- Clone of download deze repository.
- Open rnaseq_opdracht.Rmd in RStudio.
- Klik op Knit om het volledige rapport te genereren.

## Projectgroep
- Arjan Peters
- Chelaysiah Steba
- Kerem Şentürk
- Mees Hillebrink
- Shinda Mohammed
