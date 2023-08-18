---
title: "Mitt første Quarto dokument"
author: "Arnstein Gjestland"
format: pdf
editor: visual
crossref:
  fig-title: Figur
  tbl-title: Tabell
  fig-prefix: figur
  tbl-prefix: tabell
bibliography: my_bib.bib
keep-tex: true
keep-md: true
---

::: cell
``` {.r .cell-code}
library(tidyverse)
```
:::

## Quarto

Quarto enables you to weave together content and executable code into a finished document.
To learn more about Quarto see <https://quarto.org>.

## Running Code

When you click the **Render** button a document will be generated that includes both content and the output of embedded code.
You can embed code like this:

::: cell
``` {.r .cell-code}
1 + 1
```

::: {.cell-output .cell-output-stdout}
```         
[1] 2
```
:::
:::

You can add options to executable code like this

::: cell
::: {.cell-output .cell-output-stdout}
```         
[1] 4
```
:::
:::

The `echo: false` option disables the printing of code (only output is displayed).

::: {.cell .fig-cap-location-margin}
```` cell-code
```{{r}}
#| label: fig-firstPlot
#| fig-cap: 'Første plot.'
#| fig-cap-location: margin
plot(cars)
```
````

::: cell-output-display
![Første plot.](first_doc_files/figure-pdf/fig-firstPlot-1.pdf){#fig-firstPlot fig-pos="H"}
:::
:::

Mitt første plot er vist i @fig-firstPlot.

Her er samme plot, men nå i ggplot versjon.

::: {.cell .fig-cap-location-margin}
::: cell-output-display
![Samme data som ovenfor, men her i ggplot versjon. Den røde linjen er fra en orinær lineær regresjon, men den blå er en såkalt «smooth». For «smooth» versjonen er et 95% grått bånd for standarfeil tegnet inn.](first_doc_files/figure-pdf/fig-andrePlot-1.pdf){#fig-andrePlot}
:::
:::

I @fig-andrePlot er de samme dataene gjengitt med hjelp av funksjoner fra R [@rcore2023] pakken ggplot2 [@wickham2016] som er en del av tidyverse [@wickham2019].

## Referanser
