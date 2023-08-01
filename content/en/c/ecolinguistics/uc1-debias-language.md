---
title: 1 - Debias language
date: '2021-01-01'
type: book
weight: 80
tags:
  - Social representations
  - Social regressions
  - Gender bias
  - Stereotypes
  - Data.gouv.fr
  - Artificial Intelligence
  - Digital Humanities
---

Use language for social innovation.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1h20 hands on

## Gender analysis of 2 million streets in France and social regressions

{{< icon name="github" pack="fab" >}} [nlp201-street-names-gender-analysis](https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis)

{{< callout note >}}
NEW! Download our open source {{% staticref "u/Jeux-Memory-Montpellier-qui-est-ce.pdf" %}}Memory game{{% /staticref %}} based on Montpellier's street names.
{{< /callout >}}

More than 93% of the boulevards in France and on [data.gouv.fr](https://adresse.data.gouv.fr/) bear the name of a man among the names of celebrities (Victor Hugo, De Gaulle, Leclerc, Foch, etc.). By comparison, 60% of the gardens bear the name of a woman, some of which correspond to the names of trees or flowers such as Rose, Magnolia or Capucine. Previous studies quantified the rate of representation of women, in the naming of public spaces, in different cities or sectors, at different dates, by different methods. We propose indicators derived from the [National Address Database](https://adresse.data.gouv.fr/) [5] to estimate the rate of representation of women in the naming of public spaces, locally and at the scale of towns, departments and regions in France (over 2 million routes in mainland France and overseas). We find a rate of feminization of roads and public spaces close to 12% in Paris [6] and in cities like Nantes and Montpellier. We analyze the correlations with certain professions, sectors, and compare our results with public Wikipedia pages. Our analysis suggests that the imagination associated with certain professions (doctor, professor, captain, colonel) and sectors in France (mathematics, Fields medal, computer science, Turing prize) induces a gender bias in our social representations and cultivates stereotypes, amplified by the artificial intelligence models LLaMA from Facebook AI Research (FAIR) Paris [4], leading to forms of social regression. We make [our implementation](https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis) freely available to follow the evolution of these biases over time.

### Introduction

Words influence our representations from an early age and shape our collective imagination.
<i>Highly symbolic, the naming of streets and public spaces is an opportunity to pay tribute to famous people, especially women. Since 2014, the proportion of Parisian streets bearing the name of a woman has doubled, reaching 12%</i> - Paris, 2021 [6].

<b>The National Address Base</b> is one of the nine databases of the public reference data service [5]. It is the only address database officially recognized by the administration and as such placed under the responsibility of the Prime Minister. Its construction is ensured in the first place by the municipalities. It is accessible in the form of files and API.
The dataset represents more than $2$ million routes in France, of which 10% contain a gendered name from the list of names and gender of [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/list-of-names/) [18]. Figure 1 shows locally Montpellier streets containing a gendered name. In the rest of this article, we propose a method to quantify gender biases on the [National Address Database](https://adresse.data.gouv.fr/) [5]. We compare our results to public Wikipedia pages and discuss how mathematics, statistics, and the development of competitive, foundational, <i>state-of-the-art</i> artificial intelligences in Paris [4 ] can lead to social regressions in France.

{{< figure src="linguistics/img9.png" caption="Data from the [National Address Database](https://adresse.data.gouv.fr/) [5] in Montpellier. Each street is represented by a blue (male name), red (female name) or gray (other) dot. The rate of feminization of public roads in Montpellier is between 12 and 16%." numbered="true">}}

### Methodology

We annotate the street names of the [National Address Database](https://adresse.data.gouv.fr/) [5] with a label ('F', 'H' or 'other'), from the first names identified from the dataset of names and genders of [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/liste-de-prenoms/) [18]. We preprocess the street names (lowercase letters, without numbers and punctuation) before iterating over each word constituting a street name to extract the first names and gender. For example "rue Sainte Anne" contains the first name "Anne", we annotate it with the label "F". The road "av. Paul Valéry" contains "Paul", we annotate it with the label "H". Otherwise, we return the label 'other'. The vocabulary used and the Python code are freely available on Framagit under CC-BY license at [https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis](https://framagit.org/MichelDeudon/nlp201-street-names-gender-analysis).

### Results

<i> Note: All results are calculated in May 2023, they are subject to change over time. </i>

#### Spatial analysis

{{< figure src="linguistics/france-map-2023.png" caption="Street names and gender aggregated by municipalities in mainland France. Label 1 in blue (resp. 2 in red) corresponds to 100% of routes bearing the names of men (resp. women). The national rate of feminization of public roads is between 8 and 15%, which corresponds to a label between 1.08 and 1.15." numbered="true">}}

Aggregated data by municipality in mainland France is illustrated in Figure 2. For each municipality, we calculate a label between 1 and 2, which corresponds to the ratio of streets bearing a female/male first name. We report in the Table in the Appendix this indicator calculated at the national level and for the 10 largest French cities, and compare our results with other indicators such as the proportion of streets containing the word "Sainte" versus "Saint", or the proportion of female names among the most popular $k$ names. Our results highlight the disproportionality between denominations of public spaces and gender, globally and with local disparities.

#### Linguistic analysis

Among the 50 most common first names in street names, 4 are feminine: Marie, Blanche, Jeanne and Anne. The distribution of first names is skewed towards a male representation of history and its heroes, as illustrated in Figure 3.

{{< figure src="linguistics/word_pyramid.png" caption="Ranking of the 25 most popular male and female first names in the names of roads in France. The distribution of first names follows Zipf's law [23]: a minority of first names (here more than 92\% male) appear very frequently while the majority of first names (mixed) are rarely used." numbered="true">}}

The representation of women varies from one type of track to another. We observe that the gardens are connoted with deities of Nature, with names of flowers and female first names, while the avenues and boulevards are predominantly masculine and connoted with warlords and tanks or weapons of war. The tunnels are exclusively male.
We report in Table 1 the F/M representation rates associated with four professions.

|  Profession | N streets in France  | Label H  |  Label F |  F/M Representativeness (en %) |
|---|---|---|---|---|
|Doctor | 5642 | 1538 | 59 | 3.7 |
|Captain | 971 | 217 | 8 | 3.6 |
|Professor  | 616  | 241 |  4 | 1.6 |
|Colonel | 1298 | 469 | 2 | 0.4 |

<i>F/M representativeness of street names in France, for different professions in 2023 (last column). These values are significantly lower than the national average of 12%. With these gender biases and a naive statistical model, it is necessary to generate more than 25 names of doctors (Albert Tomey, Paul Pezet, Albert Schweitzer, Robert Koch...) to obtain a female name randomly, on average, and more than 60 names of teachers to obtain a female name. Examples of these biases can be obtained by writing "rue du docteur..." in a search engine, on Google Maps or by walking in French streets, curious, with your head raised.</i>

### From the National Address Database to Wikipedia

The names of public roads and spaces in France and on [data.gouv.fr](https://adresse.data.gouv.fr/) quantify centuries of gender stereotypes, such as word embeddings learned from Wikipedia [13].
Facebook AI Research (FAIR) Paris published in 2023 statistical models trained on Wikipedia, called LLaMA [4], partly funded by the CIFRE system. These models were developed during the winter of 2022/23 by 13 men out of 14 authors, including 3 normaliens and 7 polytechnicians. The models, dangerous (sexist, racist, generator of false news) according to the authors, were leaked between February 24 and March 7, 2023, in a context of a health, social and ecological crisis [3].

To the question <i>"Who are the 5 people you would like to meet?"</i>, the FAIR Paris LLaMAs answer 5 male personalities from the Western world: Albert Einstein, Leonardo da Vinci, Socrates, William Shakespeare and Abraham Lincoln [4].
This is partly explained by Zipf's law applied to Wikipedia [23] and the risks inherent in training AI models on Wikipedia and social media, known since 2009 [21], captured by the famous example <i>The doctor is to the nurse what the man is to the woman</i> [13].
Biases come first from humans before coming from algorithms or datasets. Wikipedia is governed by a bureaucracy of pairs [20], an unrepresentative, non-inclusive population [19].
These Human biases come from a lack of diversity, equity, inclusion [12] and the privatization of AI research [11] which reinforce social inequalities [15]. <i>This lack of diversity can lead algorithms to reproduce biases</i> - Villani, 2018 [12].

In 2023, the same AI models are used as in 2017 [14], with more parameters and energy at a more expensive cost. In 5-6 years, the complexity of the models has been multiplied by 1000, from 65 million parameters to 65 billion, from 27 kWh per experiment [11] to 499 MWh [4]. The same problems are there (sexism, racism, fake news) and get worse with the complexity of the models according to the principle of overfitting in statistics [22]: <i>We observe that toxicity increases with model size</i> [4]. The authors conclude, however, <i>we plan to release larger models, trained on larger training corpora in the future</i>. Can we really consider this an innovation [16, 17]? AI experts call for <i>AI to Rescue AI</i>, <i>Trusted AI</i> (Reminiscent of <i>Trusted Men</i> or <i>v-mann</i> [10]). Human biases, conflicts of interest and disinformation in the spheres of power [8] are probably more causes than correlations of the social regressions observed in France and in linguistics: the publication and leakage of LLaMA models precedes the explosion of misinformation and trivialization of violence since March 2023.

|  Indicator | F/M  Representativeness |
|---|---|
|GAFAM CEO | 0/5 | 
|French Turing award | 0/2 | 
|French Fields medal | 0/13 | 
|Deep Learning god fathers | 0/3 | 
|FAIR Paris LLaMA authors | 1/13 | 
|Personnalities LLaMA would like to meet | 0/5 | 

<i>Gender bias in the development of heavy artillery in AI (models with billions of parameters for billions of human beings).</i>

### Imaginations and ideologies

#### Social regressions and eugenics

If the term <i>regression (in statistics)</i>, ubiquitous in <i>artificial</i> intelligence comes from the regression towards the mean of the British Francis Galton in 1886 [24], Sir Galton also coined the term eugenics, used for the first time in 1883 in the context of his studies on the transmission of hereditary characteristics such as the size of individuals, without taking into account the environment, the way of life. Galton's eugenics was born from an error between correlation and causality, and proposed to produce a <i>superior human race</i> by <i>artificial</i> selections, leading in the 20th century to a policy of eradication of characters deemed to be handicapping, the establishment of forced sterilization programs, a tightening of the legal framework for marriage and immigration restriction measures.

#### AI, a colonial fantasy of white men, of the West?

In science fiction movies (2001 Space Odyssey, Her, etc.), AI is represented by a humanoid or a voice, robotic or feminine. Siri, Alexa, smartphone voice assistants actually have the names and voices of female assistants, while the Wikipedia page on the <i>beauty</i> of mathematics refers to 26 men, including Mandelbrot, Russel, Erdos, Beethoven, Dirac, Euler, Harris, Leibniz, Pythagoras, Gauss, Andrew Wiles, Robert Langl, Richard Borcherds, Alexandre Grothendieck, Claude Chevalley, Georges Théodule Guilbaud, Hermann Weyl, Bourbaki, Jean Dieudonné, Hermann Weyl, Plato, Aristotle, Galileo, Alain Badiou, Kepler, Watson, no women [7]. The page mentions <i>"deep"</i> results, reminiscent of <i>"deep"</i> learning and the three 2019 Turing Awards / god fathers of Deep Learning. The page cites what <i>"makes people hard"</i>.
The legend says there are no Nobel Prizes in Mathematics and Computer Science for a reason.
Under/over-sampling names or Wikipedia pages can simply debias statistical language models and computational linguistics, to avoid social regressions without resorting to heavy artillery. We must be wary of <i>experts</i>, who are not direct victims of the weapons produced and whose conflicts of interest can cause certain truths to be omitted and divert attention. We hypothesize that some <i>experts</i> calling for more <i>AI to rescue</i> are in good faith, but this questions the place of trainings on the social and ecological impacts of digital technology in French <i>grandes écoles</i>. This also questions the place of statistical regressions and cognitive biases to counter the decline of scientific culture in our schools, within the state and in our public policies [2]: from 2019 to today, the number of students in the final year with more than 6 hours of mathematics per week, went from 200,000, including 96,000 girls, to 100,000, including 33,000 girls.
Finally, the name given to the Bronner commission, <i>Enlightenment in the digital age</i> [8] will perhaps suffice for some to make the link between the forms of modern slavery, the colonial ideology [9] and the disinformation that characterizes the sexist and racist AI models of FAIR Paris [4], partly funded by the Ministry of Higher Education and Research, through the system of [CIFRE thesis](https://twitter.com/ylecun/status/1629845738170597376?lang=en).

#### Ecology, feminism and ecolinguistics

In the words of Christine Lagarde on March 7, 2023, if the three 2019 Turing Awards were godmothers, rather than godfathers of AI, maybe there would be fewer crises?
Maryam Mirzakhani, mathematician, first and only woman to date Fields Medal (2014), was born in Tehran, Iran. The city of Montpellier pays tribute to her since 2020 (see Appendix B). Marie Curie, born in Warsaw, Poland, is the only person to have won a Nobel Prize in two separate disciplines, physics and chemistry.
As Paul Valéry said, there are two possible visions of the world: the one that divides, the one that unites.
Alain Damasio in an interview for BLAST in May 2023 explains how his vision of science fiction has evolved over time [1] and calls for new imaginaries - in solidarity, social, ecological - and frugal innovations [17].

### Conclusion

Public roads and spaces in France, like certain public Wikipedia pages, present gender biases that stem from Humans. GAFAM's AI models, trained on Wikipedia, like FAIR Paris' <i>state-of-the-art</i> foundational LLaMAs, cultivate and amplify these stereotypes, with energy at a more expensive price as a <i>competitive</i> advantage while benefiting from public funding. In this context, the voices and representations of women in public spaces are more than symbolic.
Among the directions of future research, it could be interesting to quantify and fight against other forms of discrimination (religion, color, sexual orientation, age, nationality, handicap, physical appearance, socio-economic status), or to analyze other countries and distributions.
Authors, researchers, scientists, artists, offer alternatives, new imaginaries, stories and social representations to fight against patriarchy and surveillance capitalism. In these forms of modern resistance, libraries are to the maquis what books and culture are to weapons, a means to escape.

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

### Appendix

#### Appendix A. Rate of feminization of roads and public spaces

{{< figure src="linguistics/taux-feminisation.png">}}

#### Appendix B. Local heroines, in Occitania

| Tribute in Montpellier | Birth | Imaginary |
|---|---|---|
|Agnès Mac Laren | Edimbourg, 1837 | First woman to graduate from medical school.|
|Albertine Sarrazin | Alger, 1937 | French writer, died at 29 in Montpellier.|
|Anne Bragance | Casablanca, 1945 | French writer, Alice-Louis-Barthou prize in 1978.|
|Anne Marie de Backer | Contres, 1908 | Poetess and translator, died in Montpellier in 1987.|
|Catherine Booth | Mumford, 1829 | Co-founded the Salvation Army.|
|Clara d’Anduza | Gard, 1200 | Occitan-speaking Trobairitz.|
|Clara Haskil | Bucarest, 1895 | Romanian and Swiss pianist.|
|Chantal Mauduit | Paris, 1964 | Alpinist.|
|Clara Zetki | Wiederau, 1857 | Teacher, journalist, figure of socialist feminism.|
|Dora Maar | Paris, 1907 | Photographer and artist.|
|Elena Bonner | Mary, 1923  | Pediatrician, human rights activist.|
|Elyse Deroche | Paris, 1882 | Actress and aviator.|
|Frances de Cezelli | Montpellier, 1558 | Heroine during the religious war.|
|Frida Kalho | Coyoacan, 1907  | Mexican painter.|
|Gabriela Mistral | Vicuna, 1889 | Chilean poetess.|
|Germaine Bousquet |Castres, 1920  | Dean of Rieumes.|
|Helene de Savoie |Cetinje, 1873  | Died in Montpellier in 1952.|
|Janine Teisson |Toulon, 1948 | Novelist.|
|Jeanne Demessieux | Montpellier, 1921 | Organist, pianist, improviser, teacher and composer.|
|Jeanne Dieulafoy | Toulouse, 1851 | Archaeologist.|
|Jeanne Galzy | Montpellier, 1833 | Associate professor, writer and prize femina-happy life.|
|Joelle Wintrebert | Toulon, 1949 | Writer.|
|Judith Restnick | Akron, 1949 | American astronaut.|
|Juliette Greco | Montpellier, 1927 | Singer and actress.|
|Juliette Cauquil | Suc-et-Sentenac, 1914 | Resistant.|
|Louise Guiraud | Montpellier, 1860 | Historian.|
|Lucie Février Pascal | Hérault, 1911 | Heroine, recognized as “Righteous Among the Nations”.|
|Madeleine Roch | Mureaux, 1883 | French actress and tragedian.|
|Malika Mokeddem | Kénadsa, 1949 | Writer.|
|Marcelle Huc | Montady, 1901 | Teacher, trade union and political activist.|
|Maria Blanchard | Santander, 1881 | Artist and painter.|
|Maria Casarès | La Corogne, 1922 | Actress and tragedian.|
|Marie Agnès Péron | Calais, XX | Sailor disappeared at sea in 1991.|
|Marie Caizergues | XX, 1797 | Benefactress.|
|Marie Reynès Montlaur | Montpellier, 1866 | Writer, first woman at the Montpellier Academy.|
|Marie Sagnie | Saint-Pons-de-M, 1898 |Mathematics and physics-chemistry teacher.|
|Marie Thérèse Barbé | Limoges, 1913 | Writer.|
|Maryam Mirzakhani | Téhéran, 1977 | Mathematician, professor and Fields Medalist.|
|Paulette Hauchard | Fécamp, 1932 | President of the Secular Association.|
|Régine Detambe | Saint-Avold, 1963 | Writer.|
|Rosa Luxemburg | Zamosc, 1871 | German communist activist and revolutionary.|
|Ruth Bader Ginsburg | New York, 1933 | American lawyer, jurist, scholar and judge.|
|Suzanne Ballivet | Paris, 1904 | Painter and illustrator.|
|Suzanne Bernard | Troyes, 1893 | Aviator.|
|Sylvie et Josephine Fabre | Grenoble, 1951 | Writer and poetess, Louise-Labé Prize.|
|Yvonne le Roux | Toulon, 1882 | Resistant.|
|Yvette Llere | Amélie-les-Bains, 1939 | Writer.|
|Yvonne Molinier | Grand-Combe, 1924 | Dedicated her life to the cause of children.|

<i> Tributes to XX women in Montpellier, Occitanie.</i>

See also the page [Portraits of women from Montpellier](https://www.montpellier.fr/4412-femmes-de-montpellier.htm).