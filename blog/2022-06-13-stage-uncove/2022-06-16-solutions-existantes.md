---
slug: solutions-existantes
title: Solutions existantes
authors: joseph
tags: [Stage-2022, Ynov, Uncove]
---

# 15/06/2022 - Solutions existantes

Created: June 15, 2022 9:05 AM
Tags: Daily

## 👨🏻‍🤝‍👨🏻 Meeting

Bonne piste pour les solutions qui impriment une signature dans les pixels. Ils ont eu l’idée de créer un pixel dans l’image avec un code correspondant à l’ID de l’utilisateur (par exemple).

**Tâche du jour :**

- [ ] Continuer la recherche, approfondir sur les solutions trouvée hier.

<!--truncate-->

## 📒 Renseignement sur les solutions existantes

1️⃣ [**Digimarc**](http://www.digimarc.com/technology/about-digital-watermarking)

> **Comment nous appliquons le filigrane**
> Les filigranes Digimarc sont appliqués dans des canaux de couleur individuels, ou des séparations d'encre, où les changements sont visibles. Cependant, l'image composite combinée contient des filigranes discrets.

Point à noté : Digimarc altère assez visiblement la qualité de l’image, surtout sur les couleurs clair. (Voir le test sur leur site)

➕ **Points positifs de** **Digimarc** :

- Solution déjà faite

➖ **Points négatifs de** **Digimarc** :

- Payant
- Détériore la qualité de l’image, assez visible à l’oeil.

2️⃣ [Imatag](https://www.imatag.com/)

➕ **Points positifs de** **Imatag** :

- Notifications lors de publications de contenu protégé par leurs solution.
- Plusieurs solutions pour les différents problèmes (Leak, Copyright, etc)

➖ **Points négatifs de** **Imatag** :

- Evidemment c’est payant, et cher.

3️⃣ Stéganographie

🔍 [https://fr.wikipedia.org/wiki/Stéganographie](https://fr.wikipedia.org/wiki/St%C3%A9ganographie)

La stéganographie n’est pas un logiciel mais une technique **cryptographique** permettant de **dissimuler un message dans des textes ou des images d'apparences anodines**.

Une technique racordée à la Stéganographie est le [Micropoint](https://fr.wikipedia.org/wiki/Micropoint?tableofcontents=1) qui consite à réduire une image à une taille d’environt 1 millimètre pour quelle ressemble à un caractère typographique comme un point ou une virgule.

> **Modifications mineures d'un contenu existant**
>
> Alice peut envoyer un message contenant :
>
> - Poires : 4.0**0**
> - Cerises : 12.0**0**
> - Pommes : 5.0**1**
> - Tomates : 3.2**3**
> - Courgettes : 10.0**2**

> Les techniques informatiques décrites ci-dessous dans les rubriques **_Usage des bits de poids faible d'une image (LSB)_** et **_Modulation fine d'un texte écrit_** correspondent à cette technique.

> L'avantage de la méthode est qu'Alice pourra envoyer à Bob une information relativement longue. Toutefois, Wendy pourrait comparer les prix transmis avec les prix réels (dans le cas du procédé LSB, faire une comparaison bit à bit), pourrait s'étonner d'une précision superflue, pourrait interdire une trop grande précision (cf. plus bas : *stérilisation*).

> **Dissimulation dans un élément annexe au contenu**

> Alice peut, le lundi, envoyer un message contenant :
>
> - Poires : 4
> - Cerises : 12
> - Pommes : 6
> - Tomates : 3
> - Courgettes : 10
>
> et, le mardi, dans un ordre différent (Alice étant fantasque), mais avec des prix parfaitement exacts :
>
> - Cerises : 12
> - Poires : 4
> - Tomates : 3
> - Pommes : 6
> - Courgettes : 10

> Le contenu réel du message est dissimulé dans la variation de l'ordre des fruits par rapport à l'ordre de la veille.

> L'inconvénient de la méthode est que le message est relativement limité en taille. Si Alice se limite à 5 fruits, elle peut transmettre chaque jour à Bob une valeur comprise entre 1 et 120 ([factorielle](https://fr.wikipedia.org/wiki/Factorielle) de 5). L'avantage réside dans la difficulté pour Wendy de repérer l'existence du procédé stéganographique.

> Une technique informatique correspondante consiste à maintenir une image intacte mais à y incorporer une table des couleurs ou *palette* construite dans un ordre qui paraît arbitraire. Le contenu caché peut être une clef donnant accès à un message plus long. En outre, le contenu doit normalement inclure un procédé (généralement un **[checksum](https://fr.wikipedia.org/wiki/Checksum?tableofcontents=1)**) permettant de vérifier sa validité. L'image qui sert de [vecteur](<https://fr.wikipedia.org/wiki/Vecteur_(transport)>) à un contenu caché peut être un extrait d'une image connue mais ne peut jamais être sa reproduction exacte, au risque de permettre par comparaison de révéler l'utilisation d'une technique stéganographique.

> **Techniques rendues possibles par l'ordinateur**

> [Message transporté dans une image](https://fr.wikipedia.org/wiki/St%C3%A9ganographie#Message_transport%C3%A9_dans_une_image)

> Une des techniques les plus connus pour réaliser ce stratagème est appelée **LSB** pour [**least significant bit**](https://fr.wikipedia.org/wiki/Least_significant_bit). Elle consiste à modifier le bit de poids faible des pixels qui constituent l'image. Rappelons qu'une [image numérique](https://fr.wikipedia.org/wiki/Image_num%C3%A9rique) est un ensemble de points, que l'on appelle pixels, et **dont on code la couleur**, par exemple, à l'aide d'un triplet d'octets ([RVB](https://fr.wikipedia.org/wiki/Rouge_vert_bleu)). Chaque octet indique l'intensité de la couleur correspondante --- rouge, vert ou bleu (Red Green Blue). Il y a en tout 256 teintes différentes.

> Quand on **modifie le bit de poids faible d'un octet**, on passe d'une teinte *n* à une teinte immédiatement supérieur (_n+1_) ou inférieur (_n-1_). **Il s'agit d'un changement de teinte qui n'est pas perceptible à l'œil nu**. En effet, un bleu très légèrement plus foncé ou très légèrement plus clair ressemble au bleu non modifié.

📛 **Problème** : La compression d’image va totalement écraser le message, et donc un screen de mauvaise qualité ou une conversion au format JPEG rend le message illisible.

> [Message caché dans les images compressées](https://fr.wikipedia.org/wiki/St%C3%A9ganographie#Message_cach%C3%A9_dans_les_images_compress%C3%A9es)

> 🔎 Article détaillé : [tatouage numérique](https://fr.wikipedia.org/wiki/Tatouage_num%C3%A9rique)

> Néanmoins, **plutôt que de cacher un message dans l'image directement**, il paraît intéressant de le faire de façon encore plus discrète en **le cachant dans les coefficients de cette image**, c'est-à-dire en **travaillant dans le domaine [JPEG](https://fr.wikipedia.org/wiki/JPEG)**.

4️⃣ Concurrence : OnlyFans

Je vais essayer de me renseigner sur les méthodes utilisées par OnlyFans pour pallier à ces problèmes.

Les photos leak de OF que j’ai trouvé ont toute encore le WaterMark, les gens ne prennent pas la peine de le retirer.

### **Idée en vrac :**

Créer une watermark avec des couleurs très transparente, et avoir un moyen de les faire apparaitre avec un filtre de couleur ?

Mot clé important a noter pour la création d’une solution home made :

Invisible Watermark

## Conclusion ATM :

### Solutions pour le Copyright :

3 niveaux de protections :

- Sécurité faible : **Watermark visible sur la photo**. Pourra décourager les plus novice.
- Sécurité faibe : **Metadonnée pour le copyright**. Marchera sur les gens qui ne connaissent pas bien les médias mais inutile sur un simple screen shot.
- Sécurité Moyenne à Haute : **Créer un système de _“Invisble Watermark”_**. De loin le plus efficace, même si ca sous entendu de développer également une solution capable de le lire également.

### Solutions pour traquer le contenu volé :

- Créer un bot capable de faire une recherche inversée des images détenue (Qui prend en compte les tricks les plus connu pour détourner ces méthodes comme l’inversion du sens de la photo, le noir et blanc etc …).
