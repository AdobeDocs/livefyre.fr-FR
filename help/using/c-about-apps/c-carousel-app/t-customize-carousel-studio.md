---
description: Modifiez les options de taille, de largeur et d’interaction de l’application Carrousel.
title: Personnalisation d’un carrousel à l’aide de Studio
exl-id: f6f681ac-c601-40b9-9e99-bf5495f505f8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Personnalisation d’un carrousel à l’aide de Studio{#customize-a-carousel-using-studio}

Modifiez les options de taille, de largeur et d’interaction de l’application Carrousel.

Toutes les applications utilisent les options **[!UICONTROL Style]** et **[!UICONTROL Config]** dans **[!UICONTROL App Designer]**. Voir Personnalisation des applications pour en savoir plus sur les options **[!UICONTROL Style]** et **[!UICONTROL Config]** standard pour toutes les applications dans le **[!UICONTROL App Designer]**.

Vous pouvez personnaliser un carrousel à l’aide des options supplémentaires suivantes dans App Designer :

* **[!UICONTROL Max Number of Items]**

   Définit le nombre d’éléments à afficher dans le carrousel. La valeur par défaut est 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Pour les écrans d’ordinateur uniquement

   * Si le contenu dépasse 600 pixels, s’affiche horizontalement.
   * Si le contenu est inférieur à 600 pixels, s’affiche verticalement.
   * **Vertical.** Pour les écrans d’ordinateur ou les périphériques mobiles. Sur les périphériques mobiles, la carte se rétrécit pour s’adapter à la taille de l’écran.

* **[!UICONTROL Call-to-action button]** Vous pouvez utiliser le bouton Appel à l’action avec un catalogue de produits pour diriger les utilisateurs vers un produit ou vers votre site pour toute action ultérieure.

   * **[!UICONTROL Call-to-action button]** Activez la bascule pour afficher le bouton d’appel à l’action.
   * **[!UICONTROL Require rights to display products]** Activez cette option pour que le propriétaire du contenu ait accordé des droits sur le contenu avant qu’un bouton d’appel à l’action ne s’affiche pour le contenu.

   >[!NOTE]
   >
   >Le contenu s’affiche même si des droits ne sont pas accordés pour le contenu, mais le bouton d’appel à l’action ne s’affiche pas avec le contenu à moins que des droits pour le contenu ne soient accordés.

   * **[!UICONTROL Show call-to-action in tile]**. Choisissez d&#39;afficher le bouton d&#39;appel à l&#39;action sur une mosaïque au lieu d&#39;afficher le bouton d&#39;appel à l&#39;action uniquement lorsque le visiteur du site clique sur une carte et ouvre le contenu dans une fenêtre plus grande.
   * **[!UICONTROL Call-to-action indication text]** Texte à afficher pour inviter l’utilisateur à cliquer sur la carte pour ouvrir le module d’appel à l’action.
   * **[!UICONTROL Call-to-action header text]** Mots à afficher dans l’en-tête au-dessus du bouton Appel à l’action dans le module de contenu. Le texte par défaut est &quot;Acheter ces produits :&quot;.
   * **[!UICONTROL Call-to-action button text]** Mots à afficher dans le bouton Appel à l’action du module de contenu. Le texte par défaut est &quot;Acheter maintenant :&quot;.
   * **[!UICONTROL Product display options]** Indiquez si vous souhaitez afficher le  **[!UICONTROL Photo]** et le  **[!UICONTROL Product name]** avec le bouton Appel à l&#39;action.

   >[!NOTE]
   >
   >Les boutons Photo et Nom du produit apparaissent en bleu lorsqu’ils sont activés.

   * **[!UICONTROL Product URL referral tracking]** Basculez la bascule sur Activé pour effectuer le suivi des références depuis cette application vers la page de produits associée.
   * **[!UICONTROL Referral tracking key-value pairs]** Ajoutez des paramètres pour spécifier davantage le suivi des références à partir du contenu de votre application vers la page de produits associée.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Sélectionnez cette option pour créer une application pour plusieurs pages de produits. Filtrez l’UGC spécifique à chaque produit dans l’application pour chaque page de produit. Vous pouvez sélectionner un ou plusieurs dossiers pour associer des collections spécifiques à l’application.
   * **[!UICONTROL Select Product folders]**. Sélectionnez les dossiers de produits de niveau supérieur à utiliser pour filtrer les fichiers UGC. Utilisez CTRL/Commande + clic pour sélectionner plusieurs dossiers. Livefyre utilise ce dossier pour déterminer les produits qu’il contient à afficher dans l’application sur différentes pages.
   * **[!UICONTROL Show related content]**. Activez cette option pour afficher le contenu publié sur l’application, mais balisé avec un autre ID de produit. Une fois que le contenu spécifique à un produit pour l’application s’affiche, Livefyre affiche le contenu pour d’autres produits et le contenu qui n’est pas associé à un produit. Livefyre donne d’abord la priorité au contenu avec le même ID de produit, puis au contenu publié sur l’application avec d’autres ID de produit, puis au contenu publié sur l’application sans ID de produit.
