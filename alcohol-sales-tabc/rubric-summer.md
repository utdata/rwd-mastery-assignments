# Final project (summer)

The summer final project for Reporting with Data is a little different than during a long semester because of the compressed schedule. You basically have a week to build and write your story.

> [Here is a short video introduction](https://drive.google.com/file/d/156lZ4zXpq8N-uZKJpl9Kh7WUcY16gKFv/view?usp=sharing) about the project.

## Deliverables

For Summer 2020, this is all due Friday, Aug. 14th at 11:59 p.m. except for the editing report due the day before.

- **Story**: You'll produce an 600-word news story with at least three human sources including the two recorded sources listed below. (This means you'll have to find at least one source on your own.) You can include additional student sources in your reporting, but not from our class and they don't count toward the three sources. Properly credited published reports or studies are allowed as source material in your story, but they do not count toward your human source quota. This should be a news story, not a personalized blog post. Use Google Docs and share with me as an editor. (300 points)
- **Headline**: A good, news-oriented headline for your story**: (25 points)
- **Analysis**: You'll turn in any analysis work you've done (Workbench and any other charting tools), regardless if it is used in the story. I want all your work. (200 points)
- **Chart** You'll produce at least one publishable chart to go with your story using the tool of your choice. This chart needs to have a proper headline, description, legend, annotations and such so that the chart **can be understood outside the context of the story**. Include a screenshot and/or link in your story. I suggest using Datawrapper for this, but you could also use Flourish or Tableau if you know how (or learn). (100 points)
- **Editing partner**: You'll need to choose an editing partner from class to work with throughout the project and including a line-edit and review of their story and analysis. Use Google Docs and share with me. (50 points due Aug. 13 for Summer 2020.)
- **Promotions**: Two promotional tweets, one geared toward the story and one geared toward a chart. You don't have to actually tweet the results, just put them in a Google Doc. Include an image that might help draw attention to your tweet. This can be in your story file. (25 points each)
- **Diversity statement**: Explain you did or could better add diversity of voice to your story. Can also be included with your story file. (25 points)

## Materials to work from

