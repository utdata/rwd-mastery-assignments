# Gifted students assignment

Be sure to review the [README](README.md) for important information that precedes this.

## Rubric for Workbench

The goal is to find the answer to the following questions:

- Which districts statewide have the highest percentage of students designated as Gifted and Talented (GT students)?
- Which campuses state have the highest percentage of GT students? Filter to those with at least 100 students designated?
- Rank schools in AISD by the highest percentage of GT students.

## Special considerations

Once past the hassle of downloading the data, there are still some challenges to getting the answers above. Here are some things to consider or know:

- On the downloaded files, you have to change the filename extention `.dat` to `.csv` before they will import into Workbench.
- Since the Student and District data have just IDs instead of names of schools or districts, you'll have to join them with the Directory data. To do that you have to take special care with those ID columns, which are supposed to start with zeros. In the District file, the `CAMPUS` column is supposed to be text with the IDs starting with one or more zeros, like `001902`. There is no Workbench function to fix that (as of yet), but since it is built on Python's Pandas package, we can use some use python code to fix this. Create a new Python block and add the following for the District data:

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

- For the Directory data, the `District Number` and `School Number`fields come in with a `'` at the beginning of the ID, which keeps it as text. However, you have to remove that before they will join properly. You can do that by using **Split Column** on the `'`.
- You might want to rename columns the columns to something that makes sense based ont he data dictionaries.
- When working on the Directory data to get list of the Districts Names, you'll want to select just the ID and name columns, then use **Deduplicate** to get a joinable list that lists each district just once.
- When you are working on Directory data for School names, you don't need Deduplicate, but you still probably want to select only the ID and School names before you join.

Be sure to check the Canvas assignment for any further instructions.