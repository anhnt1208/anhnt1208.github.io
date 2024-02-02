---
title: Include diagrams into Markdown with Mermaid
subtitle: Include diagrams into Markdown with Mermaid 
tags: [Docs as Code, Markdown]
---

[**Mermaid**](https://github.com/mermaid-js/mermaid#readme) is a JavaScript based diagramming and charting tool that takes Markdown-inspired text definitions and creates diagrams dynamically in the browser. 
Maintained by Knut Sveidqvist, it supports a bunch of different common diagram types for software projects, including flowcharts, UML, Git graphs, user journey diagrams, and even the dreaded Gantt chart.

Working with Knut and also the wider community at CommonMark, we’ve rolled out a change that will allow you to create graphs inline using [Mermaid syntax](https://mermaid.js.org/#/n00b-syntaxReference?id=syntax-structure), for example:

```
  graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
The raw code block above will appear as this diagram in the rendered Markdown:

![My helpful screenshot]({% link ./rendered-diagram.webp %})

Mermaid has been getting increasingly popular with developers and has a rich community of contributors led by the maintainer Knut Sveidqvist. 
We are very grateful for Knut’s support in bringing this feature to everyone on GitHub. 
If you’d like to learn more about the Mermaid syntax, head over to the [Mermaid website](http://mermaid-js.github.io/mermaid/) or check out Knut’s first official [Mermaid book](https://amzn.to/339uQRn).