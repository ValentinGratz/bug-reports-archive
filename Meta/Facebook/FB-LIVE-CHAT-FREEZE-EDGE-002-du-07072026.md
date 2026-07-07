# Facebook Live - Commentaires viewers figés sur Edge / Windows 11

**Status** : Régression active - Récidive confirmée
**Date initiale** : 25/05/2026
**Dernière maj** : 07/07/2026
**ID** : FB-LIVE-CHAT-FREEZE-EDGE-001

## Bug
**Plateforme** : Facebook
**Fonctionnalité** : Live
**Problème** : Les commentaires côté viewer se figent et ne défilent plus en temps réel

## Reproduction
**Fréquence** : Intermittent - Récidive constatée le 07/07/2026
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
