_OpenBioBlitz est un projet initié et développé lors de la première édition de [la Nuit du Code Citoyen](https://codecitoyen.github.io/villes/rennes.html) le 4-5 mars 2017 à Rennes (Bretagne)_

* Licence repo GitHub page 
Creative Commons Attribution 3.0 Unported
http://creativecommons.org/licenses/by/3.0/

* Ressources de documentations: CC-BY licence [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) OpenBiolBlitz et contributeurs hackpad


### Quoi:

une application online/offline pour acquérir de nouvelles données d'observations biologiques lors d'un BioBlitz avec
- Traduction automatique en [Darwin Core](http://rs.tdwg.org/dwc/) 
- Intégration des informations manquantes via des sites OpenSource (OpenTree of Life, Open Street Map, Catalogue of Life, etc.)
- Exportation vers une Base de Données
- Filtrage avec l'outil DarwinCore Validator du [GBIF](www.gbif.org)
- Exportation et publications des données vers le [GBIF](www.gbif.org)
- Configuration/Paramétrage des espèces déjà présentes sur les lieux via [GBIF](www.gbif.org) et/ou l'[INPN](https://inpn.mnhn.fr/accueil/index) pour une restriction et optimisation des ajouts d’informations présentes et manquantes
- 3 niveaux de récupération d'information: débutant / intermédiaire / confirmé

NB: Il s'agit d'un outil de récupération de données et non de visualisation cartographique

### Comment:

Deux interfaces opérationnelles en mode offline (utlisateurs et DarwinCore) échangent avec une API reliée à une Base de Données en ligne.
Avant d'être exportées vers le GBIF, les données sont filtrées par l'outil du [GBIF DarwinCore Validator](http://tools.gbif.org/dwca-validator).

### Solutions techniques possibles :

**Formulaires**

Différents niveaux utilisateurs (débutant, intermédiaire, confirmé)
Se souvenir que l'information peut-être complétée automatiquement ultérieurement (taxonomie, géographie...)
Différentes sortes de catégories (box, textbox, cocombobox, listbox, list, button...)
Différents types d'insertions de données (images, geo-ref, text, etc.)
Créer une liste de champs prédéfinie via la configuration géographique et taxonomique

**Application portable**

Concevoir un formulaire offline nécessaire pour configurer les interfaces utilisateurs. => nécéssite aussi une réplication de la base de données, sous forme d'un format approprié (json) qui sera utilisé par l'API ultérieurement lors du chargement dans la base de données. Téléversement des données lorsqu'il y aura connection au réseau (et ou à la fin du BioBlitz).

**API**

Interface de programmation entre la base de données et les applications online/offline (formulaire web et applications portables).

**Base de données**

Portable
SQL ou non
Simple
Uniforme et partageable sous forme d'archive DarwinCore et d'exportation de données.

**Applis web**

Préparer les formulaires
Project access (ACL)
Visualisation des données de base => pas un objectif principal

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Licence Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">OpenBioBlitz</span> de <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/OpenBioBlitz" property="cc:attributionName" rel="cc:attributionURL">OpenBiolBlitz et contributeurs hackpad</a> est mis à disposition selon les termes de la <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">licence Creative Commons Attribution 4.0 International</a>.<br />Fondé(e) sur une œuvre à <a xmlns:dct="http://purl.org/dc/terms/" href="https://hackpad.com/OpenBioBlitz-jVIIVR11rac" rel="dct:source">https://hackpad.com/OpenBioBlitz-jVIIVR11rac</a>.
