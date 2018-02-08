# OpenBioBlitz

## Quoi

OpenBioblitz est une application online/offline pour acquérir de nouvelles données d'observations biologiques lors d'un événement naturaliste comme un [BioBlitz](https://en.wikipedia.org/wiki/BioBlitz).

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

[Source : Carnet de terrain électronique](http://carnet-terrain-electronique.fr/applications/)

<iframe style="width:1200px;height:800px;border:0px"
solid black"src="http://carnet-terrain-electronique.fr/wiki/doku.php?id=apps:naturaliste/"> </iframe>

| Application        | Open source           | Structure | Contact | Contacté | Commentaire |
| ------------------ |-----------------------| ----------|---------|------------|-------------|
| [i-Naturalist](https://www.inaturalist.org/) |   |     |         |            |             |
| [Map Of Life](https://mol.org/)              |   |     |         |            |             |
| [i-Spot](https://www.ispotnature.org/)       |   |     |         |            |             |
| [Ecobalade](http://www.ecobalade.fr/)        |   |     |         |            |             |
| [I-Record](https://www.brc.ac.uk/irecord/)   |   |     |         |            | Basé sur drupal (7?) demande beaucoup de maintenance |
| [BioCollect](https://www.ala.org.au/biocollect/)
| [Biodiv go](https://biodivgo.com/fr/)  |   |         |            |             |

TODO: finir de remplir le tableau.

## Description fonctionelle

![Schéma théorique de fonctionnement](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_jVIIVR11rac_p.564581_1488663708772_undefined)

<iframe style="width:1200px;height:800px;border:0px
solid black" src="https://framindmap.org/c/maps/320935/embed?zoom=1"> </iframe>

### Profil utilisateur

L'utilisateur choisi son profil : débutant, intermédiare ou confirmé.
Les 3 niveaux doivent être très simples pour ne pas perdre l'utilisateur.

### Formulaire

L'utilisateur rempli un formulaire qui répond au questions Qui / Quoi / Où / Quand / Comment.

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

## Contribuer

 - [Slack](openbioblitz.slack.com)
 - [Carnet de bord](https://hackmd.io/CYBgpgxsAcIMwFoCMBOALMBaBmZoJWgEMIEA2EAJjgHZhski1okg?both#)
 
 Todo:
 - contacter des institutions (associations naturalistes, Muséums (UMS PatriNat), ou autres projets d'applications naturalistes
 
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

[OpenBioBlitz](https://hackmd.io/CYBgpgxsAcIMwFoCMBOALMBaBmZoJWgEMIEA2EAJjgHZhski1okg?both#) est un projet initié et développé lors d'un [hackathon](http://movilab.org/index.php?title=Recette_frugale_d%27hackathon_citoyen_open_source:_en_32_jours_et_sans_budget) organisé en 32 jours les 4-5 mars 2017 à Rennes (Bretagne) dans le cadre de l'événement national [la Nuit du Code Citoyen](https://codecitoyen.github.io/) .

[Présentation sur les données de biodiversité](https://docs.google.com/presentation/d/1YnATN3D6lx_RndzpiwFlbN3Ja5NmFflFvmdJJ7Mi92g/edit?usp=sharing) par Olivier Norvez sous licence [CC-BY](https://creativecommons.org/licenses/by/3.0/fr/)

### Licences du projet

OpenBioBlitz est un projet sous licence [CC-BY](https://creativecommons.org/licenses/by/3.0/fr/)
