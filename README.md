# Badrum – Tänd & Släck Automation med Veckoschema, Nattläge och Failsafe

[![Home Assistant](https://img.shields.io/badge/Home_Assistant-20232A?style=for-the-badge&logo=home-assistant&logoColor=white)](https://www.home-assistant.io/)  
[![YAML](https://img.shields.io/badge/YAML-000000?style=for-the-badge&logo=yaml&logoColor=white)](https://yaml.org/)

Automatisk styrning av badrumsbelysning med rörelsesensor, lux-sensor och veckoschema. Inkluderar nattläge och en failsafe-funktion som släcker lampan efter 15 minuter för att undvika att den står på för länge.

---

## Funktioner

- Tänder lampan baserat på rörelse och ljusnivå (lux).  
- Olika tider för tändning/släckning beroende på veckodag och tid på dygnet.  
- Nattläge med egen scen och kortare släckningstid.  
- Failsafe som automatiskt släcker lampan efter 15 minuter för säkerhets skull.  
- Sparar senaste aktiverade scen i en input_text för korrekt släckningsbeteende.

---

## Installation

1. Ladda ner filen `badrum_tand_slack_blueprint.yaml`.  
2. Importera blueprinten i Home Assistant via:  
   **Inställningar > Automations & Scener > Blueprints > Importera blueprint från fil**.  
3. Skapa `input_text` i din `configuration.yaml` eller via UI:  

```yaml
input_text:
  last_scene_triggered:
    name: Senaste scen
    max: 20
