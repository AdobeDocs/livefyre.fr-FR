---
description: Permet aux utilisateurs de cliquer sur Collections à partir d’une seule mise en page et d’une seule URL de page.
title: Modifier la collection
exl-id: 5ddae18f-0279-457d-ae02-85e24fe81150
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Modifier la collection {#change-collection}

Permet aux utilisateurs de cliquer sur Collections à partir d’une seule mise en page et d’une seule URL de page.

Utilisez le délégué Modifier la collection pour modifier la collection affichée sur une page, sans modifier l’URL, pendant qu’une application Livefyre est déjà chargée. Utilisez cette fonction pour afficher des galeries de photos ou de vidéos ou d’autres applications dans lesquelles la collection affichée doit changer après une action de l’utilisateur.

Par exemple, un clic sur une vidéo ou une photo dans une galerie charge une collection spécifique à cette sélection, tandis que l’URL de la page ne change pas.

Pour [charger l&#39;une des trois collections à partir d&#39;une seule page](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count) :

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
