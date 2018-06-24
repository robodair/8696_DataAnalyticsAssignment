# Refining Actions

|Action|Reason|
| - | - |
| Set Wind speed cells containing 'Calm' or were blank to 0 | This column makes more sense being completly numerical as wind speed is a continuous value|
| Set Wind Direction for calm entries (0 wind speed) to "CALM"| This provides a categorical label for direction when there is no wind speed |
| Blank rainfall cell (2018-03-28) set to 0 | No rainfall data available, this is an assumption |
| Blank Cloud Cover cells set to 0 | There were no 0 values, assumed that blanks are 0 |
| Min Temp for 2017-07-31) = 2 | Data was missing, found data from alternative source: https://www.accuweather.com/en/au/canberra/21921/month/21921?monyr=7/01/2017 |
| Convert Maximum wind gust time to minutes from 00:00 | Made column numerical, which makes sense for the continuous value that time is |

Other Notes:
- 9 Days have no maximum wind gust data - left cells blank
- Dropped empty leading column
- Changed column names to use just 'C' instead of degree symbol and 'C', it presents better in plots.
- Renamed Columns to have time (9am/3pm) at the end to avoid 'X' name prefix when using rattle.
- Removed empty 'Evaporation' and 'Sunshine Hours' Columns
