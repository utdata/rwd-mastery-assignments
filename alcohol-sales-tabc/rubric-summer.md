# Final project (summer)

The summer final project for Reporting with Data is a little different than during a long semester because of the compressed schedule.

## Deliverables

- You'll produce an 800-word news story with at least three human source including the two recorded sources listed below. (This means you'll have to find at least one source on your own.) You can include additional student sources in your reporting, but not from our class and they don't count toward the three source. Properly credited published reports or studies are allowed as source material in your story, but they do not count toward your human source quota. **Include a headline for your story**.  Use Google Docs and share with me as an editor. (300 points)
- You have two data sets to draw from: Alcohol sales and TABC enforcement actions (more on those below). You'll need to [download these data sets](README.md) and explore them using tools you've learned in class. You **DO NOT** have to use both sets in the story. We'll discuss some story ideas in class.
  - You'll turn in any analysis work you've done (Workbench, Tableau, other charting tools), regardless if it is used in the story. I want all your work. (200 points)
  - You will need to keep a data diary to log your downloads, source contacts and any analysis notes not otherwise kept in Workbench annotations. Use Google Doc shared to me. (50 points)
  - You'll produce at least one publishable chart to go with your story using the tool of your choice. This chart needs to have a proper headline, description, legend, annotations and such so that the chart **can be understood outside the context of the story**. Include a screenshot and/or link in your story. (50 points)
- You'll need to choose an editing partner to work with and you'll need to include a short report of how you helped them focus and edit their story and analysis. Use Google Docs and share with me. (50 points)
- Two promotional tweets, one geared toward the story and one geared toward a chart. You don't have to actually tweet the results, just put them in a Google Doc. Include an image that might help draw attention to your tweet. This can be in your story file. (25 points)
- A diversity statement about how you did or could better add diversity of voice to your story. Can also be included with your story file. (25 points)

## How to tackle this project

First, take a look at this resource: [How to tackle a new data set](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit).

While there are filtering and data shaping tools in Tableau, I can see value in using Workbench to clean and shape your data before pulling it into Tableau.

For instance, if you want to use Workbench or Tableau to compare beer, wine and liquor receipts by establishment, you'll have to reshape/pivot the data to create new columns Receipt Type and Amount from each of the distinct amount columns. You can do the pivot Tableau, but you'll still probably want to use Workbench to select just the columns you need before pivoting in Tableau. Or just do it all in Workbench with some [pandas magic](https://github.com/utdata/rwd-workbench#reshaping-with-melt).

On the other hand, [other charting tools](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit) like Datawrapper, Flourish and Atlas tend to like wide instead of long data. You select and aggregate just the way you need them to make your chart.
