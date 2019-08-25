# Regular Expressions in Workbench

> Work in progress.

There are a couple of ways to use Regular Expressions in Workbench:

- **Regex extractor** extracts values in a specific column using regular expression to store them in a new column.
- **Filter by condition** has three conditions that allow use of regex:
  - **Text contains regex** keeps rows where the pattern matches.
  - **text does not contain regex** excludes rows where the pattern matches.
  - **Text exactly matches regex** (I'm actually not sure the difference is vs contains, as it doesn't work as I expect.)

We will be using the **Filter by condition** step with **Text contains regex** for this assignment.

## Goals

Start with [this workflow](https://app.workbenchdata.com/workflows/30154) and then duplicate it. Add your name to the title.

For each quest **start a new tab** from the "Locations columns" tab.

- Find establishments on The Drag. These are addresses from 1900 to 2899 GUADALUPE ST. You should end up with 12 rows.
- Find establishments on Dirty Sixth. These are addresses 100 to 799 E. 6TH ST. You should end up with 57 rows.

(On the Dirty Sixth quest, we are only finding places with an actual 6th Street address. I know there are bars in the area that face cross streets with different addresses. We'll ignore those for this assignment.)

## Hints

- As you filter the addresses, you might first make a filter that contains the street name so you can reduce the number of places you are looking at. Then you can build another filter (or an "and" condition) that targets the digits at the beginning of the address field.
- Using a token to "start at the beginning of the line" will help. (Otherwise your pattern might also match something in the middle of the line, too).
- Remember you are matching each character in order, so consider the rule you need for the first character and then run the step to check it before moving onto the next character.
- You can use a "numeric range" to limit which digits you are looking for. The [first three paragraphs of this tutorial](https://www.regular-expressions.info/numericranges.html) explain that concept.
- If you are done looking for specific/ranges of numbers in your pattern, then consider what the next "character" should be in your pattern if you don't want another digit.
- Since we are using the "Text contains regex" condition, you don't have to build a pattern to match the entire field. You can just build the filter until get the matches you need, then stop.