# HW6
## Data
#### Dow Jones
```
time
open
high
low
close
volume
id
timestamp
Relative Strength Index (momentum indicator)
Average Directional Index (trending up or down)
Correlation Coefficient (strength of the relationship between the two variables above)
```

#### UNEMPLOYMENT RATE
```
date
unemployment rate
```

## Possible Tables

#### Unemployment Rate
```
id
date_id (FK)
unemployment_rate
```

#### Dow Jones
```
id
date_id (FK)
average_directional_index_id (FK) (When populating our data, we will look at the ADX to figure out which FK to reference. This is the definition: weak < 20, flat <= 25, strong > 25) 
open
close
```

#### Reporting Dates
```
id
date
```

#### Average Directional Index
```
id
trend (weak, strong)
```

## Possible Queries
We don’t have a ton of options since our data set isn’t massive. But I think we can come up with three. Something like:

1. Get the unemployment rate reports for the last 5 years and overlay the DOW open/close for each report.
2. Get all the weak ADX and see what was the unemployment rate at each time?
3. ???
