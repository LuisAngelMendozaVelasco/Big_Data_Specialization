# Exploring Graph Data Models with Gephi

By the end of this activity, you will be able to:

1. Import a CSV file into Gephi
2. Perform statistical operations and layout algorithms on graph data in Gephi

NOTE: Gephi should be run on your native hardware, not in the Cloudera VM. Instructions for downloading, installing, and running Gephi can be found at https://gephi.org/users/install.

Step 1. Download and import CSV file. In your web browser, go to the following link:

https://raw.githubusercontent.com/words-sdsc/coursera/master/big-data-2/graph/diseaseGraph.csv

Click on File, and choose Save as to download the file 

In Gephi, click on File, and choose Import spreadsheet:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/DFTaRgy1EeaPWQ4W01MnNw_9a5cc92e2512290b975c37004f2e595c_file-import.png?expiry=1706745600000&hmac=OUMzogb4_J6vzt4Vf0FltJ0r8-mZa742nqUYmnHPoc4)

In the Import spreadsheet dialog, click on ... to choose the CSV file:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3FKMhQy1EeaoAApEy_ybaw_f91926c7ecbe09f8ad7fa205af17b292_click-dotdotdot.png?expiry=1706745600000&hmac=FB5ZNLzLVx3tqx4pmGApvMlhSxT9TSfMvoH-Wu4LqmU)

In the File dialog, choose the diseaseGraph.csv file you downloaded:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/C4yLNgy2EeaXgRIBDEQQXw_60c07fddedd4aa0bfd9f0943a7ca5c64_choose-csv.png?expiry=1706745600000&hmac=GSs3x_ci3lPn6sQKDC-ifnwq0KtaeubxJwKL55tDuGo)

Next, in the dialog, make sure As table is set to Edges table:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VJhYBQy2EeaH8A5fACH5-Q_f24761c543a1dd0620c8c0e58022ac0d_as-table.png?expiry=1706745600000&hmac=zbntisOPAmDaIjYnRhHcLBsIQ5TOL28mTPu2lOFELrs)

Click Next, and then click Finish to import the CSV data into Gephi.

Step 2. Examine graph properties. In the middle pane, Gephi displays the graph. The black circles are the nodes, and the lines between them are the edges.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/p5Ldmwy2EeaXgRIBDEQQXw_aeafd2ef8779fdf30dbf5d51de681302_graph.png?expiry=1706745600000&hmac=0C5g4t4SvtPhpC9Nvdagl0HCuYEN7Z4IpR5q52hGJ9o)

If you place the mouse on a node, then Gephi will highlight the nodes that connected to it:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1YSlygy2EeafmhI8WYbMQQ_b11072aee8e6ea1885e15cbe349e5abd_mouse-connected.png?expiry=1706745600000&hmac=F0YldCFD1zePTYhFM0B8VKvosvLzNxR1vKR3j8_u2PE)

In the top right is the Context pane, which says that the graph has 777 nodes and 998 edges.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/W5nSDQy1EeaH8A5fACH5-Q_d956d6074a4d773fa028c40edfc6a499_context.png?expiry=1706745600000&hmac=I-J31NybAEfFGUhPeButbCl9npflWMpjXkcS95HulDs)

Step 3. Perform statistical operations. Below the Context pane, is the Statistics pane, where you can perform various statistical calculations. We can calculate the average degree by clicking on Run next to Average Degree.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4SCkrwy3Eea4GxJaWHxGOw_3461082135087695d645e1bcb91d3438_average-degree.png?expiry=1706745600000&hmac=LmEMmCrUdHoRmBhydSvH34DeyxAxEnK8NYjddABi3l4)

The dialog that pops up says that the average degree is 2.569. Click on Close to close the dialog.

Next, we can calculate the connected components by clicking on Run next to Connected Components: This will present a dialog box with the title, "Connected Components settings" and ask for either "Directed" or "Undirected" calculations. 

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RZdVEwy4Eea4GxJaWHxGOw_d54e23c3b87632f8ebf379ca8ae38346_connected-components.png?expiry=1706745600000&hmac=wjLxVjErtSnN0VbuM1nrROdnZDbJN3RnjWye045Zsas)

The resulting dialog says there are 5 weakly connected components and 761 strongly connected components. Click Close to close the dialog.

Step 4. Run layout algorithms. Gephi can perform different layout algorithms on the graph. In the Layout pane on the bottom left, click on the --Choose a layout combo box and select Force Atlas, and click on the Run button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/EmXntgy5EeaPWQ4W01MnNw_fe97e3a28b8c05edbb46b46213f50c6a_choose-force-atlas.png?expiry=1706745600000&hmac=OgioSnpwpJtXC5nWnOjzTj6hz0LJvdm71UX0CzChFyA)
 
Gephi will change the layout of the graph, and after some time, click on the Stop button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Vsurqwy5Eea4GxJaWHxGOw_c825debffc7f42c4bd255dd8e2d8e3aa_force-atlas-layout.png?expiry=1706745600000&hmac=3gmWR1zIWM1UtA6PBQue-_HRCmVpvzKGeoWpCYj5i4g)

In this layout, strongly connected nodes are clustered together, and we can also see several clusters that are disconnected from the rest of the graph.

In the Layout combo box, select Fruchterman Reingold and click on the Run button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pL_gFAy5EeafQQq9AcsuKQ_68b3b07bb2f15cbcd4a46ed61ed93550_choose-fr-layout.png?expiry=1706745600000&hmac=Yej0jUm05jqWV81ZQThKWwTCPasHm9gfCFm0HeqIE1s)
 
The graph layout will change to make the nodes evenly spaced. After the graph stops moving, click on the Stop button, and then on the magnifying glass icon in the middle-left bottom to center the graph.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z3g0pgy6EeafmhI8WYbMQQ_9fc11247d1a395b5d75a50f58d614f1b_magnifying-glass.png?expiry=1706745600000&hmac=m6Wc88CnFcpvWhElmnVmB7iGEWKWo-5_4NE1hLeJacY)

In this layout, we can better see which nodes have a lot of edges.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/B1NSCAy6EeaoAApEy_ybaw_2e3a34576ed64a40682e8d23169779ec_fr-layout.png?expiry=1706745600000&hmac=8iPGzW5LRkoZhjV1SwRcdsF05NrkVdwghbTxvTpdRkc)