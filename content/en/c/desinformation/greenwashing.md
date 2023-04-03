---
title: Meta LLaMA and misinformation
date: '2023-02-24'
type: book
weight: 40
tags:
  - energy
  - climate
  - misinformation
---

Feb 2023. Training smaller foundation models like LLaMA is desirable (...) because it requires far less computing power and resources to test new approaches. FAIR Paris. {{<hl>}}Gem of greenwashing{{</hl>}}. 

<!--more-->

## [Introducing LLaMA: A foundational, 65-billion-parameter large language model](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)

As part of Meta’s commitment to open science, today we are publicly releasing LLaMA (Large Language Model Meta AI), a state-of-the-art foundational large language model designed to help researchers advance their work in this subfield of AI. Dans le cadre de l'engagement de Meta en faveur de la science ouverte, nous publions aujourd'hui LLaMA (Large Language Model Meta AI), un modèle de langage fondamental à l’état de l’art conçu pour aider les chercheurs à faire progresser leurs travaux dans ce sous-domaine de l'IA. {{<hl>}} <b>Smaller</b>, more performant models such as LLaMA{{</hl>}} enable others in the research community who don’t have access to large amounts of infrastructure to study these models, further democratizing access in this important, fast-changing field.

{{<hl>}}Training <b>smaller</b> foundation models like LLaMA is desirable{{</hl>}} in the large language model space because {{<hl>}}it requires <b>far less computing power and resources</b>{{</hl>}} to test new approaches, validate others’ work, and explore new use cases. Foundation models train on a large set of unlabeled data, which makes them ideal for fine-tuning for a variety of tasks. We are making LLaMA available at several sizes (7B, 13B, 33B, and 65B parameters) and also sharing a LLaMA model card that details how we built the model in keeping with our approach to {{<hl>}}<b>Responsible AI practices</b>{{</hl>}}.

{{< figure src="meta-paper-hours-gpu.png" caption="Carbon footprint of training different models in the same data center (see section 6 Carbon footprint), from the scientific paper LLaMA on [Arxiv](https://arxiv.org/abs/2302.13971) (see section 6 Carbon footprint)." numbered="true">}}

{{< callout warning >}}
<i>The training of our models have consumed a massive quantity of energy, responsible for the emission of carbon dioxide</i> (see section 6 Carbon footprint). <i>We plan to release larger models trained on larger pretraining corpora in the future</i> (see section 8 Conclusion). [Arxiv](https://arxiv.org/abs/2302.13971).
{{< /callout >}}

{{< callout note >}}
No communication is made on Meta AI [research blog](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/), [social networks](https://www.linkedin.com/posts/yann-lecun_github-facebookresearchllama-inference-activity-7034956639526952960-B1-d?trk=public_profile_like_view) or on [Github](https://github.com/facebookresearch/llama/blob/1076b9c51c77ad06e9d7ba8a4c6df775741732bd/MODEL_CARD.md) concerning the record carbon footprint, the environmental impact and the financing of the LLaMA model version 1.
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
- License: Non-commercial bespoke license
- Data: The data used to train the model is collected from various sources, mostly from the Web. As such, it contains offensive, harmful and biased content. We thus expect the model to exhibit such biases from the training data.
- Human life: The model is not intended to inform decisions about matters central to human life, and should not be used in such a way.
- Mitigations: We filtered the data from the Web based on its proximity to Wikipedia text and references. For this, we used a Kneser-Ney language model and a fastText linear classifier.
- Risks and harms: Risks and harms of large language models include the generation of harmful, offensive or biased content. These models are often prone to generating incorrect information, sometimes referred to as hallucinations. We do not expect our model to be an exception in this regard.
- Use cases: LLaMA is a foundational model, and as such, it should not be used for downstream applications without further investigation and mitigations of risks. These risks and potential fraught use cases include, but are not limited to: <b>generation of misinformation</b> and <b>generation of harmful, biased or offensive content</b>

{{< figure src="meta-github-bias.png" caption="Meta github model bias" numbered="true">}}

## Resources to help fight greenwashing
- The anti-greenwashing guide from [Pour un Réveil Ecologique](https://pour-un-reveil-ecologique.org/fr/les-entreprises-nous-repondent/#guide-anti-greenwashing)
- The online anti-greenwashing tool of [ADEME](https://communication-responsable.ademe.fr/antigreenwashing)

## Winter of AI and Climate (2023)

### 🔥 Energy consumption records and misinformation
- 03-14 (2023) <b style="color:blue;">Open AI</b> ChatGPT4. <i>Explosion of misinformation</i>. [BFM Business](https://www.bfmtv.com/tech/intelligence-artificielle/le-patron-de-l-entreprise-a-l-origine-de-chat-gpt-a-un-peu-peur-de-chat-gpt_AV-202303210270.html)
- 24-02 (2023) <b style="color:blue;">Facebook</b> AI Research LLaMA 65B.
- 11-30 (2022) <b style="color:blue;">Open AI</b>. ChatGPT3. 
- 11-25 (2022) <b style="color:blue;">Facebook</b> AI Research Galactica 120B. <i>More to come</i>. @[Paperswithcode](https://paperswithcode.com/paper/galactica-a-large-language-model-for-science-1) @[HuggingFace](https://huggingface.co/facebook/galactica-120b).
- 02-14 (2019) 🔥 <b style="color:blue;">OpenAI</b> ChatGPT2.
- 02-14 (2019) <i>An AI that writes convincing prose risks mass-producing fake news</i>. [MIT Technology Review](https://www.technologyreview.com/2019/02/14/137426/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/).

### 💧 Climate crisis
- 02-22 <b style="color:red;">Meteo France</b>. Drought: 32 days without rain in France, record broken. [meteofrance.com](https://meteofrance.com/actualites-et-dossiers/actualites/climat/secheresse-32-jours-sans-pluie-en-france-record-battu).
- 02-15 <b style="color:red;">CNRS</b>. Climatosceptiques: on Twitter, investigation into mercenaries of intox. [cnrs.fr](https://lejournal.cnrs.fr/articles/climatosceptiques-sur-twitter-enquete-sur-les-mercenaires-de-lintox) [Le Monde](https://www.lemonde.fr/planete/article/2023/02/13/la-france-fait-face-a-un-fort-regain-de-climatoscepticisme-sur-twitter_6161691_3244.html) @[Audrey Garric](https://twitter.com/audreygarric/status/1625416947729944579?cxt=HHwWhsC-1cSG0o4tAAAA).
- 01-23 <b style="color:red;">Meteo France</b>. <i>2022, the hottest year in France</i>. [meteofrance.com](https://meteofrance.com/actualites-et-dossiers/actualites/2022-annee-la-plus-chaude-en-france).
- 12-31 (2022) <b style="color:blue;">Emmanuel Macron</b> <i>Who could have predicted the climate crisis?</i>. [archive INA](https://www.youtube.com/watch?v=SsqYCvJvxQY&ab_channel=INAPolitique).

{{< vimeo 767800360 >}}