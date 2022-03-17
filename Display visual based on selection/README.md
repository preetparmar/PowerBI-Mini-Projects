# Display Visuals Based On Selection

![Display Visuals Based On Selection](https://github.com/preetparmar/PowerBI-Mini-Projects/blob/main/Display%20visual%20based%20on%20selection/Resources/display-visual-based-on-selection.gif)

## Problem

Sometimes, we only need to show a visual when certain filters are selected. One example is a KPI Card. A KPI card by default selects the last month from the selected date range. So if we need to use the KPI visual to compare the selected month with the previous month, we need to have only one month selected.

## Solution

The general idea is to create a visual which will show the desired text explaining the condition, which should only be visible when there is no month selected or more than one month is selected.

### General Steps

- Create a measure which shows the desired text based on the condition
  - Based on the condition, it will either return "" (blank) or "Please select a single month to view this visual"
  - This measure then can be used as a card visual above our KPI visual
- Create a measure which can be used as a function for the background property of our overlaying card visual
  - Based on the condition, it will either return "#FFFFFF00", which is White colour with 100% transparency, so that our underlying visual is visible or it will return "White", covering the underlying visual

---

For all of my projects you can visit my website [here](https://preetparmar.com/projects).

Also you can visit a blog article on this project [here](https://blog.preetparmar.com/display-visuals-based-on-selection/).
