# Documentation du hackaton OSCE days 2017 pour OpenBioBlitz

1. Repo [OpenBioBlitz](https://github.com/onorvez/OpenBioBlitz/blob/master/README.md)
2. le programme [OSCE days](https://openagenda.com/biomehacklab/events/osce-days-rennes-viens-pratiquer-apprendre-et-echanger?lang=fr) avec OpenBiobLitz sur les bactéries du sol 
3. RoadMap de contribution OpenBioBlilts pour OSCE Days 2017

# Qui et Quoi y Faire

Décrire les différents rôles de chaques intervenants dans le processus d'un BioBlitz. 
Exemple :
[Schémas fonctionnel des acteurs d'un BioBlitz](https://github.com/onorvez/OpenBioBlitz/blob/master/Capture%20d%E2%80%99e%CC%81cran%202017-05-26%20a%CC%80%2023.13.13.png)

Utilisateur Admin System:
- Gérer le serveur admin
- Installer facilement
- Mettre à jour
- Compiler les données pour en faire fichier darwin core

Utilisateur final:
- Identifier l’espèce présente devant soi
- Remplir le formulaire sur l’application en fonction des trois niveaux d’expertise (débutant, intermédiaire, confirmé)
- Application portable (offline) : concevoir un formulaire offline nécessaire pour configurer les interfaces utilisateurs. => nécéssite aussi une réplication de la base de données, sous forme d'un format approprié (json) qui sera utilisé par l'API ultérieurement lors du chargement dans la base de données. Téléversement des données lorsqu'il y aura connection au réseau (et ou à la fin du BioBlitz).

Serveur Admin:
- Doit être léger
- Le formulaire doit comprendre différents niveaux utilisateurs (débutant, intermédiaire, confirmé) Se souvenir que l'information peut-être complétée automatiquement ultérieurement (taxonomie, géographie...) Différentes sortes de catégories (box, textbox, cocombobox, listbox, list, button...) Différents types d'insertions de données (images, geo-ref, text, etc.) Créer une liste de champs prédéfinie via la configuration géographique et taxonomique


