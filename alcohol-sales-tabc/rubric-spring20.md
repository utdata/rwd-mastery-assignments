# Final project (Spring 2020)

The final project for Reporting with Data is adjusting this semester in light of COVID-19, social distancing and our compressed schedule.


## Deliverables

### The story

You'll produce an **600-word news story** drawn from supplied data sets and two pre-recorded source interviews. If you wish, you may include additional on-the-record sources you interview but it is not required. Use Google Docs and share it with me as an editor. (300 points)

The materials you have to work with are the following:

- Two recorded interviews, both recorded in the summer of 2019:
  - [Andy Kahn](https://drive.google.com/open?id=1XlalZgZ0sw0E95uYOFI0EdEEy2UdWxfG) is a bartender at the Mockingbird Saloon (then called The Local Pub and Patio). He has also served as manager at the Hole in the Wall. He talks about the business of running a bar in a college town and keeping on the right side of TABC rules.
  - [Chris Porter](https://drive.google.com/open?id=1OO1OqmvROUINN0O7I6fYmG7a0-3Iw_GN) is the public information officer for the Texas Alcoholic Beverage Commission. He talks about the TABC's role in enforcing rules around selling alcohol. If you have follow-up questions for him you could reach out at <chris.porter@tabc.texas.gov>.
- You have two data sets to draw from: Monthly alcohol sales and TABC enforcement actions. You'll need to [download these data sets](README.md) and explore them using tools you've learned in class. You **DO NOT** have to use both sets in the story.

**Include a compelling, news-focused headline for your story.** (Points off if you skip or mail it in.)

### The analysis

- You'll turn in any **analysis work** you've done (Workbench, Tableau, other charting tools), regardless if it is used in the story. I want all your work. You will need to keep a data diary to log your downloads, source contacts and any analysis notes not otherwise kept in Workbench annotations. Use Google Docs and files uploaded into Google Drive and shared to me. (200 points)
- You'll produce at least **one publishable chart**  to go with your story using the tool of your choice. This chart needs to have a proper headline, description, legend, annotations and such so that the chart _can be understood outside the context of the story_. Include a screenshot and/or link in your story. (100 points)

### Supporting elements

- **Two promotional tweets**, one geared toward the story and one geared toward a chart. You don't have to actually tweet the results, just put them in a Google Doc. _Include an image_ that might help draw attention to your tweet. This can be in your story file. (25 points)
- A **diversity statement** about how you did or could better add diversity of voice to your story. Can also be included with your story file. (25 points)

### Editing partners

**This part is due May 4th**.

- You'll need to choose an editing partner to work with. Each student will review each other's story and chart and offer suggestions and edits. (You can do this over the phone while editing Google Docs or use conference software of your choice.) This must be completed and a summary report _submitted by 11:59 p.m. Monday, May 4._ You can use class time that day to accomplish this as I will only have open lab hours and no new instructions. (50 points)
- To turn in your assignment, include the following in a Google Doc that is shared and submitted to the May 4th Canvas assignment with the following:
  - The name of your partner.
  - A brief synopsis of their story angle.
  - A description of the editing advice you offered them.

## Turning in your project

To turn in your work:

- Save and/or upload all your work into one Google Drive folder and make me an EDITOR of that folder so I can see and edit everything inside.
- Write your story in Google Docs. You can include the supplementary material in the same file, but it does not count toward the word count.
- Don't pad your story with fluff. Instead, find another fact or quote to support your story. I'll count off way more for padding than for being short.
- If you are turning in Tableau work, either publish it to Tableau Public or Export the Packaged Workbook and upload the .twbx file to Drive.
- Make sure any Workbench workflow is public or shared with me and a link is included in your story.

## How to tackle this project

First, take a look at this resource: [How to tackle a new data set](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit).

You might consider the following workflow to stay on task:

### Week starting April 20

- Download and explore the data and data dictionaries for both data sets. Get a good idea of what is available in the data.
- Listen to the recorded interviews.
- Make a list of questions to ask the data. Work through those questions and answers through Workbench, Tableau and other tools. Create and keep a data diary (Google Doc is fine) and Workbench annotations as you go along.

### Week starting April 27

- Chris Porter of the TABC will be available for some follow-up questions during a joint-class Zoom meeting starting at noon on April 27th.
- Take stock of your work and come up with an angle for a story. Write an outline and/or rough draft. Start with your data facts, then fill in with quotes and supporting material.
- Consider what chart will best illustrate your story. Prepare the data and make a rough draft of the chart.
- Set a meeting with your editor and go over both your story and chart. This should be done by the end of day on May 4th, when you provide a summary in an assignment due that day.

### Week starting May 4

- Finish out your story, chart and supporting elements. Gather your analysis materials and include in your Google Drive folder, then turn in the link to the final Canvas assignment.
- During this week you will also have a chance to present your [next data project assignment](../final-project-rubric-next-project.md) during the online meeting on May 6th, so you should prepare for that as well. See the Canvas assignment for details if you can't present in class.

## Other tips

While there are filtering and data shaping tools in Tableau, I can see value in using Workbench to clean and shape your data before pulling it into Tableau.

For instance, if you want to use Workbench or Tableau to compare beer, wine and liquor receipts by establishment, you'll have to reshape/pivot the data to create new columns `Receipt Type` and `Amount` from each of the distinct amount columns. You can do the pivot Tableau, but you'll still probably want to use Workbench to select just the columns you need before pivoting in Tableau. Or just do it all in Workbench with some [pandas magic](https://github.com/utdata/rwd-workbench#reshaping-with-melt). I will demonstrate this in "class" on April 22.

On the other hand, [other charting tools](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit) like Datawrapper and Flourish tend to like wide data instead of long data. You can use Workbench to select columns and then group/summarize the data, then export as a csv to make your chart.
