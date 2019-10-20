# Vaccination exceptions, Tableau

This assignment uses the `data/exemptions_county` data to build an interactive dashboard in Tableau that allows readers to explore this data over time by county.

## You'll need three charts

Filters will be important and explained next.

- Build a map of Texas counties that show the exemption concentrations.
- Build a bar chart that shows a ranking list of those counties and their rates.
- Build a line chart that shows the change in rate over time by county.)

### Filters

- You don't want the yearly percentages to be added together on the map or bar charts, so create/use a filter by School Year that allows only a single year to be chosen at a time, and remove the "All" option. Have it apply to both the map and bar chart at the same time.
- Create a [Dashboard filter action](https://help.tableau.com/current/pro/desktop/en-us/actions_filter.htm) that filters the line chart based on a select of either the map or the bar chart.
- Create a Dashboard highlight action to highlight the map county based on selecting one from the bar chart.
