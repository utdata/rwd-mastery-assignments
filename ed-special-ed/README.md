# Special education student change over time

In 2016, the Houston Chronicle published a multi-part series called [Denied](https://www.houstonchronicle.com/denied/1/) that outlined how a TEA policy started in 2004 would force an audit of schools with more than 8.5% of their students in Special Education. The story was a Pulitzer Prize finalist. From their story:

> Over a decade ago, the officials arbitrarily decided what percentage of students should get special education services — 8.5 percent — and since then they have forced school districts to comply by strictly auditing those serving too many kids.

> Their efforts, which started in 2004 but have never been publicly announced or explained, have saved the Texas Education Agency billions of dollars but denied vital supports to children with autism, attention deficit hyperactivity disorder, dyslexia, epilepsy, mental illnesses, speech impediments, traumatic brain injuries, even blindness and deafness, a Houston Chronicle investigation has found.

> More than a dozen teachers and administrators from across the state told the Chronicle they have delayed or denied special education to disabled students in order to stay below the 8.5 percent benchmark. They revealed a variety of methods, from putting kids into a cheaper alternative program known as "Section 504" to persuading parents to pull their children out of public school altogether.

Following the Chronicle's reporting, the Texas Legislature in 2017 [unanimously banned](https://www.chron.com/news/houston-texas/houston/article/Legislature-unanimously-approves-bill-designed-to-11134046.php) using a target or benchmark to measure how many students a district or charter school enrolls in special education.

## Our goal

The goal of this assignment is to use TEA data to find out which schools in Austin ISD have the most growth in special education students from before the change (2015) and the most recent year (2019).

We will calculate how many schools were above the 8.5% threshold in 2014 to how many would be now. That answer can lead us down reporting paths to quantify the result of the law's change.

The data comes from the Texas Education Agency's Texas Academic Performance Reports. You'll download three files:

- The campus-level **Enrollment by Program** data for two school years: 2014-2015 and 2018-2019. This is two different downloads noted below.
- A **campus locations** file. This was obtained from the TEA through an open records request. This file has campus and district names and instructional types, which are not in the program data.

> You should create a project folder on your computer to save all the files into so you can find them again.

## Download Enrollment by Program data

To download this file, go to Texas Academic Performance Reports, or [TAPR](https://tea.texas.gov/perfreport/tapr/index.html) and follow these steps. You'll do this twice for two different years:

- Click on the **2014–15 TAPR** link.
- Go to **Data Download**.
- Go to **TAPR Data in Excel (Rates Only)**.
- Click on **Campus Download**, then Continue.
  Choose **Student information**, then Continue.
- Change the Format to **Comma delimited**.
- Select **Student: Enrollment by Program**.
- Click Download. You should get a file called `CSTUD.dat`.
- Rename this file `CSTUD15.csv`.

> It's important that when you change the name you change file extension to `.csv` as Workbench doesn't understand `.dat`. If you can't see the file extensions, then adjust your computer. [Mac](https://support.apple.com/guide/mac-help/show-or-hide-filename-extensions-on-mac-mchlp2304/mac) | [Windows](https://www.thewindowsclub.com/show-file-extensions-in-windows).

While at the the download link page there is a link called "Student Information Reference". Click on that link and save the URL as you will need it later to understand the columns for each download. (The links are : [2015](https://rptsvr1.tea.texas.gov/perfreport/tapr/2015/xplore/cstud.html) | [2019](https://rptsvr1.tea.texas.gov/perfreport/tapr/2019/xplore/cstud.html).)

Repeat the steps above but for  **2018-2019 TAPR**. Rename the file `CSTUD19.csv` and save the Student Information Reference link.

If you inspect either file you'll see there are no school or district names in the data, only IDs. We will need a companion file to give us the school names.

## Campus locations

To get the campus names, the TEA has a [School and District File with Site Address](http://tea4avholly.tea.state.tx.us/tea.askted.web/Forms/Home.aspx) file available, but it does not include the latitude and longitude of the schools, something that is useful for mapping. (Though we may or may not to that in this assignment.) So I requested those locations via a **public information request** and have that file available below.

Go to this page [TEA-Campus-Locations-with-Geo-2019](data/TEA-Campus-Locations-with-Geo-2019.xls) and then use the **Download** button to save the resulting `.xls` file to your computer in your project folder.

## Assignment rubrics

- [Rubric for Workbench](rubric-wb.md)

## Ignore this

- Links for the prof: [Workbench](https://app.workbenchdata.com/workflows/76665/) | [R](https://github.com/utdata/rwd-r-tea-sped-answers).
