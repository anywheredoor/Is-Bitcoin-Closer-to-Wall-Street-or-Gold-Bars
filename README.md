# Is Bitcoin Closer to Wall Street or Gold Bars?

This repository contains an R-based correlation study comparing Bitcoin (BTC-USD) with the Nasdaq-100 ETF (QQQ) and the Gold ETF (GLD) over 2020-2024. The analysis focuses on daily log returns, full-sample correlations, and rolling correlations to assess whether Bitcoin behaves more like a risk-on equity proxy or a defensive asset.

Presentation: [Project presentation](https://youtu.be/zPuw4xVlOFM)

## Key findings

- Bitcoin exhibits substantially higher day-to-day volatility than QQQ and GLD.
- Bitcoin's returns are positively correlated with QQQ, while its correlation with GLD is weaker and closer to zero.
- Rolling correlations vary over time, but BTC-QQQ co-movement is typically stronger than BTC-GLD in 2020-2024.

## Data

- Source: Yahoo Finance (via the R package `quantmod`).
- Assets: BTC-USD, QQQ, GLD.
- Frequency: Daily adjusted close.
- Period: 2020-01-01 to 2024-12-31.
- Output dataset: `crypto_traditional_prices_2020_2024.csv`.

## Methodology

- Construct daily log returns for each asset.
- Compute summary statistics (mean, volatility, min, max).
- Estimate full-sample Pearson correlations.
- Evaluate rolling 60-day correlations to capture time variation.

## Repository structure

- `Project Report.Rmd`: Reproducible analysis and figures.
- `Project Report.html`: Rendered report.
- `crypto_traditional_prices_2020_2024.csv`: Cleaned price panel used in the report.
- `LICENSE`: MIT license.

## Reproducibility

### Requirements

- R (recent version recommended).
- Packages: `quantmod`, `dplyr`, `tidyr`, `ggplot2`, `zoo`, `knitr`, `rmarkdown`.

### Run the analysis

```r
install.packages(c("quantmod", "dplyr", "tidyr", "ggplot2", "zoo", "knitr", "rmarkdown"))
rmarkdown::render("Project Report.Rmd")
```

The report will re-download market data from Yahoo Finance and regenerate the output tables and figures.

## License

Distributed under the MIT License. See `LICENSE` for details.
