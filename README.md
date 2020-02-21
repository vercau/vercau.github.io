# FCE - Les données


## Vue d'ensemble des fournisseurs de données :

Ci-dessous, une ligne par source de données. Chaque source est détaillée par la suite.

|Organisme|Base de données|Description|
|--|--|--|
|INSEE|SIRENE|Répertoire des données Entreprises et Etablissements|
|DINUM|API Entreprise|Données inter ministérielles|
|DARES|DSN|Effectifs|
|DARES|DSN|Conventions Collectives|
|DGT|WIKI'T|Interactions de la DGT (inspection de travail)|
|DGCCRF|SORA|Interactions de la DGCCRF|
|DGEFP|MDF|Interactions de la DGEFP|
|DGE|EOS|Interactions de la DGE|
|DGT|DACCORD|Accords d'entreprise|
|DGEFP|RUPCO|Ruptures collectives (PSE et RCC)|
|DGEFP|APART|Activité partielle|
|DGEFP|ARIANE|Alternance (Contrats Pro et Apprentissage)|

Les nomenclatures nécessaires : 

|Organisme|Base de données|Description|
|--|--|--|
|INSEE|COG|Départements. [Lien COG - INSEE](https://www.insee.fr/fr/information/3720946)|
|INSEE|COG|Communes. [Lien COG - INSEE](https://www.insee.fr/fr/information/3720946)|
|INSEE|Cat Jur|Catégorie juridique des entreprises. [Lien CatJur - INSEE](https://www.insee.fr/fr/information/2028129)|
|INSEE|NAF|Activité des entreprises. [Lien NAF - INSEE](https://www.insee.fr/fr/information/2120875)|
|DGT|IDCC|Identifiant des conventions collectives. [Lien IDCC -DGT](https://travail-emploi.gouv.fr/dialogue-social/negociation-collective/article/conventions-collectives-nomenclatures)|
|DGT|UC|Unité de contrôle de Travail|


## Règles générales sur les flux de données

 1. Privilégier un accès API plutôt qu'à des fichiers d'extractions

Les règles ci-dessous concernent la mise à disposition par fichier CSV :

 2. Règle de nommage à formaliser
 3. Respecter le format identifié dans ce document (possibilité de le faire évoluer sur demande)
 4. Encodage en UTF8
 5. Séparateur de colonnes  : "," ou ";" mais stable dans le temps
 6. Encapsuler la valeur de chaque donnée par des double quote. Obligatoire pour les données au format chaine de caractères.
 
---
 
## INSEE - Base SIRENE - Données Entreprises :

|Nom|Libellé|Longueur|Type|
|--|--|--|--|
|siren|Numéro Siren|9|Texte|
|statutDiffusionUniteLegale|Statut de diffusion de l’unité légale|1|Liste de codes|
|unitePurgeeUniteLegale|Unité légale purgée|5|Texte|
|dateCreationUniteLegale|Date de création de l'unité légale|10|Date|
|sigleUniteLegale|Sigle de l’unité légale|20|Texte|
|sexeUniteLegale|Caractère féminin ou masculin de la personne physique|1|Liste de codes|
|prenom1UniteLegale|Premier prénom déclaré pour un personne physique|20|Texte|
|prenom2UniteLegale|Deuxième prénom déclaré pour un personne physique|20|Texte|
|prenom3UniteLegale|Troisième prénom déclaré pour un personne physique|20|Texte|
|prenom4UniteLegale|Quatrième prénom déclaré pour un personne physique|20|Texte|
|prenomUsuelUniteLegale|Prénom usuel de la personne physique|20|Texte|
|pseudonymeUniteLegale|Pseudonyme de la personne physique|100|Texte|
|identifiantAssociationUniteLegale|Numéro au Répertoire National des Associations|10|Texte|
|trancheEffectifsUniteLegale|Tranche d’effectif salarié de l’unité légale|2|Liste de codes|
|anneeEffectifsUniteLegale|Année de validité de la tranche d’effectif salarié de l’unité légale|4|Date|
|dateDernierTraitementUniteLegale|Date du dernier traitement de l’unité légale dans le répertoire Sirene|19|Date|
|nombrePeriodesUniteLegale|Nombre de périodes de l’unité légale|2|Numérique|
|categorieEntreprise|Catégorie à laquelle appartient l’entreprise|3|Liste de codes|
|anneeCategorieEntreprise|Année de validité de la catégorie d’entreprise|4|Date|
|dateDebut|Date de début d'une période d'historique d'une unité légale|10|Date|
|etatAdministratifUniteLegale|État administratif de l’unité légale|1|Liste de codes|
|nomUniteLegale|Nom de naissance de la personnes physique|100|Texte|
|nomUsageUniteLegale|Nom d’usage de la personne physique|100|Texte|
|denominationUniteLegale|Dénomination de l’unité légale|120|Texte|
|denominationUsuelle1UniteLegale|Dénomination usuelle de l’unité légale|70|Texte|
|denominationUsuelle2UniteLegale|Dénomination usuelle de l’unité légale – deuxième champ|70|Texte|
|denominationUsuelle3UniteLegale|Dénomination usuelle de l’unité légale – troisième champ|70|Texte|
|categorieJuridiqueUniteLegale|Catégorie juridique de l’unité légale|4|Liste de codes|
|activitePrincipaleUniteLegale|Activité principale de l’unité légale|6|Liste de codes|
|nomenclatureActivitePrincipaleUniteLegale|Nomenclature d’activité de la variable activitePrincipaleUniteLegale|8|Liste de codes|
|nicSiegeUniteLegale|Numéro interne de classement (Nic) de l’unité légale|5|Texte|
|economieSocialeSolidaireUniteLegale|Appartenance au champ de l’économie sociale et solidaire|1|Liste de codes|
|caractereEmployeurUniteLegale|Caractère employeur de l’unité légale|1|Liste de codes|

## INSEE - Base SIRENE - Données Etablissements :

|Nom|Libellé|Longueur|Type|
|--|--|--|--|
|siren|Numéro Siren|9|Texte|
|nic|Numéro interne de classement de l'établissement|5|Texte|
|siret|Numéro Siret|14|Texte|
|statutDiffusionEtablissement|Statut de diffusion de l’établissement|1|Liste de codes|
|dateCreationEtablissement|Date de création de l’établissement|10|Date|
|trancheEffectifsEtablissement|Tranche d’effectif salarié de l’établissement|2|Liste de codes|
|anneeEffectifsEtablissement|Année de validité de la tranche d’effectif salarié de l’établissement|4|Date|
|activitePrincipaleRegistreMetiersEtablissement|Activité exercée par l’artisan inscrit au registre des métiers|6|Liste de codes|
|dateDernierTraitementEtablissement|Date du dernier traitement de l’établissement dans le répertoire Sirene|19|Date|
|etablissementSiege|Qualité de siège ou non de l’établissement|5|Texte|
|nombrePeriodesEtablissement|Nombre de périodes de l’établissement|2|Numérique|
|complementAdresseEtablissement|Complément d’adresse|38|Texte|
|numeroVoieEtablissement|Numéro de voie|4|Numérique|
|indiceRepetitionEtablissement|Indice de répétition dans la voie|1|Texte|
|typeVoieEtablissement|Type de voie|4|Liste de codes|
|libelleVoieEtablissement|Libellé de voie|100|Texte|
|codePostalEtablissement|Code postal|5|Texte|
|libelleCommuneEtablissement|Libellé de la commune|100|Texte|
|libelleCommuneEtrangerEtablissement|Libellé de la commune pour un établissement situé à l’étranger|100|Texte|
|distributionSpecialeEtablissement|Distribution spéciale de l’établissement|26|Texte|
|codeCommuneEtablissement|Code commune de l’établissement|5|Liste de codes|
|codeCedexEtablissement|Code cedex|9|Texte|
|libelleCedexEtablissement|Libellé du code cedex|100|Texte|
|codePaysEtrangerEtablissement|Code pays pour un établissement situé à l’étranger|5|Liste de codes|
|libellePaysEtrangerEtablissement|Libellé du pays pour un établissement situé à l’étranger|100|Texte|
|complementAdresse2Etablissement|Complément d’adresse secondaire|38|Texte|
|numeroVoie2Etablissement|Numéro de la voie de l’adresse secondaire|4|Numérique|
|indiceRepetition2Etablissement|Indice de répétition dans la voie pour l’adresse secondaire|1|Texte|
|typeVoie2Etablissement|Type de voie de l’adresse secondaire|4|Liste de codes|
|libelleVoie2Etablissement|Libellé de voie de l’adresse secondaire|100|Texte|
|codePostal2Etablissement|Code postal de l’adresse secondaire|5|Texte|
|libelleCommune2Etablissement|Libellé de la commune de l’adresse secondaire|100|Texte|
|libelleCommuneEtranger2Etablissement|Libellé de la commune de l’adresse secondaire pour un établissement situé à l’étranger|100|Texte|
|distributionSpeciale2Etablissement|Distribution spéciale de l’adresse secondaire de l’établissement|26|Texte|
|codeCommune2Etablissement|Code commune de l’adresse secondaire|5|Liste de codes|
|codeCedex2Etablissement|Code cedex de l’adresse secondaire|9|Texte|
|libelleCedex2Etablissement|Libellé du code cedex de l’adresse secondaire|100|Texte|
|codePaysEtranger2Etablissement|Code pays de l’adresse secondaire pour un établissement situé à l’étranger|5|Liste de codes|
|libellePaysEtranger2Etablissement|Libellé du pays de l’adresse secondaire pour un établissement situé à l’étranger|100|Texte|
|dateDebut|Date de début d'une période d'historique d'un établissement|10|Date|
|etatAdministratifEtablissement|État administratif de l’établissement|1|Liste de codes|
|enseigne1Etablissement|Première ligne d’enseigne de l’établissement|50|Texte|
|enseigne2Etablissement|Deuxième ligne d’enseigne de l’établissement|50|Texte|
|enseigne3Etablissement|Troisième ligne d’enseigne de l’établissement|50|Texte|
|denominationUsuelleEtablissement|Dénomination usuelle de l’établissement|100|Texte|
|activitePrincipaleEtablissement|Activité principale de l'établissement pendant la période|6|Liste de codes|
|nomenclatureActivitePrincipaleEtablissement|Nomenclature d’activité de la variable activitePrincipaleEtablissement|8|Liste de codes|
|caractereEmployeurEtablissement|Caractère employeur de l’établissement|1|Liste de codes|

## INSEE - Base SIRENE - Données Liens succession:

|Nom|Libellé|Longueur|Type|
|--|--|--|--|
|continuiteEconomique|Indicatrice de continuité économique entre les deux établissements|5|Texte|
|dateDernierTraitementLienSuccession|Date de traitement du lien de succession|19|Date|
|dateLienSuccession|Date d'effet du lien de succession|10|Date|
|siretEtablissementPredecesseur|Numéro Siret de l'établissement prédécesseur|14|Texte|
|siretEtablissementSuccesseur|Numéro Siret de l'établissement successeur|14|Texte|
|transfertSiege|Indicatrice de transfert de siège|5|Texte|

## DINUM - API Entreprise :

## DARES - Base DSN - Effectifs

- Fréquence : mensuelle
- Mode récupération : Minio
- Format : CSV, séparateur "," 
- Volume : 20 millions de lignes

| Colonnes | Format | Commentaire |
|--|--|--|
|MOIS|YYYY-MM|Mois de référence. Ne semble pas à jour, ne pas utiliser. Prendre le mois dans le titre du fichier|
|SIRET|NUM 14|SIRET de l’établissement|
|EFF_HOMME|NUM|Nombre de salarié homme|
|EFF_FEMME|NUM|Nombre de salarié femme|
|NB_CDD|NUM|Nombre de salarié en CDD|
|NB_CDI|NUM|Nombre de salarié en CDI|
|NB_CDI_INTERIM|NUM|Nombre de CDI d'intérim|
|NB_INTER_MISSION|NUM|Nombre de salarié en inter mission (travail temporaire)|
|NB_INTERIM|NUM|Nombre de salariées intérimaires|
|DATE_MAJ|YYYY/MM/DD|Date de génération du fichier|

## DARES - Base DSN - IDCC

- Fréquence : mensuelle
- Mode récupération : Minio
- Format : CSV, séparateur "," 
- Volume : 2 millions de lignes

| Colonnes | Format | Commentaire |
|--|--|--|
|MOIS|YYYY-MM|Mois de référence. Ne semble pas à jour, ne pas utiliser. Prendre le mois dans le titre du fichier|
|SIRET|NUM 14|SIRET de l’établissement|
|IDCC|NUM 4|Code Convention Collective|
|DATE_MAJ|YYYY/MM/DD|Date de génération du fichier|

## DGT - Base WIKI’T - Interactions pôle T

- Fréquence : mensuelle
- Mode récupération : Minio
- Format : CSV, séparateur ";" 
- Volume : 150 000 lignes

| Colonnes | Format | Commentaire |
|--|--|--|
|SIRET|NUM 14|SIRET de l’établissement|
|DATE|DD/MM/YYYY|Date du dernier contrôle|
|PROPRIETAIRE|VARCHAR|Libellé de l’unité de contrôle|

## DGCCRF - Base SORA - Interactions pôle C

| Colonnes | Format | Commentaire |
|--|--|--|

## DGE - Base EOS - Interactions pôle 3E-SEER

- Fréquence : mensuelle
- Mode récupération : Minio
- Format : CSV, séparateur 
- Volume : 

| Colonnes | Format | Commentaire |
|--|--|--|
SIRET|NUM 14|SIRET de l’établissement|
DATE|YYYY-MM-DD|Date de la visite. Format à vérifier|
REGION|VARCHAR|Nom de la région|
AGENT|VARCHAR|Nom des agents|
FILIERE|VARCHAR|Libellé filière|
TYPE|VARCHAR|Type de visite|
SUIVI|VARCHAR|Type de suivi|

## DGEFP - Base MDF - Interactions pôle 3E-SRC

| Colonnes | Format | Commentaire |
|--|--|--|

## DGT - Base DACCORD - Accords d'entreprise

- Fréquence : mensuelle
- Mode récupération : Minio
- Format : CSV, séparateur ";" 
- Volume : 1 350 000 lignes

| Colonnes | Format | Commentaire |
|--|--|--|
|NUM_DOS|CHAR 12|Numéro dossier DACCORD|
|SIRET|NUM 14|SIRET de l’établissement|
|DT_SIGN|YYYY-MM-DD|Date de signature de l’accord|
|groth2_01_epargne_salariale|INT|Nb accords épargne salariale|
|groth2_02_remuneration|INT|Nb accords rémunération|
|groth2_03_duree_amenagement_temps_travail|INT|Nb accords temps de travail|
|groth2_04_conditions_travail|INT|Nb accords conditions de travail|
|groth2_05_emploi|INT|Nb accords emploi|
|groth2_06_egalite_professionnelle|INT|Nb accords égalité professionnelle|
|groth2_07_classifications|INT|Nb accords classifications|
|groth2_08_formation_professionnelle|INT|Nb accords formation professionnelle|
|groth2_09_protection_sociale|INT|Nb accords protection sociale|
|groth2_10_droit_syndical|INT|Nb accords droit syndical|
|groth2_11_autres|INT|Nb accords autres|
|groth2_12_nouvelles_technos_numeriques|INT|Nb accords nouvelles technos|

## DGEFP - Base RUPC0 - Ruptures collectibes (PSE et RCC)

- Fréquence : mensuelle
- Mode récupération : Minio
- Format : CSV, séparateur ";"
- Volume : 20 000 lignes

### Les procédures :

| Colonnes | Format | Commentaire |
|--|--|--|
|NUMERO|INT|Numero PSE|
|TYPE|VARCHAR|Type|
|DATE_ENREGISTREMENT|||
|ETAT DU DOSSIER|||
|NOM GROUPE||Ne pas utiliser|
|EFFECTIF GROUPE||Ne pas utiliser|
|SIREN ENTREPRISE|NUM 9||
|EFFECTIF ENTREPRISE||Ne pas utiliser|
|SITUATION JURIDIQUE||
|DATE_JUGEMENT|||
|ACCORD SIGNE|||
|Nombre de Ruptures de Contrats en début de procédure |||
|Nombre de Ruptures de Contrats en fin de procédure|||

### Les établissements associés :

| Colonnes | Format | Commentaire |
|--|--|--|
|NUMERO|INT|Numero PSE|
|TYPE|VARCHAR|Type|
|DATE ENREGISTREMENT|||
|EFFECTIF|INT|Effectif de l’établissement|
|SIRET|NUM 14||
|Nombre de Ruptures de Contrats en début de procédure Etab|INT||
|Nombre de Ruptures de Contrats en fin de procédure Etab|INT||
|SIREN|NUM 9|Ne pas utiliser|
|SITUATION_JURIDIQUE|VARCHAR||
|DATE_JUGEMENT|DD/MM/YYYY||

## DGEFP - Base APART  - Activité partielle

| Colonnes | Format | Commentaire |
|--|--|--|

## DGEFP - Base ARIANE ? - Contrats Pro  

- Fréquence : mensuelle
- Mode récupération : Minio
- Format : CSV, séparateur ";"
- Volume : 5 000 lignes

| Colonnes | Format | Commentaire |
|--|--|--|
|TypeContrat|NUM|Type de contrat (liste à récupérer)|
|NumeroEnregistrement|Texte|Numéro d'enregistrement. Format à vérifier, j'ai des doute sur la perte du 0 initial vu que les premiers caractères correspondent au numéro du département|
|DateDebut|DD/MM/YYYY|Date de début du contrat|
|DateRupture|DD/MM/YYYY|Date de rupture du contrat|
|EmployeurSiret|NUM 14|SIRET de l'employeur|


## DGEFP - Base Apprentissage

| Colonnes | Format | Commentaire |
|--|--|--|
|Contrat DateDebut|||
|TypeContrat|||
|NumeroEnregistrement|||
|Employeur Siret|||
|DateRupture|||


## Les Nomenclatures :

### Départements (INSEE) :

### Communes (INSEE) : 

### Catégories juridiques (INSEE) : 

### NAF (INSEE) : 

### IDCC (DGT) :

