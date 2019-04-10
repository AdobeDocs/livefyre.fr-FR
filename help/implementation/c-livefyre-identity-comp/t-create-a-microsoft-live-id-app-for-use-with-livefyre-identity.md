---
description: Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity pour
  permettre aux utilisateurs d'utiliser leurs identifiants Facebook pour interagir
  avec les applications sur votre site.
seo-description: Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity
  pour permettre aux utilisateurs d'utiliser leurs identifiants Facebook pour interagir
  avec les applications sur votre site.
seo-title: Création d'une application d'identité Microsoft Live pour une utilisation
  avec Livefyre Identité
solution: Experience Manager
title: Création d'une application d'identité Microsoft Live pour une utilisation avec
  Livefyre Identité
uuid: 0 c 13 e 1 bc -817 f -43 ed -85 d 5-09 c 9 e 95 b 6234
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Création d'une application d'identité Microsoft Live pour une utilisation avec Livefyre Identité{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Vous pouvez utiliser Livefyre Identity avec Microsoft Live Identity pour permettre aux utilisateurs d'utiliser leurs identifiants Facebook pour interagir avec les applications sur votre site.

Pour permettre aux utilisateurs de se connecter avec leurs informations d'identification Microsoft Live Identity, Livefyre requiert les informations d'identité Microsoft Live suivantes :

* ID du client (clé privée)
* Secret client (mot de passe)

Pour créer une application Microsoft Live Identity à utiliser avec Livefyre Identity :

1. Créez ou connectez-vous à un compte Microsoft Live à l'adresse [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Créez ou sélectionnez une application existante pour l'utiliser avec Livefyre Identity.
1. Cliquez sur **[!UICONTROL Add Platform]**, puis sélectionnez Web comme type de plate-forme.
1. Assurez-vous que l **[!UICONTROL Allow Implicit Flow]** 'option est cochée et saisissez l'URL de redirection en utilisant le nom du réseau plutôt que {network-name} : `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Générez une nouvelle paire de mots de passe/clé pour obtenir la clé privée.
1. Dans **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, basculez sur **[!UICONTROL Enable Microsoft Live Login]****[!UICONTROL On]**la bascule.
1. Saisissez l'ID de client Microsoft Live et la clé secrète client Microsoft Live.
1. Cliquez **[!UICONTROL Save Settings]**sur.

Une fois l'opération terminée, la page Détails de l'application de Microsoft Live Identity répertorie l'ID client de l'application (clé Consumer Key) et la clé secrète client (clé secrète Consumer) à utiliser dans la page Paramètres d'intégration de Studio.