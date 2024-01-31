# Exploring SparkSQL and Spark DataFrames

By the end of this activity, you will be able to:

1. Access Postgres database tables with SparkSQL
2. Filter rows and columns of a Spark DataFrame
3. Group and perform aggregate functions on columns in a Spark DataFrame
4. Join two SparkDataframes on a single column

Step 1. Open Jupyter Python Notebook for SparkSQL. First Open the Terminal and enter the command "pyspark" to setup the server. Next, open a web browser by clicking on the web browser icon at the top of the toolbar:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RCneZE7PEeaqTxIkdCEfsw_c491f272226b35805e44abef7a7a22a9_browser-icon.png?expiry=1706832000000&hmac=0_QPmkAUzG_X8d7sMuAOY0-flk_YfFZlKGmJ7nGn8jU)

Navigate to localhost:8889/tree/Downloads/big-data-3/spark-sql:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5UEtyVBIEeaughJrsEVARw_2f0e65d56927529ec7f5b1689ab966cc_browse-to.png?expiry=1706832000000&hmac=Glj-UcsoO3UtivlrGy9hCu4Mqau_5oofLlQAwXA-VUI)

Open the SparkSQL Notebook by clicking on SparkSQL.ipynb:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/78VwalBIEeaWRg7WBfqodw_505a38db2ed8e2d389959f3453f7d75c_notebook.png?expiry=1706832000000&hmac=5107bBDvtk9Wc4NZb7aFxQvqgCO2UzwT62KA3gVIX5k)
          
Step 2. Connect to Postgres Table. This notebook already contains three lines of code so you do not have to enter them. Run these three lines. The first line imports the SQLContext module, which is needed access SQL databases in Spark:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pncdBlA9EeaqTxIkdCEfsw_924d1f6819e45a995b9c02c7f834e9d5_import-sqlcontext.png?expiry=1706832000000&hmac=nYXTiCwwdY0MbzGfJFwsTiF8oy8X35KiJZjgW6ZIPzE)

The second line creates a new SQLContext from the SparkContext sc:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0E1CnFA9EeaubA6-qtnryw_fcdfbcc6b62cb87516285d326dfeee2c_createl-sqlcontext.png?expiry=1706832000000&hmac=k88zTMO0fpJA0kCTxOAkecAsMoLigkqyWk6WJIzKQ1E)

The third line creates a new Spark DataFrame in the variable df for the Postgres table gameclicks:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4G-BsVA9EeaqTxIkdCEfsw_c0dfe1ec70c4e944043e274174455c0e_create-dataframe.png?expiry=1706832000000&hmac=KwG7bW8f3EEE6ZiytzUG3LVC5VcI4YR7znDDFNtJdAI)

The format("jdbc") says that the source of the DataFrame will be using a Java database connection, the url option is the URL connection string to access the Postgres database, and the dbtable option specifies the gameclicks table.

Step 3. View Spark DataFrame schema and count rows. We can call the printSchema() method to view the schema of the DataFrame:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NnGlMVRGEeaWRg7WBfqodw_e51f0e320db18c932bc6c84d14ef23a0_schema.png?expiry=1706832000000&hmac=eiiTyzblhuJm1E_2TtSbss83an9ftcCMPIbSjYhAfiE)

The description lists the name and data type of each column.

We can also call the count() method to count the number of rows in the DataFrame:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/z8mHqFBHEeaX4QpLJOK7gQ_b3da30f52754f0f086019e0c90354fdb_count-rows.png?expiry=1706832000000&hmac=CIcpsqoKpiVUT3l1xc0G_23nSMHg2Pu9hTjORZC_uHk)
                   
Step 4. View contents of DataFrame. We can call the show() method to view the contents of the DataFrame. The argument specifies how many rows to display:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4Av5SVBHEeaqTxIkdCEfsw_ce0fc8d177180da1b1d4ce66c45245a1_show.png?expiry=1706832000000&hmac=UZIhcWG9u96PQ3Tn4kbamC9btF2BE-0FLMp2M7SiP_0)
                      
