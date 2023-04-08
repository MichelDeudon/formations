---
title: Identify greenwashing and conflicts of interest
date: '2023-02-24'
type: book
weight: 30
tags:
  - artificial intelligence
  - energy
  - climate
  - misinformation
  - environment and society
---

What is the goal of climate skeptics? What are they defending? Why is ChatGPT a source of misinformation? A case study of LLaMA and ChatGPT.

<!--more-->

## Disinformation is used to divert attention from the ecological emergency…

<i>[Who could have predicted the climate crisis?](https://www.youtube.com/watch?v=SsqYCvJvxQY&ab_channel=INAPolitique)</i> asked <b>Emmanuel Macron</b> end of 2022.
Six weeks later, during the [drought record](https://meteofrance.com/actualites-et-dossiers/actualites/climat/secheresse-32-jours-sans-pluie-en-france-record-battu) in France, the [CNRS](https://lejournal.cnrs.fr/articles/climatosceptiques-sur-twitter-enquete-sur-les-mercenaires-de-lintox), [ISCPIF](https://iscpif.fr/climatoscope/?p=72), [Citizen4science](https://citizen4science.org/climatoscope-du-cnrs-les-nouveaux-fronts-du-denialisme-et-du-climato-scepticisme/), [le Monde](https://www.lemonde.fr/planete/article/2023/02/13/la-france-fait-face-a-un-fort-regain-de-climatoscepticisme-sur-twitter_6161691_3244.html) and the journalist [Audrey Garric](https://twitter.com/audreygarric/status/1625416947729944579?cxt=HHwWhsC-1cSG0o4tAAAA) warned of a rise of climatosceptism on Twitter (bought by Elon Musk in 2022). A large community was structured from the summer of 2022. More than 10,000 active accounts relay false information and attack the [IPCC](https://www.ecologie.gouv.fr/publication-du-6e-rapport-synthese-du-giec), with thousands of daily tweets.

{{< figure src="desinfo/FakeNews - ChatGPT3.jpg" caption="February 2023 (ChatGPT3) Screenshot of a MIASHS undergraduate student. February 2019 (ChatGPT2) An AI that writes compelling prose risks mass-producing fake news. [MIT Technology Review](https://www.technologyreview.com/2019/02/14/137426/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/ ) (this has not prevented investments from multiplying in disinformation). March 2023 (ChatGPT4) Explosion of misinformation. [BFM Business](https://www.bfmtv.com/tech/intelligence-artificielle/le-patron-de-l-entreprise-a-l-origine-de-chat-gpt-a-un-peu-peur-de-chat-gpt_AV-202303210270.html).">}}

The purpose of disinformation as a [business](https://www.bfmtv.com/tech/intelligence-artificielle/le-patron-de-l-entreprise-a-l-origine-de-chat-gpt-a-un-peu-peur-de-chat-gpt_AV-202303210270.html) is to divert attention and influence decisions, for example in what to [invest](https://www.bpifrance.fr/nos-actualites/rencontres-economiques-daix-en-provence-un-regard-sur-le-monde-demain), what [to debate](https://www.bfmtv.com/tech/intelligence-artificielle/pour-la-premiere-fois-l-assemblee-nationale-va-debattre-d-un-amendement-redige-par-chat-gpt_AV-202303210310.html), etc. When it is toxic and viral, it generates more clicks (Click Through Rate in English) and calls for more deeptech...

{{< figure src="desinfo/mafia-desinformation.png">}}

Thus, AI developments during fall winter 2022/2023 - [Galactica 120B](https://huggingface.co/facebook/galactica-120b), ChatGPT3, LLaMA 65B, ChatGPT4 - and disinformation allowed to hijack the attention of CEOs at the [World Economic Forum](https://www.reuters.com/technology/davos-2023-ceos-buzz-about-chatgpt-style-ai-world-economic-forum-2023-01-17/) to invest in military applications rather than resilience and climate change.

In March 2023, TF1 talked about [AI and war](https://www.tf1info.fr/player/debdff38-d5d9-4685-84ef-7959f4cdd39e/), the threats of AI on [jobs, autonomous cars](https://www.tf1info.fr/sciences-et-innovation/interview-destruction-d-emplois-desinformation-faut-il-mettre-en-pause-les-recherches-sur-l-ia-intelligence-artificielle-comme-chatgpt-comme-le-demande-une-tribune-2252595.html)... ecology and youth are never mentioned. TF1's documentary and article cite one of the largest US bank, Goldman Sachs, and Bellingcat, whose business model is centered on disinformation, as a source of information.

By projecting models on a single axis (metric) without taking into account resources, energy, real costs, AI research has become a race to consume and pollute more. From [HighRes-net](https://github.com/ServiceNow/HighRes-net) (2019) to [TR-MISR](https://paperswithcode.com/sota/multi-frame-super-resolution-on-proba-v?p=highres-net-recursive-fusion-for-multi-frame) (2022), the AI metric improved by just under 2%, but with quadratic complexity instead of a logarithmic one, and a time to train once that goes from 9h to 60h on an NVIDIA Tesla V100 card. TR-MISR uses [Transformer](https://arxiv.org/abs/1706.03762) (Google, 2017), the same model found in BERT, ChatGPT and LLaMA. It is therefore not more AI, at the service of AI, that is needed (this is the goal of disinformation!).
If tomorrow Twitter was only made up of bots, fake profiles and climatosceptics, what would its value be?

### Resources to help fight greenwashing
- The anti-greenwashing guide from [Pour un Réveil Ecologique](https://pour-un-reveil-ecologique.org/fr/les-entreprises-nous-repondent/#guide-anti-greenwashing)
- The online anti-greenwashing tool of [ADEME](https://communication-responsable.ademe.fr/antigreenwashing)

### Use case A. [LLaMA](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/).
{{< icon name="calendar" pack="fas" >}} Feb 2023. Meta AI / FAIR Paris blog is a {{<hl>}}gem of greenwashing{{</hl>}}.

As part of Meta’s commitment to open science, today we are publicly releasing LLaMA (Large Language Model Meta AI), a state-of-the-art foundational large language model designed to help researchers advance their work in this subfield of AI. Dans le cadre de l'engagement de Meta en faveur de la science ouverte, nous publions aujourd'hui LLaMA (Large Language Model Meta AI), un modèle de langage fondamental à l’état de l’art conçu pour aider les chercheurs à faire progresser leurs travaux dans ce sous-domaine de l'IA. {{<hl>}} <b>Smaller</b>, more performant models such as LLaMA{{</hl>}} enable others in the research community who don’t have access to large amounts of infrastructure to study these models, further democratizing access in this important, fast-changing field.

{{<hl>}}Training <b>smaller</b> foundation models like LLaMA is desirable{{</hl>}} in the large language model space because {{<hl>}}it requires <b>far less computing power and resources</b>{{</hl>}} to test new approaches, validate others’ work, and explore new use cases. Foundation models train on a large set of unlabeled data, which makes them ideal for fine-tuning for a variety of tasks. We are making LLaMA available at several sizes (7B, 13B, 33B, and 65B parameters) and also sharing a LLaMA model card that details how we built the model in keeping with our approach to {{<hl>}}<b>Responsible AI practices</b>{{</hl>}}.

{{< callout note >}}
LLaMA was trained between December 2022 and February 2023, but no communication is made on Meta AI [research blog](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/), [social networks](https://www.linkedin.com/posts/yann-lecun_github-facebookresearchllama-inference-activity-7034956639526952960-B1-d?trk=public_profile_like_view) or on [Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732bd/MODEL_CARD.md) concerning the record carbon footprint, the environmental impact and the financing of version 1.
{{< /callout >}}

{{<hl>}}<b>Smaller</b> models{{</hl>}} trained on more tokens — which are pieces of words — are easier to retrain and fine-tune for specific potential product use cases. We trained LLaMA 65B and LLaMA 33B on 1.4 trillion tokens. Our smallest model, LLaMA 7B, is trained on one trillion tokens....

{{< callout note >}}
In reality, we are changing scale. Millions, billions, trillions... Models grew by a factor 1000 in complexity in 4 years.
{{< /callout >}}

There is still more research that needs to be done to address the risks of bias, toxic comments, and hallucinations in large language models. Like other models, LLaMA shares these challenges... We also provide in the paper a set of evaluations on benchmarks evaluating model biases and toxicity to show the model’s limitations and to support further research in this crucial area.

{{<hl>}}To maintain <b>integrity</b> and prevent <b>misuse</b>{{</hl>}}, we are releasing our model under a noncommercial license focused on research use cases. Access to the model will be granted on a case-by-case basis to academic researchers; those affiliated with organizations in government, civil society, and academia; and industry research laboratories around the world...

{{< callout warning >}}
March 8, 2023. [Model leaked](https://www.01net.com/actualites/fuite-meta-alternative-chatgpt-meta-partagee-forum.html). Risks and potential fraught use cases include, but are not limited to: <b>generation of misinformation</b> and <b>generation of harmful, biased or offensive content</b>. [Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732bd/MODEL_CARD.md). What is Facebook's economic model?
{{< /callout >}}

### Use case B. [Tackling Climate Change with Machine Learning](https://arxiv.org/abs/1906.05433).

The original article was published on [Arxiv](https://arxiv.org/abs/1906.05433v1) in June 2019, four days after [Emma Strubell](https://arxiv.org/abs/1906.02243) and the [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/)'s alert. Written by 22 authors including <b>Demis Hassabis</b>, CEO of <b>Deepmind</b>, and <b>Yoshua Bengio</b>, <i>deep learning</i> godfather, it is republished in February 2022 by the [Association for Computing Machinery](https://dl.acm.org/doi/10.1145/3485128) (ACM), the American lobby which awarded the 2019 Turing Prize to <b>Yoshua Bengio</b>, <b>Geoffrey Hinton</b> (<b>Google</b>) and <b>Yann Le Cun</b> (<b>Facebook</b>).

{{< callout note >}}
In October 2019, <b>Laure Delisle</b> and <b>Michel Deudon</b> were laid off from <b>Yoshua Bengio</b>'s startup <b>Element AI</b>, AI for Good, following [a series B round with investors](https://www.cdpq.com/en/news/pressreleases/element-ai-raises-cad-200m-us-1514m-series-b-round-to-transform-commercial) including <b>McKinsey & Company</b> which [advised France on its Covid-19 vaccination strategy](https://www.francetvinfo.fr/sante/maladie/coronavirus/vaccin/covid-19-on-vous-resume-la-polemique-autour-de-mckinsey-le-cabinet-qui-conseille-le-gouvernement-sur-la-strategie-vaccinale_4291131.html). Three years later, <b>Manon Gruaz</b> gave a talk [CTRL+ALT+Depression](https://www.youtube.com/watch?v=MN3D0uLEERU&ab_channel=GDGFrance) pointing some issues at <b>Element AI</b>.
{{< /callout >}}

In December 2022, while <b>Yann Lecun</b> and <b>Elon Musk</b> are working on models with billions of parameters (1000 times [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/)'s 2019 alert), a workshop is organized by climatechange.ai at [NeurIPS 2022](https://www.climatechange.ai/events/neurips2022) and includes 19 authors from <b>NVIDIA</b>, the world leader in artificial intelligence computing, which benefits from the explosion of model complexity and disinformation.

### Use case C. Research and gifts en IA.

The spotlight on <i>deep learning</i> godfathers, but also gifts and corruption influenced AI research to continue training ever more complex models, at the benefit of <b>GAFAM</b> and <b>NVIDIA</b>.
Submitted on [Arxiv](https://arxiv.org/abs/1905.10650) on May 25, 2019 and accepted at NeurIPS 2019, the article [Are Sixteen Heads Really Better than One?](https://arxiv.org/abs/1905.10650) by an alumni of École Polytechnique (X13) writes in the acknowledgments <i> We are also particularly grateful to <b>Thomas Wolf</b> from <b>Hugging Face</b>, whose independent reproduction efforts allowed us to find and correct a bug in our speed comparison experiments. This research was supported in part by a <b>gift from Facebook</b>. </i>

### Use case D. [ENGIE-Google](https://www.bloomberg.com/news/articles/2022-06-01/google-and-france-s-engie-team-up-to-accelerate-wind-power#xj4y7vzkg).

<i><b>Deep Mind</b> applied ML algorithms to predict wind energy. <b>Google</b> announced that this algorithm could predict wind power production thirty-six hours in advance. In June [2022], <b>ENGIE</b> (a French company) was announced as the first client of the project</i> on [Towards Data Science](https://towardsdatascience.com/machine-learning-to-tackle-climate-change-7911e004c3a2) and [Bloomberg](https://www.bloomberg.com/news/articles/2022-06-01/google-and-france-s-engie-team-up-to-accelerate-wind-power#xj4y7vzkg). 

{{< callout warning >}}
On June 25-26, 2022, <b>Total</b>, <b>EDF</b>, and <b>ENGIE</b> warned on the [threat of prices on cohesion](https://www.lejdd.fr/societe/tribune-le-prix-de-lenergie-menace-notre-cohesion-par-les-patrons-dengie-edf-et-totalenergies-9401), calling on the French for emergency sobriety [in the face of soaring energy prices](https://www.bfmtv.com/economie/total-edf-et-engie-appellent-les-francais-a-une-sobriete-d-urgence-face-a-la-flambee-des-prix-de-l-energie_VN-202206260112.html) and to reduce ["immediately"](https://www.bfmtv.com/economie/entreprises/energie/total-energies-edf-et-engie-appellent-a-reduire-immediatement-la-consommation-d-energie_AD-202206260081.html) energy consumption.
{{< /callout >}}

{{< callout warning >}}
On September 5, 2022, Macron calls for <i>individual sobriety</i>. <i>"Everyone has a role to play (...) the best energy is the one which we do not consume""</i>. The objective is <i>"to save 10% of what we currently consume"</i>. [Press conference at l'Elysee](https://www.youtube.com/watch?v=XjC1NqzyGkc&ab_channel=%C3%89lys%C3%A9e). [Sobriety plan ecologie.gouv.fr](https://www.ecologie.gouv.fr/plan-sobriete-acte-2-mobilisation-se-poursuit).
{{< /callout >}}

On November 23-24, 2022, while Patrick Pouyanne, CEO of <b>Total Energies</b>, is heard in the National Assembly within the [commission aiming at establishing the reasons for France's loss of sovereignty and energy independence](https://www.assemblee-nationale.fr/dyn/16/organes/autres-commissions/commissions-enquete/ce-independance-energetique), <b>ENGIE</b> and <b>Google</b> conclude a 100 MW contract for a period of 12 years, to supply <b>Google</b> with [more than 5 TWh of "green energy" from the Moray West project](https://newsroom.engie.com/actualites/engie-et-google-concluent-un-contrat-dachat-delectricite-renouvelable-cppa-grace-au-developpement-docean-winds-dans-leolien-offshore-e469-ff316.html), an offshore wind farm of nearly 900 MW, scheduled to be commissioned in 2025. <b>Europe</b> accuses US of profiting from the war. [Politico.eu](https://www.politico.eu/article/vladimir-putin-war-europe-ukraine-gas-inflation-reduction-act-ira-joe-biden-rift-west-eu-accuses-us-of-profiting-from-war/).

In March 2023, the French [law relating to the acceleration of the production of renewable energies](https://www.ecologie.gouv.fr/publication-loi-relative-acceleration-des-energies-renouvelables) states objectives that seem to be at odds with ENGIE's strategy - to preserve the purchasing power of the French and the competitiveness of companies, to defend the industrial, energy and political independence of France and to fight against climate change.