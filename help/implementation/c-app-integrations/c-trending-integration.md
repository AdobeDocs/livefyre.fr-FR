---
description: Présentez les collections les plus actives sur votre site ou réseau.
seo-description: Présentez les collections les plus actives sur votre site ou réseau.
seo-title: Tendances
solution: Experience Manager
title: Tendances
uuid: 3031523 d-b 487-4 eee-bba 6-5 d 8 f 9971874 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Tendances{#trending}

Présentez les collections les plus actives sur votre site ou réseau.

Utilisez les tendances pour présenter les collections avec l'activité la plus récente de votre site ou réseau.

## Analytics{#section_wtz_whb_c1b}

La méthode la plus rapide pour intégrer les tendances est d'utiliser la version construite hébergée sur le CDN Livefyre.

Ajoutez d'abord [Livefyre. js](https://github.com/Livefyre/Livefyre.js) à votre page.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionnez ensuite l'élément dans lequel l'application apparaîtra.

```
<div id="trending"></div>
```

Enfin, utilisez `Livefyre.require` pour construire le composant.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

Vous disposez maintenant d'une application de tendance. Reportez-vous à l'exemple suivant dans [cet exemple](https://codepen.io/gobengo/pen/GijEy).

## Configuration {#section_k5k_qhb_c1b}

`network`

Réseau d'où les collections seront extraites. (Obligatoire.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Indiquez l'ID du site pour afficher les collections uniquement à partir d'un seul site sur votre réseau. (Facultatif)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Fournissez une balise Collection unique pour n'afficher que les collections avec cette balise. (Facultatif)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```
