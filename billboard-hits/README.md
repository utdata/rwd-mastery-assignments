# Billboard Hot 100

This repo has a copy of data from Billboard's Weekly [Hot 100](https://www.billboard.com/charts/hot-100) singles chart between 8/2/1958 through 2020. It is a modified version of data compiled by SEAN MILLER and posted on [data.world](https://data.world/kcmillersean/billboard-hot-100-1958-2017). Some columns were removed to reduce file size, and columns were renamed.

You should source the data the Billboard Hot 100 from Billboard Media, since that is where the data comes from via an API.

## Data dictionary

This dataset contains every weekly Hot 100 singles chart from Billboard.com. **Each row of data represents a song and the corresponding position on that week's chart.** Included in each row are the following elements:

- date: Date of chart release
- current: Position on chart for the week
- title: The song name
- artist: The performer name
- previous: The previous week's position as of the chart date
- peak: Top position on chart as of the chart date
- weeks: Number of weeks on chart as of the chart date

## Assignment Rubrics

- [Rubric for Workbench (Detailed)](rubric-wb-detailed.md)
