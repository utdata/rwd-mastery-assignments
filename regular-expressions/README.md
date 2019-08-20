# Regular Expressions practice

Your goal here is to clean up Declared Dangerous Dogs data.

For cleaning the data, I want you to:

Download my copy of the data set "[Declared Dangerous dogs](data/declared_dangerous_dogs.csv?raw=true)". This came from the City of Austin's data portal, but my copy is a little easier to work with.

Your goal is to have a data set with the following columns:

The original columns:

- First Name
- Last Name
- Address
- Zip Code
- Description of Dog
- Location

New columns:

- Dog name
- Dog gender
- Dog description (which will include color and breed. Yes, it would be best to have both - color and breed as separate columns, but they are a mess and I'm giving you a break.)
- Latitude
- Longitude

To do this, you need to work on two columns separately. We'll start with the "Description of Dog" column:

- Copy/Paste the Description of Dog column into the regex101.com test string.
- Build a regular expression to separate that into three groups: Name, Gender, Color/- breed. You can leave color and breed in the same column together for this assignment, - as they are a mess.
- Build a Substitution string to put tabs between the three columns. (Remember, a tab is - "\t".)
- Copy your result as NEW columns in your spreadsheet, and name the headers properly.
- Save your Regular expression and Substitution formulas to turn in. You can save them in a different cell or as a comment in the submission.

Next, you get separate latitude and longitude columns from the Location column.

- Start by putting the Location column in the Test String of regex101.com.
- Build a regex to capture the latitude and longitude as separate groups. You can discard - the rest of the address as you have them in another column (Address) already.
- Build a Substitution string to return the Latitude and Longitude separated with a tab.
- Copy and past the result as new columns in the spreadsheet, properly labeled.
- Save your Regular expression and Substitutionformulas to turn in.

You will turn in:

- The cleaned data in a spreadsheet. The data should have both the original columns and the new ones you have created.
- The search regex you used for both columns
- The replace regex you used for both columns

Some tips and reminders:

- Don't work on the whole file at once. Just pull column you need and work on it by - itself.
- Remember your goal is to put tabs between your groups, so you can copy/paste the data back into your Spreadsheet.
