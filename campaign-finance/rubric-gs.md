# Rubric for Google Sheets assignment

> This assignment provides experiences with pivot tables.

This [data set](tec-totals-cleaned.xlsx) contains the data concerning the total election campaign funds raised by Texas Legislature members from 2009 to 2014 as provided by the Texas Ethics Commission. The data set was annotated by a reporter with the race/ethnicity of each candidate. The totals for candidates running for statewide office were removed as their totals would skew simple statistics.

The field `Candidate` is a cleaned version of the `Name` field. It updates election committee names to the candidate's name.

The goal of the story is to answer this question:

**Does the share of contributions "earned" by minority Legislators match their proportionate share in the Legislature? i.e,, do Anglo candidates earn more than their share of the pie?**.

We'll also explore some other answers that might be used in a story.

## Questions to answer

Create a new pivot table on a new sheet for each answer. In some cases you are asked to create a chart from the pivot table.

1. Who made the most overall?
    - Pivot by Candidate (not Name!) and sum the Amount. Sort by Amount descending.
2. Who made the most in the most recent election cycle?
    - Same as above (but in a new sheet), but add Election Cycle to filter.
3. What was the average amount raised each election cycle by Democrats and Republicans?
    - Pivot by Party and average the Amount.
    - Make a bar chart of the results.
4. What was the average amount raised overall by race?
    - Pivot by Race/Ethnicity and average the Amount.
    - Add an additional Value to show the "percentage of the grand total".
    - Make a pie chart from the percentage results.
5. What is their percentage of candidates by race?
    - Pivot by candidate. Add column for Race/Ethnicity.
    - Create a pie chart from the Race/Ethnicity column to show their percentages.
6. Given all of the above, answer the question in bold at the top of this rubric. (Just write it out in a new sheet.)