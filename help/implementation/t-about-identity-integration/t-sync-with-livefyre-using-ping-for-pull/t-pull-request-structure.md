---
description: Générez la structure de demande d'extraction pour recevoir et répondre
  aux demandes d'accès à votre système d'identité utilisateur.
seo-description: Générez la structure de demande d'extraction pour recevoir et répondre
  aux demandes d'accès à votre système d'identité utilisateur.
seo-title: Extraire la structure de demande
solution: Experience Manager
title: Extraire la structure de demande
uuid: bf 6 b 9 e 45-d 08 a -48 e 6-acc 6-e 4 fa 56428 d 25
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Extraire la structure de demande{#pull-request-structure}

Générez la structure de demande d'extraction pour recevoir et répondre aux demandes d'accès à votre système d'identité utilisateur.

Livefyre envoie une demande de pull à votre URL de endpoint de fin.

Par exemple, si l'URL de endpoint de fin Pull est :

```
https://example.yoursite.com/some_path/?id={id}
```

La demande Pull Livefyre à ce point de fin sera :

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

où `lftoken` est un jeton Web JSON signé avec votre clé réseau. **[!UICONTROL {userAuthToken}]** Il s'agit du jeton authentique de l'utilisateur généré par Livefyre.

1. Servez-vous `lftoken` de cette option pour vérifier que les requêtes à votre Ping pour l'URL d'extraction ont été envoyées par Livefyre et non par un agent malveillant.
1. Pour toutes les requêtes entrantes :

   * Vérifiez que la chaîne `lftoken` de requête est présente dans la requête.
   * Utilisez `validateLivefyreToken` la méthode dans les bibliothèques Livefyre pour vérifier que `lftoken` celle-ci a été signée avec votre clé réseau.

   * Si `lftoken` le paramètre est absent ou échoue, n'autorisez pas votre point de fin à répondre aux informations de profil. Répondez plutôt à un code d'état 403 (Interdit) et sans corps de réponse.

1. `userAuthToken` est générée par la méthode Livefyre `buildUserAuthToken` pour l'utilisateur, avec user - id « system ». Cet utilisateur est le premier utilisateur créé pour chaque nouveau réseau.
1. Pour tester votre page, utilisez le [test Ping pour pull](https://livefyre-p4p-wizard.herokuapp.com/home) pour vérifier que tout fonctionne comme prévu.