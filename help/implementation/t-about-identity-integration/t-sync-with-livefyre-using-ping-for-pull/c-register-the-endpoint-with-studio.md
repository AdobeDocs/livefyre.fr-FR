---
description: Enregistrez le point de terminaison de l’URL afin que Livefyre puisse utiliser l’URL pour extraire les informations de profil mises à jour.
title: Enregistrement du point de terminaison avec Studio
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Enregistrer le point de terminaison avec Studio{#register-the-endpoint-with-studio}

Enregistrez le point de terminaison de l’URL afin que Livefyre puisse utiliser l’URL pour extraire les informations de profil mises à jour.

Enregistrez l’URL Ping for Pull une seule fois par réseau. Une fois définie, cette valeur ne doit pas changer, à moins que le point de terminaison de la récupération des données de profil utilisateur de votre système de gestion des utilisateurs ne change.

1. Utilisez Studio pour enregistrer ce point de terminaison d’URL auprès de Livefyre.
1. Enregistrez l’URL à partir de laquelle Livefyre récupérera les informations de profil d’utilisateur mises à jour, accédez à **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**, puis saisissez-la dans le champ **[!UICONTROL Ping for Pull URL]**.

   Par exemple, l’URL peut se présenter comme suit : `https://example.yoursite.com/some_path/?id={id}`
