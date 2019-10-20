# Vaccination exemptions by county

Texas law allows for an exemption from immunizations for reasons of conscience, including a religious belief. A student's parent or guardian submits an official DSHS affidavit form to the child's school.

This study looks at how the use of exemptions has changed over time by county.

## Preparation of data

- The file [Printable Version of 2010-2018 Conscientious Exemptions Data for Texas (PDF)](https://www.dshs.texas.gov/uploadedFiles/Content/Prevention_and_Preparedness/immunize/coverage/schools/Exemptions%20by%20County%202010-2018.pdf) was found and downloaded from the Texas Department of State Health Services [Conscientious Exemptions Data - Vaccination Coverage Levels](https://www.dshs.texas.gov/immunize/coverage/Conscientious-Exemptions-Data.shtm). There is a copy in `/data`.
- The PDF was run through [Cometdocs](https://www.cometdocs.com) to convert to an Excel document, which is also saved in `/data/Exemptions by County 2010-2018.xlsx`.
- The Excel spreadsheet was imported into a Workbench workflow [Vaccination exemption by county, 2011-2019](https://app.workbenchdata.com/workflows/36382). The data was cleaned up, reshaped and a date-centric column added. It was exported as `data/exemptions_county.csv`.

## Assignments

- [rubric-tableau](rubric-tableau.md)
