# OpenBioBlitz

## Quoi

OpenBioblitz est une application online/offline pour acquérir de nouvelles données d'observations biologiques lors d'un événement naturaliste comme un [BioBlitz](https://en.wikipedia.org/wiki/BioBlitz).

![Schéma théorique de fonctionnement](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_jVIIVR11rac_p.564581_1488663708772_undefined)

## Comment

- Traduction automatique en [Darwin Core](http://rs.tdwg.org/dwc/) 
- Intégration des informations manquantes via des sites OpenSource (OpenTree of Life, Open Street Map, Catalogue of Life, etc.)
- Exportation vers une Base de Données
- Filtrage avec l'outil DarwinCore Validator du [GBIF](www.gbif.org)
- Exportation et publications des données vers le [GBIF](www.gbif.org)
- Configuration/Paramétrage des espèces déjà présentes sur les lieux via [GBIF](www.gbif.org) et/ou l'[INPN](https://inpn.mnhn.fr/accueil/index) pour une restriction et optimisation des ajouts d’informations présentes et manquantes
- 3 niveaux de récupération d'information: débutant / intermédiaire / confirmé

Deux interfaces opérationnelles en mode offline (utlisateurs et DarwinCore) échangent avec une API reliée à une Base de Données en ligne.
Avant d'être exportées vers le GBIF, les données sont filtrées par l'outil du [GBIF DarwinCore Validator](http://tools.gbif.org/dwca-validator).

## Contexte

[OpenBioBlitz](http://movilab.org/index.php?title=Recette_frugale_d%27hackathon_citoyen_open_source:_en_32_jours_et_sans_budget#Open_BioBlitz) est un projet initié et développé lors de la première édition de [la Nuit du Code Citoyen](https://codecitoyen.github.io/villes/rennes.html) le 4-5 mars 2017 à Rennes (Bretagne).

[Documentation de la mini NCC dédiée à OpenBioblitz](https://mensuel.framapad.org/p/miniNCC) le 26 mai 2017 à Rennnes

## Architecture

Interface de programmation entre la base de données et les applications online/offline (formulaire web et applications portables).

### Base de données

Portable
SQL ou non
Simple
Uniforme et partageable sous forme d'archive DarwinCore et d'exportation de données.

### Applis web

Préparer les formulaires
Project access (ACL)
Visualisation des données de base => pas un objectif principal

