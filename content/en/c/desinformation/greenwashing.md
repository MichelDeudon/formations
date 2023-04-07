---
title: Identify greenwashing and conflicts of interest
date: '2023-02-24'
type: book
weight: 30
tags:
  - energy
  - climate
  - misinformation
---

Hiver 2023. What is the goal of climate skeptics? What are they defending? Case study through LLaMA and ChatGPT models.

<!--more-->

## Disinformation is used to divert attention from the ecological emergency…

The purpose of disinformation as [business](https://www.bfmtv.com/tech/intelligence-artificielle/le-patron-de-l-entreprise-a-l-origine-de-chat-gpt-a-un- peu-peur-de-chat-gpt_AV-202303210270.html) is to divert attention and influence decisions, for example in what to [invest](https://www.bpifrance.fr/nos-actualites/rencontres-economiques-daix-en-provence-un-regard-sur-le-monde-demain), what [to debate](https://www.bfmtv.com/tech/intelligence-artificielle/pour-la-premiere-fois-l-assemblee-nationale-va-debattre-d-un-amendement-redige-par-chat-gpt_AV-202303210310.html), etc. When it is toxic and viral, it generates more clicks (Click Through Rate in English) and calls for more deeptech...

Thus, AI developments during fall winter 2022/2023 - [Galactica 120B](https://huggingface.co/facebook/galactica-120b), ChatGPT3, LLaMA 65B, ChatGPT4 - and disinformation allowed to hijack the attention of CEOs at the [World Economic Forum](https://www.reuters.com/technology/davos-2023-ceos-buzz-about-chatgpt-style-ai-world-economic-forum-2023-01- 17/) to invest in weapons for the benefit of HuggingFace, the GAFAMs, NVIDIA, etc.

In March 2023, TF1 talks about the threats of AI on jobs, the risks of autonomous cars... ecology and youth are not mentioned.
The [MIT](https://www.technologyreview.com/2019/02/14/137426/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/) warned, however, in 2019, of the risk that IA who writes convincing prose could mass produce fake news, referring to ChatGPT2. This has not prevented investments from multiplying in disinformation, energy consumption (x1000 in 4 years) and the generation of fake news.

## Resources to help fight greenwashing
- The anti-greenwashing guide from [Pour un Réveil Ecologique](https://pour-un-reveil-ecologique.org/fr/les-entreprises-nous-repondent/#guide-anti-greenwashing)
- The online anti-greenwashing tool of [ADEME](https://communication-responsable.ademe.fr/antigreenwashing)

## [Introducing LLaMA: A foundational, 65-billion-parameter large language model](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)
{{< icon name="calendar" pack="fas" >}} Feb 2023. The Meta AI / FAIR Paris blog is a {{<hl>}}gem of greenwashing{{</hl>}}.

As part of Meta’s commitment to open science, today we are publicly releasing LLaMA (Large Language Model Meta AI), a state-of-the-art foundational large language model designed to help researchers advance their work in this subfield of AI. Dans le cadre de l'engagement de Meta en faveur de la science ouverte, nous publions aujourd'hui LLaMA (Large Language Model Meta AI), un modèle de langage fondamental à l’état de l’art conçu pour aider les chercheurs à faire progresser leurs travaux dans ce sous-domaine de l'IA. {{<hl>}} <b>Smaller</b>, more performant models such as LLaMA{{</hl>}} enable others in the research community who don’t have access to large amounts of infrastructure to study these models, further democratizing access in this important, fast-changing field.

{{<hl>}}Training <b>smaller</b> foundation models like LLaMA is desirable{{</hl>}} in the large language model space because {{<hl>}}it requires <b>far less computing power and resources</b>{{</hl>}} to test new approaches, validate others’ work, and explore new use cases. Foundation models train on a large set of unlabeled data, which makes them ideal for fine-tuning for a variety of tasks. We are making LLaMA available at several sizes (7B, 13B, 33B, and 65B parameters) and also sharing a LLaMA model card that details how we built the model in keeping with our approach to {{<hl>}}<b>Responsible AI practices</b>{{</hl>}}.

{{< figure src="meta-paper-hours-gpu.png" caption="Carbon footprint of training different models in the same data center, from the paper LLaMA on [Arxiv](https://arxiv.org/abs/2302.13971) (section 6 Carbon footprint).">}}

{{< callout warning >}}
<i>The training of our models have consumed a massive quantity of energy, responsible for the emission of carbon dioxide</i> (section 6 Carbon footprint). <i>We plan to release larger models trained on larger pretraining corpora in the future</i> (section 8 Conclusion). [Arxiv](https://arxiv.org/abs/2302.13971).
{{< /callout >}}

{{< callout note >}}
No communication is made on Meta AI [research blog](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/), [social networks](https://www.linkedin.com/posts/yann-lecun_github-facebookresearchllama-inference-activity-7034956639526952960-B1-d?trk=public_profile_like_view) or on [Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732bd/MODEL_CARD.md) concerning the record carbon footprint, the environmental impact and the financing of the LLaMA model.
{{< /callout >}}

{{<hl>}}<b>Smaller</b> models{{</hl>}} trained on more tokens — which are pieces of words — are easier to retrain and fine-tune for specific potential product use cases. We trained LLaMA 65B and LLaMA 33B on 1.4 trillion tokens. Our smallest model, LLaMA 7B, is trained on one trillion tokens....

{{< callout note >}}
In reality, we are changing scale. Millions, billions, trillions... Models grew by a factor 1000 in complexity in 4 years.
{{< /callout >}}

There is still more research that needs to be done to address the risks of bias, toxic comments, and hallucinations in large language models. Like other models, LLaMA shares these challenges... We also provide in the paper a set of evaluations on benchmarks evaluating model biases and toxicity to show the model’s limitations and to support further research in this crucial area.

{{<hl>}}To maintain <b>integrity</b> and prevent <b>misuse</b>{{</hl>}}, we are releasing our model under a noncommercial license focused on research use cases. Access to the model will be granted on a case-by-case basis to academic researchers; those affiliated with organizations in government, civil society, and academia; and industry research laboratories around the world...

{{< callout warning >}}
March 8, 2023. [Model leaked](https://www.01net.com/actualites/fuite-meta-alternative-chatgpt-meta-partagee-forum.html). Integrity and misuse prevention? Fake news and economic model?
{{< /callout >}}

## [Ethical considerations on Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732bd/MODEL_CARD.md)
- Organization developing the model: The FAIR team of Meta AI.
- Model date: LLaMA was trained between December 2022 and February 2023.
- Model version: This is version 1 of the model
- Data: The data used to train the model is collected from various sources, mostly from the Web. As such, it contains offensive, harmful and biased content. We thus expect the model to exhibit such biases from the training data.
- Risks and harms: Risks and harms of large language models include the generation of harmful, offensive or biased content. These models are often prone to generating incorrect information, sometimes referred to as hallucinations. We do not expect our model to be an exception in this regard.
- Use cases: LLaMA is a foundational model, and as such, it should not be used for downstream applications without further investigation and mitigations of risks. These risks and potential fraught use cases include, but are not limited to: <b>generation of misinformation</b> and <b>generation of harmful, biased or offensive content</b>

### 💧 Climate crisis
- 02-15 <b style="color:red;">CNRS</b>. Climatosceptiques: on Twitter, investigation into mercenaries of intox. [cnrs.fr](https://lejournal.cnrs.fr/articles/climatosceptiques-sur-twitter-enquete-sur-les-mercenaires-de-lintox) [Le Monde](https://www.lemonde.fr/planete/article/2023/02/13/la-france-fait-face-a-un-fort-regain-de-climatoscepticisme-sur-twitter_6161691_3244.html) @[Audrey Garric](https://twitter.com/audreygarric/status/1625416947729944579?cxt=HHwWhsC-1cSG0o4tAAAA).
- 12-31 (2022) <b style="color:blue;">Emmanuel Macron</b> <i>Who could have predicted the climate crisis?</i>. [archive INA](https://www.youtube.com/watch?v=SsqYCvJvxQY&ab_channel=INAPolitique).

## [Tackling Climate Change with Machine Learning](https://arxiv.org/abs/1906.05433)

The original article is published on [Arxiv](https://arxiv.org/abs/1906.05433v1) on June 10, 2019, four days after [Emma Strubell](https://arxiv.org/abs/1906.02243) and the [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/)'s alert in 2019. Written by 22 authors including <b>Demis Hassabis</b>, CEO of <b>Deepmind</b>, and <b>Yoshua Bengio</b>, <b>Turing</b> award 2019 and deep learning godfather, it is republished on June 7 February 2022 by the [Association for Computing Machinery](https://dl.acm.org/doi/10.1145/3485128) (ACM) which awards the Turing Prize. In December 2022, while Yann Lecun and Elon Musk are working on models with billions of parameters (1000 times [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/)'s 2019 alert), a workshop is organized by climatechange.ai at [NeurIPS 2022](https://www.climatechange.ai/events/neurips2022) and includes 19 authors from <b style='color:blue;'>NVIDIA</b> which benefits from the explosion of model complexity.

## Research and gifts en IA

Gifts influence AI research to continue training ever more complex models, at the benefit of <b style='color:blue;'>GAFAM</b> and <b style='color:blue;'>NVIDIA</b>.
Submitted on [Arxiv](https://arxiv.org/abs/1905.10650) on May 25, 2019 and accepted at NeurIPS 2019, the article [Are Sixteen Heads Really Better than One?](https://arxiv.org/abs/1905.10650) by an alumni of École Polytechnique (X13) writes in the acknowledgments <i> We are also particularly grateful to <b>Thomas Wolf</b> from <b style='color:blue;'>Hugging Face</b>, whose independent reproduction efforts allowed us to find and correct a bug in our speed comparison experiments. This research was supported in part by a <b>gift from Facebook</b>. </i>

## June 2022, ENGIE first client

<i><b style='color:blue;'>Deep Mind</b> applied ML algorithms to predict wind energy. <b style='color:blue;'>Google</b> announced that this algorithm could predict wind power production thirty-six hours in advance. In June, <b>ENGIE</b> (a French company) was announced as the first client of the project</i>. On [Towards Data Science](https://towardsdatascience.com/machine-learning-to-tackle-climate-change-7911e004c3a2) and [Bloomberg](https://www.bloomberg.com/news/articles/2022-06-01/google-and-france-s-engie-team-up-to-accelerate-wind-power#xj4y7vzkg).

On November 23-24, 2022, while Patrick Pouyanne, CEO of <b>Total Energies</b>, is heard in the National Assembly within the [commission aiming at establishing the reasons for France's loss of sovereignty and energy independence](https://www.assemblee-nationale.fr/dyn/16/organes/autres-commissions/commissions-enquete/ce-independance-energetique), <b>ENGIE</b> and <b style='color:blue;'>Google</b> conclude a 100 MW contract for a period of 12 years, to supply <b style='color:blue;'>Google</b> with more than 5 TWh of "green energy" from the Moray West project, an offshore wind farm of nearly 900 MW, scheduled to be commissioned in 2025. [Engie.com](https://newsroom.engie.com/actualites/engie-et-google-concluent-un-contrat-dachat-delectricite-renouvelable-cppa-grace-au-developpement-docean-winds-dans-leolien-offshore-e469-ff316.html). <b style="color:red;">Europe</b> accuses US of profiting from the war. [Politico.eu](https://www.politico.eu/article/vladimir-putin-war-europe-ukraine-gas-inflation-reduction-act-ira-joe-biden-rift-west-eu-accuses-us-of-profiting-from-war/).

{{< callout warning >}}
On June 25-26, 2022, <b>Total</b>, <b>EDF</b>, and <b>ENGIE</b> warned on the threat of prices on cohesion. [JDD](https://www.lejdd.fr/societe/tribune-le-prix-de-lenergie-menace-notre-cohesion-par-les-patrons-dengie-edf-et-totalenergies-9401), calling on the French for emergency sobriety [in the face of soaring energy prices](https://www.bfmtv.com/economie/total-edf-et-engie-appellent-les-francais-a-une-sobriete-d-urgence-face-a-la-flambee-des-prix-de-l-energie_VN-202206260112.html) and to reduce ["immediately"](https://www.bfmtv.com/economie/entreprises/energie/total-energies-edf-et-engie-appellent-a-reduire-immediatement-la-consommation-d-energie_AD-202206260081.html) energy consumption.
{{< /callout >}}