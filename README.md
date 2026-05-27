# AB Testing - Shoefly

An A/B testing analysis project for Shoefly, a fictional shoe company. The goal is to determine which of two ad variants performs better using click-through rate data.

## Dataset

`ad_clicks.csv` contains ad impression records with the following columns:

| Column | Description |
|--------|-------------|
| `user_id` | Unique identifier for each visitor |
| `utm_source` | Traffic source (google, facebook, twitter, email) |
| `day` | Day of the week the ad was shown |
| `ad_click_timestamp` | Time of click (null if not clicked) |
| `experimental_group` | Ad variant shown to the user (A or B) |

## Analysis

The analysis is split across two files:

- **`script.py`** — standalone Python script
- **`ab_testing_shoefly.ipynb`** — Jupyter notebook with the same analysis

### Steps

1. **Traffic source breakdown** — count views per UTM source
2. **Click-through rate by source** — percentage of users who clicked per source
3. **A/B group distribution** — verify even split between groups A and B
4. **A/B click comparison** — overall clicks for Ad A vs Ad B
5. **Day-by-day breakdown** — click-through rate per day of the week for each ad

### Conclusion

Ad A outperforms Ad B on most days of the week (all except Tuesday), and has a higher average click-through rate overall. **Ad A is the recommended choice.**

## Requirements

- Python 3
- pandas

## Usage

```bash
pip install pandas
python script.py
```
