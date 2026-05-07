# Description of Methodology

## Data Source(s)

- The data used for this project was obtained from the CORGIS dataset on construction spending.
- Specifically, the dataset was accessed through the course-provided link and downloaded as a CSV file:
- https://corgis-edu.github.io/corgis/csv/construction_spending/
- The dataset includes monthly construction spending across multiple categories such as residential, commercial, and total construction.

## Data Preparation/Cleaning

- The dataset was loaded into a pandas DataFrame using pd.read_csv().
- Columns such as "annual.combined.residential", "annual.combined.commercial", and "annual.combined.total construction" were converted from strings to numeric values using pd.to_numeric().
- A new "date" column was created by combining "time.year" and "time.month".
- The data was sorted by date to display trends in chronological order.
- A groupby function was used on "time.month" to calculate average construction spending per month.

## Assumptions

- Each month represents the full month's construction spending.
- All monetary values are comparable over time without adjusting for inflation.
- Categories are consistently defined across the dataset.
- Monthly averages represent seasonal trends.

## Limitations

- The dataset does not account for weather, economic changes, or policy impacts.
- Data is aggregated nationally, so regional differences are not shown.
- Monthly comparisons may not fully reflect real construction cycles.
- Inflation is not accounted for.