R code:

---
title: "Company ABC Employee Report"
subtitle: "Combined Data Report"
output: pdf_document
---

```{r setup, include=FALSE}
# Load necessary packages
library(readxl)
library(knitr)
library(kableExtra)
```

```{r, echo=FALSE}
data <- read_excel("combined_data.xlsx")
```

```{r, echo=FALSE}
# Display the table with customized formatting
kable(data) %>%
  kableExtra::kable_styling(
    font_size = 12,  # Table font size
    full_width = FALSE,  # Do not stretch the table
    position = "center",  # Center the table
  ) %>%
  kableExtra::column_spec(1, width = "5cm", bold = FALSE)# Customize first column
```
