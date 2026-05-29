## Bug : Facebook Web - Stories - Replay depuis le début au lieu des nouvelles stories

**Repro**  
Intermittent sur Microsoft Edge dernière version / Windows 10/11

**Symptôme**  
Après avoir visionné 100% des stories d’un utilisateur, si ce dernier poste de nouvelles stories, cliquer sur sa bulle relance la lecture depuis la première story de la journée. Les stories déjà vues ne sont pas skippées. Oblige à tap/clic plusieurs fois pour atteindre le nouveau contenu.

**Console**  
Aucune erreur bloquante

**Testé**  
- Cache vidé + hard refresh
- Navigation privée  
- Extensions désactivées
- Non reproduit sur Chrome / Firefox / App mobile
- Le bug n’apparaît pas à chaque fois

**Début**  
Depuis plusieurs semaines. Non lié à une MAJ Edge ou Facebook identifiée.

**Impact**  
Utilisateurs Facebook Web sur Edge. Conséquence : friction UX, perte de temps, baisse d’engagement sur les stories récentes car l’utilisateur abandonne avant d’arriver aux nouvelles.

**User ID touché**  
`optionnel`

**ID du Live / URL**  
`https://facebook.com/stories` - concerne tous les profils
