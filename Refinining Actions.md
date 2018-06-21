# Refining Actions

|Action|Reason|
| - | - |
|Wind 'Calm' & blank = 0|Made column numerical|
|Blank rainfall cell (2018-03-28T00:00:00Z) = 0|No rainfall data available|
|Cloud Cover blank = 0 | There were no 0 values, assumed that blanks are 0)|
|Create Column 'Season' with season of each entry|Thought it might be useful to group factors contributing to rainfall|
|Min Temp for 2017-07-31T00:00:00Z) = 2 |Data was missing, found data from alternative source: https://www.accuweather.com/en/au/canberra/21921/month/21921?monyr=7/01/2017|
|Wind Direction for calm entries (0 wind speed) = "CALM"|Ensured that there were categorical labels for all cells|
|Convert Maximum wind gust time to minutes from 00:00|Made column numerical|
|Created column 'Rainfall Tomorrow (mm)', which is the Rainfall column shifted up one cell|Useful for modelling correlations|
|Derived 'RainTomorrow' column YES/NO from 'Rainfall Tomorrow (mm)'|Required for final class prediction|

Other Notes:
- 9 Days have no maximum wind gust data - left cells blank
- Dates converted to ISO8601
- Dropped empty leading column
- Changed column names to use just 'C' instead of degree symbol and 'C', it presents better in plots.
- Renamed Columns to have time (9am/3pm) at the end to avoid 'X' name prefix when using rattle.
- Removed Empty Evaporation and Sunshine Hours Columns
- 15 June 2018 had 0.8mm rainfall, used this to fill the last 'Rainfall Tomorrow' cell
