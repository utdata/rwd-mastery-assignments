# Regular Expressions practice

## Goals

The aim here is to clean up some Declared Dangerous Dogs data. The data comes from the City of Austin's data portal, but my copy is edited specifically for this lesson.

### Getting started

For cleaning the data, I want you to:

- Make a copy of this Google Sheet [Declared Dangerous dogs](https://docs.google.com/spreadsheets/d/1KKKAic3qtSUtiRHSFGOQN6G6q5D5MM0B4RCi3Wr8lAg/edit#gid=1210839306).

You'll see the data has the following columns:

- First Name
- Last Name
- Address
- Zip Code
- Description
- Location

Your goal is to use [regex101.com](https://regex101.com) to help you create these new columns, to be added to the existing columns:

- Dog name
- Dog gender
- Dog description (which will include color and breed. Yes, it would be best to have those as separate columns, but they are a mess and I'm giving you a break.)
- Latitude
- Longitude

## Steps to reach your goal

To do this, you need to work on two columns separately. We'll start with the "Description" column:

- Copy/Paste the Description column from Sheets into the [regex101.com](https://regex101.com) test string.
- Build a regular expression to separate that into three groups: Name, Gender, Color/breed. You can leave color and breed in the same column.
- Build a Substitution string to put tabs between the three columns. (Remember, a tab is "\t".)
- Copy your result as NEW columns in your spreadsheet, just to the right of your current columns. Name the headers properly.
- Save your regex101 project and keep the URL. You can put it on a new Sheet in the same workbook.

Next, you get separate latitude and longitude columns from the Location column.

- Start with a new regex101 project (Click the regularexpressions101 banner on the site).
- Copy/paste the Location column from Sheets into the Test String of regex101.com.
- Build a regex to capture the latitude and longitude as separate groups. You can discard the rest of the address as you have them in another column (Address) already.
- Build a Substitution string to return the Latitude and Longitude separated with a tab.
- Copy and past the result as new columns in the spreadsheet, properly labeled.
- Save your Regular expression URL and add it to your Sheet.

## Turning in your work

Turn in the following into Canvas:

- The cleaned data in a Google Sheet. The data should have both the original columns and the new ones you have created. Be sure to share it with me.
- The saved regex101.com URL from both quests. These can be on a new tab in the same Google Sheet as the data, or added as comments in Canvas.

## Some tips and reminders

- Don't work on the whole file at once. Just pull column you need and work on it by itself.
- Remember your goal is to put tabs between your groups, so you can copy/paste the data back into your Sheet.
