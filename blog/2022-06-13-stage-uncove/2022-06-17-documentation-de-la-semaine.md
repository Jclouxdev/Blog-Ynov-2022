---
slug: documentation-de-la-semaine
title: Documentation de la semaine
authors: joseph
tags: [Stage-2022, Semaine-1, Ynov, Uncove]
---

# 17/06/2022 - Documentation de la semaine

Created: June 17, 2022 9:10 AM
Tags: Daily, Semaine-1

## 👨🏻‍🤝‍👨🏻 Meeting

J’ai expliqué ce que j’ai trouvé hier, et que j’allais appronfondir sur la Technique sur le JPEG aujourd’hui pour voir si ca répondrait à notre problème.

**Tâche du jour :**

- [ ] Essayer de comprendre la logique pour écrire le message avec la technique du LowBit.
- [ ] Faire le permier récap des recherches sur le **Confluence**.

<!--truncate-->

# 📒 Récapitulatif de la semaine

L’objectif de ce Vendredi est de créer la documentation récapitulative de mes recherche de la semaine sur le Confluence d’Uncove.

Vous retrouverez ci-dessous les conclusions que j’ai tiré de mes recherches sur le sujet des Metadonnées et des Invisible Watermark.

## 🖼 Métadonnées des Images

La première étape est de chercher le fonctionnement de base des Métadonnées afin de maitriser un minimum le sujet pour les recherches qui arrivent.

### ✍ Conclusion sur l’utilisation des Métadonnées

Les **métadonnées dans le cadre des copyrights et de tracking de média** ne couvrent qu’**une petite partie du problème**.

Elles seront **effacée en cas de capture d’écran** et simpliment modifiable pour quelqu’un qui connait les Métadonnées des images.

Cependant, je pense qu’il est intéressant de **travailler avec plusieurs couches** pour nous faciliter le travail. On pourra donc appliquer les métadonnées lors du traitement de l’image afin de les lires sur les images retrouvées les moins retouchées.

## 🔒 Renseignement sur les solutions existantes

Une des solutions que j’ai trouvé lors de mes recherches sur les Métadonnées est appellée “Invisible Watermark”. Cette page à pour objectif d’en comprendre l’originie, et le fonctionnement.

### ✍ Conclusion sur les solutions déjà trouvées

Je suis certain qu’il faut créer plusieurs couches de protections pour contrer le maximum de situations.

3 niveaux de protections :

- 🔴 Sécurité Faible : **Watermark visible sur la photo**. Pourra décourager les plus novice.
- 🟠 Sécurité Faible : **Metadonnée pour le copyright**. Fonctionnera sur les gens qui ne connaissent pas bien les médias mais inutile sur un simple screen shot.
- 🟢 Sécurité Moyenne à Haute : **Créer un système de _“Invisible Watermark”_**. De loin le plus efficace, même si ca sous entendu de développer également une solution capable de le lire également.
