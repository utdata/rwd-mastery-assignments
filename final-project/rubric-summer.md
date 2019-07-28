# Final project (summer)

> This is a work in progress and likely to change.

The summer final project for Reporting with Data is a little different than during a long semester because of the compressed schedule.

## Deliverables

- You'll produce an 800-word news story with at least three human sources (including in-class sources) that you have personally interviewed. You can include additional student sources in your reporting, but not from our class and they don't count toward the three. Properly credited published reports or studies are allowed as source material in your story, but they do not count toward your human source quota. **Include a headline for your story**.  Use Google Docs and share with me as an editor. (300 points)
- You have two datasets to draw from: Alcohol sales and TABC enforcement actions (more below on that). You'll need to download these data sets and explore them using tools you've learned in class. You don't have to use both sets in the story, but know that you have TABC IDs in both sets to match the data together. We'll discuss story ideas in class.
  - Any work you've done in analysis (Workbench, Tableau, other charting tools) will be turned in, regardless if it is used in the story or not. (200 points)
  - You will need to keep a data diary to log your downloads, source contacts and any analysis notes not otherwise kept in Workbench annotations. (50 points)
  - You'll produce at least one publishable chart to go with your story using the tool of your choice. This chart needs to have a proper headline, description, legend, annotations and such so that the chart **can be understood outside the context of the story**. (50 points)
- You'll need to choose an editing partner and you'll need to include a short report of how you helped them focus and edit their story and analysis. Use Google Docs. (50 points)
- Two promotional tweets, one geared toward the story and one geared toward a chart. You don't have to actually tweet the results, just put them in a Google Doc. Include an image that might help draw attention to your tweet. (25 points)
- A diversity statement about how you did or could better add diversity of voice to your story. (25 points)

## The data

### Mixed Beverage Gross Receipts

- You'll be drawing from at least five years of data from the [Mixed Beverage Gross Receipts](https://data.texas.gov/Government-and-Taxes/Mixed-Beverage-Gross-Receipts/naix-2893). Before downloading, filter the data in the following ways:
  - Review the **Columns in this Dataset** so you get an idea of the data available.
  - Click the **View Data** button at the top to get to the data.
  - Filter the **Obligation End Date** from Jan. 1 2014 to present.
  - Filter by **Location City** for Austin.
  - Export as a CSV.

You should end up with around 66k records. Any further filtering can be done in your analysis tool (likely Workbench or Tableau).

### TABC enforcement actions

This one is a little more complicated to filter and download.

- Start at the [TABC site](https://www.tabc.state.tx.us/enforcement/index.asp)
- Click the **Public Inquiry** menu in the red bar.
- Click on **Create a list of licenses  or permits with administrative violations**.
- For **Location**, click on the **Add/Edit** link.
  - Add **City**, choose **Other**. Type in _AUSTIN_ and click **Submit Entry**. Then choose **Return to Prior page**.
- For **Violaton**, click on the **Add/Edit** link.
  - You'll see a list of violations. Choose **504: Sell/Serve/Dispense/Deliver AB to Minor**. Click **Submit Entry** and then **Return to Prior page**.
- For **Licence Type**, click on the **Add/Edit** link.
  - Click on **Retailers** and you'll see a list appear to the right.
  - Choose these permits (List TK)
  - Click **Submit Entry** and then **Return to Prior page**
- On **License Status** keep the two default options (Active Current, Active Suspended) and also add Inactive.
- On **Violation Start Date** choose Jan. 1, 2014 to present date.
- On **Output type** choose _Comma-delimited file_.
- Lastly, choose **Submit Query** and it will download the file.

Note at the bottom there is a link to the [Record layout](https://www.tabc.texas.gov/public_Inquiry/admin_violations_record_layout.asp) of the data, which you'll need to understand all the fields.


