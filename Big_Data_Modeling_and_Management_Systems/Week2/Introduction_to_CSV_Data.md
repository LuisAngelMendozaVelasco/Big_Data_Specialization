# Introduction to CSV Data

By the end of this activity, you will be able to:

1. Identify the key features in CSV data
2. Import CSV data to a spreadsheet and plot values

Step 1. Open a terminal shell. Open a terminal shell by clicking on the square black box on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pYW6JQWREeabsxLXkMIYiw_f85b3afcf7b7a86decd2b0eb43764ecd_click-on-terminal.png?expiry=1706745600000&hmac=0pLx028xMjONEZZGZXSYAbSScaSPUzN3l_BSMm4tems)

Run cd Downloads/big-data-2/csv to change into the directory containing the csv file. (This was downloaded in Week 1 https://www.coursera.org/learn/big-data-managementsupplement/YVDPj/instructions-for-downloading-hands-on-datasets)

```
cd Downloads/big-data-2/csv
```

Step 2. Look at CSV file. The CSV file contains census data for the United States. Run ls to see the name of the CSV file.

```
ls
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mWE-5QWSEea72QqIV6G4Sw_484621732e64603112a902bcae6ee00e_run-ls.png?expiry=1706745600000&hmac=SW0Q5QFmnhefJHZEw39GZN7MajEbILv5aW7tezCZXeM)

Run more census.csv to look at the contents of the CSV file.

```
more census.csv
```

The first line of the file is the head and the remaining lines are the data. Each entry in the file is separated by a comma.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tukduAWXEeaaqg5MSeYjIQ_a2ccda0395686ad549bf0d45998a47d4_csv-parts.png?expiry=1706745600000&hmac=a1GQDaen2RQoDN_NhyNGY5ZXixh8E3feOkQ4n46xsIQ)

Hit the spacebar to scroll down, and q to quit more.

Step 3. Open spreadsheet application. Run oocalc to start the spreadsheet application.

```
oocalc
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AHFe9AWTEeap7RJsurEyGw_eb8ea22ebc8572ade1c77b05149ce8e9_oocalc-empty.png?expiry=1706745600000&hmac=_h_uKrzNqKrPLtPLy4_35qlBBzARAI_zaIR9hTuLG4o)

Step 4. Import CSV to spreadsheet. Let's import the CSV file to the spreadsheet by clicking on File:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/h-pPPQWTEea-2xKMba84Ww_740f036e906acf90a923531f5ad74252_click-file.png?expiry=1706745600000&hmac=vrw66AR4q4ipco9elejxs6h9S6177VccTBcVBGACySY)

Next, click Open: 

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tPhtqgWTEeap7RJsurEyGw_4fd319d0cff53371f5d7d3aaffa1cfa4_click-open.png?expiry=1706745600000&hmac=SmoCY8DSzC5dyfbSE9S-k_86wPeaWUBPz8oOJUg9PK4)

Next, click Downloads in the Places pane:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/012l0wWTEea8MA4ynun-pw_11580358e66464522b93c2df538184b9_click-Downloads.png?expiry=1706745600000&hmac=yQogN4QrCUdWtoqTqyrqHWINBWJo_NeiYsPgDdNqfeU)

Next, double-click big-data-2 in the file pane:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/FaElyAWUEeafYA6MxTJr4Q_66f0f1bc3cbd53339794360b62cb25b1_click-big-data-2.png?expiry=1706745600000&hmac=Btr-WRcMdU8Jgh34-11iZymin7Kj6vsopAMWOmdCfYg)

Next, double-click csv:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QTaG2gWUEeafYA6MxTJr4Q_ee161869c6c860307fe80c8515014faa_click-csv.png?expiry=1706745600000&hmac=eVW_loWwi_PChuuL4F6rec7XmXf-lJ6MMq8sHfxl11M)

Next, double-click census.csv:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qh6b1gWUEeadmQogy2CpoQ_10ffecfb046904ebd3cb2cf00cef3b07_click-census.png?expiry=1706745600000&hmac=XiD0c2NTgmyHSwzRn1GvqedChHi2TdcAowDxtXXu1ak)

In the Text Import dialog, click OK:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GdNB8wWVEeaaqg5MSeYjIQ_d874025d329282c36140cff2006d241f_click-ok.png?expiry=1706745600000&hmac=8dzvmyJ4nwA1fpOMTnA7C_WTa8jiYT-Tktl3dhfwkCM)

The CSV data is now loaded into the spreadsheet.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NsSeegWVEea-2xKMba84Ww_88bb6223a846c6b234d0d39dcb9db0c3_loaded-csv.png?expiry=1706745600000&hmac=TC-Zv8Wi4Qi5-AU628wodQ8KcZ5IWxDF9dFqTuBxseM)

Step 5. See size of CSV. Scroll to the bottom of the spreadsheet to see the size of the CSV file.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/aUgjPAWVEea-2xKMba84Ww_97d3f6b02bdd40b605db2a2d67fca4e1_num-rows.png?expiry=1706745600000&hmac=Cj9eikUtiD95PXGGYEz61PWUw5XN0wHGex9erfYg210)

There are 3194 rows. If the CSV file had millions or more rows, then we could not import it into a spreadsheet. In this case, we would need a Big Data system such as Hadoop to analyze the data.

Scroll back to the top.

Step 6. Create chart. Let's create a chart of the estimated population of the state of Alabama. Row 2 contains the data for Alabama. Select cells in row 2 and columns J through O to get the estimated population for 2010 through 2015.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/7lVDaAWVEeafYA6MxTJr4Q_d0ad16d7d1fdbb8f6db241d4d27d6672_select-JO.png?expiry=1706745600000&hmac=jZcCE7mXIgv7QzLBK1oztHAmVAqJoZK1tmAdbzPEJeo)

Click on the chart button:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/I9Tx4QWWEeadmQogy2CpoQ_7f2e70a6dd0317a520c1e885b57f638f_click-chart.png?expiry=1706745600000&hmac=vyTiYeGGbvrn0E5H7-oXG8I_ykQWc2gX7oevQ5BrvJw)

Click Finish to display the chart:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/YgXPlAWWEea72QqIV6G4Sw_61a91bde66b75594a97476e74c61123e_click-finish.png?expiry=1706745600000&hmac=FmsRkPRtRVmoUHgd05bW0yLY88xGGhqjzlcx6UBxji0)

The chart should be displayed in the spreadsheet:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cb5RBQWWEea72QqIV6G4Sw_2a71f3d226fbc4daa8beb6b729972872_chart.png?expiry=1706745600000&hmac=T_mIpA52MzOFfruhjmw37sFcwTQWFWRf_WkKJfatf94)