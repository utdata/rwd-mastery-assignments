# Final project (Spring 2020)

The final project for Reporting with Data is adjusting this semester in light of COVID-19, social distancing and our compressed schedule.

## Deliverables

### The story

You'll produce an 600-word news story based based on supplied data sets and two recorded source interviews. You may include additional sources you interview and properly credited published reports or studies, but it is not required. Use Google Docs and share with me as an editor. (300 points)

- Include a compelling, news-focused headline for your story.
- The two recorded interviews to work from, both recorded in the summer of 2019:
  - [Andy Kahn](https://drive.google.com/open?id=1XlalZgZ0sw0E95uYOFI0EdEEy2UdWxfG) is a bartender at the Mockingbird Saloon (then called The Local Pub and Patio). He has also served as manager at the Hole in the Wall. He talks about the business of running a bar in a college town and keeping on the right side of TABC rules.
  - [Chris Porter](https://drive.google.com/open?id=1OO1OqmvROUINN0O7I6fYmG7a0-3Iw_GN) is the public information officer for the Texas Alcoholic Beverage Commission. He talks about the TABC's role in enforcing rules around selling alcohol. If you have follow-up questions for him you could reach out at <chris.porter@tabc.texas.gov>.
- You have two data sets to draw from: Monthly alcohol sales and TABC enforcement actions (more on those below). You'll need to [download these data sets](README.md) and explore them using tools you've learned in class. You **DO NOT** have to use both sets in the story.

### The analysis

- You'll turn in any analysis work you've done (Workbench, Tableau, other charting tools), regardless if it is used in the story. I want all your work. You will need to keep a data diary to log your downloads, source contacts and any analysis notes not otherwise kept in Workbench annotations. Use Google Doc shared to me. (200 points)
- You'll produce at least **one publishable chart**  to go with your story using the tool of your choice. This chart needs to have a proper headline, description, legend, annotations and such so that the chart **can be understood outside the context of the story**. Include a screenshot and/or link in your story. (100 points)

### Editing partners

- You'll need to choose an editing partner to work with and you'll need to include a short report of how you helped them focus and edit their story and analysis. Use Google Docs and share with me. (50 points)

### Supporting elements

- **Two promotional tweets**, one geared toward the story and one geared toward a chart. You don't have to actually tweet the results, just put them in a Google Doc. _Include an image_ that might help draw attention to your tweet. This can be in your story file. (25 points)
- A diversity statement about how you did or could better add diversity of voice to your story. Can also be included with your story file. (25 points)

## How to tackle this project

First, take a look at this resource: [How to tackle a new data set](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit).

You might consider the following workflow to stay on task:

### Week of March 20

- Download and explore the data and data dictionaries. Get a good idea of what is available in the data.
- Listen to the interviews.
- Make a list of questions to ask the data. Work through those questions and answers through Workbench, Tableau and other tools. Create and keep a data diary and Workbench annotations as you go along.

### Week of March 27

- Take stock of your work and come up with an angle for a story. Write an outline or rough draft.
- Consider what chart will best illustrate your story. Prepare the data and make a rough draft.
- Set a meeting with your editor and go over both your story and chart. This should be done by the end of day on May 4th, when you provide a summary in an assignment due that day.

### Week starting May 4

- Finish out your story, chart and supporting elements. Gather your analysis materials and turn in.
- During this week you will also have a chance to present your [next data project assignment](../final-project-rubric-next-project.md) during the online meeting on May 6th, so you should prepare for that as well.

## Other tips

While there are filtering and data shaping tools in Tableau, I can see value in using Workbench to clean and shape your data before pulling it into Tableau.

For instance, if you want to use Workbench or Tableau to compare beer, wine and liquor receipts by establishment, you'll have to reshape/pivot the data to create new columns `Receipt Type` and `Amount` from each of the distinct amount columns. You can do the pivot Tableau, but you'll still probably want to use Workbench to select just the columns you need before pivoting in Tableau. Or just do it all in Workbench with some [pandas magic](https://github.com/utdata/rwd-workbench#reshaping-with-melt).

On the other hand, [other charting tools](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit) like Datawrapper and Flourish tend to like wide data instead of long data. You can use Workbench to select and aggregate the data, then export as a csv to make your chart.
