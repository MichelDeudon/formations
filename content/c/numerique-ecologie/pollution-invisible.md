---
title: Pollution invisible
date: '2024-03-08'
type: book
weight: 20
highlight: true
tags:
  - Impacts du numérique
  - Pollution invisible
  - Santé Physique
  - Santé Mentale
  - Economie
  - Société
  - Environnement
---

Impacts du numérique: environnementaux, sanitaires et sociaux.

<!--more-->

## Introduction

{{< figure src="numeco/toilet.png" caption="Illustration du concept de pollution invisible. Voir aussi [Ma thèse en 180 secondes](https://www.youtube.com/watch?v=FjzK-dgE4Os&ab_channel=Paris-EstSup) de Fabien Esculier.">}}

## Le numérique, quels impacts?

{{< figure src="numeco/impacts.png" caption="Illustration des impacts environnementaux, sanitaires et sociaux du numérique.">}}

Le numérique a des impacts environnementaux, mais aussi des impacts sanitaires et sociaux, invisibles au premier regard. 
Les <b>impacts environnementaux</b> sont liés à la production des équipements, infrastructures et à leurs usages. Ils sont bien documentés par l'[ADEME](https://infos.ademe.fr/) et The Shift Project.
Les <b>impacts sanitaires</b> sont liés à la sédentarité, à l'isolement, au stress, à des émotions négatives mais aussi aux troubles moteurs, troubles du langage et de l'attention chez les enfants.
Les <b>impacts sociaux</b> sont eux liés à la transformation de nos modes de vie et de travail. 

### Impacts environnementaux

{{< figure src="numeco/infographie-Ademe.png" caption="Infographie de l'ADEME (2022). Numérique : quel impact environnemental? Source: [infos.ademe.fr/magazine-avril-2022/faits-et-chiffres/numerique-quel-impact-environnemental/](https://infos.ademe.fr/magazine-avril-2022/faits-et-chiffres/numerique-quel-impact-environnemental/). Voir aussi l'[outil de calcul des usages du numérique](https://agirpourlatransition.ademe.fr/particuliers/bureau/numerique/calculez-lempreinte-carbone-usages-numeriques).">}}

