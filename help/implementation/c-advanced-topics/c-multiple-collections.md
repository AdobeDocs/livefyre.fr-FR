---
description: Présente plusieurs collections sur une seule page.
title: Collections multiples
exl-id: 748b6ca6-635e-4bae-9b95-cfbd4651751f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 1%

---

# Collections multiples {#multiple-collections}

Présente plusieurs collections sur une seule page.

Vous pouvez inclure plusieurs collections sur une seule page de votre site. Par exemple, pour publier un événement, vous pouvez avoir un blog en direct ou une discussion en ligne pendant le événement, avec une application distincte sur le côté de votre page, affichant le contenu traité associé sur le Web social. Vous pouvez également inclure une application de commentaires sous un article, avec une discussion sur le côté.

Pour obtenir plusieurs conversations sur une page, ajoutez une ou plusieurs configurations dans une baie et transmettez la baie à l&#39;appel de chargement. Par exemple.

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
