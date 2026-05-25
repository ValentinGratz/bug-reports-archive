# WordPress Core Bug Archive: Ticket #65291

**Statut du ticket**: Reporter Feedback / Non-reproduit après test
**Lien Trac**: https://core.trac.wordpress.org/ticket/65291
**Date d'archive**: 25 mai 2026
**Doublon**: #65293 marqué comme doublon de ce ticket【4477836161245324751†L259-L260】

## 1. Résumé du bug

**Titre**: WordPress 7 – White screen when accessing posts and creating a new post
**Composant**: General
**Version concernée**: 7.0
**Sévérité**: Critical
**Milestone**: Awaiting Review
**Keywords**: reporter-feedback

Le passage à WordPress 7 provoque un écran blanc complet dans l’admin sur `Posts → All Posts` et `Posts → Add New`, rendant la gestion des articles impossible.

## 2. Description

### Symptôme
Après installation de WordPress 7, l’accès aux pages de gestion des articles affiche un écran blanc. Aucun contenu ne charge et l’éditeur n’apparaît pas.

### Étapes pour reproduire
1. Installer WordPress 7
2. Se connecter au tableau de bord admin WordPress
3. Aller dans `Articles → Tous les articles` ou `Articles → Ajouter`

### Résultat observé
La page devient complètement blanche. Aucun contenu n’est chargé et l’éditeur n’apparaît pas.

### Résultat attendu
La liste des articles et l’éditeur devraient se charger normalement sans erreurs.

## 3. Environnement

| Élément | Version |
| --- | --- |
| **WordPress** | 7.0 |
| **PHP** | 8.3.23 |
| **Serveur** | Apache 2.4.67 |
| **Thème** | Hestia 3.3.3 |
| **Plugins actifs** | Orbit Fox Companion, Rank Math SEO, Site Kit by Google, WP-Optimize, ManageWP, WP File Manager |

**Information additionnelle**: Le problème disparaît après retour à WordPress 6.9.4. Sans downgrade, tous les sites deviennent inutilisables.

## 4. Historique du ticket

### #1 - 4 days ago par @jorbin Core Committer
- Keywords `reporter-feedback` ajoutées
- Demande : "There is not enough information to make this actionable. If you switch to a default theme and disable all the plugins, does the issue persist? Is there anything in your error logs?"

### #2 - 4 days ago par @valentindu62
> Replying to jorbin:
>
> Actually, I just tried again, I switched to a twenty theme, then put Hestia back on, and I was able to successfully complete the update, and I no longer have any bugs (for the moment).

### #3 - 4 days ago par @jorbin Core Committer
- #65293 marqué comme doublon de ce ticket

## 5. Analyse technique

**Cause probable**: Conflit temporaire thème/plugin lors de la mise à jour vers WP 7.0. Le passage sur un thème Twenty puis retour à Hestia a résolu le problème, ce qui indique un souci de cache, d’option de thème, ou de compatibilité résolu par réactivation.

**Points à vérifier si réapparition**:
1. `error_log` PHP pour fatal error sur l’admin
2. Conflit avec Orbit Fox Companion - compagnon du thème Hestia
3. Incompatibilité Rank Math SEO / Site Kit avec WP 7.0 sur l’écran d’édition
4. `wp_options` corrompue pendant l’upgrade

**Fichiers potentiellement concernés**:
- `wp-admin/edit.php`
- `wp-admin/post-new.php`
- `wp-includes/script-loader.php` - chargement des assets de l’éditeur

## 6. Statut & suivi

| Date | Action | État |
| --- | --- | --- |
| Il y a 4 jours | Ticket ouvert par @valentindu62 | New |
| Il y a 4 jours | Demande d’infos par @jorbin | Awaiting Review |
| Il y a 4 jours | Reporter indique résolution après switch thème | reporter-feedback |
| Il y a 4 jours | #65293 fermé comme doublon | - |

**Statut actuel**: Non-reproductible par le reporter après changement de thème. En attente d’autres rapports. Pas de patch nécessaire pour l’instant.

**Tickets liés**: #65293 - Duplicate

## 7. Workaround validé

Si vous rencontrez un écran blanc sur WP 7.0 avec Hestia :

1. Activer un thème par défaut : `Twenty Twenty-Five`
2. Vérifier que `Posts → Add New` fonctionne
3. Réactiver Hestia 3.3.3
4. Vider tout cache : plugin + serveur + object cache

Le downgrade vers 6.9.4 résout aussi le problème mais n’est pas recommandé long terme.

## 8. Notes pour contributeurs

Si le bug réapparaît :
1. Récupérer les logs PHP : `define('WP_DEBUG_LOG', true);` dans `wp-config.php`
2. Tester avec tous plugins désactivés + thème Twenty
3. Vérifier la version d’Orbit Fox Companion - mettre à jour si < 2.26.0
4. Ouvrir un nouveau ticket seulement si reproductible sur install clean WP 7.0 + Twenty

---
**Archivé par**: @valentindu62
**Raison archive**: Suivi incident critique WP 7.0 sur parc client utilisant Hestia
**Action requise**: Monitor - Rouvrir si nouveaux cas remontent post WP 7.0.1


Fermé, car problème résolu, juste mettre un template de base comme "twenty-twenty", faire la mise à jour et remettre Hestia 
