# Military surplus transfers for Workbench

Be sure to review the [README](README.md) to learn about the data and download it.

> This is a "mastery" assignment, which means you are applying skills learned in other assignments here without detailed direction.

Your charge with this assignment is to see how several local police agencies have benefited from the Defense Logistic Agency's Law Enforcement Support program over the past five years.

## The questions to answer

> Make sure you read the guidance below _before_ you start tackling these questions.

All answers should be based on data _after_ **Dec. 31, 2015**. This gives you at least five full years of data. In addition, only consider **Texas agencies** as you answer the following.

- Which departments have received the most equipment by value in Texas?
  - FOOD FOR THOUGHT: Are there agencies that stands out? It makes sense that Houston, the fourth largest city in the nation, would have a lot because of the sheer size. Who else has benefited? Anyone local?
- What is the **total number of items** and the **total value of equipment** transferred to each of the following local agencies (Think group and sum):
  - Austin Police Department
  - Travis County Sheriff's Office
  - University of Texas System
- What are the **items**, their total quantity and total value shipped to **each local agency** listed above. i.e., for each agency make a tab that:
  - groups by the item name
  - sums the quantity
  - sums the values
  - sorts by the most expensive
- FOOD FOR THOUGHT: What are some interesting items given to agencies? (You might have to Google them to figure out what they are.)

## Some guidance as you tackle this

- Have a single tab for importing and cleaning the data, then build new tabs from that using "Start from tab". Each tab typically has only one goal or "answer".
  - (You don't need tabs for "FOOD FOR THOUGHT" items. Just think on those as story ideas.)
- After you import the data, don't forget to filter by state (Texas) and by the date (only from 2016 through 2020).
- As noted in the [README](README.md), each row is a shipment of a particular type of equipment. The `quantity` is number of items shipped, and the `acquisition_value` is the value of ONE of those items. You have to create your own "Total" to get the value of all items for that shipment (i.e. row of data). You'll then use that new Total to get the answers sought above.
- When it comes to individual local agencies, you might create a tab that starts with cleaned data and then filters for that agency so you can see all the shipments. Then you can build subsequent tabs from the agency tab to find your answers.
- Keep your tab names short. When you have lots of them, they get hard to see.
- The **Group** function and the **Sum** operations within it are your friend for this assignment.
- When you get to your "last" step on a tap, make sure your money or "value" columns are formatted as currency. Once you use a Group function you lose the currency formatting.
- Make sure you use annotations for your steps.

## Turning in the assignment

This is a two-part assignment.

### Turn in the Workbook

- Give your Workflow a name. Don't leave it Untitled. Include YOUR name in the title.
- Share your workflow. Click on the **Share** button and set it like this:

![share-workflow](img/sharing-workbench.png)

### Write a data drop

With this part of the assignment we are practicing writing sentences about the data and not a complete story. You do NOT need to explain the Ferguson angle with these few sentences. Just concentrate on how you would write the facts and attribution.

- Use Google Docs and be sure to share with me AS AN EDITOR.
- Be sure to turn in the URL to your Doc in the Canvas assignment.
- Write a four paragraph data drop from the data. Be sure to include attribution about where the data came from. (Think of the original data source, not that it came from Buzzfeed. Links are in the README.)
- You can pick the angle from any of the questions outlined above, but each paragraph should be a description of what you found in the data.

Here is a **partial** example to give you an idea of what I'm looking for. (You can't use this one ;-)).

> The Jefferson County Sheriff's Office is flying high thanks to gifts of nearly $2.5 million worth of surplus U.S. Department of Defense equipment.

> Among the items transferred over the past seven years to the department was a $923,000 helicopter in October 2016 and related parts the following year, according to data from the Defense Logistics Agency data — the agency that handles the transfers.

> The sheriff's office has received the highest value of equipment among any law enforcement agency in Texas since August 2014.

## Ignore this

- [Just for me](https://app.workbenchdata.com/workflows/78448/)
