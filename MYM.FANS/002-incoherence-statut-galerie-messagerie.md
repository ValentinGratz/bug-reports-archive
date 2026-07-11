# Bug 002 - Incohérence du statut de connexion entre la galerie privée et la messagerie

## Plateforme
MYM (mym.fans)

## Catégorie
Synchronisation des données / Interface utilisateur

## Description du problème

Le statut de connexion d'un créateur peut être différent selon la section consultée.

La galerie privée et la messagerie semblent afficher des informations différentes concernant la présence du créateur.

## Étapes pour reproduire

1. Ouvrir une conversation avec un créateur.
2. Consulter son statut de connexion dans la messagerie.
3. Accéder ensuite à sa galerie privée.
4. Comparer les informations affichées.

## Résultat attendu

Toutes les parties de la plateforme devraient afficher un statut de connexion identique et synchronisé.

## Résultat constaté

Exemple :

- Messagerie : "Connecté il y a plusieurs heures"
- Galerie privée : créateur indiqué comme connecté

Les informations affichées ne correspondent pas.

## Impact utilisateur

Cela crée une confusion sur l'activité réelle du créateur et réduit la confiance dans la fiabilité des indicateurs de présence.

## Fréquence

Observé régulièrement depuis plusieurs années.

## Hypothèse technique

Possible différence de synchronisation entre les différents services de la plateforme :
- messagerie ;
- profil créateur ;
- galerie privée.
