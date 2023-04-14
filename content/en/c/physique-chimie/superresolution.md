---
title: Super résolution
date: '2023-01-29'
type: book
weight: 30
tags:
  - Superresolution
---

From nuclear fusion to Sentinel-2 (MSc/PhD).

<!--more-->

{{< figure src="super-resolution/ESA Idea of the Week 2020-04-16.png">}}

<blockquote> The first winner of the weekly <a href="https://twitter.com/EuroDataCube?ref_src=twsrc%5Etfw">@EuroDataCube</a> #COVID19 Custom Script Contest has been announced<br>Michel Deudon from <a href="https://twitter.com/telecomparis">@TelecomParis_</a> <a href="https://twitter.com/Polytechnique?ref_src=twsrc%5Etfw">@Polytechnique</a> uses unsupervised machine learning to extract boat traffic from Sentinel-2 🇪🇺🛰imagery &amp; monitor shifts in transportation patterns #AI< - 🇪🇺 <a href="https://twitter.com/defis_eu/status/1250769302577389568">@defis_eu</a> April 16, 2020
</blockquote>

## V for Vegetation

{{< icon name="calendar" pack="fas" >}} Nov 1, 2018 - June 1, 2019. Proba-V super resolution challenge. [kelvins.esa.int](https://kelvins.esa.int/proba-v-super-resolution/problem/).

In March 2019, I joined Element AI, <i>AI for Good</i>, on a permanent contract in London, a startup co-founded by Yoshua Bengio, after doing an internship in 2017 in Montreal in [combinatorial optimization]( https://hanalog.ca/wp-content/uploads/2018/11/cpaior-learning-heuristics-6.pdf) and returning there in 2018 to present an article in [linguistics](https://proceedings.neurips.cc/paper_files/paper/2018/file/97e8527feaf77a97fc38f34216141515-Paper.pdf) and have my interviews.

{{< figure src="super-resolution/ESA Kelvin Day - 2019-09-16.png">}}

<blockquote>Throwback to <a href="https://twitter.com/esa?ref_src=twsrc%5Etfw">@ESA</a>&#39;s first Kelvins Day where the finalists of the <a href="https://twitter.com/hashtag/ProbaV?src=hash&amp;ref_src=twsrc%5Etfw">#ProbaV</a> super resolution challenge presented their achievements with mixtures of classical &amp; #AI image processing techniques to upscale <a href="https://twitter.com/hashtag/ProbaV?src=hash&amp;ref_src=twsrc%5Etfw">#ProbaV</a> data.<br>Congrats to Polytecnico di Torino for their winning solution.🛰️👏 - <a href="https://twitter.com/PROBAVegetation/status/1173540928600117248">@PROBAVegetation</a> September 16, 2019
</blockquote>

In September 2019, after the [Series B fundraising with McKinsey and Co](https://www.cdpq.com/fr/actualites/communiques/element-ai-recueille-200m-ca-1514m-us-de-serie-b-pour-transformer-les), I was layed off, for economic reasons. One year later, [ServiceNow](https://techcrunch.com/2020/11/30/servicenow-is-acquiring-element-ai-the-canadian-startup-building-ai-services-for-enterprises/) acquired Element AI. Several colleagues experienced depression, as Manon Gruaz talks about in her talk [CTRL+ALT+DEPRESSION](https://www.youtube.com/watch?v=MN3D0uLEERU&ab_channel=GDGFrance) at DevFest de Nantes 2022.

### From low to high resolution

{{< figure src="super-resolution/img3.png" caption="Deudon, Michel, Alfredo Kalaitzis, Israel Goytom, Md Rifat Arefin, Zhichao Lin, Kris Sankaran, Vincent Michalski, Samira E. Kahou, Julien Cornebise, and Yoshua Bengio. HighRes-net: Multi Frame Super Resolution by Recursive Fusion. [arxiv preprint arXiv:2002.06460 (2020)](https://arxiv.org/abs/2002.06460). Design by [Manon Gruaz](https://manongruaz.com/).">}}

Without taking into account the real costs, the complexity of the algorithms, the consumption of the models, AI research helps gain 1% with 10 to 100 times more energy. On the example of the [European Space Agency competition](https://kelvins.esa.int/proba-v-super-resolution/leaderboard/results),
- Baseline without AI. rating 1.0
- Model without AI. score 0.95 @ledzeppelin
- [HighResNet](https://arxiv.org/abs/2002.06460). score 0.94 @rarefin (logarithmic complexity)
- DeepSUM. score 0.94 @superpip (linear complexity, 1st in 2019)
- TR-MISM. score 0.93 (quadratic complexity, 1st in 2022)

## From Proba-V to Sentinel-2

With Brexit and the Covid, I returned to France. On 06/04/2020, the European Space Agency (ESA) launched a competition on the use of satellite images in connection with the COVID-19 crisis. Each week, a prize of €1,000 was awarded.

> <i>My goal was to reveal more details from public imagery to raise awareness of the marine environment and its protection.</i> Venise sans les bateaux. [Cnes.fr](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux) May 6, 2020.

The idea finished [3rd in the final ranking](https://medium.com/sentinel-hub/race-upscaling-competition-results-8a339bb8c942), and was therefore not retained, only the first two projects have been selected for the final dashboard for the European Commission. The favorite project was developed by Henrik Fisser at the end of his internship at Brockmann Consult, with the help of [Euro Data Cube](https://github.com/hfisser/Truck_Detection_Sentinel2_COVID19/commit/48bc8ab4cc431d8a044093cbd8c0385aff5511be), partner organizations of the competition for ESA (conflicts of interest?).

My idea and algorithms were initially motivated by the United Nations Decade of Ocean Science for Sustainable Development (2021-2030, [UNESCO](https://fr.unesco.org/ocean-decade)) and the need to raise awareness / protect maritime areas and the Oceans, but Covid has diverted attention from ecological concerns. I ended up returning to studies in September 2020, at the College des Ingénieurs, to have a minimum source of income.

{{< figure src="super-resolution/img4.png" caption="Venise sans les bateaux. [Cnes.fr](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux). May 6, 2020.">}}

<blockquote>#Covid19 Venise sans les bateaux, observée par les satellites européens <a href="https://twitter.com/hashtag/Sentinel2?src=hash&amp;ref_src=twsrc%5Etfw">#Sentinel2</a> 🛰️🇪🇺 <a href="https://twitter.com/CopernicusEU?ref_src=twsrc%5Etfw">@copernicuseu</a> - <a href="https://twitter.com/CNES/status/1261594992839208960">@CNES</a> May 16, 2020
</blockquote>

## Acknowledgments
Grateful to [Manon Gruaz](https://manongruaz.com/), [Elena Aversa](https://densitydesign.org/person/elena-aversa/) for the information design, as well as [Gaëlle Lahoreau](https://www.centre-valdeloire.fr/comprendre/lassemblee-regionale/annuaire-des-elus/lahoreau-gaelle), [Sabina Dolenc](https://medium.com/sentinel-hub/race-upscaling-competition-results-8a339bb8c942) and [Carre4](https://medium.com/carre4/monitoring-boat-traffic-with-public-satellites-be1c48d87802) for communications.

## Références
- CNES. [Venise sans les bateaux](https://spacegate.cnes.fr/fr/covid-19-venise-sans-les-bateaux). May 2020.
- WWF. [Failing SDG14](https://www.wwf.eu/?uNewsID=360550): EU on a cliff edge for ensuring a sustainable ocean. March 2020.
- UN. [Sustainable Development Goal 14](https://sdgs.un.org/fr/goals/goal14): Conserve and sustainably use the oceans, seas and marine resources for sustainable development. 2015.
- Convention on Biological Diversity. [Aichi Biodiversity Targets](https://www.cbd.int/sp/targets/). 2011.
- The use of the Normalized Difference Water Index (NDWI) in the delineation of open water features. International Journal of Remote Sensing. [Harvard](https://ui.adsabs.harvard.edu/abs/1996IJRS...17.1425M/abstract). 1996.