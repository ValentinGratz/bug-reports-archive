# Bug : Windows 11 - Stockage système - "Système et espace réservé" occupe anormalement 80,7 Go d'espace disque

## Environnement
- Produit : Microsoft Windows 11
- Version : Windows 11 à jour
- Type d'appareil : PC personnel
- Stockage concerné : Disque système Windows
- Date de constatation : Juillet 2026

## Description du problème
Windows indique que la catégorie **"Système et espace réservé"** utilise **80,7 Go** d'espace disque.

Cette occupation est anormalement élevée par rapport au fonctionnement habituel de Windows 11 (normalement quelques Go). Aucun fichier utilisateur visible ne correspond à cette taille et Windows ne fournit pas d'information permettant d'identifier précisément les fichiers concernés.

## Reproduction
- Fréquence : Permanente
- Étapes :
  1. Ouvrir **Paramètres Windows**
  2. Aller dans **Système > Stockage**
  3. Consulter la catégorie **"Système et espace réservé"**
  4. Constater une utilisation excessive de l'espace disque

- Résultat attendu :
  - La catégorie système doit occuper un espace raisonnable.
  - Les fichiers responsables doivent être identifiables ou nettoyables.

- Résultat observé :
  - "Système et espace réservé" occupe 80,7 Go.
  - L'origine exacte de l'espace utilisé est inconnue.

## Symptômes observés
- Espace disque utilisé qui augmente sans raison apparente.
- Fichiers responsables invisibles dans l'Explorateur Windows.
- Impossible d'identifier précisément la source de consommation.
- Les outils classiques de nettoyage Windows ne permettent pas de récupérer cet espace.

## Vérifications effectuées
- Nettoyage de disque Windows : effectué
- Nettoyage des fichiers temporaires : effectué
- Vérification des fichiers personnels : aucun fichier correspondant trouvé
- Recherche via l'Explorateur Windows : impossible d'identifier la source
- Résultat :
  - L'espace reste occupé malgré les opérations de nettoyage.

## Apparition du bug
- Depuis : Juillet 2026
- Contexte :
  - Système Windows 11 maintenu à jour.
  - Apparition constatée après des mises à jour récentes.
  - Le comportement semble similaire au problème de stockage système invisible récemment signalé par plusieurs médias spécialisés.

## Impact
- Utilisateurs concernés :
  - Utilisateurs Windows 11 pouvant rencontrer cette accumulation de données système cachées.

- Gravité : P1 (Élevée)

- Conséquences :
  - Perte importante d'espace disque disponible.
  - Risque de saturation complète du stockage.
  - Impact plus important sur les machines disposant de SSD de faible capacité.

## Informations complémentaires
- Taille anormale constatée : 80,7 Go
- Catégorie concernée : "Système et espace réservé"
- Aucun fichier utilisateur responsable identifié.

## Hypothèse technique
Possible cause :
Un fichier système caché lié au stockage Windows ou aux mécanismes de mise à jour pourrait augmenter progressivement sans nettoyage automatique.

Le problème pourrait être lié à une accumulation de données système temporaires, de fichiers de mise à jour ou d'un composant interne Windows mal géré.

## Demande
- Identifier précisément la source de cette occupation disque.
- Fournir un moyen officiel de supprimer les données inutiles.
- Déployer un correctif empêchant cette accumulation excessive.

Le pack Tuesday du 14 juillet n'a presque rien changé. 
Résultat avec le pack Tuesday du 14juillet + un nettoyage ccleaner et une aide de copilot : 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/e086511c-f2f8-48bf-90a2-9891e6ab8f92" />

et aprés quelques manip via copilot, retour à l'anormal. 

Mais en date du 15 juillet, toujours ce même bug : <img width="481" height="107" alt="image" src="https://github.com/user-attachments/assets/0a0f0ca0-61ab-418c-a977-4d9377b9dbb7" />
