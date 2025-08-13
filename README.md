# 💡Avancerad blueprint för belysning med rörelsesensor

---

# Beskrivning

Rörelsestyrd belysning 💡
(Scen eller Direkta lampor) med schema, nattläge, solstyrning och failsafe

Styr valfri belysning med rörelsesensor(er), manuella brytare och flexibla scheman.
Perfekt för både inomhus- och utomhusbelysning — med stöd för soluppgång/solnedgång, lux-sensor och failsafe som släcker om något går fel.

# ✨ Funktioner

🕰 Schema – Styr dag- och nattläge via tider och/eller soluppgång/solnedgång

🌞 Solstyrning – Aktivera styrning efter solen (valfritt)

🌜 Nattläge – Eget ljusläge, scen eller ljusstyrka på natten

🔆 Lux-sensor (valfritt) – Tänd endast vid låg ljusnivå

🎛 Flera rörelsesensorer – Lägg till fler än en sensor

🔌 Manuella brytare – Tänd även via väggströmbrytare eller annan trigger

🎭 Scen eller direkta lampor – Styr en scen eller enskilda lampor med snapshot-återställning

⏱ Failsafe – Automatisk släckning efter säkerhetstimer, med loggmeddelande i HA

⚡ Parallellt läge – Snabb reaktion, upp till 100 samtidiga körningar

# 🛠 Exempel på användning

💡 Badrum – Tänd full belysning dagtid, mysbelysning nattetid

🚪 Hall/entré – Tänd när någon kommer in, även via manuell brytare

🌲 Gårdsplan – Styr strålkastare vid rörelse, endast när det är mörkt ute

🛋 Vardagsrum – Kombinera manuell tändning och rörelse, med scenåterställning

# 📥 Installation

Importera med [1-klick](https://my.home-assistant.io/redirect/blueprint_import?blueprint_url=https://raw.githubusercontent.com/razzietheman/Avancerad-blueprint-for-belysning/main/Tand_slack_blueprint.yaml).

Fyll i fälten

Rörelsesensor(er)

Lampor eller scen

Eventuell lux-sensor

Schema för dag/natt eller solstyrning

Failsafe-tid

# ⚙ Tips
Lux-sensor kan lämnas tom för utomhusbelysning utan luxkrav

Failsafe sparar dig från att lampor står tända om något hänger sig

Du kan använda både tid och solstyrning parallellt

### Support  
Har du frågor eller förslag? Öppna gärna ett ärende i [GitHub-repot](https://github.com/razzietheman/Avancerad-blueprint-for-belysning).