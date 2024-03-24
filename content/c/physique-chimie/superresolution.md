---
title: Super résolution
date: '2023-01-29'
type: book
weight: 50
tags:
  - Superresolution
---

De la fusion nucléaire à Sentinel-2 (M1/M2).

<!--more-->

{{< figure src="super-resolution/ESA Idea of the Week 2020-04-16.png">}}

<blockquote> Le premier gagnant du concours hebdomadaire <a href="https://twitter.com/EuroDataCube?ref_src=twsrc%5Etfw">@EuroDataCube</a> #COVID19 de script personnalisé a été annoncé <br>Michel Deudon de <a href="https://twitter.com/telecomparis">@TelecomParis_</a> <a href="https://twitter.com/Polytechnique?ref_src=twsrc%5Etfw">@Polytechnique</a> utilise l'apprentissage non supervisé pour extraire le trafic de bateaux à partir d'images Sentinel-2 🇪🇺🛰 &amp; surveiller les changements dans les habitudes de transport #IA - 🇪🇺 <a href="https://twitter.com/defis_eu/status/1250769302577389568">@defis_eu</a> 16 avril 2020
</blockquote>

## V pour Végétation

{{< icon name="calendar" pack="fas" >}} 1 nov 2018 - 1 juin 2019. Proba-V super resolution challenge. [kelvins.esa.int](https://kelvins.esa.int/proba-v-super-resolution/problem/).

En mars 2019, j'ai rejoint Element AI, <i>AI for Good</i>, en CDI à Londres, startup co-fondée par Yoshua Bengio, après avoir fait un stage en 2017 à Montréal en [optimisation combinatoire](https://hanalog.ca/wp-content/uploads/2018/11/cpaior-learning-heuristics-6.pdf) et y être retourné en 2018 pour présenter un article en [linguistique](https://proceedings.neurips.cc/paper_files/paper/2018/file/97e8527feaf77a97fc38f34216141515-Paper.pdf) et passer mes entretiens.

{{< figure src="super-resolution/ESA Kelvin Day - 2019-09-16.png">}}

<blockquote> Retour sur <a href="https://twitter.com/esa?ref_src=twsrc%5Etfw">@ESA</a>&#39; premier jour Kelvin où les finalistes du défi de super résolution <a href="https://twitter.com/hashtag/ProbaV?src=hash&amp;ref_src=twsrc%5Etfw">#ProbaV</a> ont présenté leurs réalisations avec des mélanges de techniques de traitement d'image classiques &amp; de traitement d'images #IA pour améliorer les données <a href="https://twitter.com/hashtag/ProbaV?src=hash&amp;ref_src=twsrc%5Etfw">#ProbaV</a>.<br>Félicitations à Polytecnico di Torino pour leur solution gagnante.🛰️👏 - <a href="https://twitter.com/PROBAVegetation/status/1173540928600117248">@PROBAVegetation</a> 16 septembre 2019
</blockquote>

En septembre 2019, après la [levée de fonds avec McKinsey et Co](https://www.cdpq.com/fr/actualites/communiques/element-ai-recueille-200m-ca-1514m-us-de-serie-b-pour-transformer-les), j'ai été licencié, pour motif économique. Un an plus tard, [ServiceNow](https://techcrunch.com/2020/11/30/servicenow-is-acquiring-element-ai-the-canadian-startup-building-ai-services-for-enterprises/) a fait l'acquisition d'Element AI. Plusieurs collègues sont tombés en dépressions comme en parle Manon Gruaz dans [CTRL+ALT+DEPRESSION](https://www.youtube.com/watch?v=MN3D0uLEERU&ab_channel=GDGFrance) au DevFest de Nantes 2022.

## De Proba-V à Sentinel-2

Avec le Brexit et le Covid, je suis rentré en France. Le 06/04/2020, l’agence spatiale européenne (ESA) a lancé un concours sur l’utilisation des images satellites en lien avec la crise COVID-19. Chaque semaine, un prix de 1 000 € était décerné et les gagnants avaient l'opportunité de passer à l'échelle.

Ma preuve de concept a fini [3e dans le classement final](https://medium.com/sentinel-hub/race-upscaling-competition-results-8a339bb8c942), et n'a en conséquence pas été retenu, seul les deux premiers projets ont été séléctionnés pour le dashboard final pour la Commission Européenne. Le projet coup de coeur a été développé par Henrik Fisser à la fin de son stage chez Brockmann Consult, organisation partenaire du concours pour ESA (potentiel conflit d'intérêts).

Mon idée et mes algorithmes étaient initialement motivés par la décennie des Nations Unies sur les sciences océaniques pour le développement durable (2021-2030, [UNESCO](https://fr.unesco.org/ocean-decade)), le besoin de sensibiliser à l’environnement marin, et protéger les zones maritimes et les Océans, mais le Covid a détourné l'attention des préoccupations écologiques. J'ai fini par reprendre des études en septembre 2020, au Collège des Ingénieurs, pour m'assurer une source de revenues minimum.

{{< figure src="super-resolution/img4.png" caption="Venise sans les bateaux. [Cnes.fr](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux). 6 mai 2020.">}}

<blockquote>#Covid19 Venise sans les bateaux, observée par les satellites européens <a href="https://twitter.com/hashtag/Sentinel2?src=hash&amp;ref_src=twsrc%5Etfw">#Sentinel2</a> 🛰️🇪🇺 <a href="https://twitter.com/CopernicusEU?ref_src=twsrc%5Etfw">@copernicuseu</a> <a href="https://t.co/0nqgYFQikl">https://t.co/0nqgYFQikl</a> - <a href="https://twitter.com/CNES/status/1261594992839208960">@CNES</a> 16 mai 2020
</blockquote>

## Remerciements
Remerciements à [Manon Gruaz](https://manongruaz.com/) et [Elena Aversa](https://densitydesign.org/person/elena-aversa/) pour le design de l'information, ainsi que [Gaëlle Lahoreau](https://www.centre-valdeloire.fr/comprendre/lassemblee-regionale/annuaire-des-elus/lahoreau-gaelle) et [Sabina Dolenc](https://medium.com/sentinel-hub/race-upscaling-competition-results-8a339bb8c942).

## Références
- CNES. [Venise sans les bateaux](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux). Mai 2020.
- WWF. [Failing SDG14](https://www.wwf.eu/?uNewsID=360550): EU on a cliff edge for ensuring a sustainable ocean. Mars 2020.
- UN. [Sustainable Development Goal 14](https://sdgs.un.org/fr/goals/goal14): Conserve and sustainably use the oceans, seas and marine resources for sustainable development. 2015.
- Convention on Biological Diversity. [Aichi Biodiversity Targets](https://www.cbd.int/sp/targets/). 2011.
- The use of the Normalized Difference Water Index (NDWI) in the delineation of open water features. International Journal of Remote Sensing. [Harvard](https://ui.adsabs.harvard.edu/abs/1996IJRS...17.1425M/abstract). 1996.