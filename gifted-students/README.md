# Gifted students

The goal of this assignment is to us TEA data to find out which Texas School districts serve the most "gifted and talented" students.

The story idea is programs such as this cost money. What is the impact on a district that must serve a higher population of GT students?

The data comes from the Texas Education Agency. You need two things: The statewide district download for **Student: Enrollment by Program**, and a Director file of all the district and campus names.

## Enrollment by Program data

To download this file, go to Texas Academic Performance Reports, or [TAPR](https://tea.texas.gov/perfreport/tapr/index.html) and follow links:
  - **2017–18 TAPR** or the most recent available.
  - **Data Download**
  - **TAPR Data in Excel (Rates Only)**
  - **District Download**, then Continue
  - Choose **Student information**, then Continue
  - Change the Format to **Comma delimited**
  - Select **Student: Enrollment by Program**
  - Click Download

Once downloaded, inspect the file. You'll see there are no district names in the data, only a district ID. We will need at companion file to give us the names.

You'll also want to reference this [data dictionary](https://rptsvr1.tea.texas.gov/perfreport/tapr/2018/xplore/dstud.html) so you know what each column is.

## District and campus directory

- The [Directory](data-raw/Directory.csv) can be found on [AskTED](http://tea4avholly.tea.state.tx.us/tea.askted.web/Forms/Home.aspx) at the link titled "Download School and District File".

## Goals and hints

The goal is to build a list of districts in descending order of their gifted and talented percentage. Which districts have the highest percentage of GT kids?

The logical steps to do this are as follows. While I'm not telling you _how_ to do these things, do pay attention as there are many hints thrown in.

To do this, you have to join the directory data to the district data, based on the district ID, so you can get the names.

- Import both data sets
- On the directory data: This is really a list of each campus, but they all have their district information. What you need is a distinct list of the district IDs and the district names.
  - Select just the columns you need to work with
  - Use `distinct()` to get a list of only the unique values.
  - Save that as a data frame you can use later.
- On the district data: You'll notice that the district ID in this file has a `'` at the beginning of the field.
  - Use `mutate()` to modify the district ID field to remove the `'`. You might use `str_replace()` to do so.
- Use `left_join()` to join the directory information into the district file. (i.e., district on the left).
- Use the data dictionary to find out which columns you need to work with. You might rename them to something more logical. Use `select()` and `arrange()` to create your list of districts with the highest GT rates at the top.

## Other Enrollment by Program data

The GT numbers are not the only ones in this file. You might look at the data and the data dictionary to see what else might be interesting.

You can get similar Enrollment by Program data at the campus level from the same TAPR system, and use the same Directory file to find the School names. The 2017-18 data is included in this repo.

## TAPR is a wealth of info

You may have noticed there is a ton of other school information in the TAPR system. It is well worth tapping for context for education stories or exploring for new story ideas.
