<h1>Project Description</h1>
You work at a startup that sells food products. You need to investigate user behavior for the company's app.
First study the sales funnel. Find out how users reach the purchase stage. How many users actually make it to this stage? How many get stuck at previous stages? Which stages in particular?
Then look at the results of an A/A/B test. (Read on for more information about A/A/B testing.) The designers would like to change the fonts for the entire app, but the managers are afraid the users might find the new design intimidating. They decide to make a decision based on the results of an A/A/B test.
The users are split into three groups: two control groups get the old fonts and one test group gets the new ones. Find out which set of fonts produces better results.
Creating two A groups has certain advantages. We can make it a principle that we will only be confident in the accuracy of our testing when the two control groups are similar. If there are significant differences between the A groups, this can help us uncover factors that may be distorting the results. Comparing control groups also tells us how much time and data we'll need when running further tests.
You'll be using the same dataset for general analytics and for A/A/B analysis. In real projects, experiments are constantly being conducted. Analysts study the quality of an app using general data, without paying attention to whether users are participating in experiments.

<h2>Description of the data</h2>
<ul><li>Each log entry is a user action or an event</li>
<li>EventName — event name</li>
<li>DeviceIDHash — unique user identifier</li>
<li>EventTimestamp — event time</li>
<li>ExpId — experiment number: 246 and 247 are the control groups, 248 is the test group</li></ul>

<h2>Instructions for completing the project</h2>
Step 1. Open the data file and read the general information<br><br>
Step 2. Prepare the data for analysis
<ul><li>Rename the columns in a way that's convenient for you</li>
<li>Check for missing values and data types. Correct the data if needed</li>
<li>Add a date and time column and a separate column for dates</li></ul></li></ul>
Step 3. Study and check the data</li>
<ul><li>How many events are in the logs?</li>
<li>How many users are in the logs?</li>
<li>What's the average number of events per user?</li>
<li>What period of time does the data cover? Find the maximum and the minimum date. Plot a histogram by date and time. Can you be sure that you have equally complete data for the entire period? Older events could end up in some users' logs for technical reasons, and this could skew the overall picture. Find the moment at which the data starts to be complete and ignore the earlier section. What period does the data actually represent?</li>
<li>Did you lose many events and users when excluding the older data?</li>
<li>Make sure you have users from all three experimental groups.</li></ul> 
Step 4. Study the event funnel
<ul><li>See what events are in the logs and their frequency of occurrence. Sort them by frequency.</li>
<li>Find the number of users who performed each of these actions. Sort the events by the number of users. Calculate the proportion of users who performed the action at least once.</li>
<li>In what order do you think the actions took place. Are all of them part of a single sequence?</li> 
<li>You don't need to take them into account when calculating the funnel.</li>
<li>Use the event funnel to find the share of users that proceed from each stage to the next. (For instance, for the sequence of events A → B → C, calculate the ratio of users at stage B to the number of users at stage A and the ratio of users at stage C to the number at stage B.)</li>
<li>At what stage do you lose the most users?</li>
<li>What share of users make the entire journey from their first event to payment?</li></ul>
Step 5. Study the results of the experiment
<ul><li>How many users are there in each group?
<li>We have two control groups in the A/A test, where we check our mechanisms and calculations. See if there is a statistically significant difference between samples 246 and 247.
<li>Select the most popular event. In each of the control groups, find the number of users who performed this action. Find their share. Check whether the difference between the groups is statistically significant. Repeat the procedure for all other events (it will save time if you create a special function for this test). Can you confirm that the groups were split properly?</li>
<li>Do the same thing for the group with altered fonts. Compare the results with those of each of the control groups for each event in isolation. Compare the results with the combined results for the control groups. What conclusions can you draw from the experiment?</li>
<li>What significance level have you set to test the statistical hypotheses mentioned above? Calculate how many statistical hypothesis tests you carried out. With a statistical significance level of 0.1, one in 10 results could be false. What should the significance level be? If you want to change it, run through the previous steps again and check your conclusions.</li></ul>
