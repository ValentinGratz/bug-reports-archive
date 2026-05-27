# Bug: Facebook Web - Stories sautent et éléments mélangés sur Edge

## Résumé
Sur facebook.com avec Microsoft Edge, les stories sautent automatiquement à l’ouverture et les éléments à l’intérieur d’une même story ne sont pas dans l’ordre chronologique.

## Environnement
- **Plateforme :** Facebook Web
- **Navigateur :** Microsoft Edge
- **OS :** Windows 10/11
- **Date du test :** 27 mai 2026

## Étapes pour reproduire
1. Ouvrir facebook.com sur Microsoft Edge
2. Cliquer sur une story en haut du fil d’actualité
3. Observer le comportement

## Comportement observé
1. La story saute directement ou passe à la suivante toute seule dès l’ouverture
2. À l’intérieur d’une même story, les photos et vidéos sont mélangées et ne respectent pas l’ordre de publication
3. Impossible de voir une story complète dans le bon ordre

## Comportement attendu
1. La story devrait s’ouvrir sur le premier élément et rester dessus
2. Les éléments d’une story devraient défiler dans l’ordre chronologique de publication

## Logs Console
Aucune erreur bloquante

> Note : Remplacer par les erreurs JS si présentes. F12 > Console

## Tests effectués
- [x] Cache vidé
- [x] Navigation privée testée
- [x] Extensions désactivées
- [x] Fonctionne normalement sur l’app Facebook mobile Android/iOS
- [ ] Testé sur Chrome/Firefox

## Début du problème
Depuis le ___

## Impact
Toutes les stories sont illisibles sur Facebook Web Edge. Contournement : utiliser l’app mobile.

## Liens
- URL concernée : https://facebook.com
- User ID :

## Captures
Ajouter screenshot ou enregistrement d’écran du bug ici
