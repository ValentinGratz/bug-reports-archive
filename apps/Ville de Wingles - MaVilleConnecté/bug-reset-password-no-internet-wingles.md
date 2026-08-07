# Bug – Impossible de réinitialiser le mot de passe ("Pas de connexion internet") sur Android 17

## Informations

- **Application :** Ma Ville Connectée – Ville de Wingles
- **Plateforme :** Android
- **Appareil :** Google Pixel 10a
- **Version Android / iOS :** Android 17
- **Version de l'application :** 1.5.30 (version installée depuis le Google Play Store)
- **Date :** 2026-08-07
- **Statut :** Ouvert

---

## Description

Impossible de réinitialiser le mot de passe depuis l'application.

Lorsque je sélectionne **"Mot de passe oublié"**, je renseigne mon adresse e-mail puis je valide. L'application affiche immédiatement le message **"Pas de connexion internet"** alors que le téléphone dispose bien d'une connexion Internet fonctionnelle.

Le problème est reproductible aussi bien en Wi-Fi qu'en réseau mobile.

---

## Étapes pour reproduire

1. Ouvrir l'application **Ma Ville Connectée – Wingles**.
2. Appuyer sur **"Mot de passe oublié"**.
3. Saisir une adresse e-mail valide.
4. Valider la demande.

---

## Résultat attendu

L'application devrait envoyer une demande de réinitialisation du mot de passe et afficher un message de confirmation (ou envoyer un e-mail de réinitialisation).

---

## Résultat obtenu

L'application affiche le message d'erreur :

> **"Pas de connexion internet"**

Aucune demande de réinitialisation n'est envoyée.

Pourtant :

- la connexion Internet fonctionne normalement ;
- le problème est identique en Wi-Fi et en données mobiles ;
- toutes les autres applications accèdent correctement à Internet ;
- les autorisations Android de l'application ont été vérifiées (accès réseau et données en arrière-plan autorisés).

---

## Fréquence

- [ ] Une seule fois
- [ ] Parfois
- [x] Toujours

---

## Captures / preuves

<img width="570" height="1280" alt="image" src="https://github.com/user-attachments/assets/e2c5cd7e-bacc-4844-a3c5-c6e8edffa73c" />


---

## Notes complémentaires

Tests complémentaires effectués :

- ✅ Réinstallation complète de l'application.
- ✅ Test sur Google Pixel 10a sous Android 17.
- ✅ Test en Wi-Fi et en données mobiles.
- ✅ Vérification des autorisations Android.
- ✅ Internet fonctionnel sur toutes les autres applications.

Comparaison avec d'autres applications de l'éditeur :

- L'application **MaVilleConnectée** ne permet pas de trouver la commune de **Wingles**.
- Pour vérifier le fonctionnement de la plateforme, un test d'inscription a été réalisé sur une autre commune disponible dans **MaVilleConnectée**.
- Cette inscription fonctionne correctement, ce qui laisse penser que le problème est spécifique à l'application de la Ville de Wingles (ou à ses services associés).

## Impact

Le bug empêche les utilisateurs ayant oublié leur mot de passe de récupérer l'accès à leur compte depuis l'application.

Sur mon ancien smartphone (android 9 vieillissant) l'appli fonctionnait toujours. 
