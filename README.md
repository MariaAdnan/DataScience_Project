# Predicting Socioeconomic Vulnerability During Calamities
### Insights from Pakistan's COVID-19 Microdata

A machine learning project that models household-level socioeconomic vulnerability in Pakistan using nationally representative COVID-19 impact survey data, translating predictive findings into concrete, evidence-based policy recommendations.

---

## Overview

Major crises — pandemics, economic shocks, climate disasters — don't hit everyone equally. The poor consistently absorb the greatest relative harm. This project moves beyond simply observing that fact to **predicting which households are most vulnerable** to financial instability, job loss, food insecurity, and poor health during future calamities.

We built a composite vulnerability index, trained predictive models against it, and explored clustering to surface region- and occupation-specific patterns — then translated those patterns into a formal policy brief.

## Dataset

- **Source:** [Pakistan Bureau of Statistics — Microdata on COVID-19 Impact on Wellbeing](https://www.pbs.gov.pk/content/microdata-covid-19)
- **Size:** ~30,000 households, nationally representative
- **Timeframe:** Pre-, during, and shortly after the COVID-19 pandemic
- **Variables:** Income, employment status, household size, education, food consumption, coping mechanisms, government aid, and health-related responses (mixed numerical + categorical)

**Limitations:** Self-reported income/employment figures carry potential bias, and since the dataset is COVID-specific, predictive patterns may not fully generalize to crises of a different nature.

## Approach

1. **Composite vulnerability index** — constructed from income loss, food insecurity, education, and healthcare access indicators
2. **Predictive modeling** — household-level classification against the vulnerability index (Python: pandas, scikit-learn)
3. **Clustering** — unsupervised exploration to surface regional and occupational vulnerability groups
4. **Policy translation** — model outputs mapped to targeted, region- and sector-specific interventions

## Key Findings

- **Urban Sindh is the most vulnerable region nationally** — households there report 95–100% income loss, high food insecurity, and comparatively low education levels. The model performs best here, with an F1 score of 0.7868 and 83% recall for food insecurity.
- **Informal and agricultural workers absorbed the most severe shocks**, frequently losing their entire livelihoods.
- **Formal employment did not fully insulate households** — even the employer-employee sector saw substantial income disruption.
- **Large households (8+ members) showed slightly more resilience**, consistent with extended family networks acting as informal safety nets.
- **AJK and Gilgit-Baltistan show low predicted vulnerability** but limited economic diversification and geographic isolation flag them for preventive investment.
- **Current aid is cash-transfer heavy**, even in the highest-vulnerability region, offering short-term relief without addressing structural exposure.

## Policy Recommendations

1. Sector-specific social protection for agricultural/informal workers, plus a mandatory crisis-contingency savings fund for the formal sector
2. Integrated, multi-dimensional intervention in Urban Sindh (food security, employment stabilization, layoff protections, skills development)
3. Shift from cash-only assistance to capability-enhancing support (financial literacy, micro-enterprise formation, reskilling)
4. Preventive investment in low-vulnerability but structurally marginal regions (AJK, Gilgit-Baltistan)
5. Institutionalized support for community-based resilience mechanisms (food-sharing networks, welfare committees, community infrastructure)

Full analysis and citations (Sen's capability approach, informal economy literature, feminist political economy) are in [`Policy_Brief.pdf`](./Policy_Brief.pdf).

## Targeted SDGs

`SDG 1` No Poverty · `SDG 2` Zero Hunger · `SDG 3` Good Health & Well-being · `SDG 8` Decent Work & Economic Growth · `SDG 16` Peace, Justice & Strong Institutions

## Team

Madiha, Maria, and Muhammad Saad — equal contribution across data cleaning, modeling, and policy analysis.

## References

- Chen, M. A. (2012). *The informal economy: Definitions, theories and policies.* WIEGO Working Paper.
- Elson, D. (1998). The economic, the political and the domestic. *New Political Economy*, 3(2), 189–208.
- Hallegatte, S., et al. (2020). From poverty to disaster and back. *Economics of Disasters and Climate Change*, 4(2), 223–247.
- Martin, A., et al. (2020). Socio-economic impacts of COVID-19 on household consumption and poverty. *Economics of Disasters and Climate Change*, 4(3), 453–479.
- Sen, A. (1999). *Development as Freedom.*
- UNDP. (2022). *Human Development Report 2021-22.*
- World Bank. (2022). *World Development Report 2022: Finance for an Equitable Recovery.*