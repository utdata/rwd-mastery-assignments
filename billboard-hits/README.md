# Billboard Top 100 hits

Weekly Hot 100 singles chart between 8/2/1958 and 12/28/2018 pulled from [data.world](https://data.world/kcmillersean/billboard-hot-100-1958-2017) and only through 2017. See link for more information.

## Data dictionary

This dataset contains every weekly Hot 100 singles chart from Billboard.com. Each row of data represents a song and the corresponding position on that week's chart. Included in each row are the following elements:

- url: Billboard Chart URL
- WeekID: Date of chart release
- Week Position: Current week on chart
- Song: Song name
- Performer: Performer name
- SongID: Concatenation of song & performer
- Instance: This is used to separate breaks on the chart for a given song. Example, an instance of 6 tells you that this is the sixth time this song has appeared on the chart, with skips in between.
- Previous Week Position: As of the current date
- Peak Position: Top position on chart as of this date
- Weeks on Chart: Weeks on chart as of this date

## Downloading the data

The data imports fairly cleanly, but you might want to convert the `week_id` to a real date.

### Download to keep locally

I recommend downloading the csv file into your project so you can work later without being connected to the internet. You have to create the `data-raw` folder first.

```r
# download
download.file("https://raw.githubusercontent.com/utdata/rwd-r-assignments/master/billboard-hits/billboard.csv", "data-raw/billboard.csv")
# import
billboard <- read_csv("data-raw/billboard.csv")
```

### Download directly into a dataframe

Or, You can download directly into a data frame with `read_csv()`.

```r
billboard <- read_csv(url("https://raw.githubusercontent.com/utdata/rwd-r-assignments/master/billboard-hits/billboard.csv"))
```

## Rubric

1. Who are the Top 10 artists based on the number of songs on the charts?
    - Build a table (a data frame printed to the screen) to show the performer and the number of weeks they've had a song on the chart. Arrange by most at the top. Only display the top 10 rows.
2. Who had the most No. 1 hits?
    - Build a data frame that filters to only No. 1 hits, then counts the distinct performer/song combinations. Count how many times the performer is on that list and arrange by those that have most. Show only the top 10 performers.
    - Do the same as above, but first filter for the years you were in high school. [This might help](https://utdata.github.io/r-journalism-examples/dates.html#filter-by-date).
3. Who had the most hits in the Top 10? This is similar to above, but any song in the Top 10 as opposed to No. 1. Build a data frame to show the top of that list.
4. Pick an artist you like that has five or more hits:
    - Make a table that shows the songs, the number of weeks on the chart, and the peak position that song had. Arrange it by most number of weeks on the chart.
    - Make a bar chart of just the songs and number of weeks on the chart, arranged with highest on top. Make sure it has a title and clean axis names. You might need to `fct_reorder()` your data to get the bars in the right order.

### Extra credit

This one will take some work and experimentation. For your chosen artist **make a point chart that plots their song positions by week**. (You can reduce the number of individual songs to a few, if you wish.) Some hints:

- You'll want to use `fct_reorder()` to order the `song` value by the `week_id`.
- You might want to use `scale_y_reverse()` so 100 is at the bottom and 1 is at the top, since that is the "high" value.
- You might want to use `expand_limits(y = 0)` if your artist doesn't have any hits hear the "top" of the charts.
- Not required for the credit, but this is a good candidate to use the `library(plotly)` and the `ggplotly()` function to make your graphic interactive so you can explore the values for each point.

## Notes for the instructor

- Repo is [rwd-r-billboard-answers](https://github.com/utdata/rwd-r-billboard-hits-answers).