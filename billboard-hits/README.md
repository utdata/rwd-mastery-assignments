# Billboard Hot 100

In this repo has a copy of Billboard's Weekly [Hot 100](https://www.billboard.com/charts/hot-100) singles chart between 8/2/1958 and 12/28/2019 as compiled by SEAN MILLER and posted on [data.world](https://data.world/kcmillersean/billboard-hot-100-1958-2017). See link for more information.

## Data dictionary

This dataset contains every weekly Hot 100 singles chart from Billboard.com. **Each row of data represents a song and the corresponding position on that week's chart.** Included in each row are the following elements:

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

## Assignment Rubrics

- [Rubric for Workbench](rubric-wb.md)
- [Rubric for R](rubric-r.md)
