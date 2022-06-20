---
slug: steganographie
title: Stéganographie
authors: joseph
tags: [Stage-2022, Semaine-1, Ynov, Uncove]
---

# 16/06/2022 - Stéganographie

Created: June 16, 2022 11:14 AM
Tags: Daily, Semaine-1

## 👨🏻‍🤝‍👨🏻 Meeting

J’ai expliqué ce que j’ai trouvé hier, et que j’allais appronfondir sur la Technique sur le JPEG aujourd’hui pour voir si ca répondrait à notre problème.

**Tâche du jour :**

- [ ] Continuer la recherche, approfondir sur la technique avec les taux de compréssion des JPEG.

<!--truncate-->

## 📒 Stéganographie

[Message caché dans les images compressées](https://fr.wikipedia.org/wiki/St%C3%A9ganographie#Message_cach%C3%A9_dans_les_images_compress%C3%A9es)

[https://www.kapwing.com/resources/how-to-make-an-invisible-watermark-without-photoshop/](https://www.kapwing.com/resources/how-to-make-an-invisible-watermark-without-photoshop/)

Idée ? Positionner une petite watermake en transparant en la mettant en très faible d’opacité à quelques endroits de la photo.

Problème : Difficile à “tracer”, dmenade une analyse humaine pour vérifier facilement la Watermark

💡 **Site qui à l’air de bien expliquer le procédé :**

**[How invisible watermarks work](https://invisiblewatermark.net/how-invisible-watermarks-work.html)**

> Les **_invisible watermarks_** fonctionnent en **modifiant légèrement les valeurs des pixels** d'une photographie.

> Selon sa taille, les photographies auront des milliers, des millions voire des milliards de "pixels". Les pixels sont de minuscules carrés d'une seule couleur. Chaque pixel est composé de trois "canaux" : rouge, vert et bleu. En mélangeant diverses nuances de rouge, de vert et de bleu, nous pouvons en fait obtenir toutes les couleurs qu'un ordinateur peut restituer.

> À la base, les **_invisible watermarks_** fonctionnent en arrondissant ces valeurs de canal au nombre pair ou impair le plus proche pour intégrer un "code" dans la photo. Les nombres impairs signifient que "le pixel de filigrane sous-jacent est blanc" et les nombres pairs signifient que "le pixel de filigrane sous-jacent est noir". Arrondir ces valeurs à des nombres pairs ou impairs modifie en fait l'image sous-jacente, mais de manière imperceptible. Il est très difficile pour l'œil humain de faire la différence entre une teinte rouge de 177/255 et 178/255.

**Comment ajouter un _invisible watermarks_ à ma photo ?**

[InvisibleWatermarks.net](https://invisiblewatermark.net/) le fait gratuitement.

Cette solution marche super bien, et avec le format Webp. Il faut comprendre comment ce tool fonctionne pour refaire pareil.
