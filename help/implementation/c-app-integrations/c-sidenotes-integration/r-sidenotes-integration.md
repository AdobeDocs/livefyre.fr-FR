---
description: Intégration d'une application Sidenotes en suivant un processus semblable
  aux applications principales.
seo-description: Intégration d'une application Sidenotes en suivant un processus semblable
  aux applications principales.
seo-title: Intégration des balises
solution: Experience Manager
title: Intégration des balises
uuid: 4 aa 14 ada -402 a -482 d-b 43 e -96 f 37 afa 6 c 53
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Intégration des balises{#sidenotes-integration}

Intégration d'une application Sidenotes en suivant un processus semblable aux applications principales.

En règle générale, si l'intégration de l'application principale est terminée, le code écrit pour générer l `collectionMeta` 'objet peut être réutilisé pour les caractères annexes.

Vous pouvez également réutiliser vos `auth` délégués existants en fournissant `auth` un délégué créé `fyre.conv` avec les caractères annexes dans `authDelegate` le champ (facultatif).

>[!NOTE]
>
>Les balises sidenotes vous permettent d'inclure `network`, `siteId`et `articleId` dans un seul objet, plutôt que de les transmettre séparément dans d'autres parties du constructeur.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Comme indiqué dans `collectionMeta` la section Building, `collectionMeta` est un objet JSON codé. Dans l'exemple ci-dessus, l'objet JSON adopte le format suivant avant son codage JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Pour plus d'informations, consultez le `collectionMeta` jeton.

## Configuration mobile

Les commentaires de sidenotes ont été optimisés pour les périphériques mobiles. Pour obtenir de meilleurs résultats avec les versions mobiles de votre application Livefyre, définissez l'option évolutive sur non. Par exemple :

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```