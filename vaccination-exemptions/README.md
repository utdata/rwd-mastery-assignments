# Vaccination exemptions by county

Texas law allows for an exemption from immunizations for reasons of conscience, including a religious belief. A student's parent or guardian submits an official DSHS affidavit form to the child's school.

This is a soup-to-nuts study at how the use of exemptions have changed over time by county, from PDF to online data visualization. This is one of those cases where the easy part is creating the visualization. Most of the work comes in preparing and understanding the data.

## Explore the data

Visit the the Texas Department of State Health Services' [Conscientious Exemptions Data - Vaccination Coverage Levels](https://www.dshs.texas.gov/immunize/coverage/Conscientious-Exemptions-Data.shtm) web page and look for the file [Printable Version of 2010-2018 Conscientious Exemptions Data for Texas (PDF)](https://www.dshs.texas.gov/uploadedFiles/Content/Prevention_and_Preparedness/immunize/coverage/schools/Exemptions%20by%20County%202010-2018.pdf). Download and open it. (There is a copy in `data/Exemptions by County 2010-2018.pdf`.)

This is just one of several datasets that can be explored concerning statewide vaccination rates.

- What can we learn from this file?
- Take a look at the columns and rows and formulate questions. What might you want to learn or explore?
- What charts might we make? How might they work together in a dashboard?
- What shape (wide vs long) does this data have to be to get what you need?

## Convert the data from PDF

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

## Clean and reshape using Workbench

There are a number of cleaning steps you should accomplish in Workbench.

### Cleaning

- Start a new Workbench workflow and start by uploading the Excel spreadsheet that you downloaded from Cometdocs.
- We don't have a really header. You'll see the correct header row, which starts with "County" on the first column, is down at row 7 or 8. You can select that row and then use the **1 row selected** dropdown to set that as the new header row.
- Use **Filter by value** function to delete all the rows that are not a value for a county.

### Reshaping

If we want to compare exemptions over time (by their school year), then we must have a column called "School year" instead of a column for _each_ school year. You might recall this concept from the [reshape](http://help.workbenchdata.com/en/articles/1634563-reshape) from our Workbench tutorials.

- Use the **Reshape** function to change the data _Wide to long_ using `County` as the Row variable.
- Rename the new columns as "School year" and "Exemption rate".

### Adding a real date column

You might also create a new column that includes a real date based on the school year date to use for line charts in Tableau. The idea is to create a new _real_ data of Aug. 1 for each year by taking the text "08/01" and combining it with the right-most four characters from the School Year.

- Use the **Formula** function as an Excel function. The formula is `="08/01/"&RIGHT(B1,4)`. Call the column "Year".
- Now convert that "Year" column to a date format.

### Deal with NR

Some of our Exemption rates are a value of "NR**". We can't import data like that into Tablau or it won't consider it a number. We need to replace all those values with a blank value. (I'll do some sorting in class to show you these values.)

- Use the function **Search and Replace** on `Exemption rate` and search for "NR**" but leave the "Replace with" value blank.

### Export the file

- Click the **Export** button and click the download button under CSV.

## Assignments

- [rubric-tableau](rubric-tableau.md)

### Of note

(There is a complete Workbench workflow [Vaccination exemption by county, 2011-2019](https://app.workbenchdata.com/workflows/36382), but you really should do the steps above on your own. The cleaned data is also at `data/exemptions_county.csv`.)
