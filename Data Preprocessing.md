# Data Preprocessing

## Aggregation

Dates aggregated into a 'Season' column to investigate trends in each season. We thought that seasons might be a way to group different sets of numeric conditions that influenc rainfall.

## Sampling

Sampling was not required because the dataset is small anyway.

(Maybe we should sample to ensure rainfall days are in test and train?)

## Dimensionality reduction


## Feature subset selection

Variables with strong correlation investigated with scatter plots - which should be excluded?

## Feature creation

Differentials in 9am to 3pm measurements (earlier - latter) were created as the columns:
- Temperature delta
- Relative humidity delta
- Cloud amount delta
- Wind speed delta
- MSL pressure delta
- Temperature range

The column 'Temperature Range' was created to store the difference between the maximum and minimum temperatures for the day.

Created column 'Rainfall Tomorrow (mm)', which is the Rainfall column shifted up one cell, which might prove Useful for examining correlations.

Derived 'RainTomorrow' column True/False from 'Rainfall Tomorrow (mm)' as this is required for classification validation.

Create Column 'Rain Tomorrow Type' for rainfall type NONE/LOW/HIGH

## Discretization and Binarization

## Attribute Transformation
