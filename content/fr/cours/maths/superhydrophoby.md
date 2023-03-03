---
title: Super hydrophobie
date: '2023-01-29'
type: book
weight: 30
tags:
  - Superhydrophobie
---

De l'angle d'Young à l'effet Fakir

<!--more-->

## Introduction

De nombreux exemples de superhydrophobie existent dans la nature. Cette propriété permet notamment aux feuilles de lotus et de ginkgo biloba de rester secs et propres pour transformer plus efficacement le CO2 en dioxygène avec la photosynthèse. Cette même propriété permet à la plupart des oiseaux de décoller directement de l'eau, à quelques exceptions près comme le cormoran, dont les plumes hydrophiles s'imbibent d'eau (raison pour laquelle on le voit perché, se sécher après chaque plongeon).

La mesure de l'angle d'Young, défini comme l'angle formée entre une surface et une goutte d'eau posée dessus, permet de caractériser les surfaces hydrophiles des surfaces hydrophobes. Une goutte d'eau posée sur une surface hydrophile, comme le bois, a tendance à épouser la forme de la surface alors que sur une surface superhydrophobe, elle forme une perle. Cette propriété perlante a inspiré la conception de vêtements imperméables comme les K-ways.

Dans la suite, nous nous intéressons aux spores de lycopode, une plante de type fougère apparue il y a 470 millions d'années. Ses spores microscopiques sont superhydrophobes et auraient permis à la plante de peupler la Terre en traversant les océans.

## Présentation des spores de Lycopodium

{{< figure src="super-hydrophoby/img4.png" caption="Schéma du montage expérimental pour déterminer la taille des spores." numbered="true">}}

La diffraction de la lumière permet de déterminer la taille des spores. La mesure du diamètre apparent du disque d'Airy {{< math >}}$\theta${{< /math >}} illustré dans la Figure 1 permet de remonter à leur diamètre D par la relation {{< math >}}$\theta = 1,22 \frac{\lambda}{D}${{< /math >}}. Numériquement, on trouve {{< math >}}$D\approx 20 \mu m${{< /math >}}.

Les spores de lycopode sont recouverts de deux enveloppes, l'une
interne appelée endospore, l'autre externe appelée exospore. L'exospore est constitué de sporopollénine, un polymère naturel dont la composition exacte est toujours inconnue car la sporopollénine est très inerte. Cependant, des études ont montré que la structure de la sporopollénine est proche de celle de la {{< math >}}$\beta${{< /math >}} carotène, et obtenue à partir d'acide férulique et d'acide p-coumarique [1]. La présence de longues chaînes carbonées expliquerait leur hydrophobie.

{{< figure src="super-hydrophoby/img2.png" caption="Représentation de l'acide férulique (gauche) et de l'acide p-coumarique (droite)." numbered="true">}}

L'observation de spores au microscope optique (x100, x400, x600) suggère que leur surface n'est pas lisse.
Des irrégularités distantes
de quelques {{< math >}}$\mu m${{< /math >}} la rendent rugueuse et superhydrophobe. C'est l'effet Fakir: une goutte d'eau ne s'écrase pas sous l'effet de la pesanteur mais laisse sous elle des poches d'air, tel un fakir posé sur des clous. Ceci se produit lorsque la distance entre les irrégularités est inférieure à la longueur capillaire de l'eau {{< math >}}$L_c = \sqrt{\frac{\gamma}{\rho g}} \approx 3${{< /math >}} mm. 

{{< figure src="super-hydrophoby/img3.jpg" caption="Spores de Lycopodium, vus au microscope." numbered="true">}}

### Tracé d'un diagramme énergétique

{{< figure src="super-hydrophoby/img1.jpg" caption="Illustration du phénomène de coalescence" numbered="true">}}

Deux gouttes enrobées de spores de lycopode ne coalescent pas, une propriété qui peut servir pour transporter un liquide dans un fluide [2]. En revanche, si une goutte dispose de suffisamment d'énergie, la coalescence peut se produire. Dans [3], les auteurs déterminent la vitesse d'impact critique pour qu'une goutte de rayon variable R traverse une couche de spore. Nous étudierons ici la barrière énergétique que représentent des spores pour la coalescence de gouttes d'eau. Nous considérons des gouttes d'eau de volume constant {{< math >}}$\approx \mu m^3 ${{< /math >}}. On note {{< math >}}$R${{< /math >}} leur rayon.

{{< figure src="super-hydrophoby/img5.png" caption="Schéma du dispositif expérimental pour étudier l'énergie nécessaire à une goutte d'eau pour traverser une surface recouverte de spores." numbered="true">}}

### Montage et protocole

Le schéma du dispositif expérimental est illustré dans la Figure 3. {{< math >}}$S${{< /math >}} définit la surface du bécher, {{< math >}}$m${{< /math >}} la masse de spore déposée et {{< math >}}$\sigma = \frac{m}{S}${{< /math >}}
la densité surfacique de spores, supposée uniforme à l'échelle du bécher. A {{< math >}}$\sigma${{< /math >}} fixée, j'ai fait varier {{< math >}}$h${{< /math >}}, la hauteur depuis laquelle la goutte d'eau est lâchée sans vitesse initiale, l'interface de spores étant repérée par {{< math >}}$h=0${{< /math >}}. En première approximation, la vitesse d'impact est {{< math >}}$v=\sqrt{2gh}${{< /math >}}. Le résultat expérimental est binaire, soit la goutte traverse la surface, soit elle ne la traverse pas.

