# Military surplus transfers

> MAJOR UPDATE NEEDED. We need to add a Total Value to each row that is Quantity * Acquisition Value.

> Can also use my updated data instead once I reconcile my R repos.

The Defense Logistics Agency transfers surplus military equipment to local law enforcement through its [Law Enforcement Support Office](https://www.dla.mil/DispositionServices/Offers/Reutilization/LawEnforcement/PublicInformation/). They agency updates the data quarterly and the data in this lesson contains transfers through December 31, 2020. As of this date, the file name is linked from the headline "ALASKA - WYOMING AND US TERRITORIES".

The data there comes in an Excel spreadsheet that has a new sheet for each state. That is a beast of a file to combine into a single table without scripting of some kind, so I used R to do that for you.

The original idea for this assignment came from this [June 4, 2020 Buzzfeed News story](https://www.buzzfeednews.com/article/johntemplon/police-departments-military-gear-1033-program) about the amount of equipment transferred since Michael Brown was killed in Ferguson, Missouri. There was a public outcry after "what appeared to be a massively disproportionate show of force during protests brought scrutiny to a federal program that transfers unused military equipment to local law enforcement." John Templon used the data to write an update on the program and published his [data analysis](https://github.com/BuzzFeedNews/2020-06-leso-1033-transfers-since-ferguson).

## Download the data

- Go to [this page](https://github.com/utdata/rwd-r-leso/blob/main/data-processed/leso.csv) and then use the **Download** button to download the file to your computer. Use that data for your assignment below.

## About the data

There is no data dictionary or record layout with this data but I have corresponded with the Defense Logistics Agency to get a decent understanding of what is included.

- sheet: Which sheet the data came from. This is an artifact from the data merging script.
- state: A two-letter designation for the state of the agency.
- station_name_lea: 
- nsn: 
- item_name: 
- quantity: 
- ui: Unit of measurement
- acquisition_value: a cost _per unit_ for the item.
- demil_code: 
- demil_ic:
- ship_date: 
- station_type: 

Rows: 133,949
Columns: 12
$ sheet             <chr> "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", …
$ state             <chr> "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", "AL", …
$ station_name_lea  <chr> "ABBEVILLE POLICE DEPT", "ABBEVILLE POLICE DEPT", "ABBEVILLE POLICE DEPT", "ABBEVILLE POLI…
$ nsn               <chr> "2355-01-553-4634", "1240-01-411-1265", "2320-01-371-9584", "2320-01-371-9584", "1005-01-5…
$ item_name         <chr> "MINE RESISTANT VEHICLE", "SIGHT,REFLEX", "TRUCK,UTILITY", "TRUCK,UTILITY", "MOUNT,RIFLE",…
$ quantity          <dbl> 1, 9, 1, 1, 10, 1, 10, 10, 1, 1, 1, 1, 10, 3, 12, 5, 11, 1, 1, 10, 1, 2, 12, 1, 3, 1, 10, …
$ ui                <chr> "Each", "Each", "Each", "Each", "Each", "Each", "Each", "Kit", "Each", "Each", "Each", "Ea…
$ acquisition_value <dbl> 658000.00, 333.00, 62627.00, 62627.00, 1626.00, 10000.00, 926.00, 15871.59, 245.88, 600.00…
$ demil_code        <chr> "C", "D", "C", "C", "D", "Q", "D", "D", "D", "D", "D", "D", "D", "D", "D", "D", "D", "D", …
$ demil_ic          <chr> "1", "1", "1", "1", "1", "3", "1", "1", NA, "7", "1", NA, "1", "1", "1", "1", "1", "1", "1…
$ ship_date         <dttm> 2016-11-09, 2016-09-14, 2016-09-29, 2016-09-29, 2016-09-19, 2017-03-28, 2017-03-28, 2018-…
$ station_type      <chr> "State", "State", "State", "State", "State", "State", "State", "State", "State", "State", …

Each row of data is a "sale" of a particular type of item from the U.S. Department of Defense to a local law enforcement agency. The row includes the type of item, the number of them, and the cost of each one. This means to get the total value of the items you have to multiply the `quantity` times the `acquisition_value`.

## Assignments

- [Workbench rubric](rubric-wb.md)
