---
date: "2020-08-04"
tags:
- R
- code-journal
title: RMarkdown tricks
---

Quick, incomplete notes on things that make life easier when publishing to R markdown and xaringan.

### Managing Citations and References

Confession: Up til recently, I manually managed all my figure references and citations. Moving a table around meant updating the number in the text. Bibliographic references, similarly, were diligently typed up, or, if I was lucky, copy-pasted.

Yeah, not doing that anymore.

If you name r chunks (e.g., `{r fig1 [code here]}`) you can refer to them in the main text with `\@ref(fig:fig1)` for figures or `\@ref(tab:mytable)` for tables. `knitr::kable()` will automatically number tables for you. For ggplot figures, the `fig.cap` setting in the code chunk will do the same.

So, for example, the pseudocode below would result in a plot titled "Figure n: A Summary Chart"
```
{r fig1, echo=FALSE, fig.cap = "A Summary Chart"}

# ggplot object
ggplot()

```

[To be continued]