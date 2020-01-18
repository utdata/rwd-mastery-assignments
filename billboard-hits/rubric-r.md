# Billboard rubric for R

> This will need to be updated for new data schema.

Be sure to see the [README](README.md) for the source information and data dictionary.

## Downloading the data

The data imports fairly cleanly, but you might want to convert the `week_id` to a real date.

### Download to keep locally

I recommend downloading the csv file into your project so you can work later without being connected to the internet. You have to create the `data-raw` folder first.

```r
# download
download.file("https://raw.githubusercontent.com/utdata/rwd-r-assignments/master/billboard-hits/billboard.csv", "data-raw/billboard.csv")
# import
billboard <- read_csv("data-raw/billboard.csv") %>% clean_names()
```

After you have downloaded the file, comment out the `download.file` line so you don't re-download when you rerun the your notebook.

## Rubric

1. Who are the 10 artists that have had the most appearances on the Top 100 chart.
    - Build a table (a data frame printed to the screen) to show the Performer and the number of times they've had a song on the chart. Arrange by most at the top. Only display the top 10 rows.
2. Who had the most No. 1 hits?
    - Build a data frame that filters to only No. 1 hits, then counts the distinct performer/song combinations. Count how many times the performer is on that list and arrange by those that have most. Show only the top 10 performers.
    - Do the same as above, but first filter for the most recent five years. [This might help](https://utdata.github.io/r-journalism-examples/dates.html#filter-by-date).
3. Who had the most hits in the Top 10? This is similar to above, but include song in the Top 10 as opposed to No. 1. Build a data frame to show the top of that list.
4. Pick an artist you like that has five or more hits:
    - Make a table that shows the songs, the number of weeks on the chart, and the peak position that song had. Arrange it by most number of weeks on the chart.
    - Make a bar chart of just the songs and number of weeks on the chart, arranged with highest on top. Make sure it has a title and clean axis names. You might need to `fct_reorder()` your data to get the bars in the right order.

### Extra credit

This one will take some work and experimentation. For your chosen artist **make a point chart that plots their song positions by week**. (You can reduce the number of individual songs to a few, if you wish.) Some hints:

- You'll want to use `fct_reorder()` to order the `song` value by the `week_id`.
- You might want to use `scale_y_reverse()` so 100 is at the bottom and 1 is at the top, since that is the "high" value.
- You might want to use `expand_limits(y = 0)` if your artist doesn't have any hits hear the "top" of the charts.
- Not required for the credit, but this is a good candidate to use the `library(plotly)` and the `ggplotly()` function to make your graphic interactive so you can explore the values for each point. You can [review how to do that here](https://utdata.github.io/rwd-class/graphics.html#plotly-for-more-interactive-graphics).

## Notes for the instructor

- Repo is [rwd-r-billboard-answers](https://github.com/utdata/rwd-r-billboard-hits-answers).
