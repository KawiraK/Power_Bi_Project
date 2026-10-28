# Hotel Revenue Insights Dashboard (Power BI)

A personal project: an interactive Power BI dashboard that analyses revenue performance across a multi-city hotel chain.

## What it shows
- **KPIs:** Revenue, RevPAR, ADR, DSRN, Occupancy %, Realisation %, Cancellation % and Average Rating
- **Revenue by category:** Luxury vs Business split
- **Performance by booking platform:** Realisation % and ADR
- **Weekday vs weekend:** comparison of RevPAR, occupancy, ADR and realisation
- **Property-level table:** every hotel with its city and key metrics
- **Filters:** city, room class and week number

## Key insights
- Weekends outperform weekdays on RevPAR (about 8.5K vs 7.6K) and occupancy (about 67% vs 60%)
- The cancellation rate is around 25%
- Business category contributes about 62% of revenue and Luxury about 38%

## Tools and languages
- **Power BI Desktop:** data modelling and visuals
- **DAX:** measures such as Revenue, RevPAR, ADR, Occupancy and Realisation %
- **Power Query:** data cleaning and preparation

## Data model
Star schema with fact tables (`fact_bookings`, `fact_aggregated_bookings`) and dimension tables (`Dim_holets`, `Dim_date`, `dim_rooms`).

## Challenge solved
Revenue first showed the grand total (139M) on every property row. I traced it to a missing relationship and mismatched `property_id` data types. I fixed it by aligning the data types, adding an inactive relationship between `Dim_holets` and `fact_bookings`, and using `USERELATIONSHIP` in the Revenue DAX measure.

## Files
- `Reveneu_insights_Power_bi.pbix`: the Power BI report
- Dashboard screenshot

## Author
Kawira  [LinkedIn](https://linkedin.com/in/karen-kawira-95b119306)
