# Gifted students

The goal of this assignment is to use TEA data to find out which Texas school districts serve the most "gifted and talented" students.

Serving special populations of students (like GT, ESL or Special Education) cost districts money. So a story might explore the impact on a district that must serve a higher population of GT students?

The data comes from the Texas Education Agency. You need two things: The statewide district download for **Student: Enrollment by Program**, and a Directory file of all the district and campus names.

## Enrollment by Program data

To download this file, go to Texas Academic Performance Reports, or [TAPR](https://tea.texas.gov/perfreport/tapr/index.html) and follow these links:

- **2017–18 TAPR** or the most recent year available.
- **Data Download**
- **TAPR Data in Excel (Rates Only)**
- **District Download**, then Continue
  - We may also come back to this and get **Campus Download**.
- Choose **Student information**, then Continue
- Change the Format to **Comma delimited**
- Select **Student: Enrollment by Program**
- Click Download. You should get a file called `DSTUD.dat`.

Repeat the steps above but for the **Campus Download**. The file should be `CSTUD.dat`.

You'll also want to reference the [district](https://rptsvr1.tea.texas.gov/perfreport/tapr/2018/xplore/dstud.html) and [campus](https://rptsvr1.tea.texas.gov/perfreport/tapr/2018/xplore/cstud.html) data dictionary so you know what each column is.

If you use a code editor to inspect either file you'll see there are no district or school names in the data, only IDs. We will need a companion file to give us the names.

## District and campus directory

- The **Directory** that lists all school campus information can be found on [AskTED](http://tea4avholly.tea.state.tx.us/tea.askted.web/Forms/Home.aspx) at the link titled "Download School and District File". (There is also a copy in this repo.) It has the district ID that matches your program data as well as the district name and other information about districts and campuses.

## Assignment rubrics

- [Rubric for Workbench](rubric-wb.md)
- [Rubric for R](rubric-r.md)
