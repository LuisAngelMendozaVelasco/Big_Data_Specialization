# Querying Relational Data with Postgres

By this end of this activity, you will be able to:

1.  table and column definitions, and perform SQL queries in the Postgres shell
2. Query the contents of SQL tables
3. Filter table rows and columns
4. Combine two tables by joining on a column

Step 1. Open a terminal window and start Postgres shell. Open a terminal window by clicking on the square black box on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pYW6JQWREeabsxLXkMIYiw_f85b3afcf7b7a86decd2b0eb43764ecd_click-on-terminal.png?expiry=1706832000000&hmac=UMoi75LHNgxw01-3m_ArwRdGqWPeVyQ4ymfSWUl03wU)

Next, start the Postgres shell by running psql:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1VoaL07DEeaztg6Pg6w09w_4f7f627ed5c313e44580a7d3894a868c_psql.png?expiry=1706832000000&hmac=nPGSusv32LiqnILjo6Qa3GhuSj_ZIatDzHOO0D7vep0)

Step 2. View table and column definitions. We can list the tables in the database with the \d command:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4m4I9U7DEeaqTxIkdCEfsw_448f35ae2741673aaec8f65e6a36ef60_tables.png?expiry=1706832000000&hmac=05aJEW8oYdev0RRquDOHlw-9Aigjs1xW24DIB3pKONA)

The database contains three tables: adclicks, buyclicks, and gameclicks. We can see the column definitions of the buyclicks table by running \d buyclicks:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8MHJ3E7DEealpAoth2FRAw_b807f591d4faaa1215beca7933f7b41b_buyclicks-defn.png?expiry=1706832000000&hmac=mP2koKHc5qddeSnCOTl5wl7ldKTdvsjjZNl_jZI-ujo)

This shows that the buyclicks table has seven columns, and what each column name and data type is.

Step 3. Query table. We can run the following command to view the contents of the buyclicks table:

```SQL
select * from buyclicks;
```

The select * means we want to query all the columns, and from buyclicks denotes which table to query. Note that all query commands in the Postgres shell must end with a semi-colon.

The result of the query is:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sj1_b07EEea3kBK2xkPy7w_a510b271199ec21e5058218c350925bc_select-all.png?expiry=1706832000000&hmac=BtIGC14XbL2DkrnfmkvC4DUS0UIscEyvo1bCDk_lCv8)

You can hit <space> to scroll down, and q to quit.

Step 4. Filter rows and columns. We can query only the price and userid columns with the following command: 

```SQL
select price, userid from buyclicks;
```

The result of this query is:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2GxuR07EEeaughJrsEVARw_d81d31308c5f3040afcf67306bb097e4_select-filter-cols.png?expiry=1706832000000&hmac=LoOW8y493WIVH7ayoBPXmeBXAX0LAn1c854l4ou2DNQ)

We can also query rows that match a specific criteria. For example, the following command queries only rows with a price greater than 10:

```SQL
select price, userid from buyclicks where price > 10;
```

The result is:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5GHMyU7EEeaztg6Pg6w09w_ab065a549e23b2f9c07a1c362d8002a4_select-filter-rows.png?expiry=1706832000000&hmac=jUsCjG2nQGeoyiI7GnArjFKoJpviDfLGPWOM8k8IHLM)
       
Step 5. Perform aggregate operations. The SQL language provides many aggregate operations. We can calculate the average price:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Pwh53k7GEealpAoth2FRAw_f91e08836738a71e5a0350f2b6626696_select-avg.png?expiry=1706832000000&hmac=5a4Uvq1dlt8o2EsYTMD4YiOA7kZwkRQTvx29r_O4lbk)

We can also calculate the total price:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Mm8SqU7GEeaqTxIkdCEfsw_96aead1d2f42b636c420988b26530ec3_select-sum.png?expiry=1706832000000&hmac=-Pi6FKtbTiGd7zMf8E_JSWV99OK5uXusWn3xOx-EOvg)

The complete list of aggegrate functions for Postgres 8.4 (the version installed on the Cloudera VM) can be found here: 
https://www.postgresql.org/docs/8.4/static/functions-aggregate.html

Step 6. Combine two tables. We combine the contents of two tables by matching or joining on a single column. If we look at the definition of the adclicks table:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/i7LcXE7EEeaubA6-qtnryw_52ba2a41641d58f16045834d36def8ea_adclicks-defn.png?expiry=1706832000000&hmac=uAn59UYCfwfGdeI25_FBd3-4nb2uI83p0E8GJ50jPRw)

We see that adclicks also has a column named userid. The following query combines the adclicks and buyclicks tables on the userid column in both tables:

```SQL
select adid, buyid, adclicks.userid
from adclicks join buyclicks on adclicks.userid = buyclicks.userid;
```

This query shows the columns adid and userid from the adclicks table, and the buyid column from the buyclicks table. The from adclicks join buyclicks denotes that we want to combine these two tables, and on adclicks.userid = buyclicks.userid denotes which two columns to use when the tables are combined. 

The result of the query is:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SLIJbU7FEeaztg6Pg6w09w_a90fc2cf52cd7952a52b14e2452f2d63_select-join.png?expiry=1706832000000&hmac=TvxRzyDA8ZruYRUqattkw_uVs2VPFOAmpipOSEiCXBc)

Enter \q to quit the Postgres shell.