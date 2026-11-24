# Investigate the TMDB Movies Dataset

Exploratory analysis of about 10,000 movies from The Movie Database (TMDb) with pandas and matplotlib.

**Notebook:** `Investigate_a_Dataset.ipynb`

**Power BI file:** `TMDB Dataset Analysis.pbix` (built separately from the notebook and not refreshed with the cleaning below, so its numbers can differ; an earlier online copy was unavailable when checked)

## Questions and answers

1. **Budget and rating:** almost no relationship (Spearman correlation about 0.04).
2. **Budget and revenue:** positively related, correlation about 0.69 among the 3,854 movies with both values recorded. This is an association, not proof of cause.
3. **Budgets over time:** Annual median budgets peaked at $33.5 million in 1997, then declined to $15 million in 2015. These figures exclude zero-budget records and are not adjusted for inflation.
4. **Runtime and revenue:** median revenue rises with runtime, from about $24M (up to 90 minutes) to about $100M (over 150 minutes).
5. **Ratings:** the median average rating is 6.0.

## Data handling

- One exact duplicate row was removed.
- Many movies show a budget or revenue of 0 (5,696 and 6,016 of 10,865). These zeros are treated here as not recorded. This is an assumption of this analysis, not something the dataset states. Questions on budget and revenue use only movies with the needed values.
- Missing text values (cast, director, genres, companies) were labeled "unknown".

## Run it

Install pandas, numpy, matplotlib and Jupyter, then open the notebook in the same folder as `tmdb-movies.csv`.
