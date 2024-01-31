# Exploring Streaming Sensor Data

By the end of this activity, you will be able to:

1. View semi-structured data streaming in real-time from a weather station
2. Create plots of streaming weather station data

Step 1. Open a terminal shell. Open a terminal shell by clicking on the square black box on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pYW6JQWREeabsxLXkMIYiw_f85b3afcf7b7a86decd2b0eb43764ecd_click-on-terminal.png?expiry=1706745600000&hmac=0pLx028xMjONEZZGZXSYAbSScaSPUzN3l_BSMm4tems)

Change into the sensor directory:

```
cd Downloads/big-data-2/sensor
```

Run ls to see the sensor data files and scripts:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/C787xQaTEeahzgq54E2myw_f98e28ea2f30948dcecce4981268b8ad_ls.png?expiry=1706745600000&hmac=UtBtS64eRfdQcftidNl52j8Suo0CwSw07gla_87aW2s)

Step 2. View streaming weather station data. Run stream-data.py to see streaming data from the weather station: 

```
./stream-data.py
```

The measurements are appearing as they are produced by the weather station. By looking at the timestamp, we can see that they arrive about every second. Additionally, different measurement types are produced at different frequencies. For example R1 is measured every second, but R2 is less frequent.

Step 3. View key for measurements. Run more wxt-520-format.txt to see the key for the measurement fields.

```
more wxt-520-format.txt
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lK518QcjEeap7RJsurEyGw_1333c2d1438b1207f3d0f1f9c8b83f46_key.png?expiry=1706745600000&hmac=usowX5MjW7ZeFlKDf-Z9pVnOUbhl_ogylUWVyExsOwY)

Step 4. Create plot of streaming data. We can plot the streaming data by running stream-plot-data.py:

```
./stream-plot-data.py Sm
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/y7nNCgcjEea8MA4ynun-pw_5d870df7cc00e33ed7aef5433526ea97_stream-plot-sm.png?expiry=1706745600000&hmac=L4uH8z948_7_evvhNgE3ZwmuEspq0uk15Mdmca20lcs)

This show a plot of the average wind speed (Sm), and it updated every time a new measurement is produced. Notice that the plot is updated every second. We can create plots for other measurements by specifying the measurement in the last argument to stream-plot-data.py. For example, we can plot air temperature (Ta) by running:

```
./stream-plot-data.py Ta
```

This plot is updated less frequently than the first plot since air temperature measurements are produced less frequently.