# Special Education student change

The goal of this assignment is to use TEA data to find out which schools in Austin ISD have the most growth in Special Education students in the past five years.

In 2016, the Houston Chronicle published a multi-part series called [Denied](https://www.houstonchronicle.com/denied/1/) that outlined how a TEA policy started in 2004 would force an audit of schools with more than 8.5% of their students their Special Education students. From their story:

> Over a decade ago, the officials arbitrarily decided what percentage of students should get special education services — 8.5 percent — and since then they have forced school districts to comply by strictly auditing those serving too many kids.

> Their efforts, which started in 2004 but have never been publicly announced or explained, have saved the Texas Education Agency billions of dollars but denied vital supports to children with autism, attention deficit hyperactivity disorder, dyslexia, epilepsy, mental illnesses, speech impediments, traumatic brain injuries, even blindness and deafness, a Houston Chronicle investigation has found.

> More than a dozen teachers and administrators from across the state told the Chronicle they have delayed or denied special education to disabled students in order to stay below the 8.5 percent benchmark. They revealed a variety of methods, from putting kids into a cheaper alternative program known as "Section 504" to persuading parents to pull their children out of public school altogether.

We'll take a look at current Special Education levels in Austin ISD schools to see how many schools have gained or lost special education students, and how many are above or below the 2004 audit threshold (which was later prohibited by the Texas Legislature in 2017 following the Chronicle's reporting).

The data comes from the Texas Education Agency's Texas Academic Performance Reports. You'll download three files:

- The campus-level **Enrollment by Program** data for two school years: 2014-2015 and 2018-2019.
- The campus-level **Campus reference** from TEA's Accountability ratings data to  get the campus and district names and instructional types, which are not in the program data.

## Enrollment by Program data

To download this file, go to Texas Academic Performance Reports, or [TAPR](https://tea.texas.gov/perfreport/tapr/index.html) and follow these steps. You'll do this twice for two different years:

- Click on the **2014–15 TAPR** link.
- Go to **Data Download**.
- Go to **TAPR Data in Excel (Rates Only)**.
- Click on **Campus Download**, then Continue.
  Choose **Student information**, then Continue.
- Change the Format to **Comma delimited**.
- Select **Student: Enrollment by Program**.
- Click Download. You should get a file called `CSTUD.dat`.
- Rename this file `CSTUD_15.csv`.

> It's important that you change the file extension to `.csv` as Workbench doesn't understand `.dat`. If you can't see the file extensions, then adjust your computer. [Mac](https://support.apple.com/guide/mac-help/show-or-hide-filename-extensions-on-mac-mchlp2304/mac) | [Windows](https://www.thewindowsclub.com/show-file-extensions-in-windows).

While at the the download link page there is a link called "Student Information Reference". Click on that link and save the URL as you will need it later to understand the columns for each download.

> I've saved the links: [2015](https://rptsvr1.tea.texas.gov/perfreport/tapr/2015/xplore/cstud.html) | [2019](https://rptsvr1.tea.texas.gov/perfreport/tapr/2019/xplore/cstud.html).

Repeat the steps above but for  **2018-2019 TAPR**. Rename the file `CSTUD_19.csv` and save the Student Information Reference link.

If you inspect either file you'll see there are no school or district names in the data, only IDs. We will need a companion file to give us the school names.

## Campus info from Accountability ratings

The TAPR campus information data does not include any fileds to indicate if a school is disciplinary school, part of the juvenile justice department or otherwise an alternative school. To get data with the campus and district names that do have these values, we have go to TEA's [Accountability ratings](https://rptsvr1.tea.texas.gov/perfreport/account/2019/download.html) and download the Campus-level Accountability Summary for "Campus Flag Characteristics" along with the campus and district names.

- Go to the TEA's [Accountability ratings](https://tea.texas.gov/Student_Testing_and_Accountability/Accountability/State_Accountability/Performance_Reporting/2019_Accountability_Rating_System) site.
- Go down to **Data download** and click on the link.
- Choose the **Campus-level data** and **Accountability Summary** buttons and then click **Continue**.
- Change the **Format** to **Comma separated**.
- Choose the following categories:
  - Campus Flag Characteristics
  - Campus Name/Number
  - District Name/Number
- Click **Download**
- Change the filename to `CAMPRATE_19.csv` so it can be uploaded into Workbench.
- Also note the [Campus Accountability Summary Reference](https://rptsvr1.tea.texas.gov/perfreport/account/2019/download/camprate.html) which you will need later.

## Assignment rubrics

- [Rubric for Workbench](rubric-wb.md)
