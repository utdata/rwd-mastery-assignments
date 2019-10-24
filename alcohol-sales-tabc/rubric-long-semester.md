# Mixed Beverage/TABC Long Semester Assignment

Your goal is to make a short news story from one or both of two data sets available to you: Mixed Beverage Gross Receipts and Texas Alcoholic Beverage Commission enforcements for selling to a minor or an intoxicated person.

You'll need to [download these data sets](README.md) and explore them using tools you've learned in class. You **DO NOT** have to use both sets in the story. We'll discuss some story ideas in class.

- You'll produce an 500-word data drop based on the data. This should be written as a news story like most of our other data drops. Don't pad or overwrite the story to make the 500 words ... find another data fact and/or quote to support a fact. I count off way more for padding a story with fluff than for being short. (100 points)
- In addition to having the data as a source, you also have two previously recorded interviews to work from:
  - [Andy Kahn](https://drive.google.com/open?id=1XlalZgZ0sw0E95uYOFI0EdEEy2UdWxfG) is a bartender at the Mockingbird Saloon (then called The Local Pub and Patio). He also was a manager at the Hole in the Wall. He talks about the business of running a bar in a college town and keeping on the right side of TABC rules.
  - [Chris Porter](https://drive.google.com/open?id=1OO1OqmvROUINN0O7I6fYmG7a0-3Iw_GN) is the public information officer for the Texas Alcoholic Beverage Commission. He talks about the TABC's role in enforcing rules around selling alcohol.
- You'll turn in any analysis work you've done (Workbench, Tableau, other charting tools), regardless if it is used in the story. I want _ALL_ of your work. (200 points)
- You will need to keep a data diary to log your downloads, source contacts and any analysis notes not otherwise kept in Workbench annotations. (You DO NOT have to detail each work step in Tableau or other charting tools ... just keep notes about decisions and information useful to your future self.) Use a Google Doc shared to me. (50 points)
- You'll produce at least one publishable chart to go with your story using the tool of your choice. This chart needs to have a proper headline, description, legend, annotations and such so that the chart **can be understood outside the context of the story**. Include a screenshot and/or link in your story. (50 points)

## How to tackle this project

First, take a look at this resource: [How to tackle a new data set](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit).

One thing you will want to do early on is listen to the interviews by Andy Kahn and Chris Porter. What they say might influence what questions you might want to ask the data.

While there are filtering and data shaping tools in Tableau, I can see value in using Workbench to clean and shape your data before pulling it into Tableau or other charting tools. Tableau likes "long" data, while Datawrapper likes "wide" data.

For instance, if you want to use Tableau to compare beer, wine and liquor receipts by establishment, you'll have to reshape/pivot the data to create new columns Receipt Type and Amount from each of the distinct amount columns. You can do the pivot reshaping in Tableau, but you'll still probably want to use Workbench to select just the columns you need before importing in Tableau. Or just do it all the data shaping wor Workbench with some [pandas magic](https://github.com/utdata/rwd-workbench#reshaping-with-melt).

On the other hand, [other charting tools](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit) like Datawrapper, Flourish and Atlas tend to like wide instead of long data. It still makes sense to filter the data, select the columns you need and do any aggregations in Workbench to get the data just the way you need them to make your chart.