Step 5. Filter columns in DataFrame. We can filter for one or more columns by calling the select() method:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6t1LLVBHEeaFpQoKLtdtHw_10d35c0bc1fe21f9fbe21719ce1b6d80_filter-cols.png?expiry=1706832000000&hmac=HcwR_0_oYiJaFdRExn4j5FWH0n3a2QfqMGbQ9Bx27EE)
                       

Step 6. Filter rows based on criteria. We can also filter for rows that match a specific criteria using filter():

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_mEFsFBHEeaughJrsEVARw_eec7c99e6958b67a2c8ad9b04a6721e2_filter-rows.png?expiry=1706832000000&hmac=70uWDNs0Jts6x9nH3FQcg1p0V6bESVPNlLeDMtFjTj8)

The arguments to filter() are a Column, in this case specified as df["teamlevel"], and the condition, which is greater than 1. The remainder of the commander selects only the userid and teamlevel columns and shows the first five rows.

Step 7. Group by a column and count. The groupBy() method groups the values of column(s). The ishit column only has values 0 and 1. We can calculate how many times each occurs by grouping the ishit column and counting the result:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/BjjFi1BIEealpAoth2FRAw_cc892afa3939a44be81ec513d02e9eda_groupby-count.png?expiry=1706832000000&hmac=dwh5mzB5rUu-wOxNNqvrSxMg6NeejC11JuTLgZ1pmXw)
                       
Step 8. Calculate average and sum. Aggregate operations can be performed on columns of DataFrames. First, let's import the Python libraries for the aggregate operations. Next, we can calculate the average and total values by calling the mean() and sum() methods, respectively:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/D70kVVBIEeaqTxIkdCEfsw_4122fc9c609c5ce5d06ff3dcd086e3a7_avg-sum.png?expiry=1706832000000&hmac=OI-FX77qOtHBTfYz1OKX7WSa8rjsd7zOb_fTA87WlL4)

Step 9. Join two DataFrames. We can merge or join two Dataframes on a single column. First, let's create a DataFrame for the adclicks table in the Postgres database by copying the third cell in this notebook and changing gameclicks to adclicks and storing the result in a new variable df2:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/709Y-1RFEeaqTxIkdCEfsw_dadafecff636244cf7bbcaa04cda1f74_create-df2.png?expiry=1706832000000&hmac=QjxnsdShtFHefyENvclt7nuEBp6C5BcrSYrsIdQzhVE)

Let's view the columns in df2 by calling printSchema():

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ghH-UlRGEeaubA6-qtnryw_c81f49a3be2c53a0f8aecfe7f569a76c_df2-schema.png?expiry=1706832000000&hmac=2NRoRfGbxtIJQ4jnObmoNGexPJLSF8N_xHYKVWS1NDg)

We can see that the adclicks df2 DataFrame also has a column called userid. Next, we will combine the gameclicks and adclicks DataFrames by calling the join() method and saving the resulting DataFrame in a variable called merge:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lrgYvFRGEea3kBK2xkPy7w_77ce387ed9f2b52b27224885fb8e28bd_join.png?expiry=1706832000000&hmac=mIFyTQDK-kgrUuA8xpVeCsqVU1vHtjpFQkBG0iSAOSw)

We are calling the join() method on the gameclicks DataFrame; the first argument is the DrataFrame to join with, i.e., the adclicks DataFrame, and the second argument is the column name in both DataFrames to join on.

Let's view the schema of merge:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yWEnXVRGEeaX4QpLJOK7gQ_38ba8ec68d753ab5b94418f48c93503e_merge-schema.png?expiry=1706832000000&hmac=5X5MsILeBg-FYWC-lReF1XGWmQQUnh9IoZ5JalGQjQQ)

We can see that the merged DataFrame has all the columns of both gameclicks and adclicks.

Finally, let's look at the contents of merge:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4jdWhVRGEeaqTxIkdCEfsw_7d1bf26912c3ab6918347c32489ffe30_merge-show.png?expiry=1706832000000&hmac=cbNjtQsVlkaCiJY-BcA7AFwCcCa_l6N5b0MCCKBSQW8)