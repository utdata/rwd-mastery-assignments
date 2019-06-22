# School ratings for Google Sheets

> See the [main README](README.md) to see how to download the data.

## Our scenario

Today you are the education reporter for an Austin-area media outlet. The Texas Education Agency has released school ratings for all schools and districts in the state. Your editor would like a story posted ASAP with some specific details before you continue to report out the story. (I call these short stories a [Data Drop](https://docs.google.com/document/d/1gd5RR5YK43N3uE0o1vBoJfnkSo5S0JJFUCJmFsa75FM/edit#heading=h.k2b1zvdn1534).)

You editor would like the following details in this first version:

1. What percentage of charter schools received a "Needs Improvement" rating, compared to traditional public schools?
2. What are those percentages in the Austin MSA?
3. Which charter schools in the Austin MSA received a "Needs Improvement" rating?
4. Which traditional public schools in the Austin MSA received a "Needs Improvement" rating?
5. Which schools in Austin ISD received a "Needs Improvement" rating?

The Austin/Round Rock MSA: Bastrop, Caldwell, Hays, Travis and Williamson counties.

## Create a project folder

- As you always should, create a folder on your computer for all the material you'll use in this project.
- Start a [Data Diary](https://docs.google.com/document/d/1gd5RR5YK43N3uE0o1vBoJfnkSo5S0JJFUCJmFsa75FM/edit#heading=h.5i6qymvlqkwj) and record the links and steps you use to download your data. (You can do this in Google Docs, or as a text file on your computer. I use a [code editor](https://drive.google.com/open?id=1vxqW2B0JkRov-V2sRtBSuOHIOdP71WH-5qBFDQvuUY8) and store it on my computer, but do what is comfortable for you.)
- You'll use this Data Diary to keep other notes to yourself about this project. You'll turn it in with your assignment.

## Import the data into Google Sheets

- Move your data into your project folder
- Start a new Google Sheet.
- Under File, use Import and upload your data file.
- At the import screen, choose the following:

![Sheets import](img/sheets-import.png)

> The part about converting text to numbers can be important. TEA data includes IDs that start with `0`, which you will lose if you don't do this. While not as important for this story, it is a prime example of this type of situation.

## Comparing charter vs traditional public schools

You will use a pivot table to get this answer. Note that you'll be filtering out some schools that are rated on "alternative" standards.

Look through the [Campus Accountability Summary Reference](https://rptsvr1.tea.texas.gov/perfreport/account/2018/download/camprate.html) data dictionary and find the column that shows the "Overall Rating".

- Start a new pivot table: Data > Pivot table.
- Set up the pivot table to count the rows based on "Overall Rating".

You should now have a table that shows the number of schools that got each rating.

However, you need to filter out the non-traditional schools that received an Alternate rating, like juvenile detention centers and the like. Look through the data dictionary to find the column that notes if a school was "Rated under AEA Procedures".

- Use Filters to NOT include schools "Rated under AEA Procedures".

You'll see that there are still schools that did not receive a rating for whatever reason. For this story, you want to remove those as well and retain only "Met Standard" and "Improvement Required". We are only comparing stories that are rated under the regular state standards.

- Use Filters to remove the other values.

Lastly, we want to split this table to show charter schools vs other schools. Look through the data dictionary to find the column that denotes if a school is a "Charter School".

- Use Columns to split the count by "Charter School".

Now you have a breakdown of the charter schools vs traditional public schools.

- In the cells below the table, create formulas that give you the percentage of the total schools that failed for charters vs non-charters.
- Name the sheet something the signifies what you've found.

You now have your answer to the first question. Think about how you might write a sentence around that fact.

## Filtering for the Austin MSA

Now that you've created a pivot table that filters all the right things, you don't need to do all that work again to answer the other questions. You can duplicate this sheet and then continue to work on it.

- Duplicate the last pivot table sheet and name the new one something about Austin MSA.
- Look through the data dictionary to find the column that denotes the County of each school.
- Use the County column in Filters to find just schools in our coverage area.

Your failure percentages should update with the pivot table. You now have the answers for Question 2.

## List the Austin MSA schools that failed

This is probably the easiest thing to find now that you have this pivot table.

- Double-click on the value of the failed schools for Non-charters. This opens a new sheet that lists the data that made up that number. Name the sheet appropriately.
- Double-click on the value of the failed schools for Charter schools. Name the new sheet appropriately.

You now have the answers for Questions 3 & 4.

## Austin ISD schools that failed

You can now sort that list by District to see the Austin schools and their data.

The last question you need answered for your stories is the number of consecutive years that AISD schools have failed standard. The column `C_YRS_IR` is not listed in the data dictionary, unfortunately.

- Review the Austin ISD schools for `C_YRS_IR` and note how may years each of the schools has not met standards.

## Write a data drop

Now that you've explored the data, it's time to write a short story based on the details. Since you are an Austin-area reporter, you can/should lead with information about AISD, but also include the information about charter schools, even though that would naturally require more reporting to fill out the story.

For the canvas assignment, you'll want to turn in:

- Your Google Sheet of the data and pivot tables
- Your Data Diary
- Your Data Drop story

## Large files and working in Google Sheets

There are a couple of disadvantages to working with Google Sheets vs Microsoft Excel. We are working with a file that 1.8 MB with 8,700 rows by 35 columns. That's a large file but not huge by any standard. Excel could handle this without breaking a sweat, but Google Sheets starts to struggle a little. For instance, you can't edit this file with Offline editing as it is too large.
