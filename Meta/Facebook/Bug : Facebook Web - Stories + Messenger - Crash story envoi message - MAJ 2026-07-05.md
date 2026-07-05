# Bug : Facebook Web - Stories + Messenger - Crash de la story lors de l'envoi d'un message

> **Statut** : Toujours présent au 05/07/2026  
> **Signalement initial** : [Bug : Facebook Web - Stories + Messenger - Crash de la story lors de l'envoi d'un message](https://github.com/ValentinGratz/bug-reports-archive/blob/main/Meta/Facebook/Bug%20%3A%20Facebook%20Web%20-%20Stories%20%2B%20Messenger%20-%20Crash%20de%20la%20story%20lors%20de%20l'envoi%20d'un%20message.md)  
> **Mise à jour** : Confirmation de persistance du bug + ajout preuve vidéo

## Bug
**Facebook Web - Stories + Messenger - Fermeture de la story lors de l'envoi d'un message**

## Repro
**Systématique** sur Microsoft Edge dernière version / Windows 10/11

## Symptôme
Story ouverte en plein écran sur `facebook.com`. Si le chat Messenger est ouvert dans le même onglet/fenêtre et qu'un message est envoyé, la story se ferme immédiatement. L'interface remplace le contenu de la story par un écran d'erreur.

**Message d'erreur exact affiché** :  
`Impossible d’afficher la story`  
`Veuillez réessayer.`

## Console
À confirmer - Suspecté erreur réseau/WebSocket type `ERR_ABORTED` ou `story_unavailable` déclenchée au moment de l'envoi du message. Aucune erreur bloquante visible côté UI hors message affiché.

## Testé
- Navigation privée Edge : bug présent
- Extensions désactivées : bug présent  
- Messenger ouvert dans un onglet séparé : bug absent
- Chrome dernière version / Windows : non reproduit
- Firefox dernière version / Windows : non reproduit
- Cache + cookies vidés : bug présent

## Début
Depuis 2-3 semaines environ. **Toujours présent au 05/07/2026**

## Impact
Utilisateurs Microsoft Edge qui utilisent Stories + Messenger simultanément dans le même onglet. Conséquence : interruption forcée du visionnage, perte du contexte de la story, impossible de réagir/envoyer un DM sans quitter la story. Frictions UX fortes pour le multitask.

## Preuves
- **User ID touché** : `optionnel`
- **URL/ID du Live/Post** : `https://facebook.com/stories` avec chat Messenger docké
- **Vidéo/Screenshot** : 

<img width="1358" height="602" alt="msedge_WaorRPDpvy" src="https://github.com/user-attachments/assets/a4583222-4006-4156-b6d7-e1a44c4b1b84" />

<!-- Remplace "ton_lien_gif.gif" par ton lien imgur/drive direct -->

## Notes
Probable conflit de gestion WebSocket / état de session sur Edge. Facebook semble mal gérer les requêtes simultanées story + chat ou la perte de focus quand les deux modules sont actifs dans le même contexte de navigation.
