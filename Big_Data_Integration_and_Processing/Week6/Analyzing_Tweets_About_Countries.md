# Analyzing Tweets About Countries

Now that you are familiar with the dataset and exported it into a CSV file, let's start integrating this dataset with another small dataset and analyze it in Spark.

To run PySpark in the Cloudera VM, you will first need to run the setup script: [setupWeek3.sh](https://github.com/words-sdsc/courseraDataSimulation/blob/master/capstone/readings/setupWeek3.sh)

Then open PySpark in the VM with the following command: pyspark --packages com.databricks:spark-csv_2.10:1.5.0

As the Sports Analyst, you are very interested in reporting on the countries with the most popularity in Twitter. So a good way to approach this problem would be to find which countries were mentioned the most in the tweets in your dataset and to analyze what words are being used the most in these tweets.

In addition to the CSV file you just exported from MongoDB, we give you a small dataset with the codes and names of some countries. To see this additional dataset, open the following file:

- Downloads/big-data-3/final-project/country-list.csv

To get you started, we have prepared a Jupyter notebook template, and started a SparkSQL context for you. Please open the notebook in:

- Downloads/big-data-3/final-project/SoccerTweetAnalysis.ipynb. 

You will use this notebook to answer the questions below. So let’s get started.

**Question 1**: As a Sports Analyst, you are interested in how many different countries are mentioned in the tweets. Use the Spark to calculate this number. Note that regardless of how many times a single country is mentioned, this country only contributes 1 to the total.

**Question 2**: Next, compute the total number of times any country is mentioned. This is different from the previous question since in this calculation, if a country is mentioned three times, then it contributes 3 to the total.

**Question 3**: Your next task is to determine the most popular countries. You can do this by finding the three countries mentioned the most.

**Question 4**: After exploring the dataset, you are now interested in how many times specific countries are mentioned. For example, how many times was France mentioned?

**Question 5**: Which country has the most mentions: Kenya, Wales, or Netherlands?

**Question 6**: Finally, what is the average number of times a country is mentioned?

Here is a copy of the Jupyter notebook template with added HINTS:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yI6SMkGCEee3MRIl4lCYSA_de536d16bb9db9f67e2762d6e36cf76e_Screen-Shot-2017-05-25-at-12.43.07-PM.png?expiry=1706832000000&hmac=T57PqlY21-dlEzGXHn_AL4Vy7HLC0KNp1USXaFq9jk4)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/20xkB0GCEeeHpAqQsW8qwg_86ae8a48371fbcc43dead5906f0c3209_Screen-Shot-2017-05-25-at-12.43.44-PM.png?expiry=1706832000000&hmac=rgYlkdNMolLt0EeakokeJrY1gP232ZMdpguavR_Y7Pw)

Don't forget to save the results of your analysis as you will have a quiz testing the correctness of these results following this exercise.