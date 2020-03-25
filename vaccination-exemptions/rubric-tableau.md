# Vaccination exceptions, Tableau

This assignment uses the vaccinations exemptions data that you [cleaned in the previous lesson](README.md) to build an interactive dashboard in Tableau that allows readers to explore this data over time by county.

You'll build three charts:

- A map of Texas counties that show the exemption rates by year.
- A bar chart that ranks counties by their rate.
- A line chart that shows the rate change over time for each county.

Interactive filters will be an important part of this dashboard.

## Map by county

We'll make a map of Texas counties showing the exemption rate. We'll use a filter to show just one `School year` at a time.

- Create a new sheet and name it "Map".
- Select the `County`, `Exemption rate` fields.
- Use the **Show Me** tab to find the choropleth map. It's on the second row in the middle. Close the Show Me tab when you are done.
- Click on the dropdown for the `School year` field and choose **Show Filter**.
- Go to the filter at the right and use the dropdown there to choose the **Single value (dropdown)** option.
- Note there is **1 null** indicator at the bottom right of the map. If you click on the indicator and the choose **Edit Locations** and you'll see this is the value for the state, which we can safely exclude. Cancel out of that window and click on the null indicator again and choose **Filter data** to remove Texas.

<video width="320" height="240" controls>
  <source src="img/counth-map.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

Later on we'll remove the "All" option from that filter because we don't want to ever add the Exemption rates together on the map.

## Ranking counties by rate

> Add directions

## County rate over time

> Add directions

## Create dashboard

> Add Directions

## Filters

> Will need updates

- You don't want the yearly percentages to be added together on the map or bar charts, so create/use a filter by School Year that allows only a single year to be chosen at a time, and remove the "All" option. Have it apply to both the map and bar chart at the same time.
- Create a [Dashboard filter action](https://help.tableau.com/current/pro/desktop/en-us/actions_filter.htm) that filters the line chart based on a select of either the map or the bar chart.
- Create a Dashboard highlight action to highlight the map county based on selecting one from the bar chart.

### How to turn in

- Once you are done and saved, go under File to **Export packaged workbook** and submit the resulting `.twbx` file to the canvas assignment.

> Look for a tutorial link for exporting?
