# Excel pediatric growth curves

## Where to enter the data

Enter the data in the "measurement" sheets, create more as needed
- Field `B1` holds the name
- Field `B2` holds the birthdate
- In the white cells under headings date, weight, length, head enter the data points. Leave blank if unknown.

Input is in metric. Imperial units are shown on the right for reference.

The blue shaded cells are calculated values.

Percentiles are based on data from the U.S. Center for Disease Control and Prevention.

The procentiles are calculated for boys.  To switch to girls, change the first parameter in each function call, e.g.
`=calc_weight4age(2, C5, D5)`

BMI should only be calculated for ages 2 and up.

## The charts

- `length(age)`, shows the length as a function of age
- `weight(age)`, shows the weight as a function of age
- `weigth(length)`, shows the weight as a function of the length
- `head(age)`, shows the head circumference as a function of age
- `bmi(age)`, shows the BMI as a function of age

The procentile curves are based on CDC data for boys.  Feel free to switch to girls of course. To switch to girls, click on a curve and "Select Data", then for each P curve, e.g.:

| variable        | value |
|-----------------|-------|
| Series name     | `="P3 girls"`
| Series X values | `=length4age_girls[X]`
| Series Y values | `=length4age_girls[P3]`

## Trouble shooting

Make sure there are no empty dates in the table, otherwise the graphs will start at `1` instead of `0` years.

## Discussion

Questions? Leave them on the GitHub discussion board for this project.
