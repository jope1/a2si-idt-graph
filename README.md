# a2si-idt-graph
This Web application is the client to the A2SI graph APIs (a2si-service-data-api & a2si-case-data-api)

Each html file uses jquery to execute an HTTP Rest request.

The HTML files use Plotly.js to build the graphs, 
the files use JQuery components to allow start and end dates to be selected, some also allow a Service Id
or CCG to be selected to filter the data selected.

The javascript allows the graphs to be redrawn after executing the query again at regular intervals.

Currently the graphs have a user defined start date and end date but an enhancement for the service graphs would be:

- Always define the end date as the current date
- Allow the user to select the start date as the number of days to show from the current date.

The query would then always show the most up to date information but would keep the same time period as the date range.
For example, a user could select to show how long in the past they wish to see data for, the graph would continually
show the most up to date data as the end date and define the start date from that and the time period defined by the 
user. 
This is particularly effective because the graphs can auto refresh, fetching up to date data at regualr intervals. 
For dashboards etc., the graphs would need no maintenance on a regular basis and would always show the most up to 
date graphs.