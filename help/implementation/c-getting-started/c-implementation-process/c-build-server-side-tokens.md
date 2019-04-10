---
description: Guide de création de collectionmeta et de jetons authentiques.
seo-description: Guide de création de collectionmeta et de jetons authentiques.
seo-title: Création de jetons côté serveur
solution: Experience Manager
title: Création de jetons côté serveur
uuid: 8313 f 26 e -5 ceb -414 e-a 61 a -480 bb 7 a 8 ba 66
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Création de jetons côté serveur{#build-server-side-tokens}

Guide de création de collectionmeta et de jetons authentiques.

La création des jetons utilisés par Livefyre pour valider les requêtes garantit que vous seul pouvez effectuer des mises à jour sur votre réseau Livefyre.

## Collectionmeta Token

Découvrez comment créer un jeton pour créer des conversations et afficher des conversations existantes.

## Jeton authentique

Découvrez comment créer un jeton pour authentifier les utilisateurs, étape nécessaire au processus d'intégration si vous n'utilisez pas Janrain Capture pour la gestion des utilisateurs.

## Jeton authentique utilisateur {#section_l5l_hwt_bbb}

Cette section décrit comment générer l'objet JSON userauth qui crée le jeton d'authentification utilisateur requis pour enregistrer les utilisateurs dans vos applications.

Pour créer le jeton, utilisez votre bibliothèque de langue préférée pour transmettre les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| Networkname | Chaîne *requise* | nom du réseau Livefyre (fourni par Livefyre). |
| Networkkey | Chaîne *requise* | Clé secrète de ce réseau spécifique (fourni par Livefyre). |
| Userid | Chaîne *requise* | L'ID de l'utilisateur connecté est stocké dans le système de gestion des utilisateurs (seuls les caractères alphanumériques, les tirets, les tirets bas et les points sont autorisés) : `[a-zA-Z0-9_-.]`). **Remarque :** L'ID utilisateur doit être unique. |
| expire | Entier *requis* | Date à laquelle le jeton doit expirer à partir de maintenant (en secondes). **Remarque :** Cette valeur peut également être transmise sous forme de virgule flottante. Le jeton Web JSON produit stockera cette valeur dans l'heure UNIX époque. |
| Displayname | Chaîne *requise* | Texte permettant d'identifier cet utilisateur dans l'interface utilisateur et dans les commentaires. (Nombre maximal de caractères : 50.) |
