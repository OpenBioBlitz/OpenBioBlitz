# OpenBioBlitz

## SOMMAIRE
# Quoi
# Concept
# Description fonctionnelle
### - Profil utilisateur
### - Formulaire
### - Récupération des données manquantes
### - Validation darwinCore
### - Publication
### - Configuration de la zone géographique
### - Architecture
### - API Web
### - Clients
### Applications existantes
# Contribuer
# Contexte 
# Licence du projet


## Quoi

OpenBioblitz est un projet pour une application online/offline pour acquérir de nouvelles données d'observations biologiques lors d'un événement naturaliste comme un [BioBlitz](https://en.wikipedia.org/wiki/BioBlitz).

## Concept

- Traduction automatique en [Darwin Core](http://rs.tdwg.org/dwc/) 
- Intégration des informations manquantes via des sites OpenSource (OpenTree of Life, Open Street Map, Catalogue of Life, etc.)
- Exportation vers une Base de Données
- Filtrage avec l'outil DarwinCore Validator du [GBIF](www.gbif.org)
- Exportation et publications des données vers le [GBIF](www.gbif.org)
- Configuration/Paramétrage des espèces déjà présentes sur les lieux via [GBIF](www.gbif.org) et/ou l'[INPN](https://inpn.mnhn.fr/accueil/index) pour une restriction et optimisation des ajouts d’informations présentes et manquantes
- 3 niveaux de récupération d'information: débutant / intermédiaire / confirmé

Deux interfaces opérationnelles en mode offline (utlisateurs et DarwinCore) échangent avec une API reliée à une Base de Données en ligne.
Avant d'être exportées vers le GBIF, les données sont filtrées par l'outil du [GBIF DarwinCore Validator](http://tools.gbif.org/dwca-validator).

## Description fonctionelle

![Schéma théorique de fonctionnement](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_jVIIVR11rac_p.564581_1488663708772_undefined)

<iframe style="width:1200px;height:800px;border:0px
solid black" src="https://framindmap.org/c/maps/320935/embed?zoom=1"> </iframe>

### Profil utilisateur

L'utilisateur choisi son profil : débutant, intermédiare ou confirmé.
Les 3 niveaux doivent être très simples pour ne pas perdre l'utilisateur.

### Formulaire

L'utilisateur rempli un formulaire qui répond au questions Qui / Quoi / Où / Quand / Comment.

![Exemple d'interface du formaulaire](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_jVIIVR11rac_p.564581_1488717935354_undefined)

Les champs du formulaire sont décris dans cette [mind map](https://framindmap.org/c/maps/320935/edit).

**TODO** : Vulgariser le [DarwinCore](http://www.canadensys.net/publication/darwin-core?lang=fr) selon le type de profil, voir [exemple mind map débutant](https://framindmap.org/c/maps/321124/edit)

### Récupération des données manquantes

Connexion avec les API existantes :
 - Geographique : OpenStreetMap / GBIF
 - Taxonomique : Catalogue of Life
 - Phylogénétique : Open Tree of Life
 - Images : Encyclopedia Of Life / WikiSpecies

### Validation DarwinCore

Validation avec [DarwinCore Validator](https://tools.gbif.org/dwca-validator/).

### Publication

[GBIF.org > publisher](https://www.gbif.org/become-a-publisher)

### Configuration de la zone géographique

[GBIF.org > occurrence > location](https://www.gbif.org/occurrence/search) (aller voir sur _location_)

### Architecture

Les choix technologiques ne sont pas arrêtés, chaque proposition est bienvenue.

### API Web

 - [API OpenBioBliz](https://github.com/gaetan-pc/openbioblitz-core)
 - [Documentation](https://github.com/gaetan-pc/openbioblitz-core-documentation)

Choix technologiques :
 - Langage : Ruby
 - Base de données : PostgreSQL avec extensions (PostGIS, OpenFTS) et éventuellement autres outils (Elasticsearch / Alglia / HStore / Redis ?) à définir.

Todo :
 - Décrire les points d'entrées / routes.

### Clients

 - [Client mobile](https://github.com/gaetan-pc/openbioblitz-mobile)
 - [Client général](https://github.com/gaetan-pc/openbioblitz-web)

Choix technologiques :
 - React + Redux

Todo :

 - A t-on réellement besoin de plusieurs clients ?

### Applications existantes

[Source : tiré de "Carnet de terrain électronique" et modifié](http://carnet-terrain-electronique.fr/applications/)

<iframe style="width:1200px;height:800px;border:0px" src="https://docs.google.com/spreadsheets/d/1tC9VsJVBiUESoh7YoTw2YBSfmn7ER17RecpbAtuqAFE/edit?usp=sharing/"></iframe>

TODO: finir de remplir le tableau.


## Contexte

[OpenBioBlitz](https://hackmd.io/CYBgpgxsAcIMwFoCMBOALMBaBmZoJWgEMIEA2EAJjgHZhski1okg?both#) est un projet initié et développé lors d'un [hackathon organisé en 32 jours](http://movilab.org/index.php?title=Recette_frugale_d%27hackathon_citoyen_open_source:_en_32_jours_et_sans_budget) les 4-5 mars 2017 à Rennes (Bretagne, France) dans le cadre de l'événement national [la Nuit du Code Citoyen](https://codecitoyen.github.io/) .

[Présentation sur les données de biodiversité en modèle ouvert](https://docs.google.com/presentation/d/1YnATN3D6lx_RndzpiwFlbN3Ja5NmFflFvmdJJ7Mi92g/edit?usp=sharing/) par Olivier Norvez sous licence [CC-BY](https://creativecommons.org/licenses/by/3.0/fr/)

## Contribuer

 - [Slack](openbioblitz.slack.com)
 - [Carnet de bord](https://hackmd.io/CYBgpgxsAcIMwFoCMBOALMBaBmZoJWgEMIEA2EAJjgHZhski1okg?both#)
 
 Todo:
 - contacter des institutions (associations naturalistes, Muséums (UMS PatriNat), ou autres projets d'applications naturalistes
 

## Licence du projet

OpenBioBlitz est un projet sous licence [CC-BY](https://creativecommons.org/licenses/by/3.0/fr/)
