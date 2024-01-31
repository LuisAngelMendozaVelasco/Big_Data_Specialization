# Run the WordCount program Instructions

**Learning Goals**

By the end of this activity, you will be able to:

- Execute the WordCount application.
- Copy the results from WordCount out of HDFS.


1. Open a terminal shell. Start the Cloudera VM in VirtualBox, if not already running, and open a terminal shell. Detailed instructions for these steps can be found in the previous Readings.
2. See example MapReduce programs. Hadoop comes with several example MapReduce applications. You can see a list of them by running hadoop jar /usr/jars/hadoop-examples.jar. We are interested in running WordCount.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/phTfYLwcEeWdfA6efk4-Nw_aaa4689dad0a0b114dc4061ac1a1b8f6_hadoop-examples.png?expiry=1706745600000&hmac=B0uE6OodjXIVqhwvWOCARfWJhAWLIHkZrOzYuEE5iLo)

The output says that WordCount takes the name of one or more input files and the name of the output directory. Note that these files are in HDFS, not the local file system.

3. Verify input file exists. In the previous Reading, we downloaded the complete works of Shakespeare and copied them into HDFS. Let's make sure this file is still in HDFS so we can run WordCount on it. Run hadoop fs -ls

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zK2s-NHoEeWbSgqxBCBhEw_9b7235cea93cf0d51d2e05071012660b_hdfs-ls-copytohdfs.png?expiry=1706745600000&hmac=rbLri67rdFdkyK8pAtsq0OmiL1Hg1WY2b3pLSG6KBuk)

4. See WordCount command line arguments. We can learn how to run WordCount by examining its command-line arguments. Run hadoop jar /usr/jars/hadoop-examples.jar wordcount.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8RuRxrwcEeWtBA4YeZyKCw_8965d75626bc9b93bad534a1abdd0069_wc-usage.png?expiry=1706745600000&hmac=aBe6HzzfpJuyQc9Re2AgfTodRyww3bbSoz-0pfUjeGE)

5. Run WordCount. Run WordCount for words.txt: hadoop jar /usr/jars/hadoop-examples.jar wordcount words.txt out

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_o5iCtHoEeWbSgqxBCBhEw_a5ab56276d71eb5fe090494a14ff84a3_wc-start.png?expiry=1706745600000&hmac=Dkvrfqb_EEm-zVz48VzrY9hQsvV0hc4Y43lQcZzBx7c)

As WordCount executes, the Hadoop prints the progress in terms of Map and Reduce. When the WordCount is complete, both will say 100%.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CWyEm9HpEeWbSgqxBCBhEw_95fd7852882712afaa3788808ccf2fec_wc-progress.png?expiry=1706745600000&hmac=z3Lt7ZDC_5ckg5VbOTDPEYepho9TiG7U8KGzsM8zWL4)

6. See WordCount output directory. Once WordCount is finished, let's verify the output was created. First, let's see that the output directory, out, was created in HDFS by running hadoop fs –ls

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UqAk6tHpEeWJYg65RLEZEQ_3c31576c5d4b166438e384e841d7d2a1_hdfs-ls.png?expiry=1706745600000&hmac=YoMCqLFlwg2R6rPim1QkLORyFyAE4dRxmEajNbu4GQg)

We can see there are now two items in HDFS: words.txt is the text file that we previously created, and out is the directory created by WordCount. 

7. Look inside output directory. The directory created by WordCount contains several files. Look inside the directory by running hadoop –fs ls out

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/eRgC39HpEeWjTxJlqDdk5Q_3bc3a4ef35bbe134d582cb3514f4e317_hdfs-ls-out.png?expiry=1706745600000&hmac=NTLVNlAmYNT-yyMDPmrRriBU1xuv4hoTfDZ45vSPtGw)

The file part-r-00000 contains the results from WordCount. The file _SUCCESS means WordCount executed successfully.

8. Copy WordCount results to local file system.  Copy part-r-00000 to the local file system by running hadoop fs –copyToLocal out/part-r-00000 local.txt

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/juHckNHpEeWjTxJlqDdk5Q_e6308a1cba5fedb002a325946cd4467c_hdfs-copytolocal.png?expiry=1706745600000&hmac=L7szvnKkj95g2jsaCd1PWNXN1qeBfxj1kZnxaBRxbc0)

9. View the WordCount results. View the contents of the results: more local.txt

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ponFPNHpEeWbSgqxBCBhEw_53ffe3b3fbdb22779154f157b0ca909b_more-local.png?expiry=1706745600000&hmac=pDy9_BK4DFc1xE4rMsoItvP_Fq6ofkDJeOaX86H2G0s)

Each line of the results file shows the number of occurrences for a word in the input file. For example, Accuse appears four times in the input, but Accusing appears only once.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/x3NeYtHpEeWvxwo5BbZD3w_c7b0e17251de7d370bc1e54d7afca7a5_local-contents.png?expiry=1706745600000&hmac=Gt6WZCA_Vkuv_Ll0F1EERVStln2YtLRXfH-v3qfoPuU)