---
description: Renvoie un nouvel objet Site.
title: getSite Network, méthode
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# getSite Network Method{#getsite-network-method}

Renvoie un nouvel objet Site.
|Variable|Type|Description|
|— |— |— |
|siteId|String|ID fourni par Livefyre pour le site Web ou l&#39;application auquel appartient la collection. Par exemple : 303617.  |
|siteKey|String|Clé secrète fournie par Livefyre pour siteId.  |

## Exemple Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Exemple NodeJS {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## Exemple PHP {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Exemple Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Exemple Ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```
