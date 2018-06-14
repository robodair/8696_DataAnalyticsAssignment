# Refining Actions

1. Convert numeric columns to text to numeric
2. Change 'Calm' & blank values in 9am Wind speed to 0
3. Change 'Calm' value in 3pm Wind speed to 0
4. Changed blank rainfall cell (date 2018-03-28T00:00:00Z) to 0
5. Set 9am cloud amounts that were blank to 0
6. Set 3pm cloud amounts that were blank to 0
7. Added RainToday column set to 'YES' if rainfall > 0, otherwise 'NO'
8. Convert date to ISO8601 format
9. Exported File (refined_data/Canberra070351_201705to201705-refined.csv)
10. Removed empty leading column
11. Shifted RainToday column up by one row, entered 'NO' as last row value
12. Renamed RainToday Column to RainTomorrow

Refined data saved as refined_data/Canberra070351_201705to201705-refined.csv
