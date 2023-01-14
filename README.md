# HomeAssistant
Mes différents blueprint et automatisations

# Install manuel blueprint
Avec FileEditor crée un fichier yaml dans le dossier : /config/blueprints/automation/homeassitant

# Heures creuses
### Résultat attendu
* A 13h54 activer mon boolean heures creuses et envoyez une notif
* A 15h54 desactiver mon boolean
* A 00h53 activer mon boolean
* A 06h53 desactiver mon boolean

### Ajouter dans configuration.yaml
```yaml
input_boolean:
  heures_creuses:
    name: Heures creuses
    icon: mdi:clock    
```

### Nom des fichiers
######  blueprint_heures_creuses.yaml
######  automatisation_heures_creuses.yaml

	
    
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

### Nom des fichiers
######  blueprint_3detector_1light.yaml
######  automatisation_3detector_1light.yaml

# 3 detecteurs 1 lumière 1 prise
### Résultat attendu
* Si un des détécteurs détecte j'allume la lumière et la prise
* Si plus aucun détecteurs ne détecte j'éteint la lumière et la prise

### Nom des fichiers
######  blueprint_3detector_1light_1switch.yaml
######  automatisation_3detector_1light_1switch.yaml

# Poubelles
### Résultat attendu
Permet de savoir quand sortir et rentrer les poubelles
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

# Aquarium
### Résultat attendu
Gestion on/off et gestion nourriture et nettoyage

### Todo
* Carte pour la gestion
* Blueprint

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
Attention plusieurs automatisations dans le fichier
######  automatisation_aquarium.yaml
######  script_aquarium.yaml

