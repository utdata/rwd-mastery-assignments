# Notes for the professor

## Improvements from Spring 2020

- Name the first tab in the Workbench part
- In video of tooltips or text remember to tellthem to turn off the editing.
- Add highlight action between bar chart and map
- Note at the end to turn in Workbench workflow, too.
- show how to fix the axis on the line chart so counties are considered on same axis.
- I didn't realized I used just Kindergarten rates. I need to make sure a) that is the right choice, and b) it is reflected in the assignment.
- There is the latest year rates by district that could be included in the assignment, joined by county and listed when that county is selected on the dashboard. Just a thought.

## Spring 2020

- This is the [complete Workbench workflow for 2010-2020](https://app.workbenchdata.com/workflows/62289).
- Dat ais in `data/exemptions-cleaned-2020.csv`

## Fall 2019

- There is a complete Workbench workflow [Vaccination exemption by county, 2011-2019](https://app.workbenchdata.com/workflows/36382).
- The cleaned data is also at `data/exemptions_county.csv`.)

## Convert the data from PDF

> At one time way back in the fall of 2019, this data was only available via PDF and it had to be converted. There is a copy of the data used here in `data/Exemptions by County 2010-2018.pdf`. I'm storing notes here in case I need them again some day.

Before we can do anything with this data, we have to get it out of the PDF. There are many ways to do this, but [Cometdocs](https://www.cometdocs.com) is one of my favorites, and it is free for a number of uses per month. (You can get unlimited use through a $25 [IRE membership](https://www.ire.org/membership/terms-and-rates).)

- Create a free account with Cometdocs.
- Upload the PDF.
  - You might need to click the "go to Webapp" button before uploading.
- Once uploaded, Click on the "Convert" tab and then drag the file into that section.
  - Choose the "to Excel" conversion.
  - Click **Convert**.
- Watch the XLS button, and once the progress bar stops, click on the Download button and follow the steps.

(I have a copy of the [processed data](https://github.com/utdata/rwd-mastery-assignments/blob/master/vaccination-exemptions/data/Exemptions%20by%20County%202010-2018.xlsx), but you should do it yourself if at all possible.)

If you open the converted file in Excel or Sheets, you'll see it is NOT a clean data file, but at least it is in columns and rows. A clean data file would have a single header row, then have just one row for each data point, without page numbers or notes.

You could clean this up by hand, but then that would be subject to error and would not be repeatable. We'll use Workbench instead. (We'll want to do some other stuff anyway.)