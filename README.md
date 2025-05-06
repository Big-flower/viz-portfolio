# viz-portfolio
This is a short demo for my visualization
# Rural Data Visualization Portfolio

## Overview

This repository hosts code, data, and output figures for a set of static data visualizations created with **ggplot2**  and **D3.js**.
Each example follows a **data‑prep → figure** workflow.

> **Workflow conventions**
>
> 1. **data\_prep** – downloads/raw‑data, transforms or reshape data, prepares objects for plotting
> 2. **figure** – builds and exports the final graphic to **/output** at publication quality

---

## Repository structure

```
.
├── acs-broadband/           # Example 1 — ACS
│   ├── data_prep.R
│   ├── analysis.R
│   ├── figure.R
│   └── output/
│       └── broadband_subscription.png
├── bea-wage-growth/         # Example 2 — BEA
│   ├── data_prep.R
│   ├── analysis.R
│   ├── figure.R
│   └── output/
│       └── wage_growth.png
├── bls-unemployment/        # Example 3 — BLS
│   ├── data_prep.R
│   ├── analysis.R
│   ├── figure.R
│   └── output/
│       └── unemployment_gap.png
├── renv.lock                # Reproducible package versions (optional)
├── .gitignore               # Exclude cache, large raw files, etc.
└── README.md                # You are here
```

Feel free to rename, remove, or add folders as your portfolio evolves.

---

## Visualization catalog

Below is a template you can copy‑paste for each visualization folder.  Replace the text in *italics*.

### 1. *Rural vs. Urban Broadband Subscription Rates*

* **Location:** `acs-broadband/`
* **Data source:** American Community Survey 2019‑2023 5‑year, table **B28002**
* **Research question:** *e.g., How large is the rural–urban gap in household broadband access?*
* **Key takeaway:** *One‑sentence headline of the plotted finding.*
* **Figure preview:** ![](acs-broadband/output/broadband_subscription.png)

### 2. *Non‑metro Wage Growth, 2010‑2023*

*(Repeat the bullet list above for each additional figure.)*

---

## Reproducing all figures

```r
# Option 1 – run scripts one by one
source("acs-broadband/data_prep.R")
source("acs-broadband/analysis.R")
source("acs-broadband/figure.R")

# Option 2 – use {targets}
# tar_make() will rebuild everything that is out of date
```

> **Tip:** If you commit large raw data files, consider adding **Git LFS**.

---

## Environment

| Package     | Tested version |
| ----------- | -------------- |
| R           | 4.4.0          |
| ggplot2     | 3.5.0          |
| cori.charts | 0.3.1          |
| dplyr       | 1.1.5          |
| tidyr       | 1.4.0          |

Lock exact versions with **`renv::snapshot()`** (generates *renv.lock*).

---

## License

This portfolio is released under the **MIT License**.  Data sources remain subject to their respective terms of use.

---

## Contact

*Your Name* · *[email@example.com](mailto:email@example.com)* · GitHub: *@yourhandle*
