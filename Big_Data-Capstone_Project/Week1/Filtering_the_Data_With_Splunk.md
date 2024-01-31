# Filtering the Data With Splunk

## Filtering

We can filter data sets to find events that meet a specific condition or set of conditions.

**Example 1:** The file user-sessions.csv describes when users start and stop playing the game and when they advance levels. For a user id 1017, what platform(s) were used?

source="user-session.csv"  userId=1017 | stats count by platformType
    
Result is: iphone

**Example 2:** Which users completed level 2 while playing on an android device?

source="user-session.csv" sessionType=end teamLevel=2 platformType=android | table userId | sort num(userId) 

Result is: there are 182 users, with ids 1, 16, 21, 62, 65, 66, 68, etc.