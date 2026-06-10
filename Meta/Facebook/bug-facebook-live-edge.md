# Rapport de bug - Facebook Live

## Titre du problème
Les commentaires Facebook Live n'apparaissent pas sur Microsoft Edge - nouvelle interface

## Environnement
- **Plateforme** : www.facebook.com
- **Produit** : Vidéo en direct / Facebook Live
- **Navigateur** : Microsoft Edge
- **OS** : Windows
- **Date/Heure** : 10 juin 2026, ~20h00 GMT+2
- **Interface** : Nouvelle UI Facebook

## Description du bug
Sur Facebook Live avec la nouvelle interface, la section "Commentaires" reste vide même quand des commentaires existent.

### Comportement observé
1. Le compteur de commentaires affiche un nombre > 0, ex: `8`
2. La section "Affiché précédemment" avec les produits/épinglés s'affiche normalement
3. Aucun commentaire utilisateur n'apparaît dans la liste
4. Le bouton "Masquer les commentaires" / "Afficher les commentaires" n'a aucun effet
5. Le problème persiste après `F5`, hard refresh `Ctrl + Shift + R`, et vidage du cache

## Étapes pour reproduire
1. Ouvrir Microsoft Edge sur Windows
2. Se rendre sur `www.facebook.com`
3. Lancer une vidéo Live qui a des commentaires actifs
4. Observer la section "Commentaires"
5. Résultat : seuls "Affiché précédemment" et le champ "Écrivez un commentaire..." sont visibles

## Comportement attendu
Les commentaires utilisateurs doivent s'afficher sous la section "Affiché précédemment", avec possibilité de scroll et d'interaction.

## Contournement fonctionnel
1. Dézoomer la page à 90% ou 80% avec `Ctrl + -`
2. Rafraîchir avec `F5`
3. Les commentaires réapparaissent et restent visibles

## Notes supplémentaires
- Le bug n'existe pas sur `mbasic.facebook.com` ou `m.facebook.com`
- Le bug semble lié au calcul de la hauteur du bloc commentaires à 100% de zoom sur Edge
- Extensions de navigateur désactivées : le bug persiste
- Navigation InPrivate : le bug persiste

## Impact
Impossible de lire ou d'interagir avec les commentaires en live sans manipulation. L'expérience Live communautaire est cassée.

## Pièces jointes
1. `screenshot-1.png` : Vue avec compteur "8" commentaires mais section vide
2. `screenshot-2.png` : Vue rapprochée montrant uniquement "Affiché précédemment" et épinglés
