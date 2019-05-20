# Gifted students assignment

Be sure to review the [README](README.md) for important information that precedes this.

## Rubric for R

The goal is to build a list of districts in descending order of their percentage of gifted and talented students. Which districts have the highest percentage of GT kids?

The logical steps to do this are as follows. While I'm not telling you _how_ to do these things, do pay attention as there are many hints thrown in.

The main challenge is you have to join the directory data to the district data, based on the district ID, so you can get the district names.

- Import both data sets.
- On the directory data: This is really a list of each campus, but they all have their district information. What you need is a distinct list of the district IDs and the district names.
  - You'll notice that the ID fields in this file have a `'` at the beginning of the the text. You'll need to remove that before this data join with the district data.
    - Use `mutate()` to modify the district ID field to remove the `'`. You might use `str_replace()` to do so. (You might fix the other ID columns, as well.)
  - Select just the columns you need to work with, like district ID and name.
  - Use `distinct()` to get a list of only the unique values.
  - Save that as a data frame you can use later.
- Use `left_join()` to join the directory information into the district file. (i.e., district on the left).
- Use the data dictionary to find out which columns you need to work with. You might rename them to something more logical. Use `select()` and `arrange()` to create your list of districts with the highest GT rates at the top.

## Other Enrollment by Program data

The GT numbers are not the only ones in this file. You might look at the data and the data dictionary to see what else might be interesting.

You can get similar Enrollment by Program data at the campus level from the same TAPR system, and use the same Directory file to find the School names. The 2017-18 data is included in this repo.

## TAPR is a wealth of info

You may have noticed there is a ton of other school information in the TAPR system. It is well worth tapping for context for education stories or exploring for new story ideas.
