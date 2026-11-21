# Renewable Energy Development in African Countries

University of Toronto · STA130 final project · Group TUT0113-C

This project uses R and Quarto to explore how economic development, electricity access, and policy targets relate to renewable electricity generation and installed capacity in African countries covered by the Clean Air Task Force (CATF) dataset.

[View the presentation (PDF)](renewable-energy-africa.pdf) · [Read the Quarto source](renewable-energy-africa.qmd)

## Research questions and findings

| Research question | Descriptive finding |
| --- | --- |
| How does GDP relate to the share of electricity generated from renewables? | The lower-GDP group had a higher median renewable electricity share in the filtered sample. |
| How does the Human Development Index (HDI) relate to renewable electricity share? | The PDF reports a higher median renewable electricity share for the lower-HDI group. The analysis also groups observations by electricity access. |
| How does electricity access relate to installed wind and solar capacity? | Countries in higher electrification groups tended to have more installed variable renewable capacity. |
| How do renewable energy policy targets relate to installed capacity? | Countries reporting positive targets tended to have higher average installed variable renewable capacity. The largest difference was between countries with and without a wind target. |

The Q2 finding above follows the PDF's results and conclusion. The Quarto source's overall conclusion gives the opposite direction for HDI.

The analysis uses boxplots and summary tables to compare groups. For the electricity-access and policy-target questions, repeated student-reported observations were consolidated to one row per country using medians for numeric fields and the most frequent value for text fields. The comparisons are cross-sectional and describe associations.

## Team

Ruihe (Kerry) Yang, Lena Wang, Chloe Jung, and Cobe Chi. Kerry led the analysis of electricity access and installed renewable capacity (Question 3).

## Reproduce the presentation

The PDF contains the original presentation and can be viewed directly. To rebuild it, install R, Quarto, and a LaTeX distribution such as TinyTeX. The Quarto source uses R's native pipe, which requires R 4.1 or later.

1. Obtain the original course dataset, `CATF_data.csv`, and place it beside `renewable-energy-africa.qmd`. The CSV is not included in this repository.
2. Install the required R packages.

   ```r
   install.packages(c("tidyverse", "gridExtra", "knitr", "cowplot"))
   ```

3. From the project directory, render the Beamer slides.

   ```sh
   quarto render renewable-energy-africa.qmd
   ```

## Data and acknowledgements

The project used CATF's *African Electricity Sector Performance Data*. We thank CATF for providing the data and the University of Toronto STA130 instructors and teaching assistants for their guidance.
