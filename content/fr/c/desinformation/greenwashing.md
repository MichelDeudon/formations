---
title: Meta LLaMA et désinformation
date: '2023-02-24'
type: book
weight: 40
tags:
  - énergie
  - climat
  - désinformation
---

Fév 2023. L'entraînement de modèles fondamentaux plus petits comme LLaMA est souhaitable (...) car ça nécessite beaucoup moins de puissance de calcul et de ressources pour tester de nouvelles approches. FAIR Paris. Le blog de Meta AI est une {{<hl>}}perle de greenwashing{{</hl>}}.

<!--more-->

## [Présentation de LLaMA : un modèle de langage fondamental de 65 milliards de paramètres](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)

Dans le cadre de l'engagement de Meta en faveur de la science ouverte, nous publions aujourd'hui LLaMA (Large Language Model Meta AI), un modèle de langage fondamental à l’état de l’art conçu pour aider les chercheurs à faire progresser leurs travaux dans ce sous-domaine de l'IA. {{<hl>}}Des modèles <b>plus petits</b> et plus performants tels que LLaMA{{</hl>}} permettent à d'autres membres de la communauté de recherche qui n'ont pas accès à de grandes quantités d'infrastructures d'étudier ces modèles, démocratisant davantage l'accès dans ce domaine important et en évolution rapide.

{{<hl>}}L'entraînement de modèles fondamentaux <b>plus petits</b> comme LLaMA est souhaitable{{</hl>}} dans le champ des large language model, car {{<hl>}}ça nécessite beaucoup <b>moins de puissance de calcul et de ressources</b>{{</hl>}} pour tester de nouvelles approches, valider le travail des autres et explorer de nouveaux cas d'utilisation. Les modèles fondamentaux sont entraînés sur un vaste ensemble de données non étiquetées, ce qui les rend idéaux pour être ajusté à une variété de tâches. Nous rendons LLaMA disponible en plusieurs tailles (paramètres 7B, 13B, 33B et 65B) et partageons également une carte du modèle LLaMA qui détaille comment nous avons construit le modèle conformément à notre approche des {{<hl>}}<b>pratiques d'IA responsable</b>{{</hl>}}.

{{< figure src="meta-paper-hours-gpu.png" caption="Empreinte carbone de différents modèles entrainés dans le même centre de données, tiré de l'article scientifique LLaMA sur [Arxiv](https://arxiv.org/abs/2302.13971) (voir section 6 Empreinte carbone)." numbered="true">}}

