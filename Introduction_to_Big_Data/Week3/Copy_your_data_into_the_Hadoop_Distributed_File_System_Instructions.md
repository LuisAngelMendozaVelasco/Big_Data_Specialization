# Copy your data into the Hadoop Distributed File System (HDFS) Instructions

**Learning Goals**

By the end of this activity, you will be able to:

- Interact with Hadoop using the command-line application.
- Copy files into and out of the Hadoop Distributed File System (HDFS).


**Instructions**

1. Open a browser. Open the browser by click on the browser icon on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/IAQAwdHkEeWbSgqxBCBhEw_206bde98a45be54a3651d2ff048ce6e9_icon.png?expiry=1706745600000&hmac=1i_pDEFqm-ySjZfCVzmTUS5g9yMLwbH-orDCTlgV3uw)

2. Download the Shakespeare. We are going to download a text file to copy into HDFS. Enter the following link in the browser: http://ocw.mit.edu/ans7870/6/6.006/s08/lecturenotes/files/t8.shakespeare.txt

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UmAnY9HkEeWLWxKOx1I7mw_e04f8949daffccf19216b23fe8405066_browser-txtfile.png?expiry=1706745600000&hmac=izIohj068xcrHqp5fnSPHlBuPQK1KQ1iTHLBTgP5Pyo)

Once the page is loaded, click on the Open menu button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uz4lBtHrEeWJYg65RLEZEQ_49d132e1d04c5f4780248496cb2862a9_open-menu.png?expiry=1706745600000&hmac=ZjjA9dvieFaiyJf_BdNEuWKPuPc6QHYHU4-YnN9v6o0)

Click on Save Page

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yulgZtHrEeWvxwo5BbZD3w_95c855a026ca1f9ee46dcc89fdf1a684_save-page.png?expiry=1706745600000&hmac=5_Xq5blaf8pHAZTgMh-ixMKf3u7Ddv4EhnDIghOEeMY)

Change the output to words.txt and click Save.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dCpcT9HkEeWjTxJlqDdk5Q_74579ba70b10f6838ace79132920a09c_browser-saveas.png?expiry=1706745600000&hmac=Y801ghM-CAeqTNqbq_3Hd6l3gQ1ez8uy89YI_6LL_hU)

2. Open a terminal shell. Open a terminal shell by clicking on the square black box on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uDht9NHlEeWjTxJlqDdk5Q_59733dcbda748c87ea519a603c59a1b5_click-on-terminal.png?expiry=1706745600000&hmac=ymz1dKodoOHVIooO1-51HTjhPUVmWh6F6EeLEczDt4g)

Run cd Downloads to change to the Downloads directory.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/D3jbLdHmEeWvxwo5BbZD3w_21ddb2fc4b5b936ff430f4916f831499_cd-downloads.png?expiry=1706745600000&hmac=afNmBa9LPUKBRDWVoGgGt9BqFj-KV0aGGxhoP-yJO4Y)

Run ls to see that words.txt was saved.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Hd7Eq9HmEeWJYg65RLEZEQ_22db828fa4a603efd16ade721941a08b_ls-downloads.png?expiry=1706745600000&hmac=DONoOaF6Y872FbZDxV3Ye3Pvhhr0TqjenVdAlyYtqUw)

3. Copy file to HDFS. Run hadoop fs –copyFromLocal words.txt to copy the text file to HDFS.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/wn0aLNHmEeWsvw6jxkA2Kw_6293f15086358643bcd5bf838a26d1d5_hdfs-copy-from-local.png?expiry=1706745600000&hmac=HAz6URYuhErSexnZfr6kDvDfINk5Y8lHJp8uYRVo0ug)

4. Verify file was copied to HDFS. Run hadoop fs –ls to verify the file was copied to HDFS.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2yM42tHmEeWjTxJlqDdk5Q_dbf415c58b73622cd051921a03db2303_hdfs-ls-copytohdfs.png?expiry=1706745600000&hmac=enB3lI01kMyu0WPIEz5lPioXT27QWpSFlHo3FY6JULM)

5. Copy a file within HDFS. You can make a copy of a file in HDFS. Run hadoop fs -cp words.txt words2.txt to make a copy of words.txt called words2.txt

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9qrzztHmEeWvxwo5BbZD3w_326c31d619f58fc1fb1382bddfdc047a_hdfs-cp-hdfs.png?expiry=1706745600000&hmac=ze7T78Gh_8tjblf1ILN0dXn-jPnOgiMrTQkvxRjfE64)

We can see the new file by running hadoop fs -ls

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LlBnfdHnEeWsvw6jxkA2Kw_6028df5a8a40bbbbd4c693a4bf3fc637_hdfs-ls-words2.png?expiry=1706745600000&hmac=KGgWfozH4PBAI962m4RLcBo-AcjSSqyepOFcBHfLMu0)

6. Copy a file from HDFS. We can also copy a file from HDFS to the local file system. Run hadoop fs -copyToLocal words2.txt .  to copy words2.txt to the local directory.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Pmza7NHnEeWjTxJlqDdk5Q_8898294ba633ebf95a0c047ded55b59e_hdfs-copy-to-local.png?expiry=1706745600000&hmac=mIczmnFIvHTCLByuI3Lf7yVT6EXiIQ6x1cbQ7We9wiU)

Let's run ls to see that the file was copied to see that words2.txt is there.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5PQU3NHnEeWJYg65RLEZEQ_f6e6d09fbac46549007e4854d7ede006_ls-after-hdfs-cp.png?expiry=1706745600000&hmac=UHPwIzCBvSbylrCm1KTbGVy081YQ5CN4_DVI_x8cy3E)

7. Delete a file in HDFS. Let's the delete words2.txt in HDFS. Run hadoop fs -rm words2.txt

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/rAKY8NHnEeWvxwo5BbZD3w_5178f5b6bee6da6a7e6c7ea6dc3cacd2_hdfs-rm.png?expiry=1706745600000&hmac=Zdq-JE8HFPSdm1ShvPMXoBGp2EKoD1LrxcbRPM6-NMA)

Run hadoop fs -ls to see that the file is gone.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uS7w_tHnEeWsvw6jxkA2Kw_942bc95823a1bd57746d8bc68b6b14dc_hdfs-ls-after-rm.png?expiry=1706745600000&hmac=u8A14uWI41qj3xhxgQh-swWvyYqFM4nBBgg3vDcezvw)