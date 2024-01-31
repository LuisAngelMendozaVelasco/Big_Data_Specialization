# Exploring Vector Data Models with Lucene

By the end of this activity, you will be able to:

1. Import and query text documents with Lucene
2. Perform weighted queries to see how rankings change
3. View the Term Frequency-Inverse Document Frequency (TF-IDF)


NOTE: if you get the error Exception in thread "main" java.lang.NoClassDefFoundError when running the commands in this activity, you will need to download Lucene by running these commands:

```bash
cd $HOME/Downloads
wget http://archive.apache.org/dist/lucene/java/5.5.0/lucene-5.5.0.tgz
tar -xvzf lucene-5.5.0.tgz
```

Step 1. Open a terminal shell. Open a terminal shell by clicking on the square black box on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pYW6JQWREeabsxLXkMIYiw_f85b3afcf7b7a86decd2b0eb43764ecd_click-on-terminal.png?expiry=1706745600000&hmac=0pLx028xMjONEZZGZXSYAbSScaSPUzN3l_BSMm4tems)

Change into the vector directory:

```bash
cd Downloads/big-data-2/
```

Run ls to see the scripts and data directory:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JWSZLwzBEeacJw5xmvIInw_6cf6af3bb8c7860a9f8268e607abee19_ls.png?expiry=1706745600000&hmac=3NE9-rqs2UHgAYjvIQSLo-3Urjp3NCRcBwCy0y4DZ9o)

The data directory contains three CSV files, which contain textual data from the news. 

Step 2. Import and query text documents. Run runLuceneQuery.sh data to import the documents in the data directory:

```bash
./runLuceneQuery.sh data
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/kecSQwzBEeacJw5xmvIInw_273dd387cf7d586ae701654cb1394dd7_run-query-sh.png?expiry=1706745600000&hmac=PR7QB7KDV00VccOJr1-76miFWwfwrjKCHagzNkf5otU)

Enter voters to query for that term:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CPeSbQzCEealrgo0ik8CQQ_518a390ee14e512fc6b0b26c47f31f66_voters.png?expiry=1706745600000&hmac=EwBur65C13O0tdyflA1DANETJ0tSDU0O6KGsGcMod6I)

The output shows the rankings and score for each of the three CSV files for the term voters. This shows that news1.csv is ranked first, news2.csv is second, and news3.csv is third.

Next, enter delegates to query for that term:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GXAvmwzCEea86w5Bgpijyw_b48914a557b2a495bc42d3084b646a5f_delegates.png?expiry=1706745600000&hmac=udDdIcUL8J2rIkiU2sYD1oSuhClsBsXLBCbUS7IteiE)

The output shows that news2.csv is ranked first, news1.csv is ranked second, and news3.csv is not shown since the term delegates does not appear in this document.

We can query for multiple terms by entering them together; enter voters delegates to query for both terms:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/MNsOlwzCEeaz1wpXV4urCQ_4c013a2fd8e3826e967d601399f6cc93_voters-delegates.png?expiry=1706745600000&hmac=MFMQKMSn9Qxdw0vDBlsoRZvq_5xzH_4xJg-E2FrgzhE)

The output shows that news2.csv is ranked first, news1.csv ranked second, and news3.csv ranked third.

Step 3. Perform weighted queries. We can perform a weighted query (or "boosting") to give one term more importance than the others. Enter voters^5 delegates to give the term voters a boost factor of 5:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XUsi8gzDEeaY9hLgv1uMbQ_5010d8831c3572de9e82db9bc1d7bc4b_voters-delegates-boosted.png?expiry=1706745600000&hmac=c9sWXs5UzAM5lIPy9wKp_ryJian2us7VUW1aeKuLYpk)

The output shows that news1.csv is ranked first and news2.csv is ranked second. Note that these two rankings are reversed from when we performed the same query without boosting.

Enter q to quit this script.

Step 4. View the TF-IDF. Run runLuceneTF-IDF.sh data to see the TF-IDF for terms in the documents:

```bash
./runLuceneTFIDF.sh data
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_josGAzDEeaY9hLgv1uMbQ_8f2d4c5228e13d49e82d9986c5885935_tf-idf.png?expiry=1706745600000&hmac=ObSbdS8cE0_KknqxJMjtkxfdaBNDyhR6WzYJWriC5SQ)

Enter voters to see the TF-IDF for that term:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mORxQAzEEealrgo0ik8CQQ_d8e63cb7803f5b956c583b0ef4c077cf_tfidf-voters.png?expiry=1706745600000&hmac=QR6PfTSf3sgimxpcLJZ2qRpgz8QDmjTwQFCFIZUGsBU)

Enter delegates to see the TF-IDF for that term:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/edqT8QzEEeakhBLZfuBbtQ_58a50d891b65caf34e8ec66bc9d2d3cc_tfidf-delegates.png?expiry=1706745600000&hmac=UCjqplVVqs0Zbsn52AYXrT6IvWftPBiMF7342u2s-dM)

Enter q to quit this script.