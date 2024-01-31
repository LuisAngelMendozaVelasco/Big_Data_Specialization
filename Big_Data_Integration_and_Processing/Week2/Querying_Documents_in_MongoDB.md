# Querying Documents in MongoDB

By the end of this activity, you will be able to:

1. Find documents in MongoDB with specific field values.
2. Filter the results returned by MongoDB queries.
3. Count documents in a MongoDB collection and returned by queries. 

Step 1. Start MongoDB server and MongoDB shell. Open a terminal window by clicking on the square black box on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pYW6JQWREeabsxLXkMIYiw_f85b3afcf7b7a86decd2b0eb43764ecd_click-on-terminal.png?expiry=1706832000000&hmac=UMoi75LHNgxw01-3m_ArwRdGqWPeVyQ4ymfSWUl03wU)

Next, change to the mongodb directory, and start the server:

```bash
cd Downloads/big-data-3/mongodb
./mongodb/bin/mongod --dbpath db
```

The arguments --dbpath db specify that the directory db should be used for the MongoDB directory for datafiles. After starting the MongoDB server, you will see the following lines indicating that the server is running:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vUHvPVT-EeaqTxIkdCEfsw_e7e71e936f7860924a71d716af7ba1db_server-start.png?expiry=1706832000000&hmac=xc6Iu-DZMbh4KEZBBjcZTnYQjpn_ufgjEtTTsMkz4yY)

Next, let's run the MongoDB shell so that we can query the server. Open a new terminal shell window, change to the mongodb directory, and start the shell:

```bash
cd Downloads/big-data-3/mongodb
./mongodb/bin/mongo
```
              
Step 2. Show Databases and Collections. Run the show dbs command to see the databases:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1YqPclT_EeaubA6-qtnryw_50ff133f125dede0819a1095b61a5755_show-dbs.png?expiry=1706832000000&hmac=QE96ZMYEwhj4izbrHxlpNDIoxc5gRo4o3R3BXMswVj0)

The database named sample has been created and loaded with Twitter JSON data. Let's switch to that database by running the use command:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XbHn51UAEeaX4QpLJOK7gQ_667612c1f60e7b8e88d160836d94f814_use-sample.png?expiry=1706832000000&hmac=z-ZyXbbJ5mWO830d_ZezIS7zFt3krOtXjiWIUjOyfyI)

We can see the collections in the sample database by running show collections:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/R6vI_lUAEealpAoth2FRAw_5725c1daf122e4a7aa2765c28e66f505_show-collections.png?expiry=1706832000000&hmac=ikUw4AH-TLmxI9-uZLmS0opqYfWIO980B3Lg1T3KMa8)

The Twitter data is stored in the users collection. We can run db.users.count() to count the number of documents:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8ETyM1UAEeaztg6Pg6w09w_6f1d10814edde8375f05bcad18204c1f_users-count.png?expiry=1706832000000&hmac=d12ntUeBs9qPIohAB1ZV-_aTejAMJCWEc1l99UR6gEw)
         
Step 3. Look at document and find distinct values. We can examine the contents of one of the documents by running db.users.findOne():

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HLAadVUBEealpAoth2FRAw_bf370189d6465b1c0de6723009df6e04_find-one.png?expiry=1706832000000&hmac=sRR0YXsfofDDV1YN9Cpuq5TJTui_35UqGkEyheKYRHQ)

The document has several fields, e.g., user_name, retweet_count, tweet_ID, etc., and nested fields under user, e.g., CreatedAt, UserId, Location, etc.

We can find the distinct values for a specific field by using the distinct() command. For example, let's find the distinct values for user_name:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JQuUBlUCEeaWRg7WBfqodw_ac0a1c5c790e1565ab33bd8300301655_distinct-username.png?expiry=1706832000000&hmac=jXHYIW4eXfSRgdKzRs9brBG0z7OMSvp8yS41gFwLBvo)
       
Step 4. Search for specific field value. We can search for fields with a specific value using the find() command. For example, let's search for user_name with the value ActionSportsJax:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xKtuLVUHEeaughJrsEVARw_e883782f21c53dac8dace372d7962c59_find-value.png?expiry=1706832000000&hmac=rVY4g50Ji02mVNtQv-Q6MZBJ4nH5M4dnMRuYBSLlHfw)

By appending .pretty() to the end of the find command, the results will be formatted:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zlmcslUHEeaX4QpLJOK7gQ_7178433e9e4672aff7a9bc68ca49bac5_find-pretty.png?expiry=1706832000000&hmac=nrECeFVGji0J5wg7nSNTZOgqVkOeth_k_abS_SDTE6o)
       
