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

## Discretization and Binarization

## Attribute Transformation

## Target Columns

Created column 'IGNORE Rainfall Tomorrow (mm)', which is the Rainfall column shifted up one cell, which might prove Useful for examining correlations.

Derived 'TARGET Rain Tomorrow' column True/False from 'Rainfall Tomorrow (mm)' as this is required for classification validation.

Create Column 'IGNORE Rain Tomorrow Intensity' for rainfall intensity NONE/LIGHT/MODERATE/HEAVY/VIOLENT

Create Column 'IGNORE Light UP' for rainfall intensity True/False

Create Column 'IGNORE Moderate UP' for rainfall intensity True/False

Create Column 'IGNORE Heavy UP' for rainfall intensity True/False

Create Column 'IGNORE Violent UP' for rainfall intensity True/False

Create Column WEIGHT with weights inversely proportional to the count of each class in the dataset
