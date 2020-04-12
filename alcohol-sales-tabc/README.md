# Alcohol sales/TABC violations assignment

This document outlines how to download two sets of data used in various Reporting with Data projects.

Directions on what to do with the data vary based on the assignments. Links to those directions are at the bottom.

## Downloading the data

### Mixed Beverage Gross Receipts

You'll be drawing from at least five years of data from the [Mixed Beverage Gross Receipts](https://data.texas.gov/Government-and-Taxes/Mixed-Beverage-Gross-Receipts/naix-2893). Before downloading, filter the data in the following ways:

- Review the **Columns in this Dataset** so you get an idea of the fields available.
- Click the **View Data** button at the top to get to the data.
- Filter the **Obligation End Date** from Jan. 1 2014 to present.
- Filter by **Location City** for AUSTIN. (Use capital letters ... it is case sensitive.)
- Export as a CSV.

You should end up with a little over 70k records. Any further filtering can be done in your analysis tool (likely Workbench or Tableau).

### Important notes about this data

Each row of the data is the amount of total money brought in **_each month_** by the establishment, based on the Obligation End Date, which is always the last day of the reporting month. (Ignore the Responsibility dates.)

There are four values of money: Total Receipts, Wine Receipts, Beer Receipts, Liquor Receipts and Cover Charge Receipts. The beer, wine, liquor and cover charge values _should_ add up to the Total Receipts, though I've found that is not always true. I would **stay away from any analysis on Cover Charges** as there must be some special rules that would need investigation to understand. The amounts are sales amounts (i.e., total amount of money bought in for that month for that category) and not profits or number of drinks sold.

### TABC enforcement actions

This one is a little more complicated to filter and download.

The site we'll use includes data violations of rules/laws handled by the Texas Alcoholic Beverage Commission. We will concentrate on some of the most-common types of violations that are dealt with in the sale of alcohol in restaurants and bars: Sales to minors, and sales to intoxicated people.

- Start at the [TABC site](https://www.tabc.state.tx.us/enforcement/index.asp)
- Click the **Public Inquiry** menu in the red bar.
- Click on **Create a list of licenses or permits with administrative violations**.
- For **Location**, click on the **Add/Edit** link.
  - Add **City**, choose **Other**. Type in _AUSTIN_ and click **Submit Entry**. Then choose **Return to Prior page**.
- For **Violations**, click on the **Add/Edit** link.
  - You'll see a list of violations. Choose **503: Permitting Minor To Possess/Consume**. Click **Submit Entry**. Repeat this process until you have all the violations listed below.
    - 503: Permitting Minor To Possess/Consume
    - 504: Sell/Serve/Dispense/Deliver AB To Minor
    - 561: Sell/Deliver AB to Intoxicated Person
    - 562: Intoxicated Licensee/Permittee
    - 563: Sale To An Obviously Intoxicated Person
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
- Lastly, choose **Submit Query** and it will download the file.

Note at the bottom there is a link to the [Record layout](https://www.tabc.texas.gov/public_Inquiry/admin_violations_record_layout.asp) of the data, which you'll need to understand all the fields.

For this project, I suggest you stay away from directly joining the TABC data to the alcohol sales data ^^. But, you can look through it to find examples of the same establishment from both sets of records, if you like.

^^ (You _could_ join them, but you would need to be super careful that you aren't duplicating rows in either set. i.e., both data sets would have to be reshaped to have only one row per establishment before joining. Talk to me if this is important to you.)

## Assignments

- [Spring 2020 project](rubric-spring20.md)
- [Long semester project](rubric-long-semester.md)
- [Summer final project](rubric-summer.md)