Step 5. Filter fields returned by query.We can specify a second argument to the find() command to only show specific field(s) in the result. Let's repeat the previous search, but only show the tweet_ID field:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dhyyI1UIEeaubA6-qtnryw_89f1bb7b3938d3272130af19729933ed_find-filter.png?expiry=1706832000000&hmac=XPxz9K_jt2wvPadhmw-E9giS-u7VV8D48n62fPRk44w)

The _id field is primary key for every document, and we can remove it from the results with the following filter:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lHwdR1UIEeaFpQoKLtdtHw_5ce2bd8165fe95919d41e67de270ad89_find-filter-no-id.png?expiry=1706832000000&hmac=b0RhFiISp5DmlnDJBs68t3mup-MJCjiczrJNuOz3O5E)
    
Step 6. Perform regular expression search. MongoDB also supports searching documents with regular expressions. If we search for the value FIFA in the tweet_text field, there are no results:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ULQ1FlUKEeaFpQoKLtdtHw_77f0ff1da6ce5073f56e5b1e9c45195b_tweet-text-fifa.png?expiry=1706832000000&hmac=KdFRd0ZH55viPUhlCFz2eD2z8gWqiIV1H2Us65pHgfk)

However, if we search using a regular expression, there are many results:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cpipjFUKEeaqTxIkdCEfsw_c37d819a9879fe633f4998d09a06f724_tweet-text-re.png?expiry=1706832000000&hmac=NNraWS_FxrbZOFTBuE-UwZ_MI696MFzHNfG55nZsKNg)

The difference between the queries is that the first searched for where the tweet_text field value was exactly equal to FIFA, and the second searched for where the field value contained FIFA.

We can append .count() to the command to count the number of results:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/g5kUTlUKEeaqTxIkdCEfsw_83b90f0a247664cb2dcb4fffcf5393ec_tweet-text-re-count.png?expiry=1706832000000&hmac=6Av59xBpMUnwiPSFqk5Hc5KyFetcWinFkt5GEVOH9M4)
 
Step 7. Search using text index. A text index can be created to speed up searches and allows advanced searches with $text. Let's create the index using createIndex():

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Aa0Ypl2vEeaCdBI2oAYa8w_d1df8640db3f16f5b35af5917de55c42_create-index.png?expiry=1706832000000&hmac=ycR3CZ51KN5BTJ6Y2cc5SuNJ1rFKRNDFwM1fIdZl_3Y)

The argument tweet_text specifies the field on which to create the index.

Next, we can use the $text operator to search the collection. We can perform the previous query to find the documents containing FIFA:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HjV6dl2vEeaWHg4NuBHTLw_37e181106d07cd7e1d067de31f4c1433_text-search-fifa.png?expiry=1706832000000&hmac=QkCOrI-MEDVvU3JIL4smPyoj5uJxqfs8jrgbfYQG_Zg)

We can also search for documents not containing a specific value. For example, let's search for documents containing FIFA, but not Texas:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/KzVscl2vEeazDA6HAv4GcQ_62133c32f77c77606c0e5199008ec8e2_text-search-no-texas.png?expiry=1706832000000&hmac=9GS6dduOCztB9CfyUxpm39LNJoTHlWTBaHgwcpni64c)

Step 8. Search using operators. MongoDB can also search for field values matching a specific criteria. For example, we can find where the tweet_mentioned_count is greater than six:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/YeVX3lULEeaqTxIkdCEfsw_a46c8b05151f6f51f935978017214799_find-gt.png?expiry=1706832000000&hmac=DftDyKxogOBlPCiFd9LLXLymNF0mhYqmYVXVqsbaMXs)

The $gt operator search for values greater than a specific value. We can use the $where command to compare between fields in the same document. For example, the following searches for tweet_mentioned_count is greater than tweet_followers_count:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lyxIy12-EeaJrxIK7EGdww_8512cd11bd19da57f3533f43b5711e2a_where.png?expiry=1706832000000&hmac=TuLyOrsB5-GAcFIBhtI_r2kQs4B9Yaip2nc9AeEJloU)

Note that the field names for $where are required to be prefixed with this, which represent the document.

We can combine multiple searches by using $and. For example, let's search for tweet_text containing FIFA and tweet_mentioned_count greater than four:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/iM3ZDl2-EeaJrxIK7EGdww_5359918a5d09a31b0696abdf0ae0db6e_find-and.png?expiry=1706832000000&hmac=Wf8RGD3ABwaIdzO6xHOsZFyeh6_W_BAidZ8dpMk-rjg)

When you are done querying MongoDB, run exit in the MongoDB shell, and Control-C in the terminal window running the server. 