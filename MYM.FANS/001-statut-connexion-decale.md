# Bug 001 - Statut de connexion incorrect après réception d'un message

## Plateforme
MYM (mym.fans)

## Catégorie
Présence utilisateur / Synchronisation du statut

## Description du problème

Lorsqu'un créateur envoie un message privé, le statut de connexion affiché sur son profil ou dans la messagerie peut être incorrect.

Le créateur vient d'effectuer une action (envoi d'un message), mais l'interface continue d'afficher un ancien statut de connexion comme par exemple :

> "Connecté il y a 3h"

alors que l'activité vient d'avoir lieu.

## Étapes pour reproduire

1. Attendre qu'un créateur envoie un nouveau message privé.
2. Consulter le statut de connexion affiché.
3. Comparer l'heure du message reçu avec l'indication de présence.

## Résultat attendu

Le statut de connexion devrait être mis à jour après une activité récente du créateur.

Exemple :
- Message envoyé à 15h00
- Statut attendu : "Connecté récemment" ou une information cohérente.

## Résultat constaté

Le statut reste parfois bloqué sur une ancienne information :

- Message reçu récemment.
- Statut affiché : "Connecté il y a plusieurs heures".

## Impact utilisateur

Ce comportement peut donner une information erronée au fan concernant l'activité réelle du créateur.

## Fréquence

Observé régulièrement depuis plusieurs années.

## Date du premier constat

Problème observé depuis longtemps (plusieurs années).
