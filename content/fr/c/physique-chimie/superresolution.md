---
title: Super résolution
date: '2023-01-29'
type: book
weight: 50
tags:
  - Superresolution
---

De la fusion nucléaire à Proba-V et Sentinel-2 (M2/PhD).

<!--more-->

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Le premier gagnant du concours hebdomadaire <a href="https://twitter.com/EuroDataCube?ref_src=twsrc%5Etfw">@EuroDataCube</a> <a href="https://twitter.com/hashtag/COVID19?src=hash&amp;ref_src=twsrc%5Etfw">#COVID19</a> de script personnalisé a été annoncé <br>Michel Deudon de @TelecomParis_ <a href="https://twitter.com/Polytechnique?ref_src=twsrc%5Etfw">@Polytechnique</a> utilise l'apprentissage non supervisé pour extraire le trafic de bateaux à partir d'images Sentinel-2 🇪🇺🛰 &amp; surveiller les changements dans les habitudes de transport <a href="https://twitter.com/hashtag/AI?src=hash&amp;ref_src=twsrc%5Etfw">#IA</a> <a href="https://t.co/RNGQJsqVKC">pic.twitter.com/RNGQJsqVKC</a></p>&mdash; 🇪🇺 DG DEFIS #StrongerTogether (@defis_eu) <a href="https://twitter.com/defis_eu/status/1250769302577389568?ref_src=twsrc%5Etfw">April 16, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Proba-V, V pour Végétation

