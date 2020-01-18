# Billboard Hot 100

In this repo has a copy of Billboard's Weekly [Hot 100](https://www.billboard.com/charts/hot-100) singles chart between 8/2/1958 and 1/18/2019 as scraped from the site using a python api library. If you are interested, you [can see that here](https://github.com/utdata/rwd-py-billboard).

## Data dictionary

This dataset contains every weekly Hot 100 singles chart from Billboard.com. **Each row of data represents a song and the corresponding position on that week's chart.** Included in each row are the following elements:

> Consider updating this to same as the billboard.py api.

- date: Date of chart
- title: Title of song
- artist: Name of artist
- current: Current chart position
- previous: Chart position the previous week
- peak: The track's peak position on the chart at any point in time, including future dates, as an int (or None if the chart does not include this information)
- weeks: The number of weeks the track has been or was on the chart, including future dates (up until the present time).

## Assignment Rubrics

- [Rubric for Workbench](rubric-wb.md)
- [Rubric for R](rubric-r.md)

