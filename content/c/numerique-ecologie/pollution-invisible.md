---
title: Pollution invisible
date: '2024-03-08'
type: book
weight: 20
highlight: true
tags:
  - Impacts du numérique
  - Réseaux Sociaux
  - Intelligence Artificielle
  - Pollution invisible
  - Santé Physique
  - Santé Mentale
  - Economie
  - Énergie
  - Société
  - Environnement
  - Sobriété Numérique
---

Impacts du numérique, environnementaux, sanitaires et sociaux.

<!--more-->

## Introduction

{{< figure src="numeco/toilet.png" caption="Illustration du concept de pollution invisible.">}}

👉 Voir [Ma thèse en 180 secondes](https://www.youtube.com/watch?v=FjzK-dgE4Os&ab_channel=Paris-EstSup) de Fabien Esculier.

## Le numérique, quels impacts?

{{< figure src="numeco/impacts.png" caption="Illustration des impacts environnementaux, sanitaires et sociaux du numérique.">}}

Le numérique a des impacts environnementaux, mais aussi des impacts sanitaires et sociaux, invisibles au premier regard. 
Les <b>impacts environnementaux</b> sont liés à la production des équipements, infrastructures et à leurs usages. Ils sont bien documentés par l'ADEME et The Shift Project.
Les <b>impacts sanitaires</b> sont liés à la sédentarité, à l'isolement, au stress, à des émotions négatives mais aussi aux troubles moteurs, troubles du langage et de l'attention chez les enfants.
Les <b>impacts sociaux</b> sont eux liés à la transformation de nos modes de vie et de travail. 

### Impacts environnementaux

Infographie de l'ADEME (2022): [infos.ademe.fr/magazine-avril-2022/faits-et-chiffres/numerique-quel-impact-environnemental/](https://infos.ademe.fr/magazine-avril-2022/faits-et-chiffres/numerique-quel-impact-environnemental/)

{{< figure src="numeco/infographie-Ademe.png" caption="Infographie de l'ADEME (2022). Source: [infos.ademe.fr](https://infos.ademe.fr/magazine-avril-2022/faits-et-chiffres/numerique-quel-impact-environnemental/).">}}

La notion de <b>sac à dos écologique</b> fait référence au fait qu'il fait 500 fois le poids d'un smartphone en matière première pour le fabriquer (le taux d'extraction du Cuivre varie de 0.3 à 2%, celui du Lithium de 0.05% à 0.15%, etc).

{{< figure src="numeco/mendeleiv.png" caption="Elements présents dans les smartphones en 2021, par composants. La fabrication des composants repose sur l'extraction de mines, responsables de conflits et de pollution.">}}

On peut retenir le chiffre de 10% pour la consommation éléctrique annuelle des services numériques en 2022 mais c'est aussi l'évolution de ce chiffre et la tendance (croissance exponentielle des flux de données, +6% dans les émissions de GES mondiales, +12 équipements en moyenne par habitant en France, en forte augmentation) que nous sommes invités à interroger.
The Shift Project a publié une étude en mars 2021 à ce sujet: [Impact environnemental du numérique: tendances à 5 ans et gouvernance de la 5G](https://theshiftproject.org/wp-content/uploads/2021/03/Note-danalyse_Numerique-et-5G_30-mars-2021.pdf). Le rapport cite une étude de Techradar selon laquelle une question se pose quant à la capacité même d’assurer une production industrielle suffisante. Indirectement, le numérique accélere la consommation/production et les flux de matières premières et d'énergie.

{{< figure src="numeco/usages-infra-Shift.png" caption="Impacts environnementaux du numérique et facteurs de croissance. Source: The Shift Project. [Impact environnemental du numérique: tendances à 5 ans et gouvernance de la 5G](https://theshiftproject.org/wp-content/uploads/2021/03/Note-danalyse_Numerique-et-5G_30-mars-2021.pdf)">}}

{{< figure src="numeco/flux-donnees-Shift.png" caption="Evolution des flux de données. Visio, voitures autonomes, vidéosurveillance, téléchirurgie… cloud gaming, streaming ultra HD. Quels sont les nouveaux usages pertinents? Source: The Shift Project. [Impact environnemental du numérique: tendances à 5 ans et gouvernance de la 5G](https://theshiftproject.org/wp-content/uploads/2021/03/Note-danalyse_Numerique-et-5G_30-mars-2021.pdf)">}}

Selon l’observatoire de Cambridge, le Bitcoin = 10% de la consommation totale des data centers en 2021 et d’après le Haut Conseil pour le Climat en 2020, la 5G = augmentation de 18 à 44 % de l’empreinte carbone du numérique à horizon 2030. L'IA a aussi vu sa consommation explosé dans les années 2010-2020.

Le 5 juin 2019, <b>Emma Strubell</b>, doctorante et co-autrice de l'article [Energy and Policy Considerations for Deep Learning in NLP](https://arxiv.org/abs/1906.02243) informait la communauté scientifique de l'impact écologique des modèles de deep learning après avoir effectué une évaluation du cycle de vie pour entraîner plusieurs grands modèles d'IA courants (en 2019). Son article est paru dans <b>ACL2019</b> 🇮🇹, la plus grande conférence de linguistique. Le lendemain, le <b>Massachusetts Institute of Technology</b> rediffuse son message dans sa [revue technologique](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) et révèle la consommation énergétique et les émissions carbones de modèles comme [Transformers](https://arxiv.org/abs/1706.03762), [BERT](https://arxiv.org/abs/1810.04805) (Google) et [GPT-2](https://www.technologyreview.com/s/612960/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/) (OpenAI). 

> Les chercheurs notent que les chiffres ne doivent être considérés que comme des valeurs de référence. "Entrainer un seul modèle est le minimum de travail que vous pouvez faire", déclare Emma Strubell (...) en pratique, les modèles sont généralement entraînés plusieurs fois au cours de la recherche et du développement (...) Strubell et ses collègues ont utilisé un modèle qu'ils avaient produit dans un article précédent comme étude de cas. Ils ont constaté que le processus (...) a émis plus de 35 tonnes.

{{< figure src="numeco/neural-networks-LCA.png" caption="Le processus de deep learning a un impact environnemental démesuré (...) L'entraînement de modèles toujours plus grands sur des ensembles de données tentaculaires récupérées sur Internet (...) est coûteux en calcul et très gourmand en énergie. Source: Karen Hao. [L'entraînement d'un seul modèle d'IA peut émettre autant de carbone que...](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) MIT Tech Review, juin 2019.">}}

Le même jour, BERT recoit le prix du meilleur article long à [NAACL19](https://aclanthology.org/N19-1423/) 🇺🇸 et la même année les trois pères du Deep Learning recoivent le prix Turing décerné par ACM pour leur travaux sur les réseaux de neurones. On parlait alors de modèles larges allant jusqu'à 65 millions de paramètres par comparaison à [65 milliards](https://arxiv.org/abs/2302.13971) en 2023.

{{< figure src="numeco/mit-review-2019-costs.png" caption="L'intensité des ressources nécessaires pour produire des résultats dignes d'être publiés rend de plus en plus difficile pour les personnes travaillant dans le milieu universitaire de continuer à contribuer à la recherche, souligne l'article. Cette tendance à former d'énormes modèles sur des tonnes de données n'est pas réalisable pour les universitaires, en particulier les étudiants diplômés, car nous n'avons pas les <b>ressources de calcul</b>, déclare Strubell. Il y a un <b>problème d'accès équitable</b> entre les chercheurs du milieu universitaire et les chercheurs de l'industrie. Source: K. Hao. [L’entraînement d’un seul modèle d’IA peut émettre autant de carbone que…](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) MIT Tech Review, 2019.">}}

Pourtant, d'autres scénarios sont envisageable pour 2030 et 2050, avec davantage de <b>réparation, reconditionnement, sensibilisation et sobriété</b>. 

La <b>sobriété numérique</b> désigne les efforts faits afin de chercher la modération dans nos productions et nos usages numériques. Concrètement, il s’agit de chercher à réduire volontairement à la fois la quantité d’équipements numériques, leurs usages ainsi que les ressources qu’ils consomment, dans le but de répondre à nos besoins sans dégrader les conditions écologiques de la planète. Source: [Youmatter](https://youmatter.world/fr/definition/sobriete-numerique-definition).

> Scénario Génération frugale 2050: « Des transformations importantes dans les façons de se déplacer, de se chauffer, de s’alimenter, d’acheter et d’utiliser des équipements, permettent d’atteindre la neutralité carbone sans impliquer de technologies de captage et stockage. ». [presse.ademe.fr/2023/03/impact-environnemental-du-numerique-en-2030-et-2050-lademe-et-larcep-publient-une-evaluation-prospective.html](https://presse.ademe.fr/2023/03/impact-environnemental-du-numerique-en-2030-et-2050-lademe-et-larcep-publient-une-evaluation-prospective.html)

{{< figure src="numeco/generation-frugal-ADEME.png" caption="Scénario Génération frugale de l'ADEME. Source: [presse.ademe.fr](https://presse.ademe.fr/2023/03/impact-environnemental-du-numerique-en-2030-et-2050-lademe-et-larcep-publient-une-evaluation-prospective.html).">}}

Pour aller plus loin: 
- [Le Mooc INRIA/Class Code](https://www.fun-mooc.fr/fr/cours/impacts-environnementaux-du-numerique/), accessible à partir du lycée.
- [La Fresque du Numérique](https://www.fresquedunumerique.org/), un atelier pour comprendre en équipe et de manière ludique les enjeux environnementaux du numérique.
- Ressources de l'université Paul Valéry [Pour un numérique responsable](https://www.univ-montp3.fr/fr/vie-de-campus/campus-num%C3%A9rique/un-numerique-responsable).

### Impacts sanitaires et sociaux

Le plaisir ou encore le fait de scroller mobilise des circuits à dopamine. Dans les applications, et en particulier sur les réseaux sociaux (Flux Tiktok, Reels Instagram, Shorts Youtube), tout est pensé, testé, optimisé pour pousser l’utilisateur à cliquer plus, consommer plus... Voir par exemple le Ted Talk de Harrish Murugesan [Psychology Behind UI/UX Design](https://www.youtube.com/watch?v=fdXI9yznzz8) ou encore le blog de recherche de Google Brain sur la [curiosité et procrastination](https://blog.research.google/2018/10/curiosity-and-procrastination-in.html?ref=blog.floydhub.com&m=1).

On est saturé d'information (on parle d'économie de l'attention) de peur d'en manquer, ce qui impact directement notre état de <b>santé physique</b> et <b>santé mentale</b>.

> _Je me sens épuisé et en manque d'énergie par manque d'activité physique. Aussi, je sens que ma capacité d'attention a baissé à cause des réseaux sociaux._ - Étudiant en licence à Paul Valéry, mai 2023.

{{< figure src="numeco/paulva_levetoi.png" caption="Je vis mes partiels sereinement. Partie I et II. [@paulva_levetoi](https://www.instagram.com/paulva_levetoi/), en mai 2023.">}}

👉 Voir notre {{% staticref "u/Temoignages-reseaux-sociaux-Montpellier-mai-2023.pdf" %}}recueil de témoignages{{% /staticref %}} sur les réseaux sociaux en mai 2023.

Vous pouvez [enquêter auprès d'étudiants](https://framaforms.org/reseaux-sociaux-attention-et-sante-mentale-1687119437) sur le campus, du personnel de l’université, de personnes à l’extérieur, et partager vos résultats sous diverses formes.
Ce projet de sciences participatives est l’occasion de vous confronter au terrain, de développer vos compétences en animation et sensibiliser le public de votre choix au Bien Vivre Ensemble.

## Références

> [Sobriété Numérique : pourquoi, pourquoi pas et comment ?](https://atecopolmtp.hypotheses.org/352) Séminaire Atecopol Montpellier avec Françoise Berthoud, Ingénieure de Recherche CNRS, le 14 mars 2024. Lien vers le [diaporama de la présentation](https://atecopolmtp.hypotheses.org/files/2024/03/Sobriete-Numerique-atecopol-montpellier-mars-2024.pdf).

> [Impact environnemental du numérique en 2030 et 2050 : L'ADEME et l'ARCEP publient une évaluation prospective](https://presse.ademe.fr/2023/03/impact-environnemental-du-numerique-en-2030-et-2050-lademe-et-larcep-publient-une-evaluation-prospective.html). ADEME/ARCEP, mars 2023.

> [Numérique : quel impact environnemental ?](https://infos.ademe.fr/magazine-avril-2022/faits-et-chiffres/numerique-quel-impact-environnemental/) Infographie de l'ADEME (2022) et [outil de calcul des usages du numérique](https://agirpourlatransition.ademe.fr/particuliers/bureau/numerique/calculez-lempreinte-carbone-usages-numeriques).

> [Impact environnemental du numérique: tendances à 5 ans et gouvernance de la 5G](https://theshiftproject.org/wp-content/uploads/2021/03/Note-danalyse_Numerique-et-5G_30-mars-2021.pdf). The Shift Project, mars 2021.

> [L’entraînement d’un seul modèle d’IA peut émettre autant de carbone que…](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) MIT Tech Review, 2019.