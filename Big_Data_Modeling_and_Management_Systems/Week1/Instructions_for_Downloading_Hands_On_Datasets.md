# Instructions for Downloading Hands On Datasets

This Reading describes the steps to download the datasets and scripts necessary for the Hands On exercises in this course. Before proceeding, make sure have you downloaded and installed VirtualBox and the Cloudera virtual machine. Instructions for this process can be found in the Reading called Downloading and Installing the Cloudera VM.

1. Start Cloudera VM. Most of the Hands On exercises in this course use the Cloudera Virtual Machine, so we will download the datasets onto the VM. Start the VM in VirtualBox and perform the remaining steps in the VM.
2. Open web browser. Open a web browser by clicking on the web browser icon in the top toolbar.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Zc2s0wpTEea72QqIV6G4Sw_c49276790fe7fd0f65defdbcb24b12e9_web-icon.png?expiry=1706745600000&hmac=lBbisF9RGuusjIH1K_fpgKxy1I17ouqWYXtQkbfTbAI)

In the web browser, enter the following for the URL:

http://github.com/words-sdsc/coursera
  
3. Download datasets. Click on big-data-2.zip:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RE2joxIZEealrgo0ik8CQQ_6dea08fba51046a1c5ce029cb5197289_click-big-data-2.png?expiry=1706745600000&hmac=jejik_XAu2l1HWAUNwJoH2ll6UdKekROvQL21uhJSoM)

Click on the Download button:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uYg_dVW-Eea3kBK2xkPy7w_063b2d28e28ea481ec4a64571e65fdff_download.png?expiry=1706745600000&hmac=5dcmgqSXSutYZBjpKftnEEBWme0J_EsiT2NHGk0xv8g)

In the dialog, select Save File:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fWZ-QBIZEeaYgw5Bgpijyw_bf3488086a4a225faa0c7d97b4dcc3e8_select-save.png?expiry=1706745600000&hmac=X_ugRQy6BAyp2n0W_v7lVGMkx0h5qQvi199pzaW8IuA)

Click OK, and the file big-data-2.zip file will be downloaded to the Downloads directory.

4. Uncompress datasets. Open a terminal shell by clicking on the terminal shell icon in the top toolbar.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QbUwLgpVEeafYA6MxTJr4Q_0bb1c1fbfc08472b5e5046ea700e50ce_click-on-terminal.png?expiry=1706745600000&hmac=oOtnplUCWEEr0z9sEhTlu0325ucsBBUga-p8PJE9hFY)

In the terminal, run:

```
cd Downloads
unzip -o big-data-2.zip
```

5. Install tools. Finally, change directories to big-data-2 and run setup.sh to install tools and libraries.

```
cd big-data-2
./setup.sh
```