- Three [recorded interviews](https://drive.google.com/open?id=1JfH1BKvyjrN9AT_4TFIt7rTRD2sOPCgV) from two people. There are transcripts of each recording _but be sure to listen to the audio for direct quotes_ as the transcripts are FAR FROM PERFECT.
  - **Andy Kahn** is a bartender at the Mockingbird Saloon (then called The Local Pub and Patio). He has also served as manager at the Hole in the Wall. He talks about the business of running a bar in a college town and keeping on the right side of TABC rules. This was recorded in summer 2019.
  - **Chris Porter** is the public information officer for the Texas Alcoholic Beverage Commission. He talks about the TABC's role in enforcing rules around selling alcohol. If you have follow-up questions for him you could reach out at <chris.porter@tabc.texas.gov>. There are two recordings from him ... one from summer 2019 and one from spring 2020.
  - You need to find your own third source.
- You have two data sets to draw from: Alcohol sales and TABC enforcement actions (more on those below). You'll need to [download these data sets](README.md) and explore them using tools you've learned in class. You **DO NOT** have to use both sets in the story. See below for some story ideas.

## How to tackle this project

First, take a look at this resource: [How to tackle a new data set](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit).

I suggest you use Workbench to clean, analyze and shape your data for Datawrapper. (You can chart in Workbench for yourself, but your published graphic needs to be in Datawrapper, Flourish or some other tool that allows descriptions, annotations and the like.)

You might start by using Workbench to answer a series of questions. It isn't required that you find any of these ... they are just ideas for you to work from or help you brainstorm for your own idea.

### Alcohol sales data

- Which establishments have sold the most alcohol over the past five years? How does that look on a monthly basis? (Be sure to watch for multiple locations of the same name and name changes of the same location.)
  - Perhaps take the same idea geographically. The Drag (Guadalupe between 19th and 30th). West Campus (78705). The Domain area (78758). Downtown (78701). SoCo (78704). East Austin (78702) and north of there (78722). You could look at Dirty Sixth (Sixth Street between Congress and )
  - You could compare sales between popular areas. Or sales over time in a certain area.
- Is the number of restaurants or bars growing in certain areas? Like in east or south Austin?
- How do sales break down by alcohol type? Who sold the most beer last year? Wine? Again, could break down by geography.
- How do sales change over the seasons around West Campus? What do establishments do to deal with that?
- How did COVID-19 affect sales in early 2020? Can you tell who might have offered to-go alcohol and how does that compare to last March/April/May? (Remember you'll have only partial data for recent months.)
- How much does March mean to sales of alcohol downtown during SXSW? (Like what percentage of their yearly sales?) What was the difference last year to this year with the COVID shutdown?
- What owner/company has sold the most alcohol? (Taxpayer name).
- Which or what percentage of establishments have out-of-state owners (or at least out of state taxpayer addresses)?

### TABC data

- Who has had the most TABC violations over the past five years?
  - What kind of violations (from among our data)?
  - What about violations near campus (78705)?
- How do bars guard against fake licenses? (as a possible angle on those who have had violations)
- How do TABC violations compare by ZIP code to alcohol sales by ZIP code?
- If you are looking at specific locations and their violations, an additional data point for your story might be how much alcohol they sold that year, which you could get from the alcohol data.

### Notes on shaping data

When you want to make a chart from data, one of the more important aspects is to get your data in the right "shape" to support your chart. Here is how I go about that process:

- Draw a picture of what you want your chart to show.
  - What value you are plotting: Count of records, sum of some value, etc. There is almost always at least one Number value you need.
  - What categories are you showing? Different establishments? Years?
  - Keep it simple. Good charts typically explain ONE thing.
- Check the [Datawrapper academy](https://academy.datawrapper.de/) and poke around the tutorials for your desired chart. They typically give an example of what your data should look like.
- Use Workbench to prepare your data for the right format. Some common functions and tips:
  - **Filter** will get you only the rows you need.
  - **Select columns** let's you select (or delete) columns so you have only what you need for the chart.
  - **Refine**: Allows you to rename values within a row. If I'm doing a chart by month, I will use **Formula** `=MONTH(date_col)` to create a new column with the number of the month, but then use **Refine** to change the names to something readable, like January.
  - **Group** and the aggregations that come with it are sometimes all you need to reshape your data.
  - **Reshape** allows you to make extract values to make new columns for line charts. If you have your data where you have a column for "Year" with different values, you'll likely need to reshape it so you have a column for each year of data to do a line chart.^^
  - **Transpose** allows you to flip the axis of your data so rows become columns and vise versa. You can also do this in Datawrapper.

 ^^ One limitation with Workbench is you can only keep one or two of your columns on a row when you reshape. I've used a Formula to combine two rows together (Like Location Name and Location Address) to get around this limitation. There is also some [pandas magic](https://github.com/utdata/rwd-workbench#reshaping-with-melt) if you are going from wide_to_long, but that is more for Tableau instead of Datawrapper, which likes wide data.

## Editing partners

- You'll need to choose an editing partner to edit each other's story and chart. PARTNERS CAN'T HAVE THE SAME STORY ANGLE OR SHARE ANALYSIS. The purpose of this pairing is to help each other with story edits and clarity for the chart. (You can do this over the phone while editing Google Docs or use conference software of your choice.) The edit must be completed with the summary report **by 11:59 p.m. Thursday, Aug. 13th**.

To turn in your assignment, include the following in a Google Doc that is shared with me:

- The name of your partner.
- A brief synopsis of their story angle.
- A description of the editing advice you offered them.

## Turning in your project

- Save and/or upload all your work into one Google Drive folder and make me an EDITOR of that folder so I can see and edit everything inside.
- Write your story in Google Docs. You can include the supplementary material in the same file, but it does not count toward the word count.
- Make sure any Workbench workflow is public or shared with me and a link is included in your story.
- If happen to use Tableau, either publish it to Tableau Public or Export the Packaged Workbook and upload the .twbx file to Drive.
- Include a screenshot of your chart and/or link to it from the story.

## Ignore this

- [Workbench Alcohol](https://app.workbenchdata.com/workflows/79460) | [Workbench TABC](https://app.workbenchdata.com/workflows/80082/)
