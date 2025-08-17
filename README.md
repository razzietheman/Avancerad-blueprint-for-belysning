# 🌟 Rörelsestyrd belysning 3.4 – Din smarta ljusmästare med dubbla släcktider 🌟

#✨ Beskrivning

Föreställ dig att ditt hem vaknar, följer solen och somnar helt på egen hand – men nu med ännu större flexibilitet.
Rörelsestyrd belysning 3.4 bygger vidare på version 3.2 och introducerar två separata fasta släcktider, vilket ger dig full kontroll över kvällsbelysningen.

Perfekt om du vill ha:

Tidig nattbelysning på vardagar

Senare kvällsbelysning på helger

Eller helt olika tider i olika rum

Den innehåller nu:

- 🚶 Rörelsesensorer (valfritt)  
- 🔘 Manuella brytare (valfritt)  
- 🌅 Solens gång (med offset)  
- 💡 Lux-baserad styrning (valfritt)  
- 🎨 Dag- och natt-scener (valfritt)  
- ⏰ Två fasta släcktider (valfritt)  
- 📅 Arbetsdagskontroll (valfritt)  
- 🛡️ Failsafe & timeout  
- ⏳ Tändtid vid inaktivitet  
- 📝 Input Text-loggning  

Alla funktioner är fortfarande valfria – använd bara det som passar din installation.

# 🎨 Exempel på scenarion

🌅 Morgonljus – Mjuk start på dagen

Aktiveras t.ex. 07:00 på vardagar.

Rörelsesensorer känner av att du är uppe och tänder lamporna mjukt.

Lux-sensorn ser till att inget tänds i onödan om solen redan lyser in.

Din dag-scen startar och loggas automatiskt.

# 🌞 Dagljus med sol-trigger

Lampor tänds X minuter/timmar innan solnedgång (offset).

Perfekt för mörka vinterkvällar eller sena sommarkvällar.

Kan kombineras med fasta släcktider 1 och 2 för maximal flexibilitet.

# 🌙 Kvällsmys

Aktiveras via rörelse eller manuell brytare.

Lampor tänds i diskret nattläge, med möjlighet till scenstyrning.

Släcks gradvis efter inställd tändtid om ingen rörelse detekteras.

# ⏰ Arbetsdag vs Helg

Anpassa tändning och släckning efter veckodag.

På helger kan tändningen ske senare – eller inte alls.

# 🛡️ Failsafe

Säkerställer att lampor inte lyser för evigt.

Släcker automatiskt efter angiven timeout, även om något glömts bort.

# 🔧 Funktioner i detalj

| Funktion                  | Beskrivning |
|---------------------------|-------------|
| 🚶‍♂️ Rörelsesensor (valfri) | Tänd/släck med rörelse – eller lämna tomt för schemastyrning |
| 🔘 Manuell switch (valfri)  | Tänd ljus manuellt när du vill |
| 🌞 Dag- och natt-scener     | Skapa stämning med scener eller individuella lampor |
| 💡 Lux-sensor               | Tänder bara när det är tillräckligt mörkt |
| 🌅 Soluppgång/solnedgång    | Offset för exakt timing |
| ⏱ Två fasta släcktider      | Bestäm exakt klockslag för släckning – t.ex. vardag och helg |
| 📅 Arbetsdagskontroll        | Anpassar belysning beroende på vardag eller helg |
| 🛡️ Failsafe                 | Släcker alltid efter inställd timeout |
| ⏳ Tändtid                   | Hur länge lampor ska vara tända efter inaktivitet |
| 📝 Input Text-logg           | Sparar senaste scen eller trigger för logik och felsökning |


#💡 Tips: Kombinera sol-trigger med två fasta släcktider för perfekt kvällsbelysning – t.ex. tidigare släckning på vardagar och senare på helger.

# 📥 Installation

Importera med 1-klick:
   [Importera blueprint](https://my.home-assistant.io/redirect/blueprint_import?blueprint_url=https://raw.githubusercontent.com/razzietheman/Avancerad-blueprint-for-belysning/main/Tand_slack_blueprint.yaml)

2. **Fyll i fälten:**
   - Rörelsesensor(er) (valfritt)  
   - Lampor eller scen(er) för dag och natt  
   - Eventuell lux-sensor (valfritt)  
   - Schema för dag/natt eller solstyrning (valfritt)  
   - Fast släcktid (valfritt)  
   - Failsafe-tid (valfritt)  

---

## 🤝 Support  
Har du frågor eller förbättringsförslag?  
Öppna ett ärende i [GitHub-repot](https://github.com/razzietheman/Avancerad-blueprint-for-belysning).

---

Med **Rörelsestyrd belysning 3.2** blir ditt hem smartare, mysigare och mer energisnålt – utan att du behöver lyfta ett finger. ✨