# Méthodologie de la création du schéma

## Investigation

### Organisation

L'idée de création d'un schéma de données pour les entrées d'archives vient à la fois du Service Interministériel des Archives de France (SIAF) et de l'Association des Archivistes Français (AAF). 

La première étape a été de constituer un groupe de travail composé de ses deux acteurs mais également d'archivistes qui produisent les registres des entrées. L'objectif a été d'avoir un groupe assez représentatif des différents services qui peuvent exister, mais également des outils utilisés par les services. Le groupe a aussi associé un expert chargé de représenter les réutilisateurs et usagers extérieurs aux archives.

Dans le cadre de ce projet, les commanditaires (SIAF et AAF) ont également joué le rôle de sponsors et ont réellement permis de faire avancer et de faciliter le travail.

Création d'un schéma de données pour les registres d'entrées d'archives des services publics d'archives. 

* [Copil 1](https://Archivistes75.github.io/registre_entrees/20200703_COPIL1/)
* [Copil 2](https://Archivistes75.github.io/registre_entrees/20200911_COPIL2/) 
* [Copil 3](https://Archivistes75.github.io/registre_entrees/20201105_COPIL3/)
* [Copil restreint 4](https://Archivistes75.github.io/registre_entrees/20210503_COPIL4)
* [Copil 5](https://Archivistes75.github.io/registre_entrees/20210104_COPIL5)

Une documentation complète sous format pdf est accessible [ici](https://Archivistes75.github.io/registre_entrees/Documentation/Documentation_schema_registre.pdf)

**Composition du groupe de travail** : 

* Service Interministériel des Archives de France
* Association des Archivistes Français
* Datactivist
* Archives départementales de l'Eure
* Archives départementales de l'Oise
* Archives municipales d'Avignon
* Archives nationales
* Archives régionales des Pays-de-la-Loire
* INHA, Université de Paris Nanterre
* Programme Vitam

### Etat des lieux

Un état des lieux des services ayant déjà publié en open data leur registre d'entrées a ouvert la démarche. Pour cela, une recherche sur [data.gouv](https://www.data.gouv.fr/fr/) a permis d'identifier 9 jeux de données en ligne. 

Un premier constat a pu être établi :

* des services ont déjà publié ce type de données

* il n'y a pas un modèle unique de registre des entrées

* la publication reste malgré tout marginale

* la granularité et le périmètre de publication ne sont pas toujours les mêmes 

Pour compléter cet échantillon, un appel à transmission d'exemples de registres d'entrées a été lancé. Afin d'être suffisamment représentatif, des services utilisant différents logiciels métiers.

Ces versions de registres sont donc, dans la plupart des cas, des extractions des outils de gestion (Système d'Information archivistique), ils reflètent la structure même des bases de données dans lesquelles les données sont produites. Le nombre de SIA sur le marché étant assez limité, nous avons pu accéder à une version du registre pour une majorité d'éditeurs. 

L'adéquation entre SIA et registre d'entrées est forte, le travail à effectuer sur le fichier en sortie de SIA sera sans doute important (changement de nom de colonne, enrichissement, nettoyage de données...). une piste pour lutter contre ce problème serait que les éditeurs implémentent le schéma de données comme modèle de données pour les registres des entrées des SIA.

### Identification des cas d'usages des données

La compréhension des usages potentiels des jeux de données est importante car elle permet d'évaluer les besoins en données. Pour cela, un atelier sur des cas d'usages et sur les (ré)utilisateurs a été réalisé. Il posait les questions suivantes :

* *En tant que*

* *Je veux*

* *Afin de*

Cette démarche permet d'identifier le type d'utilisateurs, leurs besoins et leurs objectifs.

A l'issu de cet atelier, nous pouvons distinguer 2 grandes catégories d'usagers :

* **Usagers internes** : archivistes, services producteurs
* **Usagers externes** : étudiants, érudit, curieux et professionnels (journalistes, historiens, généalogistes professionnels, notaires)

Les premiers ayant des besoins plutôt orientés sur le pilotage, le suivi et la gestion et les seconds des besoins beaucoup plus vastes et difficiles à anticiper et prévoir.

De ce travail , il est possible d'identifier les intérêts de la publication des données des registres des entrées :

* apporte de la visibilité sur le travail de collecte

* permet de s'orienter dans les fonds

* offre une vision agrégée sur les collectes réalisées

* avoir des indicateurs d'activité 

### Analyse des données

Une fois ce premier travail effectué, il a fallu analyser les registres collectés et transmis par les services, pour cela, les différents éléments ont été regroupés dans une base de données relationnelles en procédant au :

* recensement des sources de données, producteurs, types de producteurs, source des données

* dépouillement des fichiers de données : compilation de tous les éléments présents dans les différents fichiers et tels qu'ils existent (par ex. "cote" et "cotation", même s'ils représentent la même chose, constituent chacun une entrée). Ajout d'une description du champ, du type (même si dans la très grande majorité des cas il s'agit de champ de type "chaîne de caractères")

* regroupement par la création de familles et de sous-familles. Ces éléments apparaissent assez rapidement une fois le travail d'identification effectué. Les familles et sous-familles permettent de voir les éléments importants du schéma.

## Concertation

*Les citations proviennent de [schema.data.gouv.fr](https://schema.data.gouv.fr/)*

### Profiter de l’existant

> *De nombreux standards existent déjà, qu’ils concernent des formats de données ou des formats de champs. Certains standards sont devenus incontournables aujourd’hui, comme ISO-8601 pour les dates ou WGS 84 pour les coordonnées géographiques.*

Profiter de l'existant c'est aussi le travail effectué lors de la phase d'identification. Partir de ce qui existe, en tirer le commun puis ajuster/adapter. 

### Identifier et associer l’écosystème

> *Les personnes/organisations que vous associez sont la meilleure garantie d’un schéma de données efficace et largement adopté, permettant d'aboutir à un véritable standard. Les producteurs d’une part qui connaissent la réalité de leurs données, de la collecte, etc. et qui ont leurs propres usages. Les usagers d'autre part, leurs besoins et leurs difficultés d’autres part, qu’ils soient déjà connus, « sous le radar » ou en devenir.*

Dans le cas des registres des entrées, l'association de l'écosystème a été simple car il s'agit d'une commande par le réseau et pour le réseau. C'est sans doute plus difficile d'associer des usagers mais cela a tout de même été fait en associant un expert qui avait beaucoup commenté le registre des Archives Nationales lors de sa publication.

### Prendre le temps

> *Un schéma de données est susceptible de concerner beaucoup de producteurs et d’usagers. Sa modification peut avoir un impact important. Il est donc crucial de prendre le temps d’obtenir tous les retours avant de publier un schéma utilisable par le plus grand nombre. Un schéma de données devrait être publié quand il est prêt, non pas en fonction d’un impératif de délai.*

Les pratiques de chaque service impactent assez fortement les fichiers produits. Le choix a été fait dès le départ de faire un schéma le plus exhaustif complet et avec de nombreux éléments optionnels afin de pouvoir prendre en compte la plupart des pratiques.

### Cas de l'identifiant pivot

> *Utiliser des données pivot relevant d’un référentiel ouvert pour relier les données à d’autres données, par exemple l’utilisation du numéro SIREN pour identifier des organisations*. 

Il est à noter que l'importance du recours à des référentiels partagés figure également dans le Cadre stratégique des Archives :

> **Objectif 6.1** : Promouvoir l’utilisation d’autorités et de référentiels partagés

La recherche d'une donnée pivot a été une opération assez délicate. L'utilisation du SIREN de la collectivité à laquelle appartient le service des archives ne s’avérait pas totalement satisfaisante, la notion de service public d'archives étant gommée au profit de l'institution d'appartenance. Par ailleurs, dans certains cas, cela pouvait entraîner une confusion plus préjudiciable : cas des versements réalisés par les services déconcentrés de l'Etat et conservés par les services départementaux d'archives.

Il pouvait y avoir 2 candidats à cet identifiant pivot :

* de nombreux services diffusant leurs fonds numérisés en ligne possèdent des identifiants pérennes ARK. L'ARK se compose d'une partie, le Name Assigning Authority Number (NAAN), qui permet d'identifier une institution. Mais, même si le [registre des NAAN est public](https://n2t.net/e/pub/naan_registry.txt), il n'est pas diffusé de façon structuré. Par ailleurs, tous les services n'ont pas un tel identifiant et cela semble complexe de le rendre obligatoire pour les services.

* les archivistes utilisent depuis de nombreuses années un standard de description des archives, l'*Encoded Archives Description* (EAD), l'EAD comporte une balise <eadid> qui possède l'attribut MAINAGENCYCODE. Cela fait référence à une autre norme, l'ISAD-G, qui dans son 3.1.1, définit bien les éléments d'identification d'un fonds.

  * le code du pays conformément à la dernière version de l'ISO 3166, *Codes pour la représentation des noms de pays* (FR);
      
  * le code du service d'archives conformément à la norme nationale de codification des services d'archives, ou tout autre élément d'identification du lieu de conservation (AD01);
      
  *  la cote ou tout autre élément d'identification spécifique (1W).

L'EAD précise pour sa part que le MAINAGENCYCODE doit être conforme à la norme ISO 15511, qui pour la France correspond à FR-[identifiantRCR]. Le Répertoir des centres de ressources (RCR) est lui-même structuré de la façon suivante : sur 9 chiffres reprenant : Code géog. postal, n° INSEE, numéro séquentiel. Une recherche simple et rapide permet de vite se rendre compte que ce n'est pas le cas. 

* Pour les archives départementales, le code est de type : FRAD_0COG (ex. FRAD_001)
        
* Pour les archives communales, le code est de type : FRAC_COG (ex. FRAC_06088) ou FRAC_CodePostal (FRAC_95500)
        
* Comment gérer les cas des services d'archives métropolitaines et des services mutualisés?
        
* Comment gérer les cas des entrées venant des services de l'Etat?

L'une des limites est que la liste des identifiants n'est pas publiée en open data et donc ne permet pas de réellement jouer son rôle de pivot.

Il existe d'autres identifiants (VIAF, ISNI...) mais ceux-ci ne sont pas utilisés (connus) par les services archives, qui ne les utilisent pas, en l'état actuel de diffusion de ces identifiants, ils ne constituent donc pas un pivot intéressants pour faire le lien entre un service et des IR par exemple.

### Concertation en dehors du groupe de travail

Le schéma a été ajouté à schema.data.gouv comme étant en investigation le 15 novembre 2020.

Un appel à commentaires a eu lieu du 04 janvier au 12 février 2021.Un webinaire de présentation du schéma a ouvert cet appel à commentaire le 04 janvier 2021. Sur la période, une cinquantaine de retours a été réalisé. 

Le groupe de travail a analysé les commentaires et à l'issu de ce travail, une V1.0 a été réalisée.

## Les étapes de publication d'un jeu de données

Pour préparer la publication de vos données, vous pouvez trouver des informations sur les fiches pratiques réalisées par [OpenDataFrance](https://opendatafrance.gitbook.io/odl-ressources/fiches-pratiques/premiers-pas/preparer-les-donnees-pour-une-publication-en-open-data)

### Identifier les données
Lors de la phase de création du standard, nous avons identifié deux sources de productions des données, elles peuvent :

* provenir des systèmes d'information des services d'archives (SIA)

* provenir de fichers tabulaires (excel, calc)

### Préparer les données

Il va falloir préparer les données afin qu'elles correspondent au modèle défini par le standard. Il peut être nécessaire de changer le nom des colonnes, de supprimer ou ajouter certaines colonnes, de modifier des valeurs etc.

### Documenter les données

Pour obtenir des **informations sur la publication** d'un jeu de données, vous pouvez consulter : l'[aide de data.gouv.fr](https://doc.data.gouv.fr/jeux-de-donnees/publier-un-jeu-de-donnees/).

**Métadonnées descriptives**

* Nom du producteur du jeu de données : Le nom du producteur permet d’indiquer le service qui a produit et publié le jeu de données. 

            `Archives municipales de la commune de XXX`
            `Archives départementales de XXX`
            
* Titre du jeu de données : il s’agit du nom du jeu de données et pas du nom du fichier

        `Registre des entrées de [entité productrice], année [XXXX]`
        
* Description du jeu de données :

        `Ce jeu de données contient les entrées du services des archives de [entité] pour l’année [XXXX]. Chaque entrée dans le service est enregistrée par type d’entrée (publique ou privée) avec le nom de l'entité productrice, la thématique, le volume. Les données proviennent de l'outil [préciser l'outil de gestion], et elles ont été traitées de la façon suivante avant publication [préciser les traitements : ajout d'éléments, suppression, harmonisation etc.]. [Dans le cas d'archives entrées à titre intermédiaire, des éliminations règlementaires pourront avoir lieu.]`
        
[Toutes les précisions complémentaires concernant le contenu peuvent être apportées si le jugé nécessaire]        
        
* Fréquence de mise à jour :

        `Annuelle `(à modifier le cas échéant)

* Catégories (tag) :

        `“Archives”, “Entrées d’Archives”, "Archives publiques"`

* Licence : [Licence à choisir dans le cadre règlementaire]
        
* Contact : Indiquer un mail de contact pour les réutilisateurs 

        `(archives@archives.fr)`