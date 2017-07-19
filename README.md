# Titanic Data Visualization

## Summary

The sinking of the RMS Titanic in her maiden voyage is one of the most infamous shipwrecks in history. The Titanic dataset has information about 891 people, giving some basic information about them , like their Age, Sex, Class ,the fare they paid and most importantly if they survived the disaster or no. In this visualization I  represented the counts of people survived (1) and not survived (0) across age groups and further classified each Age group across Sex and Class. From the total 891 people on record, only 342 survived and rest of 549 were dead. The visualization shows distribution of these counts across different categories.

The few observations vivid from the visualization is as follows:

Pclass 3 had the highest count of people and their death count was very high too, shown by the tall orange bars. In Pclass 2 most of the women and the children survived and the men did not survive. Pclass 1, denoted by blue, had the highest advantage and made the significant portion of the young and Adult who survived. But seniors in Pclass 1 do not seem to have that advantage(which could be voluntary too)
The visualization suggests that women and children in Pclass 1 and 2 had the highest odds of survival. Pclass 3 had the least likelihood across all age categories and across both Sex. These observations are limited by the completeness of the data which shows a significant number of records with unspecified Age.


## Design

I used bar chart to show counts of survival across each age category. I used color as visual enconding to represent Pclass for each category separately for survived 0 and survived 1. And each Pclass value is divided by a line to separate counts for male and female.

*The code for the first visualization is found in index.html. After feedback-1 and feedback-2, I made the following changes to the visualization and second visualization is saved in index\_up1.html*

1>Displayed the age category boundaries alongside each category name.
2>Sorted the Age category by the age values rather than alphabetically.
3>Added another visualization displaying the same data in percentage format.
4>Added title to the visualization.

*After feedback-3 I made the following changes and saved it in index\_up2.html*

1> Dropped the graph showing percentages and retained only the visualization with Passenger Counts
2> Fixed the Legend and added the legend title "Passenger Class"

*After feedback-4 and feedback-5 I made the following changes and saved it in updated file index\_up3.html*

1> Made the visualization explanatory by writing about the key observations from the visualization by narrating the story.
2> Removed the grid lines from the visualization. It increased the visual appeal and also made the line in each bar separating male and female data prominent enough to observe. Also this justifies not using the color hues to separate male and female data in the bar chart.
3> Changed the y axis label to "Passenger Counts"
4> Customized the tooltip text to show the Status verbally as "Survived"/"Died" instead of 1/0.

*After feedback-6 I made the following changes and saved it in updated file index\_up4.html*

1> Labelled individual bars with the status "Dead" or "Survived"
2> Fixed the error in tooltip text that would show in the console.
3> Moved the position of the tooltip box from default position of top left to alongside the bar that is pointed.
4> Used the bootstrap css to enchance the visual appeal of the visualization.

*The following changes were made to the data file after downloading and after various feedbacks*

1> I Added a column called "Age\_Category" and binned them using following criteria.
"Child" for 0-12,"Young" for 13-29,"Adult" 30-59,"Senior" for 60+,"Unspecified" for records with Age not specified.

2> I Added a column of all 1s called "Count" to aid in counting sum of people survived in individual categories.

3> After feedback-1,I changed Age\_Category values to show the age bracket they fall too. Eg: "Child" was changed to "Child 0-12" and so on. The updated data file is named as titanic\_data\_up1.tsv

4> After feedback-6, I dropped the Age\_Category "Unspecified" by deleting the records with missing Age values instead.
The updated file is named as titanic\_data\_up4.tsv

## Feedbacks

I received the following feedback from friends from various sources. I made the necessary changes to the visualization as mentioned in the design section.

### Feedback 1

What do you notice in the visualization?
Counts of people in every age group from titanic is represented in the stacked bar chart. Each bar is color coded for Pclass and further separated by a line for male and female

