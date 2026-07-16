# Bug d'affichage : bande blanche persistante en bas de l'application Doctolib

## Informations

* **Application :** Doctolib
* **Plateforme :** Android
* **Appareil :** Huawei P20 Lite
* **Version Android / iOS :** Android 9 (EMUI 9.1.0)
* **Version de l'application :** Dernière version disponible sur Google Play Store (à compléter)
* **Date :** 16/07/2026
* **Statut :** Ouvert

---

## Description

Une large bande blanche avec des bords arrondis apparaît en permanence en bas de l'application Doctolib.

Cette bande ne contient aucun texte, bouton ou élément interactif visible. Elle masque une partie de l'interface et semble correspondre à un composant d'affichage qui ne se charge pas correctement.

Le problème persiste après plusieurs tentatives de dépannage.

## Étapes pour reproduire

1. Ouvrir l'application Doctolib.
2. Se connecter au compte utilisateur.
3. Accéder à l'écran d'accueil (Historique, Recherche, etc.).
4. Observer la partie inférieure de l'écran.

## Résultat attendu

L'interface doit s'afficher normalement, sans élément blanc vide en bas de l'écran.

## Résultat obtenu

Une grande bande blanche vide est affichée en permanence en bas de l'écran.

Le problème est présent malgré :
- suppression du cache ;
- suppression des données de l'application ;
- désinstallation puis réinstallation ;
- redémarrage du téléphone ;
- vérification des paramètres d'affichage (taille de police et taille d'écran).

## Fréquence

* [ ] Une seule fois
* [ ] Parfois
* [x] Toujours

## Captures / preuves

- Capture d'écran montrant la bande blanche persistante en bas de l'application.
- (Ajouter le fichier de capture d'écran dans le dépôt GitHub.)

## Notes complémentaires

- Appareil : Huawei P20 Lite (2018)
- EMUI 9.1.0
- Android 9
- Aucun problème similaire observé avec les autres applications du téléphone.
- Le problème semble être lié à l'affichage de l'application Doctolib ou à une incompatibilité avec Android 9 / EMUI 9.
- Un signalement a été envoyé au support Doctolib (`mobile-store@doctolib.com`) avec la capture d'écran.

<img width="606" height="333" alt="photo_2026-07-16_15-44-40" src="https://github.com/user-attachments/assets/de36d514-6436-47d3-b0a5-a52f9b4532d3" />
