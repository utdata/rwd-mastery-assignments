# Vaccination exemptions by county

Texas law allows for an exemption from immunizations for reasons of conscience, including a religious belief. A student's parent or guardian submits an official DSHS affidavit form to the child's school.

This is a soup-to-nuts study at how the use of exemptions have changed over time by county, from PDF to online data visualization. This is one of those cases where the easy part is creating the visualization. Most of the work comes in preparing and understanding the data.

## Explore the data

Visit the the Texas Department of State Health Services' [Conscientious Exemptions Data - Vaccination Coverage Levels](https://www.dshs.texas.gov/immunize/coverage/Conscientious-Exemptions-Data.shtm) web page and look for the file [Printable Version of 2010-2018 Conscientious Exemptions Data for Texas (PDF)](https://www.dshs.texas.gov/uploadedFiles/Content/Prevention_and_Preparedness/immunize/coverage/schools/Exemptions%20by%20County%202010-2018.pdf). Download and open it. (There is a copy in `data/Exemptions by County 2010-2018.pdf`.)

This is just one of several datasets that can be explored concerning statewide vaccination rates.

- What can we learn from this file?
- Take a look at the columns and rows and formulate questions and pre-conceive charts or interactives. What could you build with this?
- What shape (wide vs long) does this data have to be to get what you need?

## Convert the data from PDF

Before we can do anything with this data, we have to get it out of the PDF. There are many ways to do this, but [Cometdocs](https://www.cometdocs.com) is one of my favorites, and it is free for a number of uses per month. (You can get unlimited use through a $25 [IRE membership](https://www.ire.org/membership/terms-and-rates).)

- Upload the PDF to Cometdocs.
- Use Convert to turn into an XLS file.
- Download it once it is converted. It should take less than a minute.

(A copy of the processed data is in`/data/Exemptions by County 2010-2018.xlsx`, but you should do it yourself).

If you open the converted file in Excel or Sheets, you'll see it is NOT a clean data file, but at least it is in columns and rows. This file needs to start with a single header row, then have just one row for each data point, with not page numbers or notes.

You could clean this up by hand, but then that would be subject to error and would not be repeatable. We'll use Workbench instead.

## Clean and reshape using Workbench

There are a number of cleaning steps you should accomplish in Workbench.

- Upload and the Excel spreadsheet that you downloaded from Cometdocs.
- You'll see the real header row, which starts with "County" on the first column, is down at row 7 or 8. You can select that, and then use the **1 row selected** dropdown to set that as the new header row.
- Use **Filter by value** to delete all the rows that are not a value for a county. You could also probably use **Filter by condition**, but I haven't tried to work it out.
- Do answer the questions in the Tableau rubric (which are probably similar to those raised in class), we'll need to reshape this data from wide to long so you have County, School Year and Exemption Percentage.
- You might also create a new column that includes a real date based on the school year date to use for line charts in Tableau.

(I have the [Vaccination exemption by county, 2011-2019](https://app.workbenchdata.com/workflows/36382), but you really should do your own. There is an exported version as `data/exemptions_county.csv`.)

## Assignments

- [rubric-tableau](rubric-tableau.md)
