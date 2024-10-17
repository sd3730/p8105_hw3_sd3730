# p8105_hw3_sd3730

Context
This assignment reinforces ideas in Visualization and EDA.

Due date and submission
Due: October 14 at 11:59pm.

Please submit (via courseworks) the web address of the GitHub repo containing your work for this assignment; git commits after the due date will cause the assignment to be considered late.

R Markdown documents included as part of your solutions must not install packages, and should only load the packages necessary for your submission to knit.

Points
Problem	Points
Problem 0	20
Problem 1	–
Problem 2	40
Problem 3	40
Optional survey	No points
Problem 0
This “problem” focuses on structure of your submission, especially the use git and GitHub for reproducibility, R Projects to organize your work, R Markdown to write reproducible reports, relative paths to load data from local files, and reasonable naming structures for your files.

To that end:

create a public GitHub repo + local R Project; we suggest naming this repo / directory p8105_hw3_YOURUNI (e.g. p8105_hw3_ajg2202 for Jeff), but that’s not required
create a single .Rmd file named p8105_hw3_YOURUNI.Rmd that renders to github_document
create a subdirectory to store any local data files, and use relative paths to access these data files
submit a link to your repo via Courseworks
Your solutions to Problems 1, 2, and 3 should be implemented in your .Rmd file, and your git commit history should reflect the process you used to solve these Problems.

For this Problem, we will assess adherence to the instructions above regarding repo structure, git commit history, and whether we are able to knit your .Rmd to ensure that your work is reproducible. Adherence to appropriate styling and clarity of code will be assessed in Problems 1+ using the style rubric.

This homework includes figures; the readability of your embedded plots (e.g. font sizes, axis labels, titles) will be assessed in Problems 1+.

Problem 1
This problem uses the NY NOAA data. DO NOT include this dataset in your local data directory; instead, load the data from the p8105.datasets package using:

library(p8105.datasets)
data("ny_noaa")
The goal is to do some exploration of this dataset. To that end, write a short description of the dataset, noting the size and structure of the data, describing some key variables, and indicating the extent to which missing data is an issue. Then, do or answer the following (commenting on the results of each):

Do some data cleaning. Create separate variables for year, month, and day. Ensure observations for temperature, precipitation, and snowfall are given in reasonable units. For snowfall, what are the most commonly observed values? Why?
Make a two-panel plot showing the average max temperature in January and in July in each station across years. Is there any observable / interpretable structure? Any outliers?
Make a two-panel plot showing (i) tmax vs tmin for the full dataset (note that a scatterplot may not be the best option); and (ii) make a plot showing the distribution of snowfall values greater than 0 and less than 100 separately by year.
Problem 2
Accelerometers have become an appealing alternative to self-report techniques for studying physical activity in observational studies and clinical trials, largely because of their relative objectivity. During observation periods, the devices can measure MIMS in a short period; one-minute intervals are common. Because accelerometers can be worn comfortably and unobtrusively, they produce around-the-clock observations.

This problem uses accelerometer data collected on 250 participants in the NHANES study. The participants’ demographic data can be downloaded here, and their accelerometer data can be downloaded here. Variables *MIMS are the MIMS values for each minute of a 24-hour day starting at midnight.

Load, tidy, merge, and otherwise organize the data sets. Your final dataset should include all originally observed variables; exclude participants less than 21 years of age, and those with missing demographic data; and encode data with reasonable variable classes (i.e. not numeric, and using factors with the ordering of tables and plots in mind).

Produce a reader-friendly table for the number of men and women in each education category, and create a visualization of the age distributions for men and women in each education category. Comment on these items.

Traditional analyses of accelerometer data focus on the total activity over the day. Using your tidied dataset, aggregate across minutes to create a total activity variable for each participant. Plot these total activities (y-axis) against age (x-axis); your plot should compare men to women and have separate panels for each education level. Include a trend line or a smooth to illustrate differences. Comment on your plot.

Accelerometer data allows the inspection activity over the course of the day. Make a three-panel plot that shows the 24-hour activity time courses for each education level and use color to indicate sex. Describe in words any patterns or conclusions you can make based on this graph; including smooth trends may help identify differences.

Problem 3
Citi Bike is a bike sharing system in New York City; riders can rent pedal-powered or electric bikes from starting stations and return them to another station at their destination. Introduced in 2013, the system is immensely popular and expanded rapidly. Riders who use this system often may become “members” with lower rental rates.

This zip file contains data on rides taken on the NYC Citi Bike system. Files contain 1% of all rides with a total duration less than 4 hours in each of four months. Import, clean, and tidy these data, and describe the resulting dataset.

Produce a reader-friendly table showing the total number of rides in each combination of year and month separating casual riders and Citi Bike members. Comment on these results.

Make a table showing the 5 most popular starting stations for July 2024; include the number of rides originating from these stations.

Make a plot to investigate the effects of day of the week, month, and year on median ride duration. This plot can include one or more panels, but should facilitate comparison across all variables of interest. Comment on your observations from this plot.

There were relatively few electric Citi Bikes in 2020, but many more are available now. For data in 2024, make a figure that shows the impact of month, membership status, and bike type on the distribution of ride duration. Comment on your results.