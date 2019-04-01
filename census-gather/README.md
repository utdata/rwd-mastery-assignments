# Census gather practice

This lesson actually refactors lessons you've already completed from the Reporting with Data in R book. Before completing this, make sure you've done:

- [Practice assignment: Import census](https://utdata.github.io/rwd-class/import.html#practice-assignment-import-census)
- [Practice assignment: Clean census names](https://utdata.github.io/rwd-class/columns.html#practice-assignment-clean-census-names)
- [Practice assignment: Transforms on census](https://utdata.github.io/rwd-class/transform.html#practice-assignment-transforms-on-census)

## What is refactoring

Refactoring is when you rewrite code to make it more efficient, usually because you've learned a better way to do something or you've found that you can reuse your code for more than one purpose.

In this case, in our [census transforms](https://utdata.github.io/rwd-class/transform.html#practice-assignment-transforms-on-census) lesson, we had to repeat a bunch of code chunks to find similar data: The county with the highest population of a given race.

## The new challenge

Open your existing Census project, open the "explore" notebook and run it. As part of this project, you should have a data frame that has a column for percentage of each race, like "black_prc". You may have named it differently.

Your goal is to use select, gather, group and filter to efficiently find the county that has the highest percentage of each race.

Some hints:

- Use `select()` to start with just the geography and each of your percent columns.
    - The function [`ends_with()`](https://www.rdocumentation.org/packages/dplyr/versions/0.5.0/topics/select_helpers) may be able to help you if you named your percent columns consistently.
- Use `gather()` to create a key column for race and a value column for the percentages.
- Use `group_by()` to group by the race, so the following function will apply to that.
- Use `filter()` to find the highest (or max) value in your percentage column. Since you've grouped by race, it will find it fore each race. Hint: Use [`max()`](https://www.rdocumentation.org/packages/rapportools/versions/1.0/topics/max) inside your filter.

