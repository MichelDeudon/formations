---
title: Energy and Policy Considerations
date: '2019-06-05'
type: book
weight: 20
highlight: true
tags:
  - artificial intelligence
  - energy
  - climate
  - disinformation
---

Spring 2019. Emma Strubell and MIT's alert.

<!--more-->

## [Energy and Policy Considerations for Deep Learning in NLP](https://arxiv.org/abs/1906.02243)

🚨 On June 5, 2019, Emma Strubell, PhD candidate and lead author of the paper [Energy and Policy Considerations for Deep Learning in NLP](https://arxiv.org/abs/1906.02243) gave the alert to the scientific and political community of the terrible ecological impact of deep learning models in linguistics at that time. Her article appeared in <b>ACL2019</b> 🇮🇹, the largest linguistics conference. The <b>Massachusetts Institute of Technology</b> 🇺🇸 shared her alert on energy consumption and carbon emissions of models with millions of parameters like [Transformers](https://arxiv.org/abs/1706.03762)" (<b style="color:blue;">Google</b>, 2017) and [BERT](https://arxiv.org/abs/1810.04805) (<b style="color:blue;">Google</b>, 2018) in its technology review of June 6, 2019. At that time, the largest model had up to 65 million parameters (1/1000 [LLaMA](https://arxiv.org/abs/2302.13971), 2023).

{{< callout warning >}}
The day following [Emma Strubell](https://arxiv.org/abs/1906.02243) and the [MIT](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/)'s alert, BERT received the best long paper award at [NAACL19](https://aclanthology.org/N19-1423/) 🇺🇸.
{{< /callout >}}

## [Training a single AI model can emit as much carbon as...](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/)

6 juin 2019. [MIT Technology Review](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) by Karen Hao.

{{< figure src="desinfo/2019-06 MIT.jpg" caption="MIT Technology Review, june 2019." numbered="true">}}

The [artificial-intelligence](https://www.technologyreview.com/artificial-intelligence/) industry is often compared to the oil industry: once mined and refined, data, like oil, can be a highly lucrative commodity. Now it seems the metaphor may extend even further. Like its fossil-fuel counterpart, the process of {{<hl>}}<b>deep learning has an outsize environmental impact</b>{{</hl>}}.

In a [new paper](http://arxiv.org/abs/1906.02243), researchers at the University of Massachusetts, Amherst, performed a life cycle assessment for training several common large AI models. They found that the process can emit more than 626,000 pounds of carbon dioxide equivalent—nearly five times the lifetime emissions of the average American car (and that includes manufacture of the car itself). What's more, the researchers note that the figures should only be considered as baselines. “<b>Training a single model is the minimum amount of work you can do</b>," says <b>Emma Strubell</b>, a PhD candidate at the University of Massachusetts, Amherst, and the lead author of the paper. In practice, it's much more likely that AI researchers would develop a new model from scratch or adapt an existing model to a new data set, either of which can require many more rounds of training and tuning.

### The carbon footprint of natural-language processing
The paper specifically examines the model training process for [natural-language processing](https://www.technologyreview.com/s/612975/ai-natural-language-processing-explained/) (NLP), the subfield of AI that focuses on teaching machines to handle human language. In the last two years, the NLP community has reached several noteworthy performance milestones in machine translation, sentence completion, and other standard benchmarking tasks. [OpenAI's infamous GPT-2 model](https://www.technologyreview.com/s/612960/an-ai-tool-auto-generates-fake-news-bogus-tweets-and-plenty-of-gibberish/), as one example, excelled at writing convincing fake news articles. But such advances have required <b>training ever larger models on sprawling data sets of sentences scraped from the internet. The approach is computationally expensive—and highly energy intensive</b>.

{{< figure src="desinfo/mit-review-2019 - emissions.png">}}

The researchers looked at four models in the field that have been responsible for the biggest leaps in performance: the Transformer, ELMo, [BERT](https://www.nytimes.com/2018/11/18/technology/artificial-intelligence-language.html), and GPT-2. They trained each on a single GPU for up to a day to measure its power draw. They then used the number of training hours listed in the model’s original papers to calculate the total energy consumed over the complete training process. That number was converted into pounds of carbon dioxide equivalent based on the average energy mix in the US, which closely matches the energy mix used by <b style="color:blue;">Amazon’s AWS</b>, the largest cloud services provider.

{{< callout note >}}
February 2023. <b>Macron</b> decorates <b style="color:blue;">Bezos</b> in secret. [Le Point](https://www.youtube.com/watch?v=kZPG9rmbdmw&ab_channel=LePoint).
{{< /callout >}}

### The estimated costs of training a model once
In practice, models are usually trained many times during research and development. They found that <b>the computational and environmental costs of training grew proportionally to model size and then exploded when additional tuning steps were used to increase the model’s final accuracy</b>.

Strubell and her colleagues used a model they’d produced in a previous paper as a case study. They found that the process of building and testing a final paper-worthy model required training 4,789 models over a six-month period. Converted to CO2 equivalent, it emitted more than 78,000 pounds and is likely representative of typical work in the field.

The significance of those figures is colossal—especially when considering the current trends in AI research. “<i>This kind of analysis needed to be done to raise awareness about the resources being spent [...] and will spark a debate</i>.”, says <b>Gómez-Rodríguez</b>. “<i>What probably many of us did not comprehend is the scale of it until we saw these comparisons</i>,” echoed <b>Siva Reddy</b>, a postdoc at <b>Stanford University</b> who was not involved in the research.

{{< figure src="desinfo/mit-review-2019 - costs.png">}}

### The privatization of AI research
The results underscore another growing problem in AI, too: <b>the sheer intensity of resources now required to produce paper-worthy results</b> has made it increasingly challenging for people working in academia to continue contributing to research. “<b>This trend toward training huge models on tons of data is not feasible for academics</b> — grad students especially, because we don’t have the computational resources,” says Strubell. “So there’s <b>an issue of equitable access</b> between researchers in academia versus researchers in industry.”

{{< figure src="desinfo/macron-lecun-zuckerberg.png" caption="<b style='color:blue;'>Zuckerberg</b>-<b>Macron</b> buzz at VivaTech. [Les echos](https://www.lesechos.fr/start-up/next40-vivatech/le-duo-zuckerberg-macron-fait-le-buzz-a-vivatech-132831), May 2018. <b style='color:blue;'>Mark Zuckerberg</b> and <b>Emmanuel Macron</b> met (again) at the Elysée. <i>Five days before the second edition of 'Tech for good'</i>. [Huffington post](https://www.huffingtonpost.fr/politique/article/mark-zuckerberg-et-emmanuel-macron-se-sont-encore-rencontres-a-l-elysee_144827.html), May 2019.">}}

{{< figure src="desinfo/mafia-these-CIFRE.png">}}

{{< figure src="desinfo/mafia-france-ia.png" caption="Source: @[Yann Lecun](https://twitter.com/ylecun/status/1629845738170597376?lang=en).">}}

{{< figure src="desinfo/meta-paper-hours-gpu.png" caption="Carbon footprint of training different models in the same data center, from the paper LLaMA on [Arxiv](https://arxiv.org/abs/2302.13971) (section 6 Carbon footprint).">}}

{{< callout warning >}}
<i>The training of our models have consumed a massive quantity of energy, responsible for the emission of carbon dioxide</i> (section 6 Carbon footprint). <i>We plan to release larger models trained on larger pretraining corpora in the future</i> (section 8 Conclusion). [Arxiv](https://arxiv.org/abs/2302.13971).
{{< /callout >}}

## The case of the Century ⚖ (2021)
- 04-24 <i>The digital bluff is all the impacts that we do not see</i>, with <b>Laurie Marrauld</b> from <b>the Shift Project</b> and <b>Cédric Villani</b>. [Libération](https://www.youtube.com/watch?v=6kJYR0oG3GQ&ab_channel=Lib%C3%A9ration).
- 08-22 <b>Citizen's Climate Convention</b>. A part of the 146 proposals is selected by the head of State. Code of the Environment. [Law n° 2021-1104 of August 22, 2021 on the fight against climate change and strengthening resilience to its effects (V)](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000043956924). [Article L231-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000043961211).
- 10-14 <b>Paris court</b>. <i>France sentenced for climate inaction. The State has an obligation to respect its greenhouse gas emissions reduction trajectory and must repair any overrun by <b>December 31, 2022</b>. Each departure from the road on the climate trajectory now constitutes a fault which MUST be repaired</i>. [vie-publique.fr](https://www.vie-publique.fr/en-bref/282012-changement-climatique-la-france-condamnee-pour-prejudice-ecologique).

### [Macron calls for <i>individual sobriety</i>](https://www.ladepeche.fr/2022/09/05/direct-crise-de-lenergie-quelles-mesures-complementaires-pourraient-etre-prises-suivez-en-direct-la-conference-demmanuel-macron-10524445.php)

{{< icon name="calendar" pack="fas" >}} Press conference at the Elysee, September 5, 2022

{{< callout note >}}
Macron was re-elected President on April 24, 2022, two months after the invasion of Ukraine and the energy crisis ⚡. [Elysée](https://www.elysee.fr/emmanuel-macron).
{{< /callout >}}

<i>"Everyone has a role to play"</i>, announced the French president, calling for energy sobriety and believing that <i>"the best energy is that which we do not consume"</i>. The objective stated by <b>Emmanuel Macron</b> is <i>"to save 10% of what we currently consume"</i>. [Elysée](https://www.youtube.com/watch?v=XjC1NqzyGkc&ab_channel=%C3%89lys%C3%A9e). [Sobriety plan ecologie.gouv.fr](https://www.ecologie.gouv.fr/plan-sobriete-acte-2-mobilisation-se-poursuit).