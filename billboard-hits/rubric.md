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

## Goals (or ideas)

1. Who are the Top 10 artists based on the number of songs on the charts?
2. Rank artists by the most number 1 hits
    - Do the same, but since you were born. Or the most recent 10 years. Or during the years you were in high school.
3. Rank artists by the most Top 10 hits?
4. Pick an artist you like that has more than five hits:
    - Make a table that shows the songs, the number of weeks on the chart, the top position that song had. Arrange it by most number of weeks on the chart.
    - Make a bar chart of just the songs and number of weeks on the chart, arranged with highest on top.
    - Make a point chart that shows the top 5 songs and the week the were on the charts and their position that week.
