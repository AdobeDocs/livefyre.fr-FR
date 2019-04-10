---
description: valeur nulle
seo-description: valeur nulle
seo-title: Courriels pour Livefyre Identité
solution: Experience Manager
title: Courriels pour Livefyre Identité
uuid: 4 e 807803-687 e -4 df 0-94 d 1-b 18 a 48 d 024 e 8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Courriels pour Livefyre Identité{#emails-for-livefyre-identity}

Livefyre Identity envoie les courriers électroniques suivants :

* [Adresse électronique de réinitialisation du mot de passe](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Adresse électronique de vérification](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Envoyer la vérification de courrier électronique pour les utilisateurs](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Courriel de bienvenue](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Envoyer un courriel de bienvenue aux utilisateurs](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Vous pouvez personnaliser l'aspect de tous les courriers électroniques d'identité Livefyre dans **[!UICONTROL Integration Settings > Email Notifications.]**

## Adresse électronique de réinitialisation du mot de passe {#section_nd1_whs_p1b}

Livefyre envoie automatiquement un courrier électronique de réinitialisation du mot de passe lorsqu'un utilisateur tente de réinitialiser son mot de passe.

L'adresse électronique de réinitialisation du mot de passe ressemble à ceci :

**Objet :** Réinitialiser le mot de passe

**Corps :**

Hey there *< username >*,

Une demande de modification du mot de passe de votre profil a été effectuée sur *< nom du réseau >*.

Si vous l'avez demandé, cliquez sur le lien suivant pour choisir un nouveau mot de passe : *< URL de réinitialisation du mot de passe >*.

*< Nom d'utilisateur >*, *< nom du réseau >*et *< URL de réinitialisation du mot de passe >* sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Adresse électronique de vérification {#section_ak5_xhs_p1b}

Vous pouvez envoyer un courriel vérifiant l'adresse électronique d'un utilisateur. Pour envoyer des courriers électroniques de vérification, vous devez activer l'option dans **Paramètres d'intégration > Identité Livefyre**.

L'adresse électronique de vérification ressemble à ceci :

**Objet :** Vérification de courrier électronique

**Corps :**

Hello *< username >*,

Cliquez sur le lien suivant (ou collez-le dans votre navigateur) pour vérifier votre compte : *< URL de vérification >*.

Ce lien expirera dans 24 heures.

Merci,

The *<customer name>* Team

*< Nom d'utilisateur >*, *< nom du réseau >*et *< URL de vérification >* sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Envoi d'une vérification par courrier électronique aux utilisateurs {#section_vyv_yhs_p1b}

Vous pouvez envoyer un courrier électronique à un utilisateur pour vérifier l'adresse électronique qu'il utilise pour s'inscrire à un compte. Pour envoyer un courriel de vérification :

1. Dans Studio, cliquez sur l'icône représentant un engrenage pour modifier les paramètres réseau.
1. Cliquez sur **Paramètres d'intégration > Identité Livefyre.**

1. Accédez aux types **de connexion**.
1. Cliquez **sur Exiger la vérification de courriel** pour envoyer un courrier électronique aux utilisateurs qui vérifient l'adresse électronique qu'ils utilisent pour s'inscrire à un compte.
1. Accédez à Courriel **réseau** pour configurer **le logo pour le courrier électronique**, l'adresse électronique à utiliser comme adresse électronique (**adresse électronique de)**et le nom d'affichage à utiliser pour l'adresse électronique de l'expéditeur (**nom d'affichage de courriel**).

## Courriel de bienvenue {#section_z2v_zhs_p1b}

Vous pouvez envoyer un courriel de bienvenue aux utilisateurs. Pour envoyer des e-mails de bienvenue, vous devez activer l'option dans **Paramètres d'intégration** > **Identité Livefyre**.

L'e-mail de bienvenue ressemble à ceci :

**Objet :** Bienvenue dans *< nom du client >*

**Corps :**

Hello *< username >*,

Un compte a été créé pour vous sur *< nom du client >*.

Ce compte a été créé sur *< URL de référence >* depuis l'adresse IP *< adresse IP >*.

Dans ce cas, vous pouvez ignorer ce message en toute sécurité.

Si vous n'avez pas effectué cette opération, veuillez contacter `support@livefyre.com`

Merci

The *"customer name"* Team

*« Nom d'utilisateur », « Nom du client », « URL de référence »* et « Adresse IP » sont tous générés dynamiquement en fonction du visiteur du site et de votre réseau.

## Envoyer un courriel de bienvenue à un utilisateur {#section_kjp_c3s_p1b}

Vous pouvez envoyer un courriel de bienvenue à un utilisateur après l'avoir inscrit à un compte. Studio envoie ce courrier électronique après l'envoi d'un courrier électronique de vérification, si vous avez configuré un courrier électronique de vérification. Pour envoyer un courriel de bienvenue :

1. Dans Studio, cliquez sur l'icône représentant un engrenage pour modifier les paramètres réseau.
1. Cliquez sur **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Accédez **[!UICONTROL Email Settings]**à.

1. Cliquez sur **[!UICONTROL Send Welcome Emails To New Users]** pour envoyer des courriers électroniques.
1. Accédez au **[!UICONTROL Network Email]***logo pour le courrier électronique*, à l'adresse électronique à utiliser comme adresse d'expéditeur (**adresse électronique de)**et au nom d'affichage à utiliser pour l'adresse électronique de l'expéditeur (**nom d'affichage de courriel**).