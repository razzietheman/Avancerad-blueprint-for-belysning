# 💡 Rörelsestyrd Belysning (Scen eller Direkta Lampor) med Schema, Nattläge, Solstyrning & Failsafe

Styr dina lampor med en eller flera rörelsesensorer, manuella brytare, dag/natt-scheman, lux-tröskel, solstyrning, och failsafe-timer. Snapshots av tidigare ljusstyrka ingår.

# ⚙️ Funktioner

✅ Flera rörelsesensorer

✅ Valfria manuella brytare för att trigga lampor

✅ Dag- och nattlägen (tidbaserat eller solbaserat)

✅ Lux-tröskel (valfritt)

✅ Scen eller direkta lampor

✅ Snapshot-återställning av tidigare ljusstyrka

✅ Failsafe-timer (släcker lampor automatiskt efter timeout)

# 🛠️ Inputs
Input	Beskrivning	Standardvärde
motion_sensors	Rörelsesensor(er)	Ingen
optional_switches	Valfria brytare som också triggar lampor	[]
light_entity	Lampor att styra (om ingen scen används)	Ingen
scene_day	Scen som aktiveras på dagtid (valfritt)	[]
scene_night	Scen som aktiveras på natten (valfritt)	[]
day_lights	Lampor på dagtid om ingen scen används	[]
night_lights	Lampor på natten om ingen scen används	[]
lux_sensor	Valfri lux-sensor	[]
lux_threshold	Tänd bara lampor om lux är under denna nivå	50 lx
use_sun_times	Använd soluppgång/solnedgång istället för fasta tider	false
day_start / day_end	Start- och sluttid för dagläge	07:00 / 22:00
night_start / night_end	Start- och sluttid för nattläge	22:00 / 07:00
active_weekdays_day	Aktiva dagar för dagläge	Alla
active_weekdays_night	Aktiva dagar för nattläge	Alla
failsafe_timer	Minuter innan automatisk avstängning	30
input_text_last_scene	Håller reda på senaste aktiverade scen/läge	Ingen

# 🏃‍♂️ Hur det fungerar

# Dagläge 🌞
Rörelse upptäcks under dagtid eller solbaserat läge

Lux under tröskel (valfritt)

Aktiverar dag-scen eller daglampor

Snapshots av nuvarande ljusstyrka

Uppdaterar input_text_last_scene till "dag"

# Nattläge 🌙

Rörelse upptäcks under nattid eller solbaserat läge

Lux under tröskel (valfritt)

Aktiverar natt-scen eller nattlampor

Snapshots av nuvarande ljusstyrka

Uppdaterar input_text_last_scene till "natt"

# Släckning 💡

När rörelse upphör och lampor är tända

Återställer tidigare snapshot efter fördröjning:

Dagläge: 2 minuter

Nattläge: 1 minut

# Failsafe ⏱

Säkerställer att lampor inte står tända för länge

Aktiveras efter failsafe_timer om lampor fortfarande är tända

Släcker lampor och loggar händelsen

# 📌 Tips & Notes

Fungerar med flera rörelsesensorer

Manuella brytare kan trigga lampor

Kan använda scen eller direkta lampor

Kan användas med eller utan lux-sensor

Solbaserad tid fungerar om use_sun_times är aktiverat

# 📥 Exempel på användning

Hallen – Tänd ljus nattetid endast när det är mörkt 🌙

Vardagsrum – Reagerar på rörelse dag och natt 🌞🌙

Kök – Släcker automatiskt om någon glömmer lampan ⏱

Snapshots återställer ljusmiljön perfekt 🎨

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