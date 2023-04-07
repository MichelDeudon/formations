---
title: Repérer le greenwashing et les conflits d’intérêts
date: '2023-02-24'
type: book
weight: 30
tags:
  - énergie
  - climat
  - désinformation
---

Quel est le but des climatosceptiques? Que défendent-ils? Études de cas des modèles LLaMA et ChatGPT.

<!--more-->

## La désinformation sert à détourner l’attention de l’urgence écologique…

Sur Twitter (acheté par Elon Musk en xxxx), plus de 10 000 comptes climatosceptiques actifs relaient des fausses informations [CNRS](https://lejournal.cnrs.fr/articles/climatosceptiques-sur-twitter-enquete-sur-les-mercenaires-de-lintox).

Le but de la désinformation comme [business](https://www.bfmtv.com/tech/intelligence-artificielle/le-patron-de-l-entreprise-a-l-origine-de-chat-gpt-a-un-peu-peur-de-chat-gpt_AV-202303210270.html) est de détourner l’attention et influencer les décisions, par exemple dans quoi [investir](https://www.bpifrance.fr/nos-actualites/rencontres-economiques-daix-en-provence-un-regard-sur-le-monde-demain), de quoi [débattre](https://www.bfmtv.com/tech/intelligence-artificielle/pour-la-premiere-fois-l-assemblee-nationale-va-debattre-d-un-amendement-redige-par-chat-gpt_AV-202303210310.html), etc. Lorsqu’elle est toxique et virale, elle génère plus de clics (Click Through Rate en anglais) et appelle à plus de deeptech...

Ainsi, les développements d'IA pendant l'automne hiver 2022/2023 - [Galactica 120B](https://huggingface.co/facebook/galactica-120b), ChatGPT3, LLaMA 65B, ChatGPT4 - et la désinformation a permis de détourner l'attention des CEO au [Forum Économique Mondial](https://www.reuters.com/technology/davos-2023-ceos-buzz-about-chatgpt-style-ai-world-economic-forum-2023-01-17/) pour investir dans l'armement au profit de HuggingFace, les GAFAMs, NVIDIA, etc.

En mars 2023, TF1 parle de menaces de l'IA sur les emplois, de risques des voitures autonomes... l'écologie et la jeunesse ne sont pas mentionnés.
Le [MIT](https://www.technologyreview.com/2019/02/14/137426/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/) alertait pourtant en 2019 du risque qu'IA une qui écrit une prose convaincante risquerait de produire en masse de fausses nouvelles, faisant référence à ChatGPT2. Cela n'a empêché les investissments de se multiplier dans la désinformation, la consommation énergétique (x1000 en 4 ans) et la génération de fausses nouvelles.

### Ressources pour lutter contre le greenwashing
- Le guide anti greenwashing de [Pour un Réveil Ecologique](https://pour-un-reveil-ecologique.org/fr/les-entreprises-nous-repondent/#guide-anti-greenwashing)
- L'outil en ligne anti greenwashing de l'[ADEME](https://communication-responsable.ademe.fr/antigreenwashing)

## [Présentation de LLaMA : un modèle de langage fondamental de 65 milliards de paramètres](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)
{{< icon name="calendar" pack="fas" >}} Fév 2023. Le blog de Meta AI / FAIR Paris est une {{<hl>}}perle de greenwashing{{</hl>}}.

Dans le cadre de l'engagement de Meta en faveur de la science ouverte, nous publions aujourd'hui LLaMA (Large Language Model Meta AI), un modèle de langage fondamental à l’état de l’art conçu pour aider les chercheurs à faire progresser leurs travaux dans ce sous-domaine de l'IA. {{<hl>}}Des modèles <b>plus petits</b> et plus performants tels que LLaMA{{</hl>}} permettent à d'autres membres de la communauté de recherche qui n'ont pas accès à de grandes quantités d'infrastructures d'étudier ces modèles, démocratisant davantage l'accès dans ce domaine important et en évolution rapide.

{{<hl>}}L'entraînement de modèles fondamentaux <b>plus petits</b> comme LLaMA est souhaitable{{</hl>}} dans le champ des large language model, car {{<hl>}}ça nécessite beaucoup <b>moins de puissance de calcul et de ressources</b>{{</hl>}} pour tester de nouvelles approches, valider le travail des autres et explorer de nouveaux cas d'utilisation. Les modèles fondamentaux sont entraînés sur un vaste ensemble de données non étiquetées, ce qui les rend idéaux pour être ajusté à une variété de tâches. Nous rendons LLaMA disponible en plusieurs tailles (paramètres 7B, 13B, 33B et 65B) et partageons également une carte du modèle LLaMA qui détaille comment nous avons construit le modèle conformément à notre approche des {{<hl>}}<b>pratiques d'IA responsable</b>{{</hl>}}.

{{< figure src="meta-paper-hours-gpu.png" caption="Empreinte carbone de différents modèles entrainés dans le même centre de données, de l'article LLaMA sur [Arxiv](https://arxiv.org/abs/2302.13971) (section 6 Empreinte carbone).">}}

{{< callout warning >}}
<i>L'entraînement de nos modèles a consommé une quantité massive d'énergie, responsable de l'émission de dioxyde de carbone.</i> (section 6 Empreinte carbone). <i>Nous prévoyons de publier à l'avenir des modèles plus grands, entrainés sur des corpus plus importants</i> (section 8 Conclusion). [Arxiv](https://arxiv.org/abs/2302.13971).
{{< /callout >}}

{{< callout note >}}
Aucune communication n'est faite sur [le blog](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/) de Meta AI Research, sur les [réseaux sociaux](https://www.linkedin.com/posts/yann-lecun_github-facebookresearchllama-inference-activity-7034956639526952960-B1-d?trk=public_profile_like_view) ou sur [Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732 ) concernant l'empreinte carbone record, l'impact environnemental et le financement du modèle LLaMA.
{{< /callout >}}

{{<hl>}}Des modèles <b>plus petits</b>{{</hl>}} entraînés sur plus de jetons - qui sont des morceaux de mots - sont {{<hl>}}<b>plus faciles</b> à réentraîner et affiner{{</hl>}} pour des cas d'utilisation potentiels et spécifiques de produits. Nous avons entraîné LLaMA 65B et LLaMA 33B sur 1,4 trilliard de jetons. Notre {{<hl>}}<b>plus petit</b> modèle{{</hl>}}, LLaMA 7B, est formé sur un trilliard de jetons…

{{< callout note >}}
En réalité on change d’échelle. Millions, milliards, trilliards... C’est x1000 en complexité en 4 ans.
{{< /callout >}}

Il reste encore des recherches à faire pour traiter les risques de biais, de commentaires toxiques et d'hallucinations dans les grands modèles de langage. Comme d'autres modèles, LLaMA partage ces défis... Nous fournissons également dans l'article un ensemble d'évaluations sur les biais et la toxicité du modèle pour montrer les limites du modèle et pour soutenir la poursuite des recherches dans ce domaine crucial.

{{<hl>}}Pour maintenir l'<b>intégrité</b> et prévenir les <b>abus</b>{{</hl>}}, nous publions notre modèle sous une licence non commerciale axée sur les cas d'utilisation de la recherche. L'accès au modèle sera accordé au cas par cas aux chercheurs universitaires; ceux affiliés à des organisations du gouvernement, de la société civile et du milieu universitaire; et les laboratoires de recherche de l'industrie à travers le monde...

{{< callout warning >}}
08 mars 2023. [Fuite du modèle](https://www.01net.com/actualites/fuite-meta-alternative-chatgpt-meta-partagee-forum.html). Intégrité et prévention des abus? Fausses nouvelles et modèle économique?
{{< /callout >}}

## [Considérations éthiques sur Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732bd/MODEL_CARD.md)
- Organisation développant le modèle: L'équipe FAIR de Meta AI.
- Date du modèle: LLaMA a été entraîné entre décembre 2022 et février 2023.
- Version du modèle: Il s'agit de la version 1 du modèle.
- Données: Les données utilisées pour entraîner le modèle sont collectées à partir de diverses sources, principalement du Web. En tant que tel, il contient un contenu offensant, préjudiciable et biaisé. Nous nous attendons à ce que le modèle présente de tels biais.
- Risques et préjudices: Les risques et préjudices des grands modèles linguistiques incluent la génération de contenu nuisible, offensant ou biaisé. Ces modèles sont souvent susceptibles de générer des informations incorrectes. Nous ne nous attendons pas à ce que notre modèle soit une exception à cet égard.
- Cas d'utilisation: LLaMA est un modèle fondamental et, en tant que tel, il ne doit pas être utilisé pour des applications sans une enquête plus approfondie et une atténuation des risques. Ces risques et cas d'utilisation potentiellement dangereux incluent, mais sans s'y limiter : la <b>génération de fausses informations</b> et la <b>génération de contenu nuisible, biaisé ou offensant</b>.

### 💧 Crise climatique
- 15-02 <b style="color:red;">CNRS</b>. Climatosceptiques: sur Twitter, enquête sur les mercenaires de l’intox [cnrs.fr](https://lejournal.cnrs.fr/articles/climatosceptiques-sur-twitter-enquete-sur-les-mercenaires-de-lintox) [Le Monde](https://www.lemonde.fr/planete/article/2023/02/13/la-france-fait-face-a-un-fort-regain-de-climatoscepticisme-sur-twitter_6161691_3244.html) @[Audrey Garric](https://twitter.com/audreygarric/status/1625416947729944579?cxt=HHwWhsC-1cSG0o4tAAAA).
- 31-12 (2022) <b style="color:blue;">Emmanuel Macron</b> <i>Qui aurait pu prédire la crise climatique?</i> [archive INA](https://www.youtube.com/watch?v=SsqYCvJvxQY&ab_channel=INAPolitique).

## [Lutter contre le changement climatique avec l'IA](https://arxiv.org/abs/1906.05433)

L'article original est publié sur [Arxiv](https://arxiv.org/abs/1906.05433v1) le 10 juin 2019, quatre jours après l'alerte d'[Emma Strubell](https://arxiv.org/abs/1906.02243) et du [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) en 2019. Écrit par 22 auteurs dont <b>Demis Hassabis</b>, CEO de <b>Deepmind</b>, et <b>Yoshua Bengio</b>, prix <b>Turing</b> 2019 et parrain du deep learning, il est republié le 7 février 2022 par l'[Association for Computing Machinery](https://dl.acm.org/doi/10.1145/3485128) (ACM) qui remet le prix Turing. En décembre 2022, alors que Yann Lecun et Elon Musk travaillent sur des modèles avec des milliards de paramètres (1000 fois l'alerte du [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) de 2019), un workshop est organisé par climatechange.ai à [NeurIPS 2022](https://www.climatechange.ai/events/neurips2022) et inclut 19 auteurs de <b style='color:blue;'>NVIDIA</b> qui tire profit de l'explosion de la complexité des modèles.

Les projecteurs durant ces années étaient braqués sur les parrains du <i>deep learning</i>, au profit des GAFAMs et de NVIDIA, leader mondial du calcul en intelligence artificielle. 

## Recherche et cadeaux en IA

Les cadeaux influencent la recherche en IA pour continuer d'entrainer des modèles toujours plus complexes, au profit des <b style='color:blue;'>GAFAM</b> et <b style='color:blue;'>NVIDIA</b>.
L'article [Seize têtes valent-elles vraiment mieux qu'une?](https://arxiv.org/abs/1905.10650) soumis sur [Arxiv](https://arxiv.org/abs/1905.10650) le 25 mai 2019 et accepté à NeurIPS 2019 a été co-écrit par un alumni de l'École Polytechnique (X13) qui écrit dans les remerciements <i> Nous sommes particulièrement reconnaissants à <b>Thomas Wolf</b> de <b style='color:blue;'>Hugging Face</b>, dont les efforts de reproduction indépendants nous ont permis de trouver et de corriger un bug... Cette recherche a été financée en partie par un cadeau de <b style='color:blue;'>Facebook</b>.</i>

## En juin 2022, ENGIE premier client

<i><b style='color:blue;'>Deep Mind</b> a appliqué des algorithmes de ML pour prédire l'énergie éolienne. <b style='color:blue;'>Google</b> a annoncé que cet algorithme pouvait prédire la production d'énergie éolienne trente-six heures à l'avance. En juin, <b>ENGIE</b> (une société française) a été annoncée comme le premier client du projet</i>. [Towards Data Science](https://towardsdatascience.com/machine-learning-to-tackle-climate-change-7911e004c3a2) et [Bloomberg](https://www.bloomberg.com/news/articles/2022-06-01/google-and-france-s-engie-team-up-to-accelerate-wind-power#xj4y7vzkg).

Le 23-24 novembre 2022, pendant que Patrick Pouyanne, PDG de <b>Total Energies</b>, est auditionné à l'Assemblée nationale au sein de la [commission d'enquête visant à établir les raisons de la perte de souveraineté et d'indépendance énergétique de la France](https://www.assemblee-nationale.fr/dyn/16/organes/autres-commissions/commissions-enquete/ce-independance-energetique), <b>ENGIE</b> et <b style='color:blue;'>Google</b> concluent un contrat de 100 MW, d'une durée de 12 ans, pour fournir à <b style='color:blue;'>Google</b> plus de 5 TWh d'énergie verte provenant du projet Moray West, un parc éolien offshore de près de 900 MW, dont la mise en service est prévue en 2025. [Engie.com](https://newsroom.engie.com/actualites/engie-et-google-concluent-un-contrat-dachat-delectricite-renouvelable-cppa-grace-au-developpement-docean-winds-dans-leolien-offshore-e469-ff316.html). L'<b style="color:red;">Europe</b> accuse les États-Unis de profiter de la guerre. [Politico.eu](https://www.politico.eu/article/vladimir-putin-war-europe-ukraine-gas-inflation-reduction-act-ira-joe-biden-rift-west-eu-accuses-us-of-profiting-from-war/).

{{< callout warning >}}
Le 25-26 juin 2022, <b>Total</b>, <b>EDF</b>, et <b>ENGIE</b> alertaient de la menace des prix sur la cohésion. [JDD](https://www.lejdd.fr/societe/tribune-le-prix-de-lenergie-menace-notre-cohesion-par-les-patrons-dengie-edf-et-totalenergies-9401), appellant les Français à une sobriété d'urgence [face à la flambée des prix de l'énergie](https://www.bfmtv.com/economie/total-edf-et-engie-appellent-les-francais-a-une-sobriete-d-urgence-face-a-la-flambee-des-prix-de-l-energie_VN-202206260112.html) et à réduire ["immédiatement"](https://www.bfmtv.com/economie/entreprises/energie/total-energies-edf-et-engie-appellent-a-reduire-immediatement-la-consommation-d-energie_AD-202206260081.html) la consommation d'énergie.
{{< /callout >}}

