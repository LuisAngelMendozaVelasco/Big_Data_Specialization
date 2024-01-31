# How do I figure out how to run Hadoop MapReduce programs?

Hadoop comes with several MapReduce applications. In the Cloudera VM, these applications are in /usr/jars/hadoop-examples.jar. You can see a list of all the applications by running hadoop jar /usr/jars/hadoop-examples.jar.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/aRGnngWGEeaaqg5MSeYjIQ_f7af6a98833e56939bc0d707bc711a39_hadoop-examples.png?expiry=1706745600000&hmac=hbKNzOdTSe1JDNUt_5ZXsb3KYlc5oCUkPwrZpEZlkwc)

Each of these MapReduce applications can be run in the terminal. To see how to run a specific application, append the application name to the end of the command line. For example, to see how to run wordcount, run hadoop jar /usr/jars/hadoop-examples.jar wordcount.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/PBGTrwWGEeap7RJsurEyGw_67488e1f74a0c4b83b54ef2d7ead7919_wc-usage.png?expiry=1706745600000&hmac=LYV7kN6GMVRt7wL4CmoZ54x9uaB5l7CI1iTbXA-Bojc)

The output tells you how to run wordcount:

```
Usage: wordcount <in> [<in>...] <out>
```

The \<in> and \<out> denote the names of the input and output, respectively. The square brackets around the second \<in> mean that the second input is optional, and the ... means that more than one input can be used.

This usage says that wordcount is run with one or more inputs and one output, the input(s) are specified first, and the output is specified last.