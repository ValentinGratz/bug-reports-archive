# Bug : Facebook - Live - Affichage isolé des commentaires sur Microsoft Edge PC

## Reproduction
- Fréquence : Intermittent - se produit sur certains lives uniquement
- Navigateur / OS : Microsoft Edge / Windows 11

## Symptôme
Décrire le comportement observé :
- UI impactée : Fil de commentaires des vidéos Facebook Live
- Action utilisateur : Visionnage d'un live et consultation des commentaires en temps réel

Le compteur total de commentaires s'incrémente normalement au passage de la souris, mais seuls les commentaires postés par l'utilisateur s'affichent. Les commentaires des autres spectateurs n'apparaissent pas dans le flux. L'envoi de commentaires fonctionne correctement.

## Console / Réseau
- JS errors : Non vérifié
- Network / WebSocket : Non vérifié - connexion WebSocket des commentaires semble active car le compteur se met à jour

## Tests effectués
- Cache vidé : oui
- Navigation privée : oui  
- Extensions désactivées : oui - testé en navigation privée
- Autre appareil testé : non
- Résultat : Le bug persiste après vidage du cache, en navigation privée et avec extensions désactivées. Fonctionne correctement sur d'autres lives.

## Apparition du bug
- Depuis : Date inconnue - constaté le 27/05/2026
- Contexte (update / changement / etc.) : Aucun changement connu côté utilisateur. Le live précédent fonctionnait normalement, le suivant présente le bug.

## Impact
- Utilisateurs concernés : Utilisateurs sur Microsoft Edge / PC rencontrant le bug sur des lives spécifiques
- Gravité : P2 - Fonctionnalité majeure dégradée
- Conséquence : Impossibilité d'interagir avec la communauté du live. L'expérience de visionnage en direct est fortement réduite car l'aspect social disparaît.

## Hypothèse (optionnel)
Possible cause : Bug de rendu du composant de commentaires Facebook Live sous Edge. Possible désynchronisation du flux WebSocket ou filtrage côté client qui ne débloque que les messages de l'utilisateur. Le fait que cela fonctionne sur certains lives et pas d'autres suggère une condition liée aux paramètres de modération du live ou au volume de commentaires.
