# Military surplus transfers

The Defense Logistics Agency transfers surplus military equipment to local law enforcement through its [Law Enforcement Support Office](https://www.dla.mil/DispositionServices/Offers/Reutilization/LawEnforcement/PublicInformation/). They agency updates the data quarterly and the data in this lesson contains transfers through **December 31, 2020**. As of this date, the file name is linked from the headline "ALASKA - WYOMING AND US TERRITORIES".

The data there comes in an Excel spreadsheet that has a new sheet for each state. That is a beast of a file to combine into a single table without scripting of some kind, so I used R to do that for you. Downloading instructions are below.

The original idea for this assignment came from this [June 4, 2020 Buzzfeed News story](https://www.buzzfeednews.com/article/johntemplon/police-departments-military-gear-1033-program) about the amount of equipment transferred since Michael Brown was killed in Ferguson, Missouri. There was a public outcry after "what appeared to be a massively disproportionate show of force during protests brought scrutiny to a federal program that transfers unused military equipment to local law enforcement." John Templon used the data to write an update on the program and published his [data analysis](https://github.com/BuzzFeedNews/2020-06-leso-1033-transfers-since-ferguson).

We are using the same data to tell stories about our local agencies.

## Download the data

- Go to [this page](https://github.com/utdata/rwd-r-leso/blob/main/data-processed/leso.csv) and then use the **Download** button to download the file to your computer. Use that data for your assignment below.

## About the data

There is no data dictionary or record layout with this data but I have corresponded with the Defense Logistics Agency to get a decent understanding of what is included.

- sheet: Which sheet the data came from. This is an artifact from the data merging script. You can ignore it. (I plan to remove it.)
- state: A two-letter designation for the state of the agency.
- station_name_lea: This is the agency that got the equipment.
- nsn: A special number that identifies the item. It is not germane to this specific assignment.
- item_name: The item "purchased". Googling it can sometimes yield more info on specific items.
- quantity: The number of the "units" the agency received.
- ui: Unit of measurement (item, kit, etc.)
- acquisition_value: a cost _per unit_ for the item.
- demil_code: Another special code not germane to this assignment.
- demil_ic: Another special code not germane to this assignment.
- ship_date: The date the item(s) were sent to the agency.
- station_type: What kind of law enforcement agency made the request.

Each row of data is a transfer of a particular type of item from the U.S. Department of Defense to a local law enforcement agency. The row includes the type of item, the number of them, and the cost of each unit. This means to get the total value of the items you have to multiply the `quantity` times the `acquisition_value`.

The agencies really only pay the shipping costs, so you can't say that paid for the items, and the amount you can calculate is the "value" of the items, not their cost to the agency.

## Assignments

- [Workbench rubric](rubric-wb.md)
