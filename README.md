# 💡 Rörelsestyrd Belysning 3.0

Dynamisk styrning med sol, arbetsdag och failsafe

Automatiserar belysning baserat på rörelse, solens position, scheman och arbetsdagar – med extra säkerhetsfunktioner för att undvika att lampor blir kvarslagna.

# ✨ Funktioner

🚶 Flera rörelsesensorer – Lägg till en eller flera sensorer som triggar belysningen.

🌅 Dynamiskt dags-/nattläge – Skiftar automatiskt beroende på solens upp-/nedgång.

📅 Valfritt arbetsdagsvillkor – Styr separat för arbetsdagar eller helger (kan stängas av helt).

🕒 Schema & tidsstyrning – Olika ljusstyrkor eller scener beroende på tid på dygnet.

🛡 Failsafe – Släcker ljuset om systemet missar en avstängning, så inget står tänt i onödan.

🖼 Scen eller direktstyrning – Välj att tända en scen eller direkt styra lampor/grupper.

# 🛠 Installation

Ladda ner Tand_slack_blueprint.yaml.

Placera filen i din Home Assistant-mapp:

config/blueprints/automation/

Eller importera med [1-klick](https://my.home-assistant.io/redirect/blueprint_import?blueprint_url=https://raw.githubusercontent.com/razzietheman/Avancerad-blueprint-for-belysning/main/Tand_slack_blueprint.yaml).

Gå till Inställningar → Automatiseringar och Scener → Blueprints.

Importera och skapa en ny automation baserad på denna blueprint.

# ⚙️ Parametrar

| Parameter           | Beskrivning                                                                 | Obligatorisk |
|--------------------|----------------------------------------------------------------------------|--------------|
| Rörelsesensorer     | En eller flera `binary_sensor` för rörelse                                  | ✅           |
| Lampor/Scen         | Entiteter som ska styras (lampor eller scen)                                | ✅           |
| Arbetsdags-sensor    | `binary_sensor.workday_sensor` eller liknande (kan lämnas tom för att alltid vara aktiv) | ❌           |
| Tider för dag/natt   | Separata start- och sluttider för dag- och nattläge                         | ❌           |
| Failsafe-tid         | Maximal tid lampan kan vara på utan rörelse                                 | ✅           |


# 📖 Exempel
1. Enkel nattbelysning

Rörelsesensor i hallen

Tänder en scen med svagt ljus mellan 22:00 och 06:00

Ingen arbetsdagskontroll

2. Dynamiskt kontorsljus

Flera sensorer i kontorslokalen

Arbetsdags-sensor aktiverad

Full ljusstyrka dagtid, dämpad kvällstid

Failsafe ställer av lamporna efter 15 min inaktivitet

# 🆕 Release Notes – Version 3.0

✨ Ny valfri arbetsdagskontroll – Kan nu lämnas tom om du alltid vill att automatiseringen ska köras.

🔄 Förbättrad soluppgång/-nedgångshantering.

⚡ Optimerad kod för snabbare respons.

🛡 Stabilare failsafe-logik.

🎯 Smidigare konfigurering direkt i UI.

# 📜 Licens

Fri att använda och modifiera. En länk tillbaka till originalprojektet uppskattas.

# ⚙ Tips

Lux-sensor kan lämnas tom för utomhusbelysning utan luxkrav

Failsafe sparar dig från att lampor står tända om något hänger sig

Du kan använda både tid och solstyrning parallellt

### Support  
Har du frågor eller förslag? Öppna gärna ett ärende i [GitHub-repot](https://github.com/razzietheman/Avancerad-blueprint-for-belysning).