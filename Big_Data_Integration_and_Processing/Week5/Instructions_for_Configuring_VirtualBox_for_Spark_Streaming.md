# Instructions for Configuring VirtualBox for Spark Streaming

Spark Streaming requires more than one executor. This Reading describes how to configure VirtualBox so that the Cloudera VM has more than one virtual processor.

Step 1. Stop the Cloudera VM. Before we can change the settings for the Cloudera VM, the VM needs to be powered off. If the VM is running, click on System in the top toolbar, and then click on Shutdown:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GsZrdF8SEeafuBI2oAYa8w_a598868bbbe0914586f3ee1f17313b71_shutdown.png?expiry=1706832000000&hmac=1rL0FT3hgD9WIBmSmnLazQq4D9DrJVJH9RiS-ltsris)

Next, click on Shut down:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/DdZY018SEeafuBI2oAYa8w_8e1003755bdeb2ce175c3850e9cd0124_shutdown2.png?expiry=1706832000000&hmac=2AvxsebvN1A--OK5wZ8c_i419auASeMP_WzcyVEaNok)

Step 2. Change number of processors. Once the Cloudera VM is powered off, select the Cloudera VM in the list of virtual machines in the VirtualBox Manager:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zGZKll8QEeafuBI2oAYa8w_7290e5254b633f6f5f05eb4e76ed618a_select-vm.png?expiry=1706832000000&hmac=_SrYmp1Zh3IgWAdrsgOP9qvx7ehwcisT8I8ejcMsX5s)

Next, click on Settings:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fTqm8l8QEeafuBI2oAYa8w_fffc83a3e3136eca661c460538c2408c_settings.png?expiry=1706832000000&hmac=zl0Nji1yxGEYLag4ypOeZbcX62_w4qgu2amk3j9n2DI)

Next, click on System:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hM72GV8QEeag5RL6-p1mNw_f9dcf0d85024ffc644a62738de676688_system.png?expiry=1706832000000&hmac=DzJu84i6950AstIAJpdNDRkcfaFtcTU3G69uzqX2Phk)

Next, click on Processor:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/keXKm18QEeag5RL6-p1mNw_dd6d0586d6fa10f6e33de13008d45887_processor.png?expiry=1706832000000&hmac=1gsjch3AHIqyPWWxeQGaDHdAY_jKDtvEa3vp8_Y1JJM)

The default number of processors is one. Change this to two or more:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mu_Iql8QEea_kQpIKmAlQw_ec3aebb7b7b75ec3d2ff6f8d33eb64b1_change-to-2.png?expiry=1706832000000&hmac=EpqJm_fTS28EN9AKaIAFEDK4WqqeGuWuwlb-roRgkQg)

Finally, click on OK and start the Cloudera VM.