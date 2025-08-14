# 💡 Rörelsestyrd belysning 3.0 – Dynamisk med sol, arbetsdag och failsafe

En komplett **Home Assistant blueprint** som styr belysning med rörelsesensorer, tid, lux-nivå, arbetsdagskontroll och solens position.  
Inkluderar **failsafe-timer**, **scenstöd**, **gradvis släckning** och **snapshot-funktion**.

---

## 🚀 Funktioner

- 🚶‍♂️ Rörelsestyrning med stöd för flera sensorer
- 🌅 Dag/Natt-läge via tid eller soluppgång/solnedgång
- 💡 Lux-tröskel för att undvika tändning vid dagsljus
- 🗓 Separata aktiva veckodagar för dag och natt
- 🏢 Arbetsdagskontroll med binary sensor
- 🎭 Stöd för scener eller direkta lampor
- 📸 Snapshot av tidigare ljusinställningar
- 🕒 Olika tändtider för dag och natt
- ⏱ Failsafe-timer för automatisk släckning
- 🌄 Dynamisk sol-trigger med offset
- 🌙 Gradvis släckning med transition

---

## ⚙️ Inputinställningar

| Kategori | Input | Beskrivning | Typ |
|----------|-------|-------------|-----|
| **Sensorer & brytare** | 🚶‍♂️ Rörelsesensor(er) | En eller flera rörelsesensorer | `binary_sensor` |
|  | 🔘 Valfri manuell strömbrytare | Extra brytare som triggar ljus | `switch` |
| **Lampor & scener** | 💡 Lampor | Lampor som styrs om ingen scen används | `light` |
|  | 🎭 Scen dagläge | Scen att aktivera dagtid | `scene` |
|  | 🌙 Scen nattläge | Scen att aktivera nattetid | `scene` |
|  | ☀️ Daglampor | Lampor för dag om ingen scen används | `light` |
|  | 🌙 Nattlampor | Lampor för natt om ingen scen används | `light` |
| **Lux & sol** | 📊 Lux-sensor | Lämna tom om lux ej används | `sensor` |
|  | 📉 Lux-tröskel | Max lux för att tända ljus | `number` |
|  | 🌄 Använd soluppgång/solnedgång | Dag/Natt via solens position | `boolean` |
|  | ⏳ Solnedgång offset | Justering av soltid | `text` |
|  | 📝 Input Text för sol-trigger | Loggar senaste solhändelse | `input_text` |
| **Tidsinställningar** | 🕒 Dagstart/Dagsslut | Tider för dagläge | `time` |
|  | 🌙 Nattstart/Nattsslut | Tider för nattläge | `time` |
|  | 🗓 Aktiva veckodagar (Dag/Natt) | Separata dagar för lägena | `select` |
| **Arbetsdag & failsafe** | 🏢 Arbetsdag-sensor | Binary sensor för arbetsdag | `binary_sensor` |
|  | ⏱ Failsafe-timer dag/natt | Timeout innan släckning | `number` |
|  | 📝 Input Text – Senaste scen | Sparar senaste läge | `input_text` |
| **Tändtider** | ☀️ Tändtid dag | Tid efter rörelse slocknar (dag) | `number` |
|  | 🌙 Tändtid natt | Tid efter rörelse slocknar (natt) | `number` |

---

## 🔄 Funktionsflöde

1. **Rörelse upptäcks**  
   → Kollar lux, tid/sol, arbetsdag → Tänder dag- eller nattbelysning.
2. **Ingen rörelse**  
   → Väntar definierad tändtid → Släcker med mjuk transition.
3. **Failsafe**  
   → Om ljus är på för länge → Släcker automatiskt.
4. **Soluppgång/Solnedgång**  
   → Växlar automatiskt mellan dag- och nattläge.

---

## 📝 Tips & tricks

- Använd **scener** om du vill ha avancerad belysningskontroll (färg, dimning m.m.).
- Lux-tröskel kräver att du anger en lux-sensor.
- Vill du köra utan arbetsdagskontroll → sätt en sensor som alltid är `on`.

---

## 📌 Krav

- Home Assistant 2025.4 eller senare
- Minst en `binary_sensor` för rörelse
- Lampor eller scener att styra

---

## 📚 Versionshistorik

### **3.0**
- Omarbetad struktur för tydlighet och robusthet
- Failsafe för dag och natt separat
- Stöd för scener och lampor parallellt
- Förbättrad loggning
- Dynamisk sol-trigger med offset

---

## 🛠 Installation

1. Spara filen som `Tand_slack_blueprint.yaml` i `config/blueprints/automation/`.
2. I Home Assistant: **Inställningar → Automatiseringar & Scener → Blueprints**.
3. Klicka på **Importera Blueprint** och välj filen.
4. Skapa en ny automation från blueprinten och fyll i enheter och tider.


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