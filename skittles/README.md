# Distribution of Skittles

For this assignment students in class all contributed to a dataset that counted the number of Skittles in a traditional 61.5g package. Our goal is to find out:

- Are candy colors evenly distributed within a package of Skittles?
- Does the candy color distribution change over a series of packages?

If you participated in the data gathering exercise then you likely know the answer to the first question. They are often not even as some packages have more candies of certain colors. But what about a number of packages?

We'll use Workbench to find out and Datawrapper to visualize. We'll be making a bar chart so you might look over the [Datawrapper Academy entry](https://academy.datawrapper.de/article/7-bar-chart) on that.

## Preparing data in Workbench

Since we collected this data using a Google Form that ends up as a Google Sheet, we can import the data directly from the sheet. We can even update it as more data comes in.

- Start a new Workbench workflow and title it **YourName - Skittles**.
- Start a new tab and use **Import from URL** and name it `Import`.
- Enter this URL. Make sure you copy the whole URL if it scrolls off the screen:

``` text
https://docs.google.com/spreadsheets/d/1JHS1yIbbVg7lUZzTMzJIlQGaZsEzWtNuM9_xKGHOknk/gviz/tq?tqx=out:csv
```

> How did I get this URL? First I just guessed there must be a way to access a Google Sheet as a csv file, so I [Googled it](https://www.google.com/search?ei=S5uPXYGtBMjwtAWlprrADg&q=View+google+sheet+as+csv+url&oq=View+google+sheet+as+csv+url&gs_l=psy-ab.3..33i22i29i30l2.1863.3505..3934...0.2..0.134.416.2j2......0....1..gws-wiz.......0i71.OIkQk-bM6Dg&ved=0ahUKEwjB_tiaiPTkAhVIOK0KHSWTDugQ4dUDCAs&uact=5). One article I found was [this one](https://stackoverflow.com/questions/33713084/download-link-for-google-spreadsheets-csv-export-with-multiple-sheets), which allowed me to figure it out after a little trial and error.

### Reshaping the data for grouping

This data is in a "wide" format where each row has many observations and the columns headers describe them. In this case how many of a different colors of candy are in a bag of Skittles.

For us to consider all of these observations together we need to reshape the data as "long" data so we can use **Group** by `Color` to do aggregations like averages, sums and counts. We need each row to consider one color and value from each bag.

- Start a new tab and name it `Color stats`.
- Start from the **Import** tab.
- Delete the `Timestamp` column as we don't need it and it will get in the way.
- Start a **Reshape** step.
  - Choose **Wide to long**.
  - For _Row variable_ choose **Name**.

This reshaped our data so there is one row for each observation. We don't actually need the `Name` field for our visualization, but we needed a column to pivot upon. (This is a failing in Workbench IMHO, but I don't want to get into it here.)

Our new columns have un-descriptive names, so let's rename them.

- Start a **Rename** step.
- Change `variable` to `Color`.
- Change `value` to `Total`.

Now for the grouping to get our averages for each color. This might be the first time we've grouped on something other than **Count**.

- Start a new **Group** step.
  - For _Column_ choose `Color`
  - For _Operations_ choose `Average (Mean)`.
  - In the column dropdown, choose the `Total` column.
  - Name the field `Average count`.

## Make a Datawrapper bar chart

Now you have the data you need to make a bar chart in Datawrapper. While we haven't made a bar chart yet, you've had enough practice in Datawrapper to make it work. You can do it!

Be sure to give all the information a reader would need to understand your chart. You'll be graded on that.

## Going further with the data

This isn't required, but I find this data fascinating. (OK, I'm a data dork.) Some other things you might explore if you want:

- What was the most or least of any color of candy in a bag? Who got them?
- Who got got the least and most total number of candies?

## Turn in your work

- Share your Workbench workbook and submit the link to the assignment.
- Publish your Datawrapper chart and submit the link to the assignment.
