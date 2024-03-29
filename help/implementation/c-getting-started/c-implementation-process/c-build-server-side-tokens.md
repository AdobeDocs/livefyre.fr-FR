---
description: Guide pour la création de jetons CollectionMeta et Auth.
title: Créer des jetons côté serveur
exl-id: f709b79e-9236-443e-b862-c7d281815d91
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# Créer des jetons côté serveur{#build-server-side-tokens}

Guide pour la création de jetons CollectionMeta et Auth.

La création des jetons utilisés par Livefyre pour valider les requêtes garantit que vous seul pouvez effectuer des mises à jour sur votre réseau Livefyre.

## CollectionMeta Token

Découvrez comment créer un jeton pour créer et afficher des conversations existantes.

## Jeton d’authentification

Découvrez comment créer un jeton pour authentifier les utilisateurs, étape nécessaire du processus d’intégration si vous n’utilisez pas Janrain Capture pour la gestion des utilisateurs.

## Jeton d&#39;authentification de l&#39;utilisateur {#section_l5l_hwt_bbb}

Cette section décrit comment générer l’objet JSON UserAuth qui crée le jeton d’authentification utilisateur requis pour connecter les utilisateurs à vos applications.

Pour créer le jeton, utilisez votre bibliothèque de langues préférée pour transmettre les paramètres suivants :

| Paramètre | Type | Description |
|---|---|---|
| networkName | Chaîne *requise* | Nom du réseau Livefyre (fourni par Livefyre). |
| networkKey | Chaîne *requise* | La clé secrète de ce réseau spécifique (fournie par Livefyre). |
| l’userID | Chaîne *requise* | ID de l’utilisateur se connectant tel qu’il est stocké dans votre système de gestion des utilisateurs (seuls les caractères alphanumériques, les tirets, les traits de soulignement et les points sont autorisés) : `[a-zA-Z0-9_-.]`). **Remarque :** l’ID utilisateur doit être unique. |
| expire | Entier *requis* | Date à laquelle le jeton doit expirer à partir de maintenant (en secondes). **Remarque :** Cette valeur peut également être transmise sous la forme d’un nombre flottant. Le jeton Web JSON produit stockera cette valeur dans l’époque UNIX. |
| displayName | Chaîne *requise* | Texte permettant d’identifier cet utilisateur dans l’interface utilisateur et dans les commentaires. (Nombre maximal de caractères : 50.) |
