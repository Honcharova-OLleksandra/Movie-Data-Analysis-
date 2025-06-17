# Movie-Data-Analysis
## Table of Content

 - [Project Overview](#project-overview)

 - [Data Sources](#data-sources)

 - [Results and Findings](#results-and-findings)

### Project Overview
In this project, we’re taking a closer look at how movies performed from 2012 to 2017. By digging into the data, we want to spot trends, see what stands out, and get a better feel for how the movie industry changed over those years. The idea is to use what we find to make smart, data-based suggestions.

### Data Sources

Movie Data: 

The primary dataset used for this analysis is the "Movie Data.xmls" file, containing detailed information about each movie's performance, actors, directors etc.


### Tools
- Power Query - I used Power Query for Data Cleaning
- Excel, Pivot Tables - I used them for Data Analysis, Creating reports and Visualizations

### Data Cleaning ad Preparation
To get things started, we went through a few key steps to get the data ready for analysis:
- Loaded the data and took a first look to understand what we were working with.
- Fixed any issues, such as errors or missing values, to make sure everything was accurate.
- Cleaned and formatted the data so it’s neat and consistent.
  
After all that, the cleaned-up Excel file is ready to go and can be downloaded here: 
[Movies Data.xlsx](https://github.com/user-attachments/files/20782661/AANPLdFKQ5qgmO5lWys6_Movies.Data.Ready.for.Dashboard.xlsx)

### Results and Findings
In results we can see a dashboard that shows the best and worst profitable movies and the top 5 in budget and box office revenue, plus the top 5 actors with revenue.

![Appple TV dashboards](https://github.com/user-attachments/assets/57707fbc-231c-434a-ba93-5a14a8d1c7c4)

#### M Language 

One of interesting features I was working with was a specific code for Grouping in M language which enable me to Combine genres together for further analysis.

```

= Table.Group(#"Sorted Rows1", {"Movie Title"}, 
  {{"Combined Genre", each Text.Combine([Concat Genre], " / "), type text},
  {"AllData", each _, type table [Movie Title=nullable text, Release Date=nullable date, Wikipedia URL=nullable text,
    Concat Genre=nullable text, Director=nullable text, Actor First=nullable text, Actor Second=nullable text,
     Actor Third=nullable text, Actor Fourth=nullable text, Actor Fifth=nullable text, #"Budget ($)"=nullable number,
    #"Box Office Revenue ($)"=nullable number]}}

```

### Excel Dashboard
Can be downloaded here [Dashboards](https://github.com/user-attachments/files/20783038/Honcharova_Homework10.xlsx)
