## Bug : Facebook Web - Stories + Messenger - Crash de la story lors de l'envoi d'un message

**Repro**  
Systématique sur Microsoft Edge dernière version / Windows 10/11

**Symptôme**  
Une story est ouverte en plein écran sur facebook.com. Si j'ouvre le chat Messenger dans le même onglet/fenêtre et que j'envoie un message, la story se ferme immédiatement et affiche un écran d'erreur à la place du contenu.

**Message d'erreur exact affiché**  
`Impossible d’afficher la story`  
`Veuillez réessayer.`

**Console**  
À vérifier - probable erreur réseau/WebSocket type `ERR_ABORTED` ou `story_unavailable` au moment de l'envoi du message

**Testé**  
- Navigation privée testée
- Extensions désactivées
- Bug non présent si Messenger est ouvert dans un onglet séparé
- Non reproduit sur Chrome / Firefox

**Début**  
Depuis 2-3 semaines environ

**Impact**  
Utilisateurs Edge qui multitask Stories + Messenger. Conséquence : interruption de visionnage, frustration, perte de contexte. Impossible de commenter une story en DM sans la perdre.

**User ID touché**  
`optionnel`

**ID du Live / URL**  
`https://facebook.com/stories` + chat Messenger intégré

**Notes**  
Les 2 bugs semblent liés à la gestion des WebSocket / état de session sur Edge. Facebook semble mal gérer le focus ou les requêtes simultanées story + chat sur ce navigateur.
