# Car Dealership EDA

Exploratory data analysis of **558,837 US used-car sales** to help a California dealership that is losing ground to new competitors decide what to stock, how to price, and where to expand.

## Questions answered
- Which makes and models sell best (locally and in the top-performing dealerships)?
- How do condition, mileage and model year relate to selling price?
- How do sale prices compare with the market (MMR) index? A new `price_diff` feature captures this.
- State-level consumer preferences, e.g. which colours sell highest in Tennessee.

## Key findings
- US buyers prefer American-made cars overall; the **Ford Focus SE** is the most popular single model.
- **Nissan, Ford and Chevrolet** dominate the inventory of the best-performing dealerships.
- Condition, mileage and year relationships give a basis for trade-in (barter) and inventory decisions.
- In Tennessee, brown cars sold highest on average (~$19.2k), ahead of yellow (~$16.2k).

## Approach
1. Load and profile the data (16 columns, model years 1982–2015).
2. Clean: VIN as index, merge `model` + `trim`, drop redundant columns, handle missing values (545,544 rows kept).
3. Feature engineering: `price_diff = sellingprice - MMR`.
4. Answer business questions with grouped aggregations and charts.

## Tech stack
Python · pandas · Matplotlib · Seaborn · Plotly · Basemap

## Repository contents
| File | Description |
|------|-------------|
| `Dealership EDA.ipynb` | Full analysis notebook |
| `Car_Dealership_EDA_Farid_Rahimli.htm` | Rendered HTML report (open in a browser) |

## Run it
The dataset (`car_prices.csv`) is not included. Place it next to the notebook, then:
```bash
pip install pandas matplotlib seaborn plotly basemap jupyter
jupyter notebook "Dealership EDA.ipynb"
```
