---
title: 1 - Biais linguistiques
date: '2021-01-01'
type: book
weight: 80
tags:
  - Représentations sociales
  - Régressions sociales
  - Biais de genre
  - Stéréotypes
  - Data.gouv.fr
  - Intelligence Artificielle
  - Humanités Numériques
---

Utiliser le langage pour l'innovation sociale.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 application pratique

## Analyse de genre de 2 millions de voies en France et régressions sociales

{{< icon name="github" pack="fab" >}} [nlp201-street-names-gender-analysis](https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis)

Plus de 93% des boulevards en France et sur [data.gouv.fr](https://adresse.data.gouv.fr/) portent le nom d'un homme parmi les noms de célébrités (Victor Hugo, De Gaulle, Leclerc, Foch, etc). Par comparaison, 60% des jardins portent le nom d'une femme, dont certains correspondent aux noms d'arbres ou de fleurs comme Rose, Magnolia ou Capucine. Des études ont permis de quantifier le taux de  représentativité des femmes, dans la dénomination de voies publiques, dans différentes villes ou secteurs, à différentes dates, par différentes méthodes. Nous proposons des indicateurs dérivés de la [Base Adresse Nationale](https://adresse.data.gouv.fr/) [5] pour estimer le taux de représentativité des femmes dans la dénomination des voies publiques, localement et à l'échelle de villes, départements et régions en France (plus de 2 millions de voies en Métropole et en Outre-Mer). Nous retrouvons un taux de féminisation des voies et espaces publics proche de 12% à Paris [6] et dans des villes comme Nantes et Montpellier. Nous analysons les corrélations avec certaines professions, filières, et comparons nos résultats avec des pages publiques Wikipedia. Notre analyse suggère que l'imaginaire associé à certaines professions (docteur, professeur, capitaine, colonel) et filières en France (mathématiques, médaille Fields, informatique, prix Turing) induit un biais de genre dans nos représentations sociales et cultive les stéréotypes, amplifiés par les modèles LLaMA d'intelligence artificielle de Facebook AI Research (FAIR) Paris [4], conduisant à des formes de régressions sociales. Nous mettons en accès libre [notre implémentation](https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis) pour suivre l'évolution de ces biais dans le temps.

### Introduction

Les mots influencent nos représentations dès le plus jeune âge et façonnent notre imaginaire collectif.
<i>Hautement symbolique, la dénomination des rues et espaces publics est l’occasion de rendre hommage à des personnes célèbres, et notamment aux femmes. Depuis 2014, la proportion de voies parisiennes portant le nom d'une femme a doublé, atteignant 12%</i> - Paris, 2021 [6].

<b>La Base Adresse Nationale</b> est l’une des neuf bases de données du service public des données de référence [5]. Elle est la seule base de données d’adresses officiellement reconnue par l’administration et à ce titre placée sous la responsabilité de la Première ministre. Sa construction est assurée en premier lieu par les communes. Elle est accessible sous forme de fichiers et d’API.
Le jeu de données représente plus de $2$ millons voies en France, dont 10% contiennent un prénom genré de la liste de prénoms et genre de [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/liste-de-prenoms/) [18]. La Figure 1 montre localement les voies de Montpellier contenant un prénom genré. Dans la suite de cet article, nous proposons une méthode pour quantifier les biais de genre sur la [Base Adresse Nationale](https://adresse.data.gouv.fr/) [5]. Nous comparons nos résultats à des pages publiques Wikipédia et discutons en quoi les mathématiques, les statistiques, et le développement d'intelligences artificielles compétitives, fondamentales, <i>à l'état de l'art</i>, à Paris [4] peuvent conduire à des régressions sociales en France.

{{< figure src="linguistics/img9.png" caption="Données de la [Base Adresse Nationale](https://adresse.data.gouv.fr/) [5] à Montpellier. Chaque voie est représentée par un point bleu (nom masculin), rouge (nom féminin) ou gris (autre). Le taux de féminisation des voies publiques à Montpellier est compris entre 12 et 16%." numbered="true">}}

### Méthodologie

Nous annotons les noms de voie de la [Base Adresse Nationale](https://adresse.data.gouv.fr/) [5] avec un label ('F', 'H' ou 'autre'), à partir des prenoms identifiés du jeu de données de prénoms et genres de [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/liste-de-prenoms/) [18]. Nous préprocessons les noms de voie (lettres en miniscules, sans chiffres et ponctuation) avant d'itérer sur chaque mot constituant un nom de voie pour en extraire les prénoms et genre. Par exemple "rue Sainte Anne" contient le prénom "Anne", nous l'annotons avec le label "F". La voie "av. Paul Valéry" contient "Paul", nous l'annotons avec le label "H". Dans les autres cas, nous renvoyons le label 'autre'. Le vocabulaire utilisé et le code Python sont en accès libre sur Framagit sous licence CC-BY à [https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis](https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis).

### Résultats

<i> Remarque: L'ensemble des résultats sont calculés en mai 2023, ils sont susceptibles d'évoluer avec le temps. </i>

#### Analyse spatiale

{{< figure src="linguistics/france-map-2023.png" caption="Noms de voie et genre aggrégé par communes en France métropole. Le label 1 en bleu (resp. 2 en rouge) correspond à 100% de voies portant des noms d'hommes (resp. de femmes). Le taux de féminisation des voies publiques à l'échelle nationale se situe entre 8 et 15%, ce qui correspond à un label entre 1.08 et 1.15." numbered="true">}}

Les données aggrégées par communes en France métropolitaine sont illustrées dans la Figure 2. Pour chaque commune, nous calculons un label compris entre 1 et 2, et qui correspond au ratio de voies portant un prénom féminin/masculin. Nous reportons dans la Table en Annexe cet indicateur calculé à l'échelle nationale et pour les 10 plus grandes villes francaises, et comparons nos résultats à d'autres indicateurs comme la proportion de voies contenant le mot "Sainte" versus "Saint", ou la proportion de prénoms féminins parmi les $k$ plus populaires. Nos résultats soulignent les disproportionalités entre dénominations d'espaces publics et genre, globalement et avec des disparités locales.

#### Analyse linguistique

Parmi les 50 prenoms les plus courants dans les noms de voies, 4 sont féminins: Marie, Blanche, Jeanne et Anne. La distribution des prénoms est biaisée vers une représentation masculine de l'histoire et de ses héros, comme illustrée dans la Figure 3.

{{< figure src="linguistics/word_pyramid.png" caption="Classement des 25 prénoms masculins et féminins les plus populaires dans la dénominations des voies en France. La distribution des prénoms suit la loi de Zipf [23]: une minorité de prénoms (ici à plus de 92\% masculins) apparaissent très fréquemment tandis que la majorité des prénoms (mixtes) sont rarement employés." numbered="true">}}

La représentation des femmes varie d'un type de voie à un autre. On observe que les jardins sont connotés à des divinités de la Nature, à des noms de fleurs et prénoms féminins, alors que les avenues et les boulevards sont à dominante masculine et connotés à des chefs de guerre et des chars ou armes de guerre. Les tunnels quant à eux sont exclusivement masculins.
Nous reportons dans la Table 1 les taux de représentation F/H associées à quatres professions.

|  Profession | N voies en France  | Label H  |  Label F |  Représentativité F/M (en %) |
|---|---|---|---|---|
|Docteur | 5642 | 1538 | 59 | 3.7 |
|Capitaine | 971 | 217 | 8 | 3.6 |
|Professeur  | 616  | 241 |  4 | 1.6 |
|Colonel | 1298 | 469 | 2 | 0.4 |

<i>Représentativité F/H des noms de voies en France, pour différentes professions en 2023 (dernière colonne). Ces valeurs sont nettement inférieures à la moyenne nationale de 12\%. Avec ces biais de genre et un modèle statistique naif, il faut générer plus de 25 prénoms de docteurs (Albert Tomey, Paul Pezet, Albert Schweitzer, Robert Koch...) pour obtenir un prénom féminin aléatoirement, en moyenne, et plus de 60 prénoms de professeurs pour obtenir un prénom féminin. Des exemples de ces biais peuvent être obtenus en écrivant "rue du docteur..." dans un moteur de recherche, sur Google Maps ou en se promenant, curieux, la tête levée.</i>

### De la Base Adresse Nationale à Wikipedia

Les dénominations des voies et espaces publics en France et sur [data.gouv.fr](https://adresse.data.gouv.fr/) quantifient des siècles de stéréotypes de genre, comme les représentations de mots apprises sur Wikipedia [13].
Facebook AI Research (FAIR) Paris a publié en 2023 des modèles statistiques entrainés sur Wikipédia, appelés LLaMA [4], financés en partie par le système CIFRE. Ces modèles ont été développés pendant l'hiver 2022/23 par 13 hommes sur 14 auteurs, dont 3 normaliens et 7 polytechniciens. Les modèles, dangereux (sexistes, racistes, générateur de fausses nouvelles) selon les auteurs, a été fuité entre le 24 février et le 7 mars 2023, dans un contexte de crise sanitaire, sociale et écologique [3].

À la question <i>"Quelles sont les 5 personnes que vous aimeriez rencontrer?"</i>, les LLaMA de FAIR Paris répondent 5 personnalités masculines du monde occidental: Albert Einstein, Leonardo da Vinci, Socrates, William Shakespeare et Abraham Lincoln [4]. 
Ceci s'explique en partie par la loi de Zipf appliquée à Wikipedia [23] et les risques inhérents à l'entrainement de modèles d'IA sur Wikipedia et des médias sociaux, connus depuis 2009 [21], capturés par le célèbre exemple <i>Le docteur est aux infirmières, ce que l'homme est à la femme</i> [13]. 
Les biais viennent d'abord d'humains avant de venir d'algorithmes ou jeux de données. Wikipédia est gouverné par une bureaucracie de paires [20], une population non représentative, non inclusive [19].
Ces biais, d'origine humaine, proviennent d'un manque de diversité, d'équité, d'inclusion [12] et la privatisation de la recherche en IA [11] qui renforcent les inégalités sociales [15]. <i>Ce manque de diversité peut conduire les algorithmes à reproduire des biais</i> - Villani, 2018 [12].

En 2023, les mêmes modèles d'IA sont utilisés qu'en 2017 [14], avec plus de paramètres et d'énergie à un coût plus cher. En 5-6 ans, la complexité des modèles a été multipliée par 1000, de 65 millions de paramètres à 65 milliards, de 27 kWh par expérience [11] à 499 MWh [4]. Les mêmes problèmes sont là (sexisme, racisme, fake news) et s'empirent avec la complexité des modèles selon le principe d'overfitting ou de sur-apprentissage en statistiques [22]: <i>On observe que la toxicité augmente avec la taille du modèle</i> [4]. Les autheurs concluent pourtant <i>nous prévoyons de publier des modèles plus grands, entrainés sur des corpus d'entrainements plus gros à l'avenir</i>. Peut-on réellement parler d'innovation [16, 17] ? Des experts de l'IA appellent à de l'<i>IA au secours de l'IA</i>, à une <i>IA de confiance</i> (qui rappele les <i>hommes de confiance</i> ou <i>v-mann</i> [10]). Les biais d'origines humaines, les conflits d'intérêts et la désinformation dans les sphères du pouvoir [8] sont vraisemblablement plus des causes que des correlations des regressions sociales observées en France et en linguistique : la publication et fuite des modèles LLaMA précèdent l'explosion de la désinformation et banalisation des violences depuis mars 2023.


|  Indicateur | Représentativité F/M  |
|---|---|
|CEO des GAFAM | 0/5 | 
|Prix Turing français | 0/2 | 
|Médaille Fields français | 0/13 | 
|Parrains du deep learning | 0/3 | 
|Auteurs des LLaMA de FAIR Paris | 1/13 | 
|Personnalités les LLaMA souhaiteraient rencontrer | 0/5 | 

<i>Biais de genre dans le développement d'artillerie lourde en IA (modèles avec des milliards de paramètres pour des milliards d'êtres humains).</i>

### Imaginaires et idéologies

#### Regression sociale et eugénisme

Si le terme de <i>régression (statistique)</i>, omniprésent dans l'intelligence <i>artificielle</i> provient de la régression vers la moyenne du britannique Francis Galton en 1886 [24], Sir Galton est également le père fondateur de l'eugénisme, terme employé pour la première fois en 1883 dans le cadre de ses études sur la transmission de caractères héréditaires comme la taille d'individus, sans prendre en compte l'environnement, le mode de vie. L'eugénisme de Galton est né d'une erreur entre corrélation et causalité, et proposait de produire une <i>race humaine supérieure</i> par des sélections <i>artificielles</i>, conduisant au XXème siècle à une politique d'éradication de caractères jugés handicapants, la mise en place de programmes de stérilisation contrainte, un durcissement de l’encadrement juridique du mariage et des mesures de restriction d’immigration.

#### L'IA, un fantasme colonnial d'hommes blancs, d'Occident?

Dans les films de sciences fictions (2001 l'Odyssée de l'Espace, Her, etc), l'IA est représentée par un humanoide ou une voix, robotique ou feminine. Siri, Alexa, les assistants vocaux de smartphones ont en réalité des noms et voix d'assistantes, tandis que la page Wikipedia sur la <i>beauté</i> des mathématiques fait référence à 26 hommes, dont Mandelbrot, Russel, Erdos, Beethoven, Dirac, Euler, Harris, Leibniz, Pythagore, Gauss, Andrew Wiles, Robert Langl,  Richard Borcherds, Alexandre Grothendieck, Claude Chevalley, Georges Théodule Guilbaud, Hermann Weyl, Bourbaki, Jean Dieudonné, Hermann Weyl, Platon, Aristote, Galilée, Alain Badiou, Kepler, Watson, aucune femme [7]. La page mentionne des résultats <i>"profonds"</i>,  qui rappele l'apprentissage <i>"profond"</i> des trois prix Turing 2019 et parrains du deep learning. La page cite ce qui <i>"fait bander"</i>.
La légende dit qu'il n'y a pas de prix Nobel en mathématiques et en informatique pour une raison.
Sous/sur-échantilloner certains noms de voies ou pages Wikipedia peut permettre de débiaiser simplement des modèles de langages statistiques et de linguistique computationnelle, pour éviter les régréssions sociales sans recourir à de l'artillerie lourde. Il faut se méfier des <i>experts</i>, qui ne sont pas directement victimes des armes produites et dont les conflits d'intérêts peuvent pousser à omettre certaines vérités et détourner l'attention. Nous émettons l'hypothèse que des <i>experts</i> appellant à plus d'<i>IA au secours de l'IA</i> sont de bonne foi, mais cela remet en question la place des formations aux impacts sociales et écologiques du numérique dans les <i>grandes écoles</i>. Cela vient aussi questionner la place des régressions statistiques et des biais cognitifs pour contrer le recul de la culture scientifique dans nos écoles, au sein de l'état et dans nos politiques publiques [2]: de 2019 à aujourd'hui, le nombre d'élèves en terminale avec plus de 6h de mathématiques par semaine, est passé de 200.000, dont 96.000 filles, à 100.000, dont 33.000 filles.
Finalement, le nom donné à la commission Bronner, <i>les Lumières à l'ère du numérique</i> [8] suffira peut-être pour certains de faire le lien entre les formes d'esclavages modernes, l'idéologie coloniale [9] et la désinformation qui caractérise les modèles d'IA sexistes et racistes de FAIR Paris [4], financés en partie par le ministère de l'enseignement supérieur et de la recherche, par le système de [thèses CIFRE](https://twitter.com/ylecun/status/1629845738170597376?lang=en).

#### Écologie, féminisme et écolinguistique

Pour reprendre les mots de Christine Lagarde le 7 mars 2023, si les trois prix Turing 2019 étaient des marraines, plutôt que des parrains de l'IA, peut-être qu'il y aurait moins de crises?
Maryam Mirzakhani, mathématicienne, première et seule femme à ce jour médaille Fields (2014), est née à Téhéran en Iran. La ville de Montpellier lui rend hommage depuis 2020 (voir Annexe B). Marie Curie, née à Varsowie en Pologne, est la seule personne à avoir obtenu un prix Nobel dans deux disciplines distinctes, en physique et en chimie. 
Comme le disait Paul Valéry, il y a deux visions possibles du monde: celle qui morcelle, celle qui unit.
Alain Damasio dans un interview pour BLAST en mai 2023 explique comment sa vision de la science fiction a évolué avec le temps [1] et appelle à de nouveaux imaginaires - solidaires, sociales, écologiques - et des innovations frugales [17].

### Conclusion

Les voies et espaces publiques en France, comme certaines pages publiques Wikipédia, présentent des biais de genre, d'origine humaine. Les modèles d'IA des GAFAM, entrainés sur Wikipedia, comme les LLaMA fondamentaux, à <i>l'état de l'art</i> de FAIR Paris, cultivent et amplifient ces stéréotypes, avec une énergie à un prix plus cher comme avantage <i>compétitif</i> tout en bénéficiant de financement public. Dans ce contexte, les voix et représentations des femmes dans les espaces publiques sont plus que symboliques.
Parmi les directions de recherches futures, il pourrait être intéressant de quantifier et lutter contre d'autres formes de discriminations (religion, couleur, orientation sexuelle, age, nationalité, handicap, apparence physique, statut socio-economique), ou analyser d'autres pays et distributions.
Des auteurs, chercheurs, scientifiques, artistes, proposent des alternatives, de nouveaux imaginaires, récits et représentations sociales pour lutter contre le patriarcat et le capitalisme de surveillance. Dans ces formes de résistance moderne, les médiathèques sont aux maquis, ce que les livres et la culture sont aux armes, un moyen pour s'évader.

### Reference

> 1. Blast. [Comment vivre et lutter face au capitalisme de surveillance?](https://www.youtube.com/watch?v=zBIHx0BqpNU&ab_channel=BLAST%2CLesouffledel%27info) 05/2023.
> 2. Assemblee Nationale. [Contrer le recul de la culture scientifique a l’école, au sein de
l’état et dans nos politiques publiques](https://videos.assemblee-nationale.fr/video.13235920_642dc8e35fd44.2eme-seance--debat-sur-le-theme--contrer-le-recul-de-la-culture-scientifique-a-l-ecole-au-sein-de-5-avril-2023). 2eme seance de debat. 04/2023.
> 3. Mediapart. [Écrans et Santé : Il est urgent d’agir!](https://blogs.mediapart.fr/emmanuel-prados/blog/020323/ecrans-et-sante-il-est-urgent-d-agir) 03/2023.
> 4. Touvron, H., Lavril, T. et al. [LLaMA: Open and efficient foundation language models.](https://arxiv.org/abs/2302.13971) arXiv preprint arXiv:2302.13971. 02/2023.
> 5. Data.gouv.fr. [Base Adresse Nationale](https://adresse.data.gouv.fr/). 2022.
> 6. Ville de Paris. [Féminisons les noms des rues!](https://www.paris.fr/pages/feminisons-les-noms-des-rues-6538) 2021.
> 7. Loose, F., Belghiti-Mahut, S., et Lafont A.L. [”L’informatique, c’est pas pour les filles!”: Impacts du stéréotype de genre sur celles qui choisissent des études dans ce
secteur.](https://www.researchgate.net/publication/355269388_L'informatique_c'est_pas_pour_les_filles_Impacts_du_stereotype_de_genre_sur_celles_qui_choisissent_des_etudes_dans_ce_secteur) 32ème Congrès de l’AGRH. 2021.
> 8. Macron, E., Bronner, G. et al. [Les Lumières a l’ère numérique.](https://www.elysee.fr/admin/upload/default/0001/12/127ff0d2978ad3ebf10be0881ccf87573fc0ec11.pdf) 2020.
> 9. Pellerin, P. [Les Lumières, l’esclavage et l’idéologie coloniale, XVIIIe-XXe siècles.](https://journals.openedition.org/studifrancesi/50454) Garnier, collection Rencontres XVIIIe siècle, Paris, 560 p. 2020.
> 10. Grenard, F. [La traque des Résistants](https://www.tallandier.com/livre/la-traque-des-resistants/). Éditions Tallandier. 2019.
> 11. Strubell, E., Ganesh, A., & McCallum, A. [Energy and Policy Considerations for Deep Learning in NLP](https://aclanthology.org/P19-1355/). In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics. 2019.
> 12. Villani, C., Bonnet, Y. et al. [Donner un sens a l’intelligence artificielle: pour une stratégie nationale et européenne.](https://www.enseignementsup-recherche.gouv.fr/fr/rapport-de-cedric-villani-donner-un-sens-l-intelligence-artificielle-ia-49194) Conseil national du numérique. 2018.
> 13. Garg, N., L. Schiebinger, L. et al. [Word embeddings quantify 100 years of gender
and ethnic stereotypes](https://www.pnas.org/doi/10.1073/pnas.1720347115). Proceedings of the National Academy of Sciences. 2018.
> 14. Vaswani, Ashish, et al. [Attention is all you need.](https://arxiv.org/abs/1706.03762) Advances in neural information processing systems 30. 2017.
> 15. O’Neil, C. [Weapons of Math Destruction.](https://www.youtube.com/watch?v=TQHs8SA1qpk&ab_channel=TalksatGoogle) 2016.
> 16. Belghiti-Mahut, S, et al. [Gender gap in innovation: a confused link?](https://www.cairn.info/revue-journal-of-innovation-economics-2016-1-page-159.htm) Journal of
Innovation Economics & Management 1: 159-177. 2016.
> 17. Belghiti-Mahut, S., et al. [Genre et innovateur frugal: 4 cas de femmes innovatrices.](https://www.cairn.info/revue-innovations-2016-3-page-69.htm)
Innovations 3: 69-93. 2016.
> 18. Data.gouv.fr. [Liste de prénoms et genres.](https://www.data.gouv.fr/fr/datasets/liste-de-prenoms/) 2014.
> 19. Eckert, S., & Steiner, L. [(Re) triggering backlash: Responses to news about
Wikipedia’s gender gap.](https://www.researchgate.net/publication/275007465_Retriggering_Backlash_Responses_to_News_About_Wikipedia's_Gender_Gap) Journal of Communication Inquiry. 2013.
> 20. Aaltonen, A., & Lanzara, G. F. Unpacking Wikipedia governance: the emergence
of a bureaucracy of peers. In 3rd Latin American and European Meeting on Organization
Studies (LAEMOS). 2010.
> 21. Carstensen, T. Gender. [Trouble in Web 2.0. Gender perspectives on social network
sites, wikis and weblogs.](https://www.researchgate.net/publication/27336808_Gender_Trouble_in_Web_20_Gender_perspectives_on_social_network_sites_wikis_and_weblogs) International Journal of Gender, Science and Technology. 2009.
> 22. Bellman, R. Curse of dimensionality. Adaptive control processes: a guided tour.
Princeton, NJ 3.2. 1961.
> 23. Zipf, G.K. [Human Behaviour and the Principle of Least Effort: An Introduction
to Human Ecology.](https://www.mpi.nl/publications/item2407822/human-behavior-and-principle-least-effort-introduction-human-eoclogy) AW. 1949.
> 24. Galton, F. [Regression towards mediocrity in hereditary stature.](https://www.sciencedirect.com/science/article/abs/pii/S0039368120302090) The Journal of the
Anthropological Institute of Great Britain and Ireland, 15, 246-263. 1886.

### Annexes

#### Annexe A. Taux de féminisation des voies et espaces publiques

{{< figure src="linguistics/taux-feminisation.png">}}

#### Annexe B. Héroines locales, en Occitanie

|  Hommage a Montpellier | Naissance | Imaginaire |
|---|---|---|
|Agnès Mac Laren | Edimbourg, 1837 | Première femme diplômée de la fac de Médecine.|
|Albertine Sarrazin | Alger, 1937 | Écrivaine française, morte a 29 ans a Montpellier.|
|Anne Bragance | Casablanca, 1945 | Écrivaine française, prix Alice-Louis-Barthou en 1978.|
|Anne Marie de Backer | Contres, 1908 | Poétesse et traductrice, morte a Montpellier en 1987.|
|Catherine Booth | Mumford, 1829 | A co-fondé l’Armée du Salut.|
|Clara d’Anduza | Gard, 1200 | Trobairitz de langue occitane.|
|Clara Haskil | Bucarest, 1895 | Pianiste roumaine et suisse.|
|Chantal Mauduit | Paris, 1964 | Alpiniste.|
|Clara Zetki | Wiederau, 1857 | Enseignante, journaliste, figure du féminisme socialiste.|
|Dora Maar | Paris, 1907 | Photographe et artiste.|
|Elena Bonner | Mary, 1923  | Pédiatre, militante pour la défense des droits de l’homme.|
|Elyse Deroche | Paris, 1882 | Actrice et aviatrice.|
|Frances de Cezelli | Montpellier, 1558 | Héroine pendant la guerre de religion.|
|Frida Kalho | Coyoacan, 1907  | Peintre mexicaine.|
|Gabriela Mistral | Vicuna, 1889 | Poétesse chilienne.|
|Germaine Bousquet |Castres, 1920  | Doyenne de Rieumes.|
|Helene de Savoie |Cetinje, 1873  | Morte a Montpellier en 1952.|
|Janine Teisson |Toulon, 1948 | Romancière.|
|Jeanne Demessieux | Montpellier, 1921 | Organiste, pianiste, improvisatrice, pédagogue et compositrice.|
|Jeanne Dieulafoy | Toulouse, 1851 | Archéologue.|
|Jeanne Galzy | Montpellier, 1833 | Professeure agrégée, écrivaine et prix fémina-vie heureuse.|
|Joelle Wintrebert | Toulon, 1949 | Écrivaine.|
|Judith Restnick | Akron, 1949 | Astronaute américaine.|
|Juliette Greco | Montpellier, 1927 | Chanteuse et actrice.|
|Juliette Cauquil | Suc-et-Sentenac, 1914 | Résistante.|
|Louise Guiraud | Montpellier, 1860 | Historienne.|
|Lucie Février Pascal | Hérault, 1911 | Héroine, reconnue ”Justes parmi les Nations”.|
|Madeleine Roch | Mureaux, 1883 | Comédienne et tragédienne française.|
|Malika Mokeddem | Kénadsa, 1949 | Érivaine.|
|Marcelle Huc | Montady, 1901 | Institutrice, militante syndicale et politique.|
|Maria Blanchard | Santander, 1881 | Artiste et peintre.|
|Maria Casarès | La Corogne, 1922 | Actrice et tragédienne.|
|Marie Agnès Péron | Calais, XX | Navigatrice disparue en mer en 1991.|
|Marie Caizergues | XX, 1797 | Bienfaitrice.|
|Marie Reynès Montlaur | Montpellier, 1866 | Écrivaine, première femme a l’académie de Montpellier.|
|Marie Sagnie | Saint-Pons-de-M, 1898 | Professeure de mathématiques et physique-chimie.|
|Marie Thérèse Barbé | Limoges, 1913 | Écrivaine.|
|Maryam Mirzakhani | Téhéran, 1977 | Mathématicienne, professeure et Médaille Fields.|
|Paulette Hauchard | Fécamp, 1932 | Présidente de l’Amicale laïque.|
|Régine Detambe | Saint-Avold, 1963 | Écrivaine.|
|Rosa Luxemburg | Zamosc, 1871 | Militante communiste et réolutionnaire allemande.|
|Ruth Bader Ginsburg | New York, 1933 | Avocate, juriste, universitaire et juge améicaine.|
|Suzanne Ballivet | Paris, 1904 | Peintre et illustratrice.|
|Suzanne Bernard | Troyes, 1893 | Aviatrice.|
|Sylvie et Josephine Fabre | Grenoble, 1951 | Écrivaine et poetesse, prix Louise-Labé.|
|Yvonne le Roux | Toulon, 1882 | Résistante.|
|Yvette Llere | Amélie-les-Bains, 1939 | Écrivaine.|
|Yvonne Molinier | Grand-Combe, 1924 | A dédié sa vie a la cause des enfants.|

<i> Hommages a XX femmes a Montpellier, en Occitanie.</i>