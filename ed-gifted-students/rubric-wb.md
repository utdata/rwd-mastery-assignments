# Gifted students assignment

Be sure to review the [README](README.md) for important information that precedes this.

## Rubric for Workbench

The goal is to find the answer to the following questions:

- Which campuses in the state have the highest percentage of GT students? Filter to those with at least 100 students designated.
  - More importantly, find and rank AISD schools by the highest percentage of GT students.
- Which districts statewide have the highest percentage of students designated as Gifted and Talented (GT students)? Might you look further at any schools in local districts?

To do this, you'll have to "join" directory data to your gifted schools data to get the names of schools and districts.

## Import and clean the data sets

Once past the hassle of downloading the data, there are still some challenges to getting the answers above. Here are some things to consider or know:

- On the downloaded files, you have to change the filename of the CSTUD and DSTUD extension from `.dat` to `.csv` before they will import into Workbench.
- Import each data file into its own Tab. Clean the data as described below. Any other work should be started with a new tab using **Start from tab**.
- Since the Student and District data have just IDs instead of names of schools or districts, you'll have to join them with the Directory data. To do that you have to take special care with those ID columns, which are supposed to start with zeros. In the District file, the `DISTRICT` column is supposed to be text with the IDs starting with one or more zeros, like `001902`. There is no Workbench function to fix that (as of yet), but since it is built on Python's Pandas package, we can use some use Python code to fix this. Create a new Python block and add the following for the District data:

```python
def process(table):
    table['DISTRICT'] = table['DISTRICT'].astype(str).str.replace(',', '').str.zfill(6)
    return table
```

- In the Student data, it is similar but the column name and zfill values are different:


```python
def process(table):
    table['CAMPUS'] = table['CAMPUS'].astype(str).str.replace(',', '').str.zfill(9)
    return table
```

- For the Directory data, the `District Number` and `School Number`fields come in with a `'` at the beginning of the ID, which keeps it as text. However, you have to remove that before they will join properly. You can do that by using **Split Column** on a delimiter of `'`. (Another way would be to Split using "x from from the right".)
- You might want to rename the columns to something that makes sense based on the data dictionaries. See below that you want the DistrictID and CampusID match their partner columns in your Directory data.

## Working the Campus data

The easiest way to start with joins is to begin with the Campus data:

- Start a new tab from the CSTUD cleaned data.
- Use **Select columns** to keep just the ID and the gifted count and percentage columns.
- Use **Join Tab** to join with the Directory data. This is where you have to make sure that the District ID is named the same in cleaned both data sets.
- Choose to include the school name and district name into you data.

Now you can continue on your quest to find the schools with the highest GT percentage:

- Filter your data to include only schools that have at least 100 GT students (the gifted count field).
- Sort by highest percentage.

There are quite a few schools with 100% GT students because they cater to them. That isn't all that interesting, but you might note how many there are. If/when you write about it, be sure to note you are only looking at schools with at least 100 gifted students identified.

## Working with District data

For the district data, if we join directly to the Directory data we'll get multiple matches for each district, as many as there are schools in that district. To solve this, we first have to create a "District Directory" that one row for each district.

- Start a new tab from the Directory data and call it "Dist Directory" or something like that.
- Use **Select columns** get keep just the ID and name columns, then use **Deduplicate** to get a joinable list that lists each district just once.

> This is where i am

- When you are working on a new tab for Campus or District data, you might use Select Columns to just the columns you need.
- When you are working on the Directory data for School names, you don't need Deduplicate, but you still probably want to select only the ID and School names before you join.


Now you have the districts with the most students identified as GT. A local district, LEANDER ISD, as typically been near the top. That is a fact for your data drop.

## Turning in your work

With this assignment I expect two things:

- A very short "story" that outlines the answers to the questions posed above. i.e., sentences that explain your findings, written as a short news story/data drop.
- Share your Workbench project (or projects) with my email and submit the private link as a comment in the assignment.
