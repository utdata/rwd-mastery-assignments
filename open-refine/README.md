# Open Refine notes

- create columns
- facet
- replace(value,"search","replace")
- common transformations
  - make uppercase
  - trim
- filter
- export

## Demos

- [Using facets](demo-facets.md)
- [Clustering](demo-facets.md)

## Case studies

### AHRQ diagnostic codes

Main challenges are:

- Original document was pdf
- Multiple pages with headers, footers
- Desired data in multiple columns

### ASH Cemetery records

In this example I don't have 


`Create new column AdmitPart based on column Date Admitted by filling 1368 rows with grel:row.record.cells["Date Admitted"].value[-1]`

### Resources

- [OpenRefine.org](https://openrefine.org/) has some demo videos
- OpenRefine's Documentation page has list of tutorials and books.

- [Tutorial course](https://courses.tranzf.org/course/view.php?id=18)
- Official OpenRefine [Documentation](https://docs.openrefine.org/)
- 
