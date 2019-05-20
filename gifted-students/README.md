# Gifted students

The goal of this assignment is to use TEA data to find out which Texas school districts serve the most "gifted and talented" students.

Serving special populations of students (like GT, ESL or Special Education) cost districts money. So a story might explore the impact on a district that must serve a higher population of GT students?

The data comes from the Texas Education Agency. You need two things: The statewide district download for **Student: Enrollment by Program**, and a Directory file of all the district and campus names.

## Enrollment by Program data

To download this file, go to Texas Academic Performance Reports, or [TAPR](https://tea.texas.gov/perfreport/tapr/index.html) and follow these links:
  - **2017–18 TAPR** or the most recent available.
  - **Data Download**
  - **TAPR Data in Excel (Rates Only)**
  - **District Download**, then Continue
  - Choose **Student information**, then Continue
  - Change the Format to **Comma delimited**
  - Select **Student: Enrollment by Program**
  - Click Download

Once downloaded, inspect the file. You'll see there are no district names in the data, only a district ID. We will need at companion file to give us the names.

You'll also want to reference the [data dictionary](https://rptsvr1.tea.texas.gov/perfreport/tapr/2018/xplore/dstud.html) so you know what each column is.

## District and campus directory

- The **Directory** that lists all school campus information can be found on [AskTED](http://tea4avholly.tea.state.tx.us/tea.askted.web/Forms/Home.aspx) at the link titled "Download School and District File". (There is also a copy in this repo.) It has the district ID that matches your program data as well as the district name and other information about districts and campuses.

## Rubrics

- [Rubric for Workbench](rubric-wb.md)
- [Rubric for R](rubric-r.md)