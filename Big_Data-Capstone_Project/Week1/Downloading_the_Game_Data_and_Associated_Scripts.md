# Downloading the Game Data and Associated Scripts

For most of this capstone you will be working with a predefined dataset generated by our development team. The reason for this is so that we can be sure you move through each week of the Capstone with as little difficulty as possible, and any quizzes and peer reviews which you are tasked with will be equivalent and consistent for each Learner.

To download the predefined dataset and the scripts needed to fulfill the Capstone assignments, click the following link:

[big data capstone datasets and scripts](https://d3c33hcgiwev3.cloudfront.net/_de5ad40e9a4965ee4b6aad31eea4ac7a_big_data_capstone_datasets_and_scripts.zip?Expires=1706832000&Signature=kCsqQ47CoH731E1Lv~d5YtZ6BOuWeHh8IjieM0SAc5CACPPUaQGdIzmx0jh4DczTZEFpaifEvoALMf9ZI3SMlP3Ye1uc~-ZkY6EV21L44Pet7QfgiVcZIStt1Pdx7~voui1HfWLsadlsYoQZ~HZSEcx7csawW38E83GvIno84kE_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

## Description of Downloaded Content

The above zip archive contains the following archives and scripts. 

**flamingo-data.zip**

The zip archive "flamingo-data.zip" contains 8 CSV files containing simulated game data and log data for the Catch the Pink Flamingo Simulated Game Data. These files are described in greater detail in an accompanying Reading for this week, "[Understanding the CSV Files Generated by the Scripts](https://www.coursera.org/learn/big-data-project/supplement/qxoHK/understanding-the-csv-files-generated-by-the-scripts)".

**combined-data.zip**

The zip archive "combined-data.zip" contains a single CSV file created by aggregating data from several game data files. It is intended to be used in Week 2 with KNIME. This file is described in greater detail in the Reading "[Description of combined-data.csv](https://www.coursera.org/learn/big-data-project/supplement/5iPBb/description-of-combined-data-csv)".

**chat-data.zip**

The zip archive "chat-data.zip" contains 6 CSV files representing simulated chat data related to the Catch the Pink Flamingo game to be used in the Week 4 Graph Analytics. These files are described in greater detail in the Reading "[Understanding the Simulated Chat Data Generated by the Scripts](https://www.coursera.org/learn/big-data-project/supplement/rb4ku/understanding-the-simulated-chat-data-generated-by-the-scripts)".

**Week 3 pySpark MLlib Clustering.ipynb**

This is an iPython Notebook containing instructions for what you need to do in Week 3. [You may view this notebook online](https://github.com/words-sdsc/courseraDataSimulation/blob/master/capstone/readings/Week%203%20pySpark%20ML%20Clustering.ipynb) or on your computer if you have iPython installed. [We also provide a PDF as an alternative](https://www.coursera.org/learn/big-data-project/supplement/VqbUU/practice-with-pyspark-mllib-clustering) if you do not already have iPython installed. Instructions for running the scripts (described below) are provided in a Week 3 Reading. 

**setupWeek3.sh**

This is a shell script you will run in the Cloudera VM for the Week 3 assignment on Spark MLlib.

**sparkMLlibClustering.py**

This is a python script you will need to perform Spark MLlib clustering for Week 3.

**load-neo4j.cypher** 

This file is a text file containing the CYPHER commands needed to load the chat data into Neo4j. You can edit it with any text editor and copy the contents into the Neo4j command line.