---
title: Visualisation
date: '2021-01-01'
type: book
weight: 30
highlight: true
tags:
  - Data Visualisation
---

Apprend à visualiser des données avec Plotly.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1-2 heures par semaines, sur 8 semaines

## Apprendre

{{< youtube hSPmj7mK6ng >}}

## Quiz

{{< spoiler text="Quand une carte thermique (heatmap) est-elle utile?" >}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{{< /spoiler >}}

{{< spoiler text="Écrire du code Plotly pour afficher un graphique à barres (bar chart)" >}}

```python
import plotly.express as px
data_canada = px.data.gapminder().query("country == 'Canada'")
fig = px.bar(data_canada, x='year', y='pop')
fig.show()
```

{{< /spoiler >}}
