# Facebook Live - Commentaires viewers figés sur Edge / Windows 11

**Status** : Régression active
**Date** : 25/05/2026
**ID** : FB-LIVE-CHAT-FREEZE-EDGE-001

## Bug
**Plateforme** : Facebook
**Fonctionnalité** : Live
**Problème** : Les commentaires côté viewer se figent et ne défilent plus en temps réel

## Reproduction
**Fréquence** : Intermittent - régression constatée le 25/05/2026
**Navigateur** : Microsoft Edge 148.0.3967.83 (Version officielle) (64 bits)
**OS** : Windows 11

**Étapes** :
1. Ouvrir Edge en navigation normale
2. Rejoindre n’importe quel live Facebook
3. Observer la zone de commentaires

## Symptôme
Les premiers commentaires s’affichent au chargement du live puis le flux se fige complètement. Aucun nouveau message n’apparaît en temps réel. La vidéo et le compteur de viewers continuent de fonctionner normalement. Seul un refresh complet de la page fait apparaître les messages manqués.

## Console
Aucune erreur bloquante liée au WebSocket ou au chat. Seuls logs présents :
3eZiCoyW1Mb.js:321 Permissions policy violation: unload is not allowed in this document.
Me80Z13eYqn.js:245 Stop!
Me80Z13eYqn.js:245 Il s’agit d’une fonctionnalité de navigateur conçue pour les développeurs...
Me80Z13eYqn.js:245 Consultez https://www.facebook.com/selfxss pour plus d’informations.

→ Messages standard Facebook anti-self-XSS, non corrélés au bug.[Violation]

## Testé / Éliminé
- [x] Cache + cookies vidés
- [x] Extensions désactivées
- [x] Mode navigation InPrivate testé
- [x] Pas de mise à jour Edge entre la période fonctionnelle et la régression
- [x] Le problème avait disparu ce week-end sans action utilisateur, revenu le 25/05/2026

## Début
Réapparu le 25/05/2026. Bug déjà connu auparavant, résolu temporairement ce week-end du 23-24/05, régression depuis aujourd’hui sans changement côté client.

## Impact
**Touché** : Viewers utilisant Edge sur Windows 11
**Conséquence** : Impossible de suivre ou participer au chat en temps réel. Perte totale d’interaction live. Obligation de refresh manuel pour voir les nouveaux messages.

## Liens
**Live de repro** : https://www.facebook.com/61563854194437/videos/1455670039666716
**User ID touché** : [optionnel]

## Contournements temporaires
1. **Navigation privée** : Ouvrir le live dans un onglet InPrivate `Ctrl+Shift+N`
2. **Autre navigateur** : Le bug semble spécifique à Edge au moment du test
3. **Refresh forcé** : F5 toutes les 10-15s, mais perte de l’aspect temps réel

## Notes
Régression probable côté serveur Facebook sur la gestion WebSocket / SSE pour Edge. Le fait que le bug disparaisse puis revienne sans maj Edge indique un déploiement côté Meta.
