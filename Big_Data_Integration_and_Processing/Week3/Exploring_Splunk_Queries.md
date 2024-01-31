# Exploring Splunk Queries

By the end of this activity, you will be able to:

- Import CSV files into Splunk.
- Query, filter, and plot data.
- Perform statistical calculations.

NOTE: Steps 4 and 5 below contain examples using the 'sort' command which are not covered in the video lecture but which will be covered in the accompanying quiz.

The Census CSV data used in this activity can be downloaded here:

[census](https://d3c33hcgiwev3.cloudfront.net/_4ad3909e53d833feb4a196e8181d1e3c_census.zip?Expires=1706832000&Signature=h0Dqt0fp6qtVKMud1Ep4XeGo0PKboIajn4a91E6lz-atoj4n-4Ifb16Q~ACOyF7ro5eClvBq8UlN48-dZ-BNR72KWxk-1Xo9NO8D4uqE0S6w5f7nmmVnzlwAKmG5~SGQf-RBzyTLmzcSXNSPu4hrCZ3Zc32eM6G1PeRVZmnu3GA_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

After downloading, unzip the file.

Step 1. Login to Splunk. Open a web browser and navigate to localhost:8000:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zvzHDFKmEeaWRg7WBfqodw_d940a899e27bac098b80fb117ba71408_localhost.png?expiry=1706832000000&hmac=sYA0Nt1cWY3gXt7pWhpw7Pymk5h1h9R5y9R1qgDe9OA)

Next, login to Splunk by enter admin and the default password changeme:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2DvfnVKmEeaWRg7WBfqodw_89c5a80c41f68b6a94c05a202a980d81_login-password.png?expiry=1706832000000&hmac=0Wf8iRWVIbUc8x_S8Tetpf9q9FRFZ2dTlolV8ihQ6Vo)
                    
Step 2. Import census data. Let's import the census data CSV file to Splunk. First, click on Settings in the top right, then click on Add Data: 

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_WKGUFKmEeaughJrsEVARw_71017d267c9494c235ca6bfff055b438_settings-add-data.png?expiry=1706832000000&hmac=eb4Sh6oPJsK5DxOofn_fIutk-ymD-iz52UWgceRqzGs)

Next, click on Upload:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/FNE15lKnEeaztg6Pg6w09w_c5343ebbe880aa83c96e6bfdc4fca587_upload.png?expiry=1706832000000&hmac=FI2dFHAqsY280811D-VI54pXIulP2Z0dtzzJRr54u3s)

Click on Select File:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HkojzVKnEeaubA6-qtnryw_3b33e4cd5eb3bad2f189853ef404ae0f_select-file.png?expiry=1706832000000&hmac=jdnplCl_E9ndghuou68H6_NvyusjtaisEIXZzwj-TVE)

Navigate to census.csv, and select it. Then click Next>:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LSoe11KnEeaX4QpLJOK7gQ_9ab8481a019e7b690b52307ec18090aa_next.png?expiry=1706832000000&hmac=qjmip4dBPaDTA8HF3wle3IyS3h13HuamCeXOMeIKY3k)

On the left, make sure the Source type is csv:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ini6aVKoEealpAoth2FRAw_b54c524870d717bae0b6bd0eb78f369c_source-type-csv.png?expiry=1706832000000&hmac=V305mUXTTtqNgbX9-doZ7i6iBCulbofVQSLoJujwtBc)

If the Source type is not csv, click on Source type, go down to Structured, and select csv:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sVBFoVKoEeaqTxIkdCEfsw_eeb45402a9573eac60c21f698409b2bc_select-csv.png?expiry=1706832000000&hmac=vrGpZt_RLqjXc97cmDfiYdZ7zMixxDbRqoPWvXEdB9o)

The table on the right is a preview of the CSV data. It shows the values for different fields:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/COO0z1KpEeaughJrsEVARw_73e7d48e290e007cc6f21dbef9161f2a_import-preview.png?expiry=1706832000000&hmac=RSPwhL0z6EIIeNQ27MZ4oY6aTovWHEjOhEOeIzDilY4)

Next, click on Next, click on Review, and then click Submit. Splunk will say the file is successfully uploaded:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dACp-VKpEeaztg6Pg6w09w_f0a73d763fcc9f839ed86c04d3c4f743_import-success.png?expiry=1706832000000&hmac=lMsJXP3HNd4oSypm5f44irN6XTDGWa0rIWnj-bsbxE8)

Step 3. View data. Click on Start Searching:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uBgAEFKpEeaqTxIkdCEfsw_988184dec26909a26fb177bf2b559a43_start-searching.png?expiry=1706832000000&hmac=dvIDHms2xdCTqM5oV3paqfbFjWaGL6BY3GuyfgAQ_7c)

