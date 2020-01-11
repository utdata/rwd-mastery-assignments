# Special Education student change

The goal of this assignment is to use TEA data to find out which schools in Austin ISD (and the state in general) have the most growth in Special Education students in the past five years.

Serving special populations of students (like Gifted and Talented, English as a Second Language or Special Education) cost districts money. So a story might explore the impact on a school that serves a high population of Special Education students.

The data comes from the Texas Education Agency. You need three things:

- The statewide district download for **Student: Enrollment by Program** for years 2014 and 2019
- A Directory file of all the district and campus names, which are note included in the program data.

## Enrollment by Program data

To download this file, go to Texas Academic Performance Reports, or [TAPR](https://tea.texas.gov/perfreport/tapr/index.html) and follow these steps. You'll do this twice for two different years:

- Click on the **2014–15 TAPR** link.
- Go to **Data Download**
- Go to **TAPR Data in Excel (Rates Only)**
- Click on **Campus Download**, then Continue
  Choose **Student information**, then Continue
- Change the Format to **Comma delimited**
- Select **Student: Enrollment by Program**
- Click Download. You should get a file called `CSTUD.dat`.
- Rename this file `CSTUD_2015.csv`.

> It's important that you change the file extension to `.csv` as Workbench doesn't understand `.dat`. If you can't see the file extensions, then adjust your computer. [Mac](https://support.apple.com/guide/mac-help/show-or-hide-filename-extensions-on-mac-mchlp2304/mac) | [Windows](https://www.thewindowsclub.com/show-file-extensions-in-windows).
> Also: At the download link page there is a link called "Student Information Reference". Click on that link and save the URL as you will need it later to understand the columns for each download. The links: [2015](https://rptsvr1.tea.texas.gov/perfreport/tapr/2015/xplore/cstud.html) | [2019](https://rptsvr1.tea.texas.gov/perfreport/tapr/2019/xplore/cstud.html).

Repeat the steps above but for the **2018-2019 TAPR**. Rename the file  `CSTUD_2019.csv`.

If you use a code editor to inspect either file you'll see there are no district or school names in the data, only IDs. We will need a companion file to give us the names.

## District and campus directory

- The **Directory** that lists all school campus information can be found on [AskTED](http://tea4avholly.tea.state.tx.us/tea.askted.web/Forms/Home.aspx) at the link titled "Download School and District File". (There is also a copy in this repo.) It has the district ID that matches your program data as well as the district name and other information about districts and campuses.

## Assignment rubrics

- [Rubric for Workbench](rubric-wb.md)
