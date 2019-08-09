# Final project (summer)

The summer final project for Reporting with Data is a little different than during a long semester because of the compressed schedule.

## Deliverables

- You'll produce an 800-word news story with at least three human sources (including in-class sources) that you have personally interviewed. (This means you'll have to find at least one source on your own.) You can include additional student sources in your reporting, but not from our class and they don't count toward the three. Properly credited published reports or studies are allowed as source material in your story, but they do not count toward your human source quota. **Include a headline for your story**.  Use Google Docs and share with me as an editor. (300 points)
- You have two data sets to draw from: Alcohol sales and TABC enforcement actions (more on those below). You'll need to download these data sets and explore them using tools you've learned in class. You do NOT have to use both sets in the story. We'll discuss some story ideas in class.
  - You'll turn in any analysis work you've done (Workbench, Tableau, other charting tools), regardless if it is used in the story. I want all your work. (200 points)
  - You will need to keep a data diary to log your downloads, source contacts and any analysis notes not otherwise kept in Workbench annotations. Use Google Doc shared to me. (50 points)
  - You'll produce at least one publishable chart to go with your story using the tool of your choice. This chart needs to have a proper headline, description, legend, annotations and such so that the chart **can be understood outside the context of the story**. Include a screenshot and/or link in your story. (50 points)
- You'll need to choose an editing partner to work with and you'll need to include a short report of how you helped them focus and edit their story and analysis. Use Google Docs and share with me. (50 points)
- Two promotional tweets, one geared toward the story and one geared toward a chart. You don't have to actually tweet the results, just put them in a Google Doc. Include an image that might help draw attention to your tweet. This can be in your story file. (25 points)
- A diversity statement about how you did or could better add diversity of voice to your story. Can also be included with your story file. (25 points)

## The data

### Mixed Beverage Gross Receipts

- You'll be drawing from at least five years of data from the [Mixed Beverage Gross Receipts](https://data.texas.gov/Government-and-Taxes/Mixed-Beverage-Gross-Receipts/naix-2893). Before downloading, filter the data in the following ways:
  - Review the **Columns in this Dataset** so you get an idea of the fields available.
  - Click the **View Data** button at the top to get to the data.
  - Filter the **Obligation End Date** from Jan. 1 2014 to present.
  - Filter by **Location City** for Austin.
  - Export as a CSV.

You should end up with around 66k records. Any further filtering can be done in your analysis tool (likely Workbench or Tableau).

### Important notes about this data

Each row of the data is the amount of total money brought in _each month_ by the establishment, based on the Obligation End Date, which is always the last day of the reporting month. (Ignore the Responsibility dates.)

There are four values of money: Total Receipts, Wine Receipts, Beer Receipts, Liquor Receipts and Cover Charge Receipts. The beer, wine liquor and cover charge values _should_ add up to the Total Receipts, though I've found that is not always true. I would stay away from any analysis on Cover Charges as there must be some special rules that would need investigation to understand.

If you want to use Workbench or Tableau to compare beer, wine and liquor receipts by establishment, you'll have to reshape the data to create a new single column of Receipt Type that includes the key and values from each of the distinct amount columns. Hopefully we'll get a chance to talk about this in class.

### TABC enforcement actions

This one is a little more complicated to filter and download.

- Start at the [TABC site](https://www.tabc.state.tx.us/enforcement/index.asp)
- Click the **Public Inquiry** menu in the red bar.
- Click on **Create a list of licenses or permits with administrative violations**.
- For **Location**, click on the **Add/Edit** link.
  - Add **City**, choose **Other**. Type in _AUSTIN_ and click **Submit Entry**. Then choose **Return to Prior page**.
- For **Violatons**, click on the **Add/Edit** link.
  - You'll see a list of violations. Choose **504: Sell/Serve/Dispense/Deliver AB to Minor**. (You can include others if you really want to study them.) Click **Submit Entry** and then **Return to Prior page**.

> POSSIBLE FUTURE EDIT OF VIOLATIONS LIST
> - 504: Sell/Serve/Dispense/Deliver AB To Minor
> - 503: Permitting Minor To Possess/Consume
> - 561: Sell/Deliver AB to Intoxicated Person
> - 562: Intoxicated Licensee/Permittee
> - 563: Sale To An Obviously Intoxicated Person

- For **Licence Type**, click on the **Add/Edit** link.
  - Click on **Retailers** and you'll see a list appear to the right.
  - Choose these permits:
    - Beer Retailer’s On-Premise License (BE)
    - Wine & Beer Retailer’s On-Premise Permit (BG)
    - Brewpub License (BP)
    - Mixed Beverage Permits (MB)
    - Private Club Permit (N)
    - Mixed Beverage Permit with Food & Beverage Certificate (RM)
  - Click **Submit Entry** and then **Return to Prior page**
- On **License Status** keep the two default options (Active Current, Active Suspended) and also add Inactive.
- On **Violation Start Date** choose Jan. 1, 2014 to present date.
- On **Output type** choose _Comma-delimited file_.
- Lastly, choose **Submit Query** and it will download the file.

Note at the bottom there is a link to the [Record layout](https://www.tabc.texas.gov/public_Inquiry/admin_violations_record_layout.asp) of the data, which you'll need to understand all the fields.

For this project, I think I would stay away from directly joining the TABC data to the alcohol sales data ^^. But, you can look through it to find examples of any of the bars or restaurants you are otherwise studying.

^^ (You _could_ join them, but you would need to be super careful that you aren't duplicating rows in either set. i.e., both data sets would have to be reshaped to have only one row per establishment before joining. Talk to me if this is important to you.)

## How to tackle this project

First, take a look at this resource: [How to tackle a new data set](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit).

While there are filtering and data shaping tools in Tableau, I can see value in using Workbench to clean and shape your data before pulling into Tableau. I think this would be especially true if you plan on using Datawrapper, Atlas or [other charting tools](https://docs.google.com/document/d/1ql3NcPihfTsWb5qFxWIxthybpSvFh_cAcPuMi1McM_0/edit), which tend to like wide instead of long data.

Expect a little trial and error, especially as you are learning. It's part of the process.
