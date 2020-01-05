# Gifted students assignment

Be sure to review the [README](README.md) for important information on how to download the data.

## Rubric for Workbench

The goal is to find the answer to the following questions:

- Which campuses in the state have the highest percentage of Gifted and Talented (GT) students? Filter to those with at least 100 students designated.
  - Which AISD schools have the highest percentage of GT students.
- Which districts statewide have the highest percentage of students designated as GT students?
  - Since there is a local district near the top, look further into their schools.

To find these answers, you'll have to "join" directory data to your gifted schools data to get the names of schools and districts.

## Import and clean the data sets

Once past the hassle of downloading the data, there are still some challenges to getting the answers above. Here steps to import and prepare the data:

- On the downloaded files, you have to change the filename of the CSTUD and DSTUD extension from `.dat` to `.csv` before they will import into Workbench.
- Import each data file into its own Workbench tab. Clean the data as described below. Any other work should be started with a new tab using **Start from tab**.

### Fix the IDs in gifted data

Since the Student and District data have just IDs instead of names of schools or districts, you'll have to join them with the Directory data. To do that you have to take special care with those ID columns, which are supposed to start with zeros. In the District file, the `DISTRICT` column is supposed to be text with the IDs starting with one or more zeros, like `001902`. There is no Workbench function to fix that (as of yet), but since it is built on Python's Pandas package, we can use some use Python code to fix this.

- On the DSTUD data, create a new Python block and add the following:

```python
def process(table):
    table['DISTRICT'] = table['DISTRICT'].astype(str).str.replace(',', '').str.zfill(6)
    return table
```

This does two things: First, it changes the numbers to a string of text, then it looks at the number of characters in that string and fills with zeros at the beginning until there are six characters.

- In the Student data, it is similar but the column name and zfill values are different:


```python
def process(table):
    table['CAMPUS'] = table['CAMPUS'].astype(str).str.replace(',', '').str.zfill(9)
    return table
```

### Fix the IDs in the directory data

For the Directory data, the `District Number` and `School Number`fields come in with a `'` at the beginning of the ID, which help it import as text. However, you have to remove that `'` to match the district ID in your gifted data. We'll do that by splitting the field into a new column that doesn't include the apostrophe.

- On the District Number column, use **Split Column** on a delimiter of `'`.
  - (An alternative way would be to Split using "x from from the right" for the right number of characters.)
- Repeat this for the School Number column.
- You might want to rename the columns to something that makes sense based on the data dictionaries. Note below that you want your District ID and Campus ID column names match their partner columns in your gifted data.

## Working the Campus data

The easiest way to start with joins is to begin with the Campus data:

- Start a new tab from the CSTUD cleaned data.
- Use **Select columns** to keep just the ID and the gifted count and percentage columns.
- Use **Join Tab** to join with the Directory data. This is where you have to make sure that the Campus ID is named the same in cleaned both data sets. For **Join Type**, choose an "Inner" join. This just keeps matching records.[^1]
- Choose to include the school name and district name into you data.

Now you can continue on your quest to find the schools with the highest GT percentage:

- Filter your data to include only schools that have at least 100 GT students (the gifted count field).
- Sort by highest percentage.

There are quite a few schools with 100% GT students because they cater to them. That isn't all that interesting, but you might note how many there are. If/when you write about it, be sure to note you are only looking at schools with at least 100 gifted students identified.

## Working with District data

For the district data, if we join directly to the Directory data we'll get multiple matches for each district, as many as there are schools in that district. To solve this, we first have to create a "District Directory" where there is one row for each district.

- Start a new tab from the Directory data and call it "Dist Directory" or something like that.
- Use **Select columns** get keep just the District ID and District Name columns.

You'll notice that the same district is repeated over and over. This is because there were multiple schools in the data. You can fix this with Deduplicate.

- Use **Deduplicate** to remove all the repeated rows.

Now it it is time to start a new tab with the cleaned DSTUD data and join with your cleaned district directory.

- Create a new tab, and use "Start from tab" and use the cleaned DSTUD data.
- Use **Join tab** to join with the district directory you just created. Bring over the district name column.

Now you can sort the data to get the districts with the hightest GT percentage.

- **Sort** by the gifted percentage in descending order.

Note that the Leander ISD is near the top of the list. That is a local district, and worth writing about in your data drop.

## Look further into Leander

Use the same techniques you used to find AISD schools to instead find Leander ISD schools. How do their schools compare to AISD?

## Turning in your work

With this assignment I expect two things:

- A very short "story" that outlines the answers to the questions posed above. i.e., sentences that explain your findings, written as a short news story/data drop. Three sentences as the most.
- Share your Workbench project with my email and submit the private link as a comment in the assignment.

[^1]: There are some campus numbers in the gifted data that have no match in the directory data. By using Inner join, we can exclude those schools. If we were doing this for publication, we would want to understand which schools don't match and track them down. There are 89 such schools in the 2018 data.

## Ignore this

A [link just for me](https://app.workbenchdata.com/workflows/16608/).