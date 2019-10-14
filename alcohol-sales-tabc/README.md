# Alcohol sales/TABC violations assignment

This document outlines how to download two sets of data used in various Reporting with Data projects.

Directions on what to do with the data vary based on the assignments. Links to those directions are at the bottom.

## Downloading the data

### Mixed Beverage Gross Receipts

- You'll be drawing from at least five years of data from the [Mixed Beverage Gross Receipts](https://data.texas.gov/Government-and-Taxes/Mixed-Beverage-Gross-Receipts/naix-2893). Before downloading, filter the data in the following ways:
  - Review the **Columns in this Dataset** so you get an idea of the fields available.
  - Click the **View Data** button at the top to get to the data.
  - Filter the **Obligation End Date** from Jan. 1 2014 to present.
  - Filter by **Location City** for Austin.
  - Export as a CSV.

You should end up with just shy of 70k records. Any further filtering can be done in your analysis tool (likely Workbench or Tableau).

### Important notes about this data

Each row of the data is the amount of total money brought in _each month_ by the establishment, based on the Obligation End Date, which is always the last day of the reporting month. (Ignore the Responsibility dates.)

There are four values of money: Total Receipts, Wine Receipts, Beer Receipts, Liquor Receipts and Cover Charge Receipts. The beer, wine liquor and cover charge values _should_ add up to the Total Receipts, though I've found that is not always true. I would stay away from any analysis on Cover Charges as there must be some special rules that would need investigation to understand.


### TABC enforcement actions

This one is a little more complicated to filter and download.

- Start at the [TABC site](https://www.tabc.state.tx.us/enforcement/index.asp)
- Click the **Public Inquiry** menu in the red bar.
- Click on **Create a list of licenses or permits with administrative violations**.
- For **Location**, click on the **Add/Edit** link.
  - Add **City**, choose **Other**. Type in _AUSTIN_ and click **Submit Entry**. Then choose **Return to Prior page**.
- For **Violatons**, click on the **Add/Edit** link.
  - You'll see a list of violations. Choose **504: Sell/Serve/Dispense/Deliver AB to Minor**. Click **Submit Entry** and then **Return to Prior page**. Repeat this process until you have all the violations listed below.
    - 504: Sell/Serve/Dispense/Deliver AB To Minor
    - 503: Permitting Minor To Possess/Consume
    - 561: Sell/Deliver AB to Intoxicated Person
    - 562: Intoxicated Licensee/Permittee
    - 563: Sale To An Obviously Intoxicated Person
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

## Assignments

- [Long semester project](rubric-long-semester.md)
- [Summer final project](rubric-summer.md)
