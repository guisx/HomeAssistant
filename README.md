# HomeAssistant
Mes différents blueprint et automatisations

# Install manuel blueprint
Avec FileEditor crée un fichier yaml dans le dossier : /config/blueprints/automation/homeassitant

# Heures creuses
## Résultat attendu
* A 13h54 activer mon boolean heures creuses et envoyez une notif
* A 15h54 desactiver mon boolean
* A 00h53 activer mon boolean
* A 06h53 desactiver mon boolean

######  blueprint_heures_creuses.yaml
######  automatisation_heures_creuses.yaml

## Ajouter dans configuration.yaml
`  
heures_creuses:
name: Heures creuses
icon: mdi:clock  
	`
    
# Telecommande 4 Bouttons
######  blueprint_telecommande_4btn.yaml

# Telecommande 6 Bouttons
######  blueprint_telecommande_6btn.yaml

# 3 detecteurs 1 lumière
## Résultat attendu
* Si un des détécteurs détecte j'allume la lumière
* Si plus aucun détecteurs ne détecte j'éteint la lumière

######  blueprint_3detector_1light.yaml
######  automatisation_3detector_1light.yaml

# 3 detecteurs 1 lumière 1 prise
## Résultat attendu
* Si un des détécteurs détecte j'allume la lumière et la prise
* Si plus aucun détecteurs ne détecte j'éteint la lumière et la prise

######  blueprint_3detector_1light_1switch.yaml
######  automatisation_3detector_1light_1switch.yaml

# Poubelles
## Résultat attendu
Permet de savoir quand sortir et rentrer les poubelles
Poubelle noire 2 fois par semaine
Poubelle verte 1 fois par semaine

## Todo
Carte pour la gestion

Attention plusieurs automatisations dans le fichier
######  automatisation_poubelles.yaml
######  script_poubelles.yaml

# Aquarium
## Résultat attendu
Gestion on/off et gestion nourriture et nettoyage

## Todo
Carte pour la gestion

Attention plusieurs automatisations dans le fichier
######  automatisation_aquarium.yaml
######  script_aquarium.yaml

