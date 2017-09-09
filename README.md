# OpenBioBlitz

## Quoi

OpenBioblitz est une application online/offline pour acquérir de nouvelles données d'observations biologiques lors d'un événement naturaliste comme un [BioBlitz](https://en.wikipedia.org/wiki/BioBlitz).

![Schéma théorique de fonctionnement](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_jVIIVR11rac_p.564581_1488663708772_undefined)

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

### Applications existantes

| Application        | Open source           | Structure | Contact | Contacté ? | Commentaire |
| ------------------ |-----------------------| ----------|---------|------------|-------------|
| [i-Naturalist](https://www.inaturalist.org/) |   |     |         |            |             |
| [Map Of Life](https://mol.org/)              |   |     |         |            |             |
| [i-Spot](https://www.ispotnature.org/)       |   |     |         |            |             |
| [Ecobalade](http://www.ecobalade.fr/)        |   |     |         |            |             |
| [I-Record](https://www.brc.ac.uk/irecord/)   |   |     |         |            | Basé sur drupal (7?) demande beaucoup de maintenance |
| [BioCollect](https://www.ala.org.au/biocollect/)|  |   |         |            |             |

TODO: finir de remplir le tableau.

## Description fonctionelle

![Schéma théorique de fonctionnement](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_jVIIVR11rac_p.564581_1488663708772_undefined)

### Profil utilisateur

L'utilisateur choisi son profil : débutant, intermédiare ou confirmé.

### Formulaire

L'utilisateur rempli un formulaire qui répond au questions Qui / Quoi / Ou / Comment.

Les champs du formulaire sont décris dans cette [mind map](https://framindmap.org/c/maps/320935/edit).

**TODO** : Vulgariser le [DarwinCore](http://www.canadensys.net/publication/darwin-core?lang=fr) selon le type de profil, voir [exemple mind map débutant](https://framindmap.org/c/maps/321124/edit)

### Récupération des données manquantes

Connexion avec les API existantes :
 - Geographique : OpenStreetMap
 - Taxonomique : Catalogue of Life
 - Phylogénétique : Open Tree of Life

### Validation DarwinCore

Validation avec [DarwinCore Validator](https://tools.gbif.org/dwca-validator/).

### Publication

[GBIF.org > publisher](https://www.gbif.org/become-a-publisher)

### Configuration de la zone géographique

[GBIF.org > occurrence > location](https://www.gbif.org/occurrence/search) (aller voir sur _location_)

## Contribuer

 - [Slack](openbioblitz.slack.com)
 - [Carnet de bord](https://hackmd.io/CYBgpgxsAcIMwFoCMBOALMBaBmZoJWgEMIEA2EAJjgHZhski1okg?both#)
 - résidence à l'Hotel Pasteur à Rennes du 4 septembre au 15 décembre de 9h30 à 19h30 (selon les disponibilitées de chacuns)

## Architecture

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

## Contexte

[OpenBioBlitz](http://movilab.org/index.php?title=Recette_frugale_d%27hackathon_citoyen_open_source:_en_32_jours_et_sans_budget#Open_BioBlitz) est un projet initié et développé lors de la première édition de [la Nuit du Code Citoyen](https://codecitoyen.github.io/villes/rennes.html) le 4-5 mars 2017 à Rennes (Bretagne).

[Documentation de la mini NCC dédiée à OpenBioblitz](https://mensuel.framapad.org/p/miniNCC) le 26 mai 2017 à Rennnes
