# Homework5_Scheduler
User story:
AS AN employee with a busy schedule
I WANT to add important events to a daily planner
SO THAT I can manage my time effectively


Criteria:
GIVEN I am using a daily planner to create a schedule
WHEN I open the planner
THEN the current day is displayed at the top of the calendar
WHEN I scroll down
THEN I am presented with timeblocks for standard business hours
WHEN I view the timeblocks for that day
THEN each timeblock is color coded to indicate whether it is in the past, present, or future
WHEN I click into a timeblock
THEN I can enter an event
WHEN I click the save button for that timeblock
THEN the text for that event is saved in local storage
WHEN I refresh the page
THEN the saved events persist


My Process:

1. I started off with the html to have a framwork of the planner.

2. started with a row which included three columns one for the time block, one for the textarea so that the user can input their activities and the last colum being the save button.

3. this same row was copied 8 more times under the first one but changing the time block text with increments of one hour starting from 9AM - 5 PM.

4. Then I added appropriate css features to make the planner look visually appealing but also keep each column distinct. an icon was used for the save button from font awsome.

5. Finally after the css was done went on to the JS. 

6. firstly added variables to set the current date in the jumbotron by using moment.js

7. then went on making a function called hourIndicator() which shows which time block is the present time which is the past and which is the future. This was acheived by using a for loop and acquiring the values attribute from each time-block looping through them and if the value was greater than the current hour than the classList of future was added, if it was less than past and thus if it equaled eachother it was given the present class. The three classes can be distinguished by the background color that was already set through the css.

8. Then the saveInfo function was made, with each save button in the html a onclick attribute was added so that if those buttons were pressed it will call the saveInfo() function.

9. this function again usues localStorage to store the activities and the time corresponding to that activity.

10. Finally the function displayInfo was made this also uses localStorage but the getItem method to pull the information from the local storage and display them in the textarea.

