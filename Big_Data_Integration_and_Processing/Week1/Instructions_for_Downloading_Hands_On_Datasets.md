# Instructions for Downloading Hands On Datasets

This Reading describes the steps to download the datasets and scripts necessary for the Hands On exercises in this course. Before proceeding, make sure have you downloaded and installed VirtualBox and the Cloudera virtual machine. Instructions for this process can be found in the Reading called Downloading and Installing the Cloudera VM.

Step 1. Start the Cloudera VM. Most of the Hands On exercises in this course use the Cloudera Virtual Machine, so we will download the datasets onto the VM. Start the VM in VirtualBox and perform the remaining steps in the VM.

Step 2. Open a web browser. Open a web browser by clicking on the web browser icon in the top toolbar.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Zc2s0wpTEea72QqIV6G4Sw_c49276790fe7fd0f65defdbcb24b12e9_web-icon.png?expiry=1706832000000&hmac=eeVDUYZRTAwuX8cxmS6I-uqGXtcjBMl1gekk9OUvNS0)

In the web browser, enter the following for the URL:

http://github.com/words-sdsc/coursera

Step 3. Download the datasets. Click on big-data-3.zip:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CeqUAFRKEeaFpQoKLtdtHw_3f1b27de02366c8b2da53b158a2bcc42_big-data-3-zip.png?expiry=1706832000000&hmac=JnGCZ4mdN64-E8o7h39X3Tsc-wQmMrmrP10zcUvM-2c)

Click on the Download button:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LQ9mjVW-EeaWRg7WBfqodw_ff3372ce9839c06375e0908164430626_download.png?expiry=1706832000000&hmac=eIoME82xWhl2khpqs6_4vtKlzYoCdk8I0bfUiMQi1sU)

In the dialog, select Save File:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fWZ-QBIZEeaYgw5Bgpijyw_bf3488086a4a225faa0c7d97b4dcc3e8_select-save.png?expiry=1706832000000&hmac=jRVCfkrog5UauIRII1tolckEZFRBBFgq7lpwKXxsKx4)

Click OK, and the file big-data-3.zip file will be downloaded to the Downloads directory.

Step 4. Uncompress the datasets. Open a terminal shell by clicking on the terminal shell icon in the top toolbar.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QbUwLgpVEeafYA6MxTJr4Q_0bb1c1fbfc08472b5e5046ea700e50ce_click-on-terminal.png?expiry=1706832000000&hmac=aK7ilXM_d6u7yS8SH4DuhkwzxCCM3B3ln1vfhZzctKY)

In the terminal, run:

```bash
cd Downloads
unzip -o big-data-3.zip
```

Step 5. Install tools. Change directories to big-data-3 and run setup.sh to install tools and libraries.

```bash
cd big-data-3
./setup.sh
```

During the setup process, Anaconda will give you a series of prompts. First, press enter to continue the installation:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/K7L8TlXEEeaWRg7WBfqodw_85ff85761217f5381e7d24a752727315_anaconda-enter.png?expiry=1706832000000&hmac=nxT7wYH_7m2xOR6fZvdyinkSiLURNXO1HBlHY3Xhya8)

Next, read and accept the license:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RuD-OlXEEeaX4QpLJOK7gQ_725952c670089d2d9619ed65513b1dfa_anaconda-license.png?expiry=1706832000000&hmac=Sl6qUXNiJtIi6oDw5X1cJunelkXg60_CG2B1NGNZEq4)

Next, press enter to accept the default installation location:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Y6nr3VXEEeaubA6-qtnryw_7f071cc1f69ca98c8b6ca1226ffe4cf9_anaconda-location.png?expiry=1706832000000&hmac=AXKu-vBo7rleX8Lrmh_aF4qIqex47gxsjcb7ZeTSYdY)

Next, enter yes when it asks if you want to prepend the install location to PATH:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/i9UgMFXEEeaFpQoKLtdtHw_1aa3ab3deebc8bc0c65ca0b00b19f016_anaconda-path.png?expiry=1706832000000&hmac=PZoy1FmlZI_-XjEDRn5FlozX9Ul_kWhFZzIcdFMI85E)

The setup of tools and datasets should continue.

Finally, source $HOME/.bashrc:

```bash
source $HOME/.bashrc
```