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

## Queries
We don’t have a ton of options since our data set isn’t massive:

1. We will get the unemployment rate reports for the last `n` years and overlay the opening and closing values of the DOW Jones Industrial Average for each report’s release date. This will allow one to determine if the unemployment rate affects the DOW and if so, positively or negatively.
  - User input: `<select name="year"><option value="2015">2015</option></select>`. 
2. We will get all the weak Average Directional Index instances then using the date reference, get the unemployment rate for each of the weak reports. Doing this will allow us to determine if a weak Average Directional Index is followed by a relative-high or relative-low unemployment rate.
3. Lastly, we will find all the strong Average Directional Index instances and using the date reference, get the unemployment rate for each of the strong reports. We will be able to gather whether the strong ADX reflects in the unemployment rate data.
