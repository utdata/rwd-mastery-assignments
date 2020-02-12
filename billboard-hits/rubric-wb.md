# Billboard Hot 100 rubric for Workbench

Be sure to see the [README](README.md) for the source information and data dictionary.

## Connect to the data

To pull in the Billboard data into Workbench use the **Add from URL** option and use this link:

```
https://github.com/utdata/rwd-mastery-assignments/blob/master/billboard-hits/billboard.csv?raw=true
```

It will take several seconds to load.

## Your quests

Each goal listed below should have its own tab in Workbench. **Explain the goal/purpose of EACH STEP using the annotations within the tool.**

1. Review the data, clean up dates and save as a tab.
2. Who are the 10 artists with the most appearances on the Hot 100 chart?
    - Start a new sheet from the cleaned data. (Do this for each new quest.)
    - **Group** all the records by Performer, **count**ing the rows, which is each time they've had a song on the chart. Keep the top 10 performers.
    - Build a column chart from the data that shows the top performers and the number of times they've had a song on the chart. Make sure the chart has a title and good axis names.
3. Who had the most No. 1 hit songs? Here's the logic (and some hints):
    - First you need to filter for only the No. 1 songs.
    - Next you need to make that a unique list that only shows each song/performer combination once. Here are two different ways you could do this. I stress, use only ONE of these methods:
        - You could **group** by both Performer and Song. This will give you a row for each Performer/Song combination along with the numbers of times it was No. 1. The key there is you have a unique list of performer/song.
        - Or, you could use **Select columns** to keep just Performer and Song, and then use **Deduplicate** to make the list unique, showing each Performer/Song combination only once.
    - Now you can group by Performer to count how my times they show up on the unique list of No. 1 songs.
4. Who had the most No. 1 hits in the most recent five years?
    - Very similar to Goal 3 but with a data filter applied upstream in the workflow. You can copy the tab you made before and then add a filter upstream to get just the most recent hits. Include only those with more than one No. 1 hit.
5. Who had the most top 10 hits overall?
    - Also similar to Goal 3 but you are looking for the artists who had the most songs in the top 10. Again, you can duplicate that tab and modify an existing filter to get the answer.
6. What song has been on the charts the most number of weeks at any position?
7. What song was No. 1 for the most number of weeks?

## Write a data drop

A [Data Drop]((https://docs.google.com/document/d/1gd5RR5YK43N3uE0o1vBoJfnkSo5S0JJFUCJmFsa75FM/edit#heading=h.k2b1zvdn1534)) is a short story that outlines your findings in readable sentences. It needs to read like a news story, but in this case won't have any sources beyond the data.

In this case (and this is the only case for this class) you can add some personal flavor in the story. Write this in Google Docs and include at least one chart from the Workbench. (You can upload the PNG into the Doc.)

## Turn it in

- Once complete, **Share** your Workbench project with my email and submit the private link as a comment in the assignment.
- **Share** your Google Doc to my email as AN EDITOR and submit the link to the Canvas assignment.
