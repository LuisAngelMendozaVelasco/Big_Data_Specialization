# Downloading and Installing the Cloudera VM Instructions (Windows)

**Learning Goals**

In this activity, you will:

- Download and Install VirtualBox.
- Download and Install Cloudera Virtual Machine (VM) Image.
- Launch the Cloudera VM.

Hardware Requirements: (A) Quad Core Processor (VT-x or AMD-V support recommended), 64-bit; (B) 8 GB RAM; (C) 20 GB disk free. How to find your hardware information: Open System by clicking the Start button, right-clicking Computer, and then clicking Properties. Most computers with 8 GB RAM purchased in the last 3 years will meet the minimum requirements.You will need a high speed internet connection because you will be downloading files up to 4 Gb in size.

**Instructions**

Please use the following instructions to download and install the Cloudera Quickstart VM with VirutalBox before proceeding to the Getting Started with the Cloudera VM Environment video. The screenshots are from a Mac but the instructions should be the same for Windows. Please see the discussion boards if you have any issues.

1. Install VirtualBox. Go to https://www.virtualbox.org/wiki/Downloads to download and install VirtualBox for your computer. The course uses Virtualbox 5.1.X, so we recommend clicking [VirtualBox 5.1 builds](https://www.virtualbox.org/wiki/Download_Old_Builds_5_1) on that page and downloading the older package for ease of following instructions and screenshots. However, it shouldn't be too different if you choose to use or upgrade to VirtualBox 5.2.X. For Windows, select the link "VirtualBox 5.1.X for Windows hosts x86/amd64" where 'X' is the latest version.
2. Download the Cloudera VM. Download the Cloudera VM from https://downloads.cloudera.com/demo_vm/virtualbox/cloudera-quickstart-vm-5.4.2-0-virtualbox.zip. The VM is over 4GB, so will take some time to download.
3. Unzip the Cloudera VM:

    Right-click cloudera-quickstart-vm-5.4.2-0-virtualbox.zip and select “Extract All…”

4. Start VirtualBox.
5. Begin importing. Import the VM by going to File -> Import Appliance

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1YHbnrvaEeWbLwqB7NyVNQ_18b3b1a489e3d9ce53e7b3975d38910a_Untitled.png?expiry=1706745600000&hmac=DZGRq9576bvyjlIBEIs_XRJN9l30V6ulYXDEqAOYzgk)

6. Click the Folder icon.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/EUf7pLvbEeWHhw4MvaB3nw_98aed876336d826ba38b3ff967f59341_Untitled1.png?expiry=1706745600000&hmac=Or3uu3lvGBeu6AcIC6XigXMT3VpIQKcuPTD55U0GySU)

7. Select the cloudera-quickstart-vm-5.4.2-0-virtualbox.ovf from the Folder where you unzipped the VirtualBox VM and click Open.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/kvXZY7vdEeW6FApX76Rguw_04212a7fd040cdd18258055596ba98a7_Untitled2.png?expiry=1706745600000&hmac=ol5ihABPzmzFb45cupGdM6m_WrRSBPYzuK1GwQ2i7I4)

8. Click Next to proceed.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/05MjOLvdEeWHhw4MvaB3nw_d8ba793c18835387ddb02defba586569_Untitled3.png?expiry=1706745600000&hmac=qRKavH4L_LDe11B_7O2tOAikGrOk2nwZoYEznydWHqY)

9. Click Import.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8ZNYCrvdEeWg-hLO0rEOAw_af0950df42ffc15de1631a512eb6aa46_Untitled4.png?expiry=1706745600000&hmac=hoVsiX739AoDNqy6-WeGSHbx-EVQ2qnhR4fzW7YrVhE)

10. The virtual machine image will be imported. This can take several minutes.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AoLTKrveEeWW3xLV17cwNw_b371ba33d261f8b00ac357da5590e2d6_Untitled5.png?expiry=1706745600000&hmac=K7g7rPTgYjtaI1uStsv3bFFSK_Y_nYUD5fmpBbQ_Nm0)

11. Launch Cloudera VM. When the importing is finished, the quickstart-vm-5.4.2-0 VM will appear on the left in the VirtualBox window. Select it and click the Start button to launch the VM.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HdSw4rveEeWg-hLO0rEOAw_8e77353aeafcc336742baf76aa647c8a_Untitled6.png?expiry=1706745600000&hmac=J5Hwjajvb84KHhJM2FW4mG0-Pm-r-S_jhZqzgUnYnOs)

12. Cloudera VM booting. It will take several minutes for the Virtual Machine to start. The booting process takes a long time since many Hadoop tools are started.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VKeShLveEeWHhw4MvaB3nw_bfb04aa6c0c0e0705514e617f45b1a86_Untitled7.png?expiry=1706745600000&hmac=0Rmf8VnBGN-AEJ-Qvl9OCYYUTPCJst8gftL_xyTqENs)

13. The Cloudera VM desktop. Once the booting process is complete, the desktop will appear with a browser.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vlPlZruyEeWHhw4MvaB3nw_f128a6a6651d531d31a01f8c4ed79f53_vm-started.png?expiry=1706745600000&hmac=Bauu_hwcZGzypRGjfP3KbF-pfe4hpf7WGwTDA2zt2Vs)