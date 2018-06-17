# Refining Actions

1. Change 'Calm' & blank values in 9am Wind speed to 0
1. Change 'Calm' value in 3pm Wind speed to 0
1. Changed blank rainfall cell (date 2018-03-28T00:00:00Z) to 0
1. Set 9am cloud amounts that were blank to 0 (There were no 0 values, assumed that blanks are 0)
1. Set 3pm cloud amounts that were blank to 0 (There were no 0 values, assumed that blanks are 0)
1. Added RainToday column set to 'YES' if rainfall > 0, otherwise 'NO'
1. Convert date to ISO8601 format
1. Removed empty leading column
1. Changed column names to use just 'C' instead of degree symbol and 'C'. (Presents better in Plots)
1. Renamed Columns to have time (9am/3pm) at the end (Presents better in plots)
1. Remove Empty Evaporation and Sunshine Hours Columns
1. Create Column 'Season' with season of each entry
1. Changed blank Min Temp cell (date 2017-07-31T00:00:00Z) to '2' (Source: https://www.accuweather.com/en/au/canberra/21921/month/21921?monyr=7/01/2017)
1. Change Wind Direction 9am for calm entries (0 wind speed) to "CALM"
1. Change Wind Direction 3pm for calm entries (0 wind speed) to "CALM"

Refined data saved as `refined_data/Canberra070351_refined.csv`

1. Shifted RainToday Column up by one row, entered 'YES' as last row value (15 June 2018 had 0.8mm rainfall)
1. Renamed RainToday Column to RainTomorrow

Notes:
- 9 Days have no maximum wind gust data - left blank
