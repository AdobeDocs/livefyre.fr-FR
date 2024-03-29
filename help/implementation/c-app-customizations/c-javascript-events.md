---
description: Événements disponibles auxquels vous pouvez lier JavaScript pour les applications de conversation (par exemple, Comments, Chat, Live Blog, Reviews et Sidenotes).
title: Définitions et exemples de Événements JavaScript
exl-id: 5b865974-69aa-4d51-ac26-60f1d8a114fc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 11%

---

# Définitions et exemples de Événements JavaScript{#javascript-events-definitions-and-examples}

Événements disponibles auxquels vous pouvez lier JavaScript pour les applications de conversation (par exemple, Comments, Chat, Live Blog, Reviews et Sidenotes).

Livefyre fournit des événements JavaScript pour suivre l’activité des utilisateurs dans vos applications Livefyre. Par exemple, vous pouvez mettre à jour la page lorsque les utilisateurs aiment ou partagent du contenu sur Twitter ou Facebook, ou lorsque du nouveau contenu est publié.

Livefyre vous permet également d’ajouter des événements à des intégrations d’analyses tierces (Adobe Analytics JS, Google Analytics, gestion dynamique des balises, etc.), afin d’effectuer le suivi des événements d’application. Pour plus d’informations, demandez à votre gestionnaire d’intégration tiers de fournir les événements appropriés.

Pour établir une liaison avec ces événements, ajoutez le code suivant à la page lors de l’instanciation de votre application sur une page. Remplacez le nom du événement par `{eventName}` :

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>Les objets de données sont fournis pour tous les gestionnaires de événement. Les exemples d’objets de données suivent chaque événement.

## commentPosted {#section_qfr_51p_xz}

Un utilisateur a publié un commentaire.

* Un parent dont la valeur est nulle est un nouveau commentaire.
* Un parent sur Aucun est un commentaire qui a été modifié.
* Un numéro pour parent est l’identifiant parent de la réponse.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## commentFlagged {#section_szy_s1p_xz}

Un utilisateur a marqué un commentaire.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

Un utilisateur a aimé un commentaire.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

Un utilisateur a partagé un commentaire du flux. (Ce événement ne se déclenche pas lorsque les utilisateurs partagent des commentaires depuis l’éditeur de commentaires.) Ce événement est déclenché lorsque l’utilisateur clique sur le bouton Partager.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdate {#section_qdq_f1p_xz}

Le nombre total de commentaires visibles dans cette conversation a changé (incrémenté ou décrémenté).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggingIn {#section_yjt_vz4_xz}

Un utilisateur s&#39;est connecté.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggingOut {#section_tsg_5z4_xz}

Un utilisateur s’est déconnecté.

les données ne sont pas définies.

## socialMention {#section_a1w_tz4_xz}

Un utilisateur a inclus une mention @dans un commentaire. Renvoie un tableau des éléments suivants :

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatured

Un utilisateur modérateur a présenté un commentaire. Renvoie un tableau des éléments suivants :

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

Le flux de commentaires a été chargé et l’ensemble initial de contenu a été récupéré du serveur et affiché à l’utilisateur.

les données ne sont pas définies.

## showMore {#section_pqg_nz4_xz}

Un utilisateur a cliqué sur le bouton **[!UICONTROL Show More]**.

les données ne sont pas définies.

## userSulowed {#section_xxw_jz4_xz}

Renvoie true lorsqu’un utilisateur clique sur le bouton **[!UICONTROL Follow]** et false lorsqu’un contenu est publié dans le flux.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnfollowed {#section_wm1_gz4_xz}

Renvoie true lorsqu’un utilisateur clique sur le bouton **Annuler le suivi** et false lorsqu’un contenu est publié dans le flux.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```
