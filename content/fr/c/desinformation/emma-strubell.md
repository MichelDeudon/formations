---
title: Considérations énergétiques et politiques
date: '2019-06-05'
type: book
weight: 20
highlight: true
tags:
  - intelligence artificielle
  - énergie
  - climat
  - désinformation
---

Printemps 2019. Alerte d'Emma Strubell et du MIT.

<!--more-->

## [Considérations énergétiques et politiques pour l'IA](https://arxiv.org/abs/1906.02243)

🚨 Le 5 juin 2019, Emma Strubell, candidate au doctorat et auteur principal de l'article [Energy and Policy Considerations for Deep Learning in NLP](https://arxiv.org/abs/1906.02243) donnait l'alerte à la communauté scientifique et politique du terrible impact écologique des modèles de deep learning en linguistique, à l'époque. Son article est paru dans <b>ACL2019</b> 🇮🇹, la plus grande conférence de linguistique. Le <b>Massachusetts Institute of Technology</b> a rediffusé l'alerte sur la consommation énergétique, les émissions carbones de modèles avec des millions de paramètres comme Transformers (papier "[Attention is all you need](https://arxiv.org/abs/1706.03762)" de <b style="color:blue;">Google</b>, 2017) et [BERT](https://arxiv.org/abs/1810.04805) (<b style="color:blue;">Google</b>, 2018) dans sa revue technologique du 6 juin 2019. On parlait alors de modèles allant jusqu'à 65 millions de paramètres (1/1000 [LLaMA](https://arxiv.org/abs/2302.13971), 2023).

🔥 Le lendemain de l'alerte d'[Emma Strubell](https://arxiv.org/abs/1906.02243) et du [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/), le 7 juin 2019, BERT recoit le prix du meilleur article long à [NAACL19](https://aclanthology.org/N19-1423/) 🇺🇸. Trois jours plus tard, le 10 juin 2019, 22 auteurs, dont le CEO de <b style="color:blue;">Deep Mind</b> Demis Hassabis, publient sur [Arxiv](https://arxiv.org/abs/1906.05433) un article intitulé "Lutter contre le changement climatique avec l'IA", republié sur [ACM](https://dl.acm.org/doi/10.1145/3485128) début février 2022.

## [L'entraînement d'un seul modèle d'IA peut émettre autant de carbone que...](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/)

6 juin 2019. [MIT Technology Review](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/). Par Karen Hao.

{{< figure src="2019-06 MIT.jpg" caption="MIT Technology Review, juin 2019." numbered="true">}}

L'industrie de l'[intelligence artificielle](https://www.technologyreview.com/artificial-intelligence/) est souvent comparée à l'industrie pétrolière : une fois extraites et raffinées, les données, comme le pétrole, peuvent être une marchandise très lucrative. Maintenant, il semble que la métaphore puisse s'étendre encore plus loin. {{<hl>}}Comme son homologue fossile, <b>le processus de deep learning a un impact environnemental démesuré</b>{{</hl>}}.

Dans un [nouvel article](http://arxiv.org/abs/1906.02243), des chercheurs de l'Université du Massachusetts à Amherst ont effectué une évaluation du cycle de vie pour entraîner plusieurs grands modèles d'IA courants. Ils ont découvert que le processus peut émettre plus de 280 tonnes d'équivalent en dioxyde de carbone, soit <b>près de cinq fois les émissions liées au cycle de vie d'une voiture américaine moyenne</b> (et cela inclut la fabrication de la voiture elle-même). De plus, les chercheurs notent que les chiffres ne doivent être considérés que comme des valeurs de référence. "<b>Entrainer un seul modèle est le minimum de travail que vous pouvez faire</b>", déclare <b>Emma Strubell</b>, candidate au doctorat à l'Université du Massachusetts, Amherst, et auteur principal de l'article. En pratique, les chercheurs en IA développent un nouveau modèle à partir de zéro ou adaptent un modèle à un nouveau jeu de données, nécessitant de nombreuses autres expériences d'entraînements et d'ajustements.

### L'empreinte carbone du traitement du langage naturel
L'article examine spécifiquement le processus d'entraînement de modèles de linguistique pour le [traitement du langage naturel](https://www.technologyreview.com/s/612975/ai-natural-language-processing-explained/) (NLP), le sous-domaine de l'IA qui se concentre sur la compréhension du langage humain par des machines. Les deux dernières années ont été jalonnées de performances remarquables dans la traduction automatique, la complétion de phrases et d'autres tâches. Le [tristement célèbre modèle GPT-2 d'OpenAI](https://www.technologyreview.com/s/612960/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/), par exemple, excellait dans la rédaction de faux articles convaincants. Mais de telles avancées ont nécessité <b>l'entraînement de modèles toujours plus grands sur des ensembles de données tentaculaires</b> récupérées sur Internet. <b>L'approche est coûteuse en calcul et très gourmande en énergie</b>.

L'équipe a examiné quatre modèles qui ont été à l'origine des plus grandes avancées en matière de performances : le Transformer, ELMo, [BERT](https://www.nytimes.com/2018/11/18/technology/artificial-intelligence-language.html) et GPT-2. Ils les ont entraînés chacun sur un seul GPU pendant jusqu'à une journée pour mesurer sa consommation d'énergie. Ils ont ensuite utilisé le nombre d'heures d'entraînement indiqué dans les documents originaux du modèle pour calculer l'énergie totale consommée au cours du processus d'entraînement complet. Ce nombre a été converti en livres d'équivalent dioxyde de carbone sur la base du mix énergétique moyen aux États-Unis, qui correspond étroitement au mix énergétique utilisé par <b style="color:blue;">AWS</b> d'Amazon, le plus grand fournisseur de services cloud.

{{< callout note >}}
Février 2023 <b>Macron</b> décore <b style="color:blue;">Bezos</b> en secret. [Le Point](https://www.youtube.com/watch?v=kZPG9rmbdmw&ab_channel=LePoint).
{{< /callout >}}

### Les coûts estimés d'entraîner un modèle une fois
En pratique, les modèles sont généralement entraînés plusieurs fois au cours de la recherche et du développement. Ils ont constaté que <b>les coûts informatiques et environnementaux de l'entraînement augmentent proportionnellement à la taille du modèle, puis explosent lorsque des étapes de réglage supplémentaires sont utilisées pour augmenter le score final du modèle.</b>

Strubell et ses collègues ont utilisé un modèle qu'ils avaient produit dans un article précédent comme étude de cas. Ils ont constaté que le processus de construction et de test d'un modèle final digne d'un article nécessite l'entraînement de 4 789 modèles sur une période de six mois. Converti en équivalent CO2, il a émis plus de 35 tonnes.

L'importance de ces chiffres est colossale, surtout si l'on considère les tendances actuelles de la recherche en IA. "<i>Ce type d'analyse doit être fait pour sensibiliser sur les ressources dépensées [...] et susciter un débat</i>", explique Gómez-Rodríguez. "<i>Ce que beaucoup d'entre nous n'ont probablement pas compris, c'est son ampleur jusqu'à ce que nous ayons vu ces comparaisons</i>", a fait écho Siva Reddy, post-doctorant à l'<b>Université de Stanford</b> qui n'a pas participé à la recherche.

### La privatisation de la recherche en IA
Les résultats soulignent également un autre problème croissant dans le domaine de l'IA : <b>l'intensité des ressources désormais nécessaires pour produire des résultats dignes d'être publiés</b> rend de plus en plus difficile pour les personnes travaillant dans le milieu universitaire de continuer à contribuer à la recherche. "<b>Cette tendance à former d'énormes modèles sur des tonnes de données n'est pas réalisable pour les universitaires</b>, en particulier les étudiants diplômés, car nous n'avons pas les <b>ressources de calcul</b>", déclare Strubell. "Il y a donc un <b>problème d'accès équitable</b> entre les chercheurs du milieu universitaire et les chercheurs de l'industrie."

{{< figure src="macron-lecun-zuckerberg.png" caption="Macron Lecun Zuckerberg et Vivatech 2023. <b style='color:blue;'>Zuckerberg</b>-<b>Macron</b> fait le buzz à VivaTech. [Les echos](https://www.lesechos.fr/start-up/next40-vivatech/le-duo-zuckerberg-macron-fait-le-buzz-a-vivatech-132831), Mai 2018. <b style='color:blue;'>Zuckerberg</b> et <b>Macron</b> se sont (encore) rencontrés à l'Élysée. <i>Cinq jours avant la deuxième édition 'Tech for good'</i>. [Huffington post](https://www.huffingtonpost.fr/politique/article/mark-zuckerberg-et-emmanuel-macron-se-sont-encore-rencontres-a-l-elysee_144827.html), Mai 2019.">}}

{{< figure src="mafia-these-CIFRE.png">}}

{{< figure src="mafia-france-ia.png" caption="Source: @[Yann Lecun](https://twitter.com/ylecun/status/1629845738170597376?lang=en).">}}

## L'affaire du Siècle ⚖ (2021)
- 24-04 <i>Le bluff numérique, ce sont tous les impacts qu’on ne voit pas</i>, avec <b>Laurie Marrauld</b> du <b>Shift Project</b> et <b>Cédric Villani</b>. [Libération](https://www.youtube.com/watch?v=6kJYR0oG3GQ&ab_channel=Lib%C3%A9ration).
- 22-08 <b>Convention citoyenne pour le climat</b>. Une partie des 146 propositions est retenue par le chef de l'État. Code de l'environnement. [LOI n° 2021-1104 du 22 août 2021 portant lutte contre le dérèglement climatique et renforcement de la résilience face à ses effets (V)](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000043956924). [Article L231-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000043961211)
- 14-10 <b>Tribunal de Paris</b>. France condamnée pour inaction climatique. L'État a l’obligation de respecter sa trajectoire de réduction d’émissions de gaz à effet de serre et doit réparer tout dépassement, d’ici le <b>31 décembre 2022</b>. Chaque sortie de route sur la trajectoire climatique constitue à présent une faute qui DOIT être réparée. [vie-publique.fr](https://www.vie-publique.fr/en-bref/282012-changement-climatique-la-france-condamnee-pour-prejudice-ecologique).

### [Macron appelle à la <i>sobriété individuelle</i>](https://www.ladepeche.fr/2022/09/05/direct-crise-de-lenergie-quelles-mesures-complementaires-pourraient-etre-prises-suivez-en-direct-la-conference-demmanuel-macron-10524445.php)

{{< icon name="calendar" pack="fas" >}} Conférence de presse à l'Elysee, le 5 septembre 2022

{{< callout note >}}
Macron a été réélu Président le 24 avril 2022, deux mois après l'invasion de l'Ukraine et début de la crise énergétique ⚡. [Elysée](https://www.elysee.fr/emmanuel-macron).
{{< /callout >}}

<i>"Chacun a son rôle à jouer"</i>, annonce le président français, appelant à la sobriété énergétique et estimant que <i>"la meilleure énergie est celle qu’on ne consomme pas"</i>. L’objectif énoncé par <b>Emmanuel Macron</b> est <i>"d’économiser 10 % de ce que nous consommons actuellement"</i>. [Elysée](https://www.youtube.com/watch?v=XjC1NqzyGkc&ab_channel=%C3%89lys%C3%A9e).