{{< callout warning >}}
<i>L'entraînement de nos modèles a consommé une quantité massive d'énergie, responsable de l'émission de dioxyde de carbone.</i> (voir section 6 Empreinte carbone). <i>Nous prévoyons de publier à l'avenir des modèles plus grands, entrainés sur des corpus plus importants</i> (voir section 8 Conclusion). [Arxiv](https://arxiv.org/abs/2302.13971).
{{< /callout >}}

{{< callout note >}}
Aucune communication n'est faite sur [le blog](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/) de Meta AI Research, sur les [réseau sociaux](https://www.linkedin.com/posts/yann-lecun_github-facebookresearchllama-inference-activity-7034956639526952960-B1-d?trk=public_profile_like_view) ou sur [Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732 ) concernant l'empreinte carbone record, l'impact environnemental et le financement du modèle LLaMA version 1.
{{< /callout >}}

{{<hl>}}Des modèles <b>plus petits</b>{{</hl>}} entraînés sur plus de jetons - qui sont des morceaux de mots - sont {{<hl>}}<b>plus faciles</b> à réentraîner et affiner{{</hl>}} pour des cas d'utilisation potentiels et spécifiques de produits. Nous avons entraîné LLaMA 65B et LLaMA 33B sur 1,4 trilliard de jetons. Notre {{<hl>}}<b>plus petit</b> modèle{{</hl>}}, LLaMA 7B, est formé sur un trilliard de jetons…

{{< callout note >}}
En réalité on change d’échelle. Millions, milliards, trilliards... C’est les modèles de 2017-2019 x1000 en complexité en 4 ans.
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
- Licence: Licence sur mesure non commerciale
- Données: Les données utilisées pour entraîner le modèle sont collectées à partir de diverses sources, principalement du Web. En tant que tel, il contient un contenu offensant, préjudiciable et biaisé. Nous nous attendons à ce que le modèle présente de tels biais.
- Vie humaine: Le modèle n'est pas destiné à éclairer les décisions sur les questions essentielles à la vie humaine et ne doit pas être utilisé de cette manière.
- Atténuations: Nous avons filtré les données du Web en fonction de leur proximité avec des textes et références de Wikipédia.
- Risques et préjudices: Les risques et préjudices des grands modèles linguistiques incluent la génération de contenu nuisible, offensant ou biaisé. Ces modèles sont souvent susceptibles de générer des informations incorrectes. Nous ne nous attendons pas à ce que notre modèle soit une exception à cet égard.
- Cas d'utilisation: LLaMA est un modèle fondamental et, en tant que tel, il ne doit pas être utilisé pour des applications sans une enquête plus approfondie et une atténuation des risques. Ces risques et cas d'utilisation potentiellement dangereux incluent, mais sans s'y limiter : la <b>génération de fausses informations</b> et la <b>génération de contenu nuisible, biaisé ou offensant</b>.

{{< figure src="meta-github-bias.png" caption="Meta github model bias" numbered="true">}}

## Ressources pour lutter contre le greenwashing
- Le guide anti greenwashing de [Pour un Réveil Ecologique](https://pour-un-reveil-ecologique.org/fr/les-entreprises-nous-repondent/#guide-anti-greenwashing)
- L'outil en ligne anti greenwashing de l'[ADEME](https://communication-responsable.ademe.fr/antigreenwashing)

## Hiver de l'IA et du Climat (2023)

### 🔥 Records de consommation énergétique et désinformation
- 14-03 (2023) <b style="color:blue;">Open AI</b> ChatGPT4. <i>Explosion de la désinformation</i>. [BFM Business](https://www.bfmtv.com/tech/intelligence-artificielle/le-patron-de-l-entreprise-a-l-origine-de-chat-gpt-a-un-peu-peur-de-chat-gpt_AV-202303210270.html)
- 24-02 (2023) <b style="color:blue;">Facebook</b> AI Research LLaMA 65B.
- 30-11 (2022) <b style="color:blue;">Open AI</b> ChatGPT3. 
- 25-11 (2022) <b style="color:blue;">Facebook</b> AI Research Galactica 120B. <i>Plus à venir</i>. @[Paperswithcode](https://paperswithcode.com/paper/galactica-a-large-language-model-for-science-1) @[HuggingFace](https://huggingface.co/facebook/galactica-120b).
- 14-02 (2019) 🔥 <b style="color:blue;">OpenAI</b> ChatGPT2.
- 14-02 (2019) <i>Une IA qui écrit une prose convaincante risque de produire en masse de fausses nouvelles</i>. [MIT Technology Review](https://www.technologyreview.com/2019/02/14/137426/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/).

### 💧 Crise climatique
- 22-02 <b style="color:red;">Meteo France</b>. <i>Sécheresse: 32 jours sans pluie en France, record battu</i>. [meteofrance.com](https://meteofrance.com/actualites-et-dossiers/actualites/climat/secheresse-32-jours-sans-pluie-en-france-record-battu).
- 15-02 <b style="color:red;">CNRS</b>. Climatosceptiques: sur Twitter, enquête sur les mercenaires de l’intox [cnrs.fr](https://lejournal.cnrs.fr/articles/climatosceptiques-sur-twitter-enquete-sur-les-mercenaires-de-lintox) [Le Monde](https://www.lemonde.fr/planete/article/2023/02/13/la-france-fait-face-a-un-fort-regain-de-climatoscepticisme-sur-twitter_6161691_3244.html) @[Audrey Garric](https://twitter.com/audreygarric/status/1625416947729944579?cxt=HHwWhsC-1cSG0o4tAAAA).
- 23-01 <b style="color:red;">Meteo France</b>. <i>2022, année la plus chaude en France</i>. [meteofrance.com](https://meteofrance.com/actualites-et-dossiers/actualites/2022-annee-la-plus-chaude-en-france).
- 31-12 (2022) <b style="color:blue;">Emmanuel Macron</b> <i>Qui aurait pu prédire la crise climatique?</i> [archive INA](https://www.youtube.com/watch?v=SsqYCvJvxQY&ab_channel=INAPolitique).

{{< vimeo 767800360 >}}