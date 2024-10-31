# Architecture décisionnelle - Étude de cas

## Contexte

La société de Facturation Automatisée avec Délivrabilité Assurée est leader dans le domaine de la dématérialisation.

Elle permet à ses clients de délivrer électroniquement tout élément comptable (devis, facture, avoir, etc), logistique (bon de commande, bordereau de livraison, accusé de réception), et RH (offre d'emploi, offre de pré-embauche, contrat, bulletin de salaires, document de fin de contrat, etc) à leur destinataire, de façon fiable et sécurisée.
Les éléments (fichiers PDF ou EDI) sont générés par la FADA, en se basant sur des données transmises par ses clients (par exemple, un fichier XML regroupant les méta-données de 150'000 factures à produire, à archiver, et à envoyer, et le template de document à utiliser).
Elle met également à disposition ces éléments dans un Coffre-Fort Électronique (CFE), et les stocke à long terme dans un Système d'Archivage Électronique (SAE).

La FADA a été fondée en 2003 par 3 associés, et compte aujourd'hui près de 150 salariés.
Elle produit environ 2,5 millions de documents par mois, sur des serveurs qu'elle loue chez un prestataire spécialisé (OVH).

La société a grossi organiquement (en recrutant de nouveaux salariés), mais aussi par concentration verticale par rachats successifs de ses partenaires, pour internaliser certains fonctionnalités.


## Problématique

Afin d'organiser son activité au quotidien et à court terme, les managers de la société se connectent à de nombreuses sources différentes de données :
    - des fichiers plats de logs, répartis sur plusieurs dizaines de serveurs
    - des logs enregistrés au niveau système, soit côté Windows, soit côté Linux
    - de très nombreuses métriques sont collectées par plusieurs agents installés sur les machines (postes clients et serveurs), qui renvoient chacun à des systèmes différents (GLPI, Grafana, Centréon)
    - des exports de base de données, au format CSV, qu'ils importent dans Excel pour les traiter
    - des interfaces web développées en interne, pour se connecter à des API mises à disposition par les fournisseurs (OVH, mailjet, Arkhineo, etc)
    - l'ERP de l'entreprise, basé sur Dolibar
    - un outil interne de gestion des compétences
    
Les décisions stratégiques sont prises sur la base de PKI remontés par les managers lors des CoPil/ComEx, dans des diaporamas PowerPoint.
Ils sont ensuite transmis au format Excel aux dirigeants.

La préparation de ces indicateurs est estimée à plusieurs dizaines de jour-homme par mois, ce qui représente un coût non négligeable pour l'entreprise, et ralentit considérablement le processus de décision dans un environnement très dynamique (notamment la loi de finance 2022 qui entre en vigueur en 2026).

De plus, certains employés remontent parfois des intuitions intéressantes sur le taux d'utilisation des serveurs, et des nombreuses pannes rencontrées. Le DSI souhaiterait pouvoir approfondir la question, mais il se perd dans la quantité d'endroits où il pourrait trouver des informations pertinentes.

M. René, dirigeant de la société, a donc décidé de lancer un grand chantier de mise en place d'un SID, afin de centraliser la gestion de toutes les données de l'entreprise, et permettre aux cadres de bénéficier en temps réel de l'ensemble des données nécessaires à la planification à long terme de l'activité de l'entreprise.

Votre cabinet de conseil a donc été missionné pour étudider les solutions suivantes :

  - mise en place d'un SID hébergé localement par l'entreprise, basé sur des solutions open-source
  - mise en place d'un SID hébergé localement par l'entreprise, basé sur des solutions propriétaires ; une alternative possible serait l'utilisation de versions Cloud de ces solutions
  - mise en place d'un SID hébergé chez Azure, en utilisant les composants Microsoft dédiés
  - mise en place d'un SID hébergé chez AWS, en utilisant les composants dédiés.
    
## Livrables attendus 

  - en milieu de projet (jeudi 31/10/2024 à 18h) : un document présentant l'avancement de vos recherches, l'architecture telle que vous la préconisez, et une liste des avantages/inconvénients de la solution
  - en fin de projet (mardi 10/12/2024 à 18h) :
    - un document détaillant votre solution, avec en plus une étude (rapide) des coûts de mise en place puis d'éventuels frais mensuels/annuels
    - un diaporama expliquant votre solution, que vous présenterez au client et aux autres membres du cabinet en 10 à 12 minutes.
   
  Votre préconisation de solution sera mise à disposition des autres membres du cabinet via 360Learning.

  **Il n'est pas attendu de démonstration technique, vous n'avez que 6h pour préparer !**

## Organisation du travail

4 groupes :
  - groupe 1 : 4 apprenants, travaillent sur les solutions open-source
  - groupe 2 : 4 apprenants, travaillent sur les solutions propriétaires
  - groupe 3 : 3 apprenants, travaillent sur Azure
  - groupe 4 : 3 apprenants, travaillent sur AWS