{{< icon name="calendar" pack="fas" >}} 1 nov 2018 - 1 juin 2019. Proba-V super resolution challenge. [kelvins.esa.int](https://kelvins.esa.int/proba-v-super-resolution/problem/).

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Retour sur <a href="https://twitter.com/esa?ref_src=twsrc%5Etfw">@ESA</a>&#39;s premier jour Kelvin où les finalistes du défi de super résolution <a href="https://twitter.com/hashtag/ProbaV?src=hash&amp;ref_src=twsrc%5Etfw">#ProbaV</a> ont présenté leurs réalisations avec des mélanges de techniques de traitement d'image classiques &amp; de traitement d'images <a href="https://twitter.com/hashtag/AI?src=hash&amp;ref_src=twsrc%5Etfw">#IA</a> pour améliorer les données <a href="https://twitter.com/hashtag/ProbaV?src=hash&amp;ref_src=twsrc%5Etfw">#ProbaV</a>.<br>Félicitations à Polytecnico di Torino pour leur solution gagnante.🛰️👏 <a href="https://t.co/7v9l9xZdxj">pic.twitter.com/7v9l9xZdxj</a></p>&mdash; PROBA-V (@PROBAVegetation) <a href="https://twitter.com/PROBAVegetation/status/1173540928600117248?ref_src=twsrc%5Etfw">September 16, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

En mars 2019, j'ai rejoint Element AI, <i>AI for Good</i>, en CDI à Londres, après avoir fait un stage en 2017 à Montréal en [optimisation combinatoire](https://hanalog.ca/wp-content/uploads/2018/11/cpaior-learning-heuristics-6.pdf) et y être retourné en 2018 pour présenter mon mémoire de master en [linguistique](https://proceedings.neurips.cc/paper_files/paper/2018/file/97e8527feaf77a97fc38f34216141515-Paper.pdf) et passer mes entretiens. Six mois plus tard, en septembre 2019, après la [levée de fonds avec McKinsey et Co](https://www.cdpq.com/fr/actualites/communiques/element-ai-recueille-200m-ca-1514m-us-de-serie-b-pour-transformer-les), j'ai été licencié, pour motif économique, de la startup co-fondée par Yoshua Bengio et acquise par [ServiceNow](https://techcrunch.com/2020/11/30/servicenow-is-acquiring-element-ai-the-canadian-startup-building-ai-services-for-enterprises/) en novembre 2020. Parmi les collègues qui sont restés dans la startup, plusieurs sont tombés en dépressions comme en parle Manon Gruaz dans son talk [CTRL+ALT+DEPRESSION](https://www.youtube.com/watch?v=MN3D0uLEERU&ab_channel=GDGFrance) au DevFest de Nantes 2022.

### De basse à haute résolution, avec plusieurs captures

{{< figure src="super-resolution/img3.png" caption="HighRes-net: Multi Images Super Resolution par Fusion Récursive. [arxiv](https://arxiv.org/abs/2002.06460).">}}

Sans prendre en compte les coûts réels de la recherche, la complexité des algorithmes, la consommation des modèles, on optimise pour gagner quelques points sans vraie valeur ajoutée. Sur l'exemple du concours de l'Agence Spatiale Européenne,
- Baseline sans IA. score 1.0
- HighResNet (complexité logarithmique). score 0.94
- DeepSUM (complexité linéaire). score 0.94 (1er en 2019)
- TR-MISM (complexité quadratique). score 0.93 (1er en 2022)
Pour 1% d'écart, la recherche en IA est devenue est une course à polluer et consommer toujours plus d'énergie sans réelle justification.

## Appliqué à Sentinel-2

Avec le Brexit et le Covid, je suis rentré en France. Le 06/04/2020, l’agence spatiale européenne (ESA) a lancé un concours sur l’utilisation des images satellites en lien avec la crise COVID-19. Chaque semaine, un prix de 1 000 € est décerné. J'étais [le 1er gagnant français](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux)!

Mon idée a fini 3e dans le classement final des idées pour la Commission Européenne, par Brockmann Consult, Euro Data Cube et les organisations partenaires du concours ESA x SentinelHub. Mon idée n'a en conséquence pas été retenu, seul les deux premiers projets ont été séléctionnés pour le dashboard final de la Commission Européenne. Le projet coup de coeur a été développé par Henrik Fisser à la fin de son stage chez Brockmann Consult et avec l'aide d'[Euro Data Cube](https://github.com/hfisser/Truck_Detection_Sentinel2_COVID19/commit/48bc8ab4cc431d8a044093cbd8c0385aff5511be) sur Github (conflits d'intérêts des organisateurs du concours). 

> <i>Mon objectif était de révéler plus de détails à partir de l'imagerie publique pour sensibiliser à l’environnement marin et sa protection</i>. Venise sans les bateaux. [Cnes.fr](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux)

Mon idée et mes algorithmes étaient initialement motivés par la décennie des Nations Unies sur les sciences océaniques pour le développement durable ({{< icon name="calendar" pack="fas" >}}  2021-2030, [unesco.org](https://fr.unesco.org/ocean-decade)) et le besoin de sensibiliser / surveiller les zones maritimes protégées et les Océans, mais le Covid a détourné l'attention des préoccupations écologiques. J'ai repris des études au Collège des Ingénieurs en septembre pour m'assurer une source de revenues.

{{< figure src="super-resolution/img4.png" caption="Venise sans les bateaux. [spacegate.cnes.fr](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux).">}}

<blockquote class="twitter-tweet"><p lang="fr" dir="ltr"><a href="https://twitter.com/hashtag/Covid19?src=hash&amp;ref_src=twsrc%5Etfw">#Covid19</a> Venise sans les bateaux, observée par les satellites européens <a href="https://twitter.com/hashtag/Sentinel2?src=hash&amp;ref_src=twsrc%5Etfw">#Sentinel2</a> 🛰️🇪🇺 <a href="https://twitter.com/CopernicusEU?ref_src=twsrc%5Etfw">@copernicuseu</a> <a href="https://t.co/0nqgYFQikl">https://t.co/0nqgYFQikl</a> <a href="https://t.co/6ClxLaeHAx">pic.twitter.com/6ClxLaeHAx</a></p>&mdash; CNES (@CNES) <a href="https://twitter.com/CNES/status/1261594992839208960?ref_src=twsrc%5Etfw">May 16, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Références
- Tweets. @[defis_eu](https://twitter.com/defis_eu/status/1250769302577389568) @[CNES](https://twitter.com/CNES/status/1261594992839208960)
- Medium. @[Carre4](https://medium.com/carre4/monitoring-boat-traffic-with-public-satellites-be1c48d87802) @[sentinel-hub](https://medium.com/sentinel-hub/race-upscaling-competition-results-8a339bb8c942) 
- Cnes.fr. [Venise sans les bateaux](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux)

## Remerciements
<b>Communication and information design</b>
- [Manon Gruaz](https://manongruaz.com/)
- [Elena Aversa](https://densitydesign.org/person/elena-aversa/)