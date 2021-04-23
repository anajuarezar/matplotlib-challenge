# matplotlib-challenge

Matplotlib Homework - The Power of Plots

The first thing we have to do is import the dependencies, then we need to import the data. In order to do this we create a path then we open it as a dataframe. 
Since we have two dataframes, we need to merge them. Because there are have not the same information, we will use the outer merging using the Mouse ID as the merging point. We use
head() function to scan the complete information available. 
Our next task is to drop the duplicates and clean the df, in order to do this we must first count all the mice, to do this we use nunique function. We have 249 mice. In order to find
that mouse, we use drop.duplicate and subset to find the mouse that is repeated in both columns. We found is the g989 mouse. To drop it, we use loc and the specifications of all but
specific mouse. Once we have the clean df, we count the mice once again to check if we were successful. We got 248 mice.
The next task is to create a df the statistical summary by drug regimen. To do this we first need to group by drug regimen. Once this is done, we use the functions mean(), median(),
std() and sem() to create it. We use concat to join them into a df and we give it a format. Later, we must use the aggregation method to create that same df in one single line. 
Now, it is time to plot. We need to make a bar plot using pandas to show the number of measurements by drug regimen. We used the grouped df from before to select the mouse id and count 
them. Once we have this, we create a bar plot and give it the format we want. The following task is to create the same bar plot using matplotlib. 
Next, we must create a pie bar for the mice count by sex, once again we group clean df by sex and use pandas to plot it. Similar to the previous task, we creat the pie plot using 
matplotlib.
After this, we have to calculate the final tumor volume of each mouse across four of the treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. To do this, we first need
to group by Mouse ID and Drug Regimen and use the max function to find the lastest timepoint for each mouse. To merge this new df we need to reset the index so we are able to join
them by the index. To merge them as we want (by the new index of the lastest timepoint) we use right merge. Now it's time for the loops. We create a list with the drugs we are going
to use, then an empty list. The loop will go through each drug in the drug list and obtain the quartiles, the iqr, the upper and lower bound. We print the results we need.
After this we must use the box plot to find the outliers and the distribution of the final volume of the tumor.
Now, it is time for the correlation and linear regression. To begin, we use loc once again to select only the information of the drug we need. We use loc again to select a mouse, we
used the first one. Using this df we generate the line plot and give the format we desire. 
Our next task needs the previous df, we groupby mouse ID and obtain the mean of the volume of the tumor and the weight of the mouse. We use this df to create a scatter plot, we obtain
the linear regression to analyse if the correlation is postive or negative. And finally, we obtained the Pearson Coefficient. 
