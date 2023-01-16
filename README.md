# HomeAssistant
Mes différents blueprint et automatisations

# Installation manuelle d'un blueprint
Avec FileEditor crée un fichier yaml dans le dossier : /config/blueprints/automation/homeassitant

# Heures creuses
### Résultat attendu
* Heures creuses française 13h54/15h54 // 00h53/06h53
* A 13h54 active le boolean "heures_creuses" et envoie une notification sur les téléphones du réseau
* A 15h54 desactive le boolean "heures_creuses"
* A 00h53 activer le boolean "heures_creuses"
* A 06h53 desactiver le boolean "heures_creuses"

### Gestion boolean vacances
Remplacer condition: [] par
```yaml
condition:
  - condition: state
    entity_id: input_boolean.vacances
    state: "off"  
```

### Ajouter dans configuration.yaml
```yaml
input_boolean:
  heures_creuses:
    name: Heures creuses
    icon: mdi:clock    
```

### Nom des fichiers
######  heures_creuses_blueprint.yaml
######  heures_creuses_automatisation.yaml (ancienne utilisation avant blueprint / Attention 2 automatisation)

# Aquarium
### Résultat attendu
* Blueprint - Gestion on/off par une prise de la lumière 
* Script/Card - Gestion nourriture et nettoyage

### Ajouter dans configuration.yaml
```yaml
input_datetime: 
  aquarium_nourriture:
    name: Aquarium nourriture
    icon: mdi:food-fork-drink
    has_date: true
    has_time: false
  aquarium_nettoyage:
    name: Aquarium nettoyage
    icon: mdi:spray-bottle
    has_date: true
    has_time: false 
```

### Nom des fichiers
######  aquarium_blueprint.yaml
######  aquarium_script.yaml
######  aquarium_card.yaml (plugin banner-card)
######  aquarium_automatisation.yaml (ancienne utilisation avant blueprint)
	
    
# Telecommande 4 Bouttons
### Nom des fichiers
######  blueprint_telecommande_4btn.yaml

# Telecommande 6 Bouttons
### Nom des fichiers
######  blueprint_telecommande_6btn.yaml

# 3 detecteurs 1 lumière
### Résultat attendu
* Si un des détécteurs détecte j'allume la lumière
* Si plus aucun détecteurs ne détecte j'éteint la lumière

### Todo
Simplifié les conditions off

### Nom des fichiers
######  blueprint_3detector_1light.yaml
######  automatisation_3detector_1light.yaml

# 3 detecteurs 1 lumière 1 prise
### Résultat attendu
* Si un des détécteurs détecte j'allume la lumière et la prise
* Si plus aucun détecteurs ne détecte j'éteint la lumière et la prise

### Todo
Simplifié les conditions off

### Nom des fichiers
######  blueprint_3detector_1light_1switch.yaml
######  automatisation_3detector_1light_1switch.yaml

# Poubelles
### Résultat attendu
Permet de savoir quand sortir et rentrer les poubelles avec notif sur téléphone
Poubelle noire 2 fois par semaine
Poubelle verte 1 fois par semaine

### Ajouter dans configuration.yaml
```yaml
counter:
  poubelle_noir:
    initial: 0
    step: 1    
  poubelle_verte:
    initial: 0
    step: 1      
```

### Nom des fichiers
Attention plusieurs automatisations dans le fichier
######  automatisation_poubelles.yaml
######  script_poubelles.yaml
###### card_poubelles.yaml
