# Community-based sharia micro-insurance for traditional fishermen in Bulak, Surabaya

Student Creativity Program (PKM-RSH) 2025, funded by Belmawa, Kemdiktisaintek. I led the five-person team and did the quantitative analysis.

The notebook prices boat-damage cover for traditional fishermen from a survey of 93 respondents:
- **Damage counts:** Poisson, binomial and negative binomial fitted; the binomial (n = 2, p = 0.3656) fits best, so E[N] = 0.7312 events per boat a year.
- **Repair costs:** exponential, gamma, lognormal and normal fitted; the lognormal fits best under the Kolmogorov–Smirnov test, with E[X] = Rp169,064.29.
- **Pure premium:** E[N] × E[X] = Rp123,616.90 a year. The gross premium, Rp164,822.53 a year or **Rp13,735.21 a month**, splits the contribution into 75% for claims (tabarru'), 10% ujrah and 15% investment, and was reviewed by an insurer's head actuary and an ITS actuarial academic.

**Try it:** the interactive premium calculator on my portfolio: [https://naufalabdul11.github.io/#models/premium](https://naufalabdul11.github.io/#models/premium).

## About the data
The real survey is not published. `data/survey_synthetic.csv` is synthetic: 93 boats with 68 damage events in total, and repair costs generated so that their log-mean and log-standard deviation equal the estimates from the real survey. The notebook therefore reproduces the published figures (p = 0.3656, E[X] = Rp169,064.29 and the premium) while no row belongs to a real respondent. Goodness-of-fit statistics and the ranking of the other candidate distributions will differ from the article.

## Run it
```bash
pip install -r requirements.txt
jupyter notebook notebooks/premium_pricing.ipynb
```

Credit: PKM-RSH 2025 team, ITS. Portfolio: https://naufalabdul11.github.io