La notion de <b>sac à dos écologique</b> fait référence au fait qu'il fait 500 fois le poids d'un smartphone en matière première pour le fabriquer (le taux d'extraction du Cuivre varie de 0.3 à 2%, celui du Lithium de 0.05% à 0.15%, etc). Ceci produit d'importantes quantités de déchets et représente des sources de pollution de l'environnement (eau, sols...).

{{< figure src="numeco/mendeleiv.png" caption="Elements présents dans les smartphones en 2021, par composants. La fabrication des composants repose sur l'extraction de mines, responsables de conflits et de pollution. Source: [Sobriété Numérique : pourquoi, pourquoi pas et comment ?](https://atecopolmtp.hypotheses.org/352) Séminaire Atecopol Montpellier avec Françoise Berthoud, Ingénieure de Recherche CNRS, le 14 mars 2024. Lien vers le [diaporama de la présentation](https://atecopolmtp.hypotheses.org/files/2024/03/Sobriete-Numerique-atecopol-montpellier-mars-2024.pdf).">}}

On peut retenir le chiffre de 10% pour la consommation éléctrique annuelle des services numériques en 2022 mais c'est aussi la tendance, la croissance exponentielle des flux de données (+12 équipements en moyenne par habitant en France, en forte augmentation) que nous sommes invités à interroger.
The Shift Project a publié en mars 2021 le rapport [Impact environnemental du numérique: tendances à 5 ans et gouvernance de la 5G](https://theshiftproject.org/wp-content/uploads/2021/03/Note-danalyse_Numerique-et-5G_30-mars-2021.pdf) qui cite une étude de Techradar : une question se pose quant à la capacité même d’assurer une production industrielle suffisante. Indirectement, le numérique accélere la consommation et les flux de matières premières et d'énergie.

{{< figure src="numeco/usages-infra-Shift.png" caption="Impacts environnementaux du numérique et facteurs de croissance.">}}

{{< figure src="numeco/flux-donnees-Shift.png" caption="Evolution des flux de données.">}}

Visio, voitures autonomes, vidéosurveillance, téléchirurgie, cloud gaming, streaming ultra HD... quels sont les nouveaux usages pertinents? 

Le Bitcoin représenterait à lui seul 10% de la consommation totale des data centers en 2021 d'après l’observatoire de Cambridge.

La 5G pourrait entrainer une augmentation de 18 à 44% de l’empreinte carbone du numérique à horizon 2030 d'après le Haut Conseil pour le Climat en 2020.

L'IA aussi est gourmande en énergie et a vu sa consommation exploser dans les dernières années. En 2019, dans l'article [Energy and Policy Considerations for Deep Learning in NLP](https://arxiv.org/abs/1906.02243) d'Emma Strubell, Ganesh Ananya et Andrew McCallum, il est question de modèles avec des millions de paramètres par comparaison à [des milliards](https://arxiv.org/abs/2302.13971) en 2023 (changement d'ordres de grandeur). En projetant les modèles sur un axe, <i>la performance</i>, sans prendre en compte les ressources et l'énergie, <i>la performance</i> s’est améliorée mais avec une complexité accrue, au profit d'entreprises comme Google Cloud Platform (GCP), Amazon Web Services (AWS), Microsoft (Azure) et NVIDIA (hardware).

{{< figure src="numeco/neural-networks-LCA.png" caption="<i>Le processus de deep learning a <b>un impact environnemental démesuré</b> (...) L'entraînement de modèles toujours plus grands sur des ensembles de données tentaculaires récupérées sur Internet (...) est coûteux en calcul et très gourmand en énergie</i>. Source: Karen Hao. [L'entraînement d'un seul modèle d'IA peut émettre autant de carbone que...](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) MIT Tech Review, juin 2019.">}}

{{< figure src="numeco/mit-review-2019-costs.png" caption="<i>L'intensité des ressources nécessaires pour produire des résultats dignes d'être publiés rend de plus en plus difficile pour les personnes travaillant dans le milieu universitaire de continuer à contribuer à la recherche, souligne l'article. Cette tendance à former d'énormes modèles sur des tonnes de données n'est pas réalisable pour les universitaires, en particulier les étudiants diplômés, car nous n'avons pas les <b>ressources de calcul</b>, déclare Strubell. Il y a un <b>problème d'accès équitable</b> entre les chercheurs du milieu universitaire et les chercheurs de l'industrie</i>. Source: K. Hao. [L’entraînement d’un seul modèle d’IA peut émettre autant de carbone que…](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) MIT Tech Review, 2019.">}}

Pourtant, d'autres scénarios sont envisageable pour 2030 et 2050, avec davantage de <b>réparation, reconditionnement, sensibilisation et sobriété</b>. 

La <b>sobriété numérique</b> désigne les efforts faits afin de chercher la modération dans nos productions et nos usages numériques. Concrètement, il s’agit de chercher à réduire volontairement à la fois la quantité d’équipements numériques, leurs usages ainsi que les ressources qu’ils consomment, dans le but de répondre à nos besoins sans dégrader les conditions écologiques de la planète. Source: [Youmatter](https://youmatter.world/fr/definition/sobriete-numerique-definition).

{{< spoiler text="La sobriété est-elle souhaitable ou subie?" >}}
En juin 2022, Total, EDF et ENGIE alertaient de la [menace des prix de l'énergie sur la cohésion](https://www.lejdd.fr/societe/tribune-le-prix-de-lenergie-menace-notre-cohesion-par-les-patrons-dengie-edf-et-totalenergies-9401), appellant les Français à une sobriété d'urgence. En septembre 2022, le Président Macron appellait les français.es à une [sobriété individuelle](https://www.youtube.com/watch?v=XjC1NqzyGkc&ab_channel=%C3%89lys%C3%A9e) et les français.es sont parvenus à réduire leur consommation, mais de manière inégale avec notamment un effort plus important pour les femmes vivant dans des situations plus précaires. Voir aussi la présentation [Les inégalités de genre dans la transition écologique - Exemple: La sobriété énergétique est une histoire de femme](https://www.youtube.com/watch?v=bTXib713IDo&ab_channel=INRAE) d'Amandine Richaud-Crambes de l’ADEME, le 8 mars 2024 à l'INRAE.
{{< /spoiler >}}

{{< figure src="numeco/generation-frugal-ADEME.png" caption="<b>Scénario Génération frugale de l'ADEME</b>. <i>Des transformations importantes dans les façons de se déplacer, de se chauffer, de s’alimenter, d’acheter et d’utiliser des équipements, permettent d’atteindre la neutralité carbone sans impliquer de technologies de captage et stockage.</i> Source: [Impact environnemental du numérique en 2030 et 2050 : L'ADEME et l'ARCEP publient une évaluation prospective](https://presse.ademe.fr/2023/03/impact-environnemental-du-numerique-en-2030-et-2050-lademe-et-larcep-publient-une-evaluation-prospective.html), mars 2023.">}}

Pour aller plus loin: 
- [Le Mooc INRIA/Class Code](https://www.fun-mooc.fr/fr/cours/impacts-environnementaux-du-numerique/), accessible à partir du lycée.
- [La Fresque du Numérique](https://www.fresquedunumerique.org/), un atelier pour comprendre en équipe et de manière ludique les enjeux environnementaux du numérique.
- Ressources de l'université Paul Valéry [Pour un numérique responsable](https://www.univ-montp3.fr/fr/vie-de-campus/campus-num%C3%A9rique/un-numerique-responsable).

### Impacts sanitaires et sociaux

Le plaisir ou encore le fait de scroller mobilise des circuits à dopamine. Dans les applications, et en particulier sur les réseaux sociaux (Flux Tiktok, Reels Instagram, Shorts Youtube), tout est pensé, testé, optimisé pour pousser l’utilisateur à cliquer plus, consommer plus... Voir par exemple le Ted Talk de Harrish Murugesan [Psychology Behind UI/UX Design](https://www.youtube.com/watch?v=fdXI9yznzz8) ou encore le blog de recherche de Google Brain sur la [curiosité et procrastination](https://blog.research.google/2018/10/curiosity-and-procrastination-in.html?ref=blog.floydhub.com&m=1).

On est saturé d'information de peur d'en manquer ou simplement par ennui (économie de l'attention), ce qui impacte directement notre état de <b>santé physique</b> et <b>santé mentale</b>.

{{< figure src="numeco/paulva_levetoi.png" caption="Je vis mes partiels sereinement. Partie I et II. [@paulva_levetoi](https://www.instagram.com/paulva_levetoi/), en mai 2023.">}}

> _Je me sens épuisé et en manque d'énergie par manque d'activité physique. Aussi, je sens que ma capacité d'attention a baissé à cause des réseaux sociaux._ - Étudiant en licence, mai 2023.

👉 Voir notre {{% staticref "u/Temoignages-reseaux-sociaux-Montpellier-mai-2023.pdf" %}}recueil de témoignages{{% /staticref %}} sur les réseaux sociaux en mai 2023.

Vous pouvez [enquêter autour de vous](https://framaforms.org/reseaux-sociaux-attention-et-sante-mentale-1687119437).
Ce projet de <b>sciences participatives</b> est l’occasion de vous confronter au terrain et de développer vos compétences de détective.

Nous verrons en cours comment agir avec des <b>mises en situation</b> concrètes (au travail, en famille, dans les transports).