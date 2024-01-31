# Exploring Pandas 

By the end of this activity, you will be able to:

1. Read a CSV file into a Pandas DataFrame
2. View the contents and shape of a DataFrame
3. Filter rows and columns of a DataFrame
4. Calculate the average and sum of a column in a DataFrame
5. Combine two DataFrames by joining on a single column

This activity consists of programming in a Jupyter Python Notebook. If you have not already started the Jupyter server, follow the instructions in the Reading entitled Starting Jupyter for Python Notebooks.

Step 1. Open a web browser and create a new Jupyter Python Notebook. Open a web browser by clicking on the web browser icon at the top of the toolbar: 

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RCneZE7PEeaqTxIkdCEfsw_c491f272226b35805e44abef7a7a22a9_browser-icon.png?expiry=1706832000000&hmac=0_QPmkAUzG_X8d7sMuAOY0-flk_YfFZlKGmJ7nGn8jU)

Navigate to localhost:8889/tree/Downloads/big-data-3:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TC6iOk7PEeaqTxIkdCEfsw_19f522873b2ae8800db929013dfa1913_notebook-browse.png?expiry=1706832000000&hmac=ziergEYtVfksihNu4HCdehgMG-v00Xu_cdFj1--ow90)

Create a new Python Notebook by clicking on New, and then click on Python 3:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XNgTF07PEeaFpQoKLtdtHw_761dc4d5af4e3c2d274102d2b41196cf_new-notebook.png?expiry=1706832000000&hmac=PdHGE1pDquFYVmJlv0UXbSDGO0Q3GaPt5v7z-Zi-VBI)
  
Step 2. Load Pandas and Read a CSV file into a DataFrame. We first load the Pandas library:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/DiAYqE7PEeaztg6Pg6w09w_382a062c2d05e19ec227ec529e3a4f89_import.png?expiry=1706832000000&hmac=EwrJBSkyf7nbBWiQOsnIKuL0DI6U7gkktLXtvWDhu1c)

Note that to execute commands in Jupyter Notebooks, hold the <shift> key and press <enter>.

We can load the file buy-clicks.csv into a Pandas DataFrame:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/A_FwW07PEea3kBK2xkPy7w_0355e2202cd657d25e079dd0e99745a3_readcsv.png?expiry=1706832000000&hmac=21uGTpNNPXScHRSPq3Cg1jmgBL5RJPjaIq5QBwOWIpY)

This command assigns the DataFrame to a new variable named buyclicksDF, and reads the CSV using pandas.read_csv().

Step 3. View the contents and shape of a DataFrame. We can view the contents of the DataFrame by executing the variable:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sxifxk7TEeaWRg7WBfqodw_060fb6d77f7f725ac4e63dbbace7e065_buyclicksDF.png?expiry=1706832000000&hmac=bIhC5a2vvUc5_z0uaeg88GLS-bQNtvyKOtUVBnTUEE4)

Note that the Notebook does not display all the rows and displays the missing ones as .... :

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6sGvAE7OEealpAoth2FRAw_4e735d1e5a08a0d3d2c01f0f51d1c8bf_truncated.png?expiry=1706832000000&hmac=7NvvvpTq7bdfX-oEB73T2VvK9t4tkygV_eHRrL6E0fg)

We can view the first five rows by using the head(5) command: 

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4Ty0CU7OEeaqTxIkdCEfsw_235074cdfab2dfa423f57edaf1926e78_head.png?expiry=1706832000000&hmac=Ot26_nz53KkckZNmWAxgSJ9tGOtxEVbvGivDjCQqLes)

We can see how many rows and columns are in the DataFrame by looking at its shape:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2BVoqE7OEeaubA6-qtnryw_ac4ed73f9844e5fd4ae3542b81d11df5_shape.png?expiry=1706832000000&hmac=Lt1wxTLlShAmYScjkFC0sx1Ld-jIqmr_kIbmLcUNtTU)

The result says that there are 2947 rows and 7 columns.

Step 4. Filter rows and columns of a DataFrame. We can view only the price and userId columns of the DataFrame:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Qz9sfE7REea3kBK2xkPy7w_5523d6523c4cff6f3101ae100ce9b91d_filter-cols.png?expiry=1706832000000&hmac=ONG5K7yD29z_QWdYrXxht92s5pMS7RLyASaYn33yOwQ)

The [[ ]] creates a copy of the DataFrame with only the specified columns.

We can also filter rows based on a criteria. The following selects rows with a price less than 3:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TqdYDU7REeaX4QpLJOK7gQ_265e55ee63b3dcbbf73795eb1807afd3_filter-rows.png?expiry=1706832000000&hmac=M7yInHjJVvU98zD3qN95SLjhATgHiwFrCtJ_xabfqEg)
  
Step 5. Calculate sum and average of a column. Pandas DataFrames provide many aggregation operations. We can calculate the total price:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ZOYTn07REeaX4QpLJOK7gQ_5d4ae75276f803dc70f118b4b62e173e_sum.png?expiry=1706832000000&hmac=eHg1gLQnut9CArz5Pru4qHTnrsFiFa9oNPIwWcuFBO0)

We can also calculate the average price:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cbbe307REea3kBK2xkPy7w_a671ee6f01cda24dfb7590c5591de3d7_mean.png?expiry=1706832000000&hmac=bQ4EiOcdZOv9PscykfCGyOph_jFwghoakfC5qpQQ4IE)

A complete list of statistical aggregation operations for Pandas DataFrames is at http://pandas.pydata.org/pandas-docs/stable/api.html#computations-descriptive-stats

Step 6. Combine two DataFrames. We can combine two DataFrames on a single column. First, we will load ad-clicks.csv into a new DataFrame:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/33y3_k7SEeaughJrsEVARw_0a8944e993975c41c91bcd9266640ed0_read-adclicks.png?expiry=1706832000000&hmac=KF8txzJKj9GsoUMnssbziPBv-X8YtSk5W1NRpLuIDYA)

If we look at the contents, we see that adclicksDF also has a column named userId:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yZ66CU7SEea3kBK2xkPy7w_345865394c11ee3be9f9e92efb9dde19_display-adclicks.png?expiry=1706832000000&hmac=iKc1C66JGsU4pfdsa6YfUuHHIljyFEmQ2jz6XSSzH-8)

We can create a combine buyclicksDF and adclicksDF on the userId column with the following command:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6UIXG07SEeaX4QpLJOK7gQ_a49a6f98fb18fe62a2a5c37bec71b76c_merge.png?expiry=1706832000000&hmac=Qe61BN9bujsUzE1BvzEhF-L7SfUhxo2eEUEntCag4LU)

The combined DataFrame is assigned to a new variable named mergeDF. The command adclicks.merge() combines adclicksDF with the first argument buyclicksDF, and on='userId' denotes which column to join on.

We can see that the combined DataFrame contains the columns from both adclicksDF and buyclicksDF:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8jw3z07SEeaWRg7WBfqodw_94a9c6a8b432e9bec1a26537d358be91_merge-contents.png?expiry=1706832000000&hmac=EN_mLpNrlfYS05uTSqOSni_3CR7VU_1mEFHUJM_55Hg)