What questions do you have about the data?
I want to know the exact bracket in Age\_Category. What ages is classified as Adult and Young etc.

What relationships do you notice?
The death count is largest for young and specifically the males from pclass 3. For children who did not survive, most seem to be from pclass 3 too. Survival count is largest for Adults in pcalss 1.   

What do you think is the main takeaway from this visualization?
Survival chances would be better for people in Pclass1 and and very low in pclass 3. There were fewer people in Pclass 2 compared to pclass 3 and pclass 1.

Is there something you don’t understand in the graphic?
The visualization seems nice and self explanatory. Though it would be nice to see data in percent format too.

### Feedback 2

The overall visualisation seems very intuitive. Though I'd recommend few changes.

1>Change the order of the Age categories to follow natural order of smallest to oldest rather than alphabetical as it is now.
2>Explicitly specify in the visualization what survived 0 vs survived 1 means.
3>Displaying percentages alongside the count will give greater insight into the visual.
4>Also do add a title to your visualization. Although it may seem trivial, it is the vital aspect of any data visualization.


### Feedback 3

Hi there,

I would say that you are trying to put too much data into a single visualization. Therefore it is hard to spot the relationships presented. Also, the second graph is unclear: not a good idea to use bar charts when everything adds to 100% in total (I would get rid of it altogether).

I would propose the following changes:

leaving just 1 graph with survival percentages/counts
if you want to include the counts you could try to implement a scatter plot for percentages and use bubble sizes to reflect on counts. Or vice versa: scatter plot for counts and sizes for percentages.
Fix the legend: it is not clear what 3, 2 and 1 are.
not immediately clear where female / male data is, may be add a note or a legend.
may be you could aggregate survival across gender and just focus on passenger classes.
In terms of relationships I see that middle age is much better for survival and also that the 1st class helps seniors quite a lot. But comparison between genders on the second graph is hard to read because color bars are not on the same level (not facing each other).

I hope I gave you some useful feedback and ideas for further improvement!

Regards,
Alex /Kanfibl

### Feedback 4

Hi @arundathi.ga,

Your visualization looks good. Adding a couple of points to Kanfibl,

Here are my suggestions.

The basic idea of this project is to narrate a story. You should write some summary/description in the beginning that explains about your graphs. Probably you could use the suggestions by Kanfibl for this.

It is a good idea to animate your graph. May be something like clicking on 3,2 and 1 at a time and showing the relevant data?

Hope that helps.

### Feedback 5

colour coding - it is great that you've added a line to break up male and female passengers but I really don't feel this is clear enough. Could you not use further colour coding to distinguish the bars further? If you don't want to use six distinct colours, you could choose a darker hue for male and a lighter hue for female across the each class? This may mean having two legends - one for male, one for female? Colorbrewer is a great place to start for custom colours. Here's a link for assigning custom colours in dimple. Another solution would be to remove Sex from this particular visualisation and stick to Age v Passenger Class.

Would "Passenger Count" be more informative than "Count"?

did you know you can customize the tooltip text? This way you wouldn't need to explain what 0 and 1 mean? See link here.

Might it be easier on the eye without the gridlines? See link here.

another really good touch would be to add bar labels - "Survived","Died" above each bar.

finally, is the Unspecified category relevant here? Would it not be better to delete this data for the purposes of this chart or use some further data analysis logic to reallocate these records to a different age group?

### Feedback 6

Your visualisation renders perfectly EXCEPT the tooltips. There is an error and they are appearing top left instead of by the relevant bar.

Your design choices are looking great and the changes you've implemented have made a significant difference to reader/graphic communication.

However, I still feel you could improve things further if you wish to

Since you've changed the tooltips you don't need to explain what 0 and 1 mean in the text.
I still feel it would be better to use colour coding to distinguish the male and female bars.
Again, is the Unspecified category necessary?

## Resources

https://www.kaggle.com/c/titanic
http://dimplejs.org/advanced_examples_index.html
