# Aggregate Calculations Using Splunk

## Aggregate Calculations Using Splunk 

In this Reading we will review how to perform aggregate calculations using Splunk. We will run these calculations on the Catch the Pink Flamingo data sets to compute several statistics. By the end of this Reading, you will be able to:

1. Perform aggregation operations such as sum and average
2. Locate the types of aggregations that are supported by Splunk

### Part 1. Simple aggregation

The file game-clicks.csv has a line for each click when a user plays the game. The field isHit is either 1 or 0 denoting if the click was on a flamingo. We can calculate the hit ratio by computing the average of this field:

source="game-clicks.csv" | stats avg(isHit)

The result is: 0.110323

The lines in buy-clicks.csv describe a user purchasing an item and the field price says how much the item costs. Let’s find the minimum and maximum prices, and the total amount of money spent by users.

**Minimum price:**

source="buy-clicks.csv" | stats min(price)

Result is 1.00.

**Maximum price:**

source="buy-clicks.csv" | stats max(price)

Result is 20.00.

**Total money:**

source="buy-clicks.csv" | stats sum(price)

Result is: 21407.0

### Part 2. Filtering and aggregation

The previous examples demonstrated how to perform aggregate calculations on fields for the entire data set. We can combine aggregate operations with filtering to calculate on a subset of the data.

The file user-sessions.csv describes when users start and stop playing the game and when they advance levels. For all the “end” events, what is average team level for users playing on windows? What about playing on either Windows or Mac?

**For windows:**

source="user-session.csv" platformType="windows" sessionType="end" | stats avg(teamLevel)

Result is: 4.364516

**For iphone or mac:**

source="user-session.csv" (platformType="iphone" OR platformType="mac") sessionType="end" | stats avg(teamLevel)

Result is: 4.352079

### Part 3. Locating the types of aggregate operations
Splunk allows you to perform many different types of aggregate operations on the data. Below are links that list the available operations for each platform:

**Statistical functions in Splunk:**

http://docs.splunk.com/Documentation/Splunk/6.1.4/SearchReference/Commonstatsfunctions#Aggregate_functions