### Etude statistique

A {{< math >}}$\sigma${{< /math >}} et h fixées j'ai lâché successivement entre 5 et 10 gouttes. Le résultat est une fraction comprise
entre 0 (aucune goutte lâchée n'a traversé les spores) et 1 (toutes les gouttes lâchées ont traversé).
Ainsi, à {{< math >}}$\sigma${{< /math >}} donnée, en réitérant ce qui précède pour différentes valeurs de h, je définis deux hauteurs {{< math >}}$h_{min}${{< /math >}} et {{< math >}}$h_{max}${{< /math >}}.
Si {{< math >}}$h<h_{min}${{< /math >}} la goutte ne traverse jamais et si {{< math >}}$h>h_{max}${{< /math >}} la goutte traverse toujours: l'apport d'énergie est suffisant. L'intervalle {{< math >}}$[h_{min}-h_{max}]${{< /math >}} correspond aux incertitudes de mesure.

Après plus de 800 gouttes lâchées, j'ai obtenu un diagramme énergétique où {{< math >}}$\sigma${{< /math >}} est porté en abscisse, {{< math >}}$h_{min}${{< /math >}} et {{< math >}}$h_{max}${{< /math >}} en ordonné. On distingue trois domaines. Un premier où {{< math >}}$h${{< /math >}} est proportionnelle à {{< math >}}$\sqrt{\sigma}${{< /math >}}, puis une évolution linéaire et enfin quadratique. On remarque aussi qu'il existe une densité surfacique critique {{< math >}}$\sigma_c${{< /math >}}. Si {{< math >}}$\sigma< \sigma_c${{< /math >}} une goutte d'eau traverse la couche de spores, quelque soit sa hauteur de chute.

{{< figure src="super-hydrophoby/img6.png">}}

### Modélisation de la déplétion locale de spores

#### Enoncé d'un principe

Lorsque la déformation de l'interface est maximale (état repéré par * et dépendant de la hauteur de chute h),
si la densité surfacique apparente {{< math >}}$\sigma^*${{< /math >}} est inférieure à {{< math >}}$\sigma_c${{< /math >}}, la goutte traverse.
Sinon la goutte ne traverse pas. Le cas limite {{< math >}}$\sigma^*=\sigma_c${{< /math >}} correspond à la frontière entre les deux régimes. Pour déterminer {{< math >}}$\sigma^*${{< /math >}} en fonction des paramètres {{< math >}}$h${{< /math >}} et {{< math >}}$\sigma${{< /math >}}, je me suis rendu à l'institut d'Alembert de Jussieu pour filmer la déformation. Arnaud Antkowiak, professeur à l'UPMC et chercheur en mécanique des fluides, m'a accueilli et permis de réaliser des videos avec une caméra rapide (plus de 1000 images par seconde).

#### Modélisation du domaine linéaire

{{< figure src="super-hydrophoby/img7.png" caption="Exemple dans le domaine linéaire du diagramme énergétique." numbered="true">}}

Les séquences photos montrent que dans ce domaine, il
n'y a pas de projections de spores. La conservation de la matière se traduit par
{{< math >}}$$
    S^* \sigma^*=S\sigma
$${{< /math >}}
En première approximation, la surface de spores qui se déforme se situe directement sous la goutte. La variation de la surface est donc donnée par
{{< math >}}$$
    \Delta S = S^* - S \approx \Pi R^2 (\frac{\sigma}{\sigma^*}-1)
$${{< /math >}}
Par ailleurs, la conservation de l'énergie se traduit par 
{{< math >}}$$
    \rho (\frac{4}{3} \pi R^3) gh= \gamma \Delta S
$${{< /math >}}
où le terme de gauche correspond à l'énergie potentielle de la goutte d'eau lachée, et le terme de droite correspond à la variation d'énergie de surface due à sa déformation.
L'équation du diagramme énergétique s'obtient en remplaçant {{< math >}}$\sigma^*${{< /math >}} par {{< math >}}$\sigma_c${{< /math >}} dans les équations (2) et (3). On obtient bien une relation linéaire entre {{< math >}}$h${{< /math >}} et {{< math >}}$\sigma${{< /math >}}, valable pour {{< math >}}$\sigma \geq \sigma_c${{< /math >}}
{{< math >}}$$
    h \approx \frac{4}{3} \frac{\gamma}{\rho Rg} (\frac{\sigma}{\sigma_c}-1)
$${{< /math >}}
{{< math >}}$h${{< /math >}} est propotionnel à {{< math >}}$\gamma${{< /math >}} et inversement proportionnel à la masse de la goutte d'eau, cela semble cohérent.

### Conclusion

Pour qu'une goutte d'eau traverse effectivement des spores de Lycopode de densité surfacique {{< math >}}$\sigma${{< /math >}}, il faut un apport d'énergie cinétique suffisant pour permettre
une déplétion locale de spores conséquente. Le transfert et l'échange d'énergie sont déterminants dans la nature de la réponse.

### Reference

[1] S. Barrier. Physical and chemical properties of sporopollenin exine particles. PhD Thesis. University of Hull. 2008.

[2] P. Aussillous. Les gouttes enrobées. PhD Thesis. Université Paris VI. 2002.

[3] E. Lorenceau, C. Planche, A. L. Biance et al. Coalescence of armored interface under impact. 2013.