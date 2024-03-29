---
description: Événements disponibles auxquels vous pouvez lier JavaScript pour les applications de conversation (par exemple, Comments, Chat, Live Blog, Reviews et Sidenotes).
title: Événements JavaScript pour les applications de conversation
exl-id: 2497346e-b2cc-44b2-bcd9-906dd443fe38
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 73%

---

# Événements JavaScript pour les applications de conversation{#javascript-events-for-conversation-apps}

Événements disponibles auxquels vous pouvez lier JavaScript pour les applications de conversation (par exemple, Comments, Chat, Live Blog, Reviews et Sidenotes).

## Matrice des applications et des Événements de conversation {#section_y4j_x4m_ybb}

Voici une matrice des événements disponibles pour les applications de conversation. Un X indique que le événement est disponible pour l’application, S/O indique que le événement ne s’applique pas à l’application et qu’aucun marquage ne signifie que le événement n’est pas disponible pour cette application :

### Événements d’application de conversation

| Requête  | Commentaires | Chat | Liveblog | Critiques | Sidenotes | Sondages | Suivi des tendances |
|---|---|---|---|---|---|---|---|
| Init | X | X | X | X | X |  |  |
| Load | X | X | X | X |  |  |  |
| Affichage | X | X | X | X |  |  |  |
| Publication | X | X | X | X |  | N/D | N/D |
| Publié | X | X | X | X | X | N/D | N/D |
| Réponse Twitter | X | X | X | N/D | N/D | N/D | N/D |
| Twitter Like | X | X | X | N/D | N/D | N/D | N/D |
| LF | X | X | X | X | N/D | N/D | N/D |
| LF | X | X | X | X | N/D | N/D | N/D |
| Partager sur publication | X | X |  | X | N/D | N/D | N/D |
| Bouton Partager | X | X | X | X |  | N/D | N/D |
| Partager Twitter | X | X | X | X | X | N/D | N/D |
| Partager Facebook | X | X | X | X | X | N/D | N/D |
| URL de partage | X | X | X | X |  | N/D | N/D |
| DévelopperRéponses | X | S.O. | X | X | N/D | N/D | N/D |
| Réduire les réponses | X | S.O. | X | X | N/D | N/D | N/D |
| Bouton Indicateur | X | X | X | X | N/D | N/D | N/D |
| Marquer d’un indicateur | X | X | X | X | X | N/D | N/D |
| Annuler l&#39;indicateur | X | X | X | X | N/D | N/D | N/D |
| S’abonner | X | S.O. | X | X | N/D | N/D | N/D |
| Annuler | X | S.O. | X | X | N/D | N/D | N/D |
| RequestMore | X | X | X | X | N/D | N/D | N/D |
| ModalView |  | N/D | N/D | N/D | N/D | N/D | N/D |
| Retweet twitter | X | X | X | N/D | N/D | N/D | N/D |
| Bouton Publication | N/D | N/D | N/D | N/D | N/D | N/D | N/D |
| Nombre de commentaires mis à jour | X | X | X | X | N/D | N/D | N/D |
| Utilisateur connecté |  |  |  |  |  | N/D | N/D |
| Utilisateur déconnecté |  |  |  |  |  | N/D | N/D |
| Commentaires présentés |  | N/D |  |  | N/D | N/D | N/D |
| Commentaire non présenté |  | N/D |  |  | N/D | N/D | N/D |
| Commentaire voté | N/D | N/D | N/D | X | X | N/D | N/D |
| Sondage | N/D | N/D | N/D | N/D | N/D |  | N/D |
| Élément de tendance sélectionné | N/.A | N/D | N/D | N/D | N/D | N/D |  |
| ID réseau |  |  |  |  |  |  |  |
| ID application | X | X | X | X |  |  |  |
| ID de contexte | X | X | X | X |  |  |  |
| Type d’application | X | X | X | X |  |  |  |
| Type de contenu | X | X | X | X |  |  |  |
| Date de publication dans l’application |  |  |  |  |  |  |  |
| Connecté à l’application destinée aux utilisateurs finaux |  |  |  |  |  |  |  |
