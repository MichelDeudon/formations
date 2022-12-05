---
title: A primer on languages and alphabets
date: '2021-01-01'
type: book
weight: 30
highlight: true
tags:
  - Data Visualization
---

On the origins

<!--more-->

{{< icon name="clock" pack="fas" >}} 4h30 per week, for 3 weeks

## A primer on languages and alphabets

- **Culture**: A primer on languages and alphabets
- **Model**: Bag of char (word embed)
- **Theory**: Message passing. How to transform and pass some information with minimum loss and memory footprint? Ideas from statistical physics, psychology and other fields. No need to be a computer scientist to study computational linguistics.
- **Tip**: Apply minimum steps. Simpler models are better. Ask the right question. Einstein, Feynman
- **Homework**: Setup your environment (Github, Python) for the course use cases

## Quiz

{{< spoiler text="When is a heatmap useful?" >}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{{< /spoiler >}}

{{< spoiler text="Write Plotly code to render a bar chart" >}}

```python
import plotly.express as px
data_canada = px.data.gapminder().query("country == 'Canada'")
fig = px.bar(data_canada, x='year', y='pop')
fig.show()
```

{{< /spoiler >}}
