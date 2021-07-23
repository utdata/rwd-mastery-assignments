# Alcohol sales/TABC violations assignment

This document outlines how to download two sets of data used in various Reporting with Data projects.

Directions on what to do with the data vary based on the assignments. Links to those directions are at the bottom.

## Downloading the data

### Mixed Beverage Gross Receipts

You'll be drawing from at least five years of data from the [Mixed Beverage Gross Receipts](https://data.texas.gov/Government-and-Taxes/Mixed-Beverage-Gross-Receipts/naix-2893). Before downloading, filter the data in the following ways:

- Review the **Columns in this Dataset** so you get an idea of the fields available.
- Click the **View Data** button at the top to get to the data.
- Filter the **Obligation End Date** to AFTER Dec. 31 2013.
- Filter the **Location County** to "227", which is the code for TRAVIS County.
- Export as a CSV.

You should end up with a little over 80k records. Any further filtering can be done in your analysis tool (like Workbench, Tableau or R).

### Important notes about this data

Each row of the data is the amount of total money brought in **_each month_** by the establishment, based on the Obligation End Date, which is always the last day of the reporting month. (Ignore the Responsibility dates.)

There are four values of money: Total Receipts, Wine Receipts, Beer Receipts, Liquor Receipts and Cover Charge Receipts. The beer, wine, liquor and cover charge values _should_ add up to the Total Receipts, though I've found that is not always true. I would **stay away from any analysis on Cover Charges** as there must be some special rules of when they need to be reported that would need investigation to understand. The amounts are sales amounts (i.e., total amount of money bought in for that month for that category) and not profits or number of drinks sold.

VERY IMPORTANT: Establishments have until the 20th day of the following month to upload their data, and then it takes some days to become live. Because of this, you might not have full records for the month you download OR THE MONTH BEFORE. Be aware of that and be careful to not compare recent months. **If you are downloading in early August, then you probably only have data through June!**.

Sometimes names of taxpayers and locations are obscured. Hotel chains may have a company that serves all their hotels. A beverage company may hold license to sell in multiple locations. Each Taxpayer Name has only one Taxpayer Number, but that company could own many establishments in many locations.

### TABC enforcement actions

This one is a little more complicated to filter and download.

The site we'll use includes data violations of rules/laws handled by the Texas Alcoholic Beverage Commission. We will concentrate on some of the most-common types of violations that are dealt with in the sale of alcohol in restaurants and bars: Sales to minors, and sales to intoxicated people.

- Start at the [TABC Public Inquiry page](https://apps.tabc.texas.gov/publicinquiry/)
- Click on **Create a list of licenses or permits with administrative violations**.
- For **Location**, click on the **Add/Edit** link.
  - Under **County**, choose **TRAVIS**.
  - Click **Submit Entry**. Then choose **Return to Prior page**.
- For **Violations**, click on the **Add/Edit** link.
  - You'll see a list of violations. Choose **503: Permitting Minor To Possess/Consume**. Click **Submit Entry**. Repeat this process until you have all the violations listed below.
    - 503: Permitting Minor To Possess/Consume
    - 504: Sell/Serve/Dispense/Deliver AB To Minor
    - 561: Sell/Deliver AB to Intoxicated Person
    - 562: Intoxicated Licensee/Permittee
    - 563: Sale To An Obviously Intoxicated Person
    - 585: Emergency order (This is for Spring 2021 -- see note in assignment details)
  - Once you have them all, then **Return to Prior page**
- For **Licence Type**, click on the **Add/Edit** link.
  - Click on **Retailers** and you'll see a list appear to the right.
  - Choose these permits:
    - BE - Beer Retailer's On Premise License
    - BG - Wine&Beer Retailer's On Premise Permit
    - BP - Brewpub License
    - MB - Mixed Beverage Permit
    - N - Private Club Registration Permit
    - RM - Mixed Beverage Restaurant Permit with FB
  - Click **Submit Entry** and then **Return to Prior page**
- On **License Status** add "Inactive" to the two default options (Active Current, Active Suspended).
- On **Violation Start Date** choose 01/01/2014 to present date.
- On **Output type** choose _Comma-delimited file_.
- Type in the security measure code.
- Lastly, choose **Submit Query** and it will download the file.

Note at the bottom there is a link to the [Record layout](https://www.tabc.texas.gov/static/4d47ecaf160f3ba76b8b4f3bd8ecb255/administrative-violations-record-layout.pdf) of the data, which you'll need to understand all the fields.

## Assignments

- [Long semester project](rubric-long-semester.md)