Splunk will enter a default query in the search box to show the data we just imported:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4OZ4s1KpEealpAoth2FRAw_ac9e07a9b1b00e2aabb7e13de43b241f_default-query.png?expiry=1706832000000&hmac=lbYyEWaTNzzml_fyAsebGc9RJXKcQ-9z0u39LuNoJsQ)

This query shows all the data from the census.csv file and whose data type is CSV. In general, we can use source= to query from different file names, and sourcetype= to query from different formats.

The table shows the results matching this query:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z0F18VKqEeaztg6Pg6w09w_9bc9c8f8c9f02324912fb56fe935efb9_default-query-values.png?expiry=1706832000000&hmac=8wgXdsebRY-qZzl1cnoM1m7OgyovfSQKLPd5iQSwSro)
        
Step 4. Filtering for specific values. We can filter the results by looking for a field with a specific value. For example, we can find the entries where the state is California:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QMGLt1KrEea3kBK2xkPy7w_2c59ca8b274f46dba173bcfc8d36beab_stnme-ca.png?expiry=1706832000000&hmac=x1P_klTPTsQd2gYjE6vMlFsBBBe-_qDTA_WTrzoK1v0)

The field STNAME contains the name of the state, and the above query only shows the results where the state is California. We can use an OR to search for multiple values on the same field:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6_2orlKwEealpAoth2FRAw_74a2c7c9f5ad184fbdac4dca41d62cf2_stname-ca-ak.png?expiry=1706832000000&hmac=8jHiiU7xoWfdgGAHJDf9hEZ8RIY1mzEH1pFXTMwGHEM)

We can search multiple fields with specific values by adding them to query. For example, let's search for state name California and 2010 population greater than one million people:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9gi2Y1KrEeaqTxIkdCEfsw_5e381f999e05ca02fd03cfb0d172aa3f_ca-pop-one-million.png?expiry=1706832000000&hmac=5tlUrIagKXR-KfSaKh8O68kHUlk_olojQo1sM_NIMAo)

We can filter our results to just show a single column. For example, let's just show the county names of the previous query:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mN5cWVKwEeaubA6-qtnryw_cd69c3177b318417f7e47d4044359b79_ca-pop-one-million-table-county.png?expiry=1706832000000&hmac=uLHIihOAaaSpL5Er0nAczxVsbS-yejV4-9PCsfDtHAk)

The | (pipe) is the syntax for sending the results from one query to the next, and the table command creates a table using only the specified column name(s).

We can sort the results based on any of the fields, such as population, and order them in either ascending or descending order. The image below shows an example of a search for all items with a population greater than 100000, sorts the results in descending order, and creates a table containing the population and state name. [To sort in ascending order you would replace "desc" with "asc"].

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xf1vMVs6Eeag5RL6-p1mNw_295cb0cf08c276da319aa410dc3e0f62_sort_desc.jpg?expiry=1706832000000&hmac=ffUlxqUO9uruXBVsHuZlgbDklY_log7GRqLA5Ubn6z0)

Instead of using "desc" you can use a dash before the sorting field, e.g. "...| sort -CENSUS2010POP | table ..." for the above query. 

We can view plots of search results by clicking on the Visualization tab. For example, if we use our last query and add the 2010 population value to the table:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xtOmbFKwEeaubA6-qtnryw_4181da528af3a421c3e0f35c572886db_ca-pop-million-all.png?expiry=1706832000000&hmac=u-slAwrlp6892NQFcTq86yu0Gkf1k2Hg9l3pBBqycuk)

We can click on the Visualization tab to see a chart of the results:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uq1CS1KvEeaFpQoKLtdtHw_38afa24673d2e01d2582c3f9a04b21e3_ca-pop-million-chart.png?expiry=1706832000000&hmac=pKnWxDBvt7Gf9AccQlVON_gxgrwAL7MLuz0zOJa4yok)
       
Step 5. Perform statistical calculations. The Splunk stats command is used to perform statistical calculations on the data. Let's count the results where the state is California:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/wjrE6FKtEeaX4QpLJOK7gQ_b57876491f52a23b4400139e93625d7d_stats-count.png?expiry=1706832000000&hmac=E_Xl5vEqFFYveeSGVRXUBoyfZ-2g4ndCEH65-q9hISQ)

We can sort based on the count by adding "| sort count" to the above query. This would sort in ascending order. if we want to sort in descending order we would use " | sort -count". 

Next, let's compute the total 2010 population for California:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fERZpVKuEea3kBK2xkPy7w_ad6ace2bb40ed2fd4d6e54564a18b0e1_stats-sum.png?expiry=1706832000000&hmac=-Wua-w8VIQ5FqBivBK_GnAoXvYHAXMJ-ZhDJxxp8OTw)

Finally, let's compute the average 2010 population for California:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/74tqkVKtEealpAoth2FRAw_5e261481f054fa09fd92282d1c55bd56_stats-mean.png?expiry=1706832000000&hmac=_rj8RtTaV4q2QpYGAxVIPNpP-7iM8ukPZFHvYkybvIA)