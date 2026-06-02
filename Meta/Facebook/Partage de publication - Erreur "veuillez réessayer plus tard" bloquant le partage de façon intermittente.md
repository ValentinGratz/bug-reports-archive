# Bug : Facebook - Partage de publication - Erreur "veuillez réessayer plus tard" bloquant le partage de façon intermittente

## Reproduction
- Fréquence : Intermittent - taux ~60% sur 48h de tests. Apparaît par vagues, souvent résolu après 2-24h
- Navigateur / OS : Chrome 125.0.0.0 / Android 14 + Firefox 126 / Windows 11 + App Facebook iOS 510.0

## Symptôme
Décrire le comportement observé :
- UI impactée : Bouton "Partager" sur posts fil d’actualité, groupes, pages. Modal de partage + publication story/reel
- Action utilisateur : Clic sur "Partager maintenant" ou "Partager dans un groupe" -> toast d’erreur instantané "veuillez réessayer plus tard" ou "Vous ne pouvez pas utiliser cette fonctionnalité pour le moment". Le post n’est pas publié. Aucun brouillon créé

## Console / Réseau
- JS errors : Aucune erreur bloquante visible côté client sur web. Erreur catchée silencieusement
- Network / WebSocket : Requête POST `https://www.facebook.com/api/graphql/` retourne `error 500` ou `errorSummary: "Please try again later"` avec `errorCode: 368`. WebSocket stable

## Tests effectués
- Cache vidé : oui
- Navigation privée : oui
- Extensions désactivées : oui
- Autre appareil testé : oui - Android + iOS + Desktop
- Résultat : Bug persistant sur tous les environnements. Changement Wi-Fi <-> 4G sans effet. Facebook Lite donne le même résultat. Seul facteur qui corrige : attendre plusieurs heures

## Apparition du bug
- Depuis : Pic d’occurrences signalé entre avril et juin 2026 sur groupes FR. Bug récurrent depuis mai 2024 mais aggravé Q2 2026【6135097223510253675†L11-L12】
- Contexte (update / changement / etc.) : Corrélé aux déploiements serveur de Meta. Pas lié à une MAJ appli spécifique. Utilisateurs non restreints impactés【6135097223510253675†L26-L27】

## Impact
- Utilisateurs concernés : Ensemble des utilisateurs Facebook, comptes non sanctionnés inclus. Signalements massifs FR/EU/US【post-028502794050151195253】
- Gravité : P2 - Fonction majeure dégradée mais contournement = attendre. Pas de perte de données
- Conséquence : Impossibilité de partager du contenu UGC, impact pages créateurs, community managers et groupes. Frustration utilisateur + perte d’engagement organique

## Identifiants (optionnel)
- User ID :
- URL / Live ID : `https://www.facebook.com/` - tous types de posts : texte, image, reel, lien

## Hypothèse (optionnel)
Possible cause : Rate limiting trop agressif côté serveur ou défaillance du service `ShareComposerMutation`. Code 368 correspond à "Temporary block" mais déclenché à tort sur comptes clean. Peut être lié à une saturation des files de publication ou bug dans le feature flag `sharing_story_v2`
