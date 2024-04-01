# Troubleshooting FAQ
This document will go over the issues that arose with my experience and how I fixed them.
 
# 
 






- What GPS adapter should I use?
  
Most guides I've read use the [GlobalSat BU-353-S4](https://www.amazon.com/GlobalSat-BU-353-S4-Receiver-Black-Improved-New/dp/B098L799NH). In this guide, we used the [Waveshare L76X](https://www.waveshare.com/l76x-gps-hat.htm). I'm sure that's the better option if you're into following the consensus of more expereienced people. In hindsight, the Waveshare option is fine. We mostly ignored the manual since it suggests you download software that's entirely Chinese. I'm not necessarily saying that it is or isn't malware, it just seems entirely unncessary to use since we completed the project without using it (despite me actually attempting to use it at first).

- What network adapter should I use?

We used the [Panda Wireless PAU05](https://www.pandawireless.com/panda300mbps.htm). This was supplied by our instructor, thankfully. Can't really go too wrong with whatever network adapter you choose. We were going to use the [AWUS036ACH](https://www.alfa.com.tw/products/awus036ach?variant=36473965871176), but downloading the drivers onto our RPI was extremely annoying for some reason.

- Why can't I download GPSD?

Probably because you didn't update/upgrade. Double-check and make sure you ran the commands as listed in the doc. I skipped at first this thinking it was just another "did you turn it on and off?" type of step. If it's still not working, check out their troubleshooting guide [here](https://gpsd.gitlab.io/gpsd/troubleshooting.html).

- Why won't the PPS light turn on

The antenna has to be in an area where it can receieve some sort of signal. First, make sure it's properly connected. The small pin connector onto the board is really annoying to connect. Second, make sure the antenna is (preferably) outside or on a window. If it can't receieve a signal, it won't turn on. 

- Why does Kismet tell me I can't convert my files to .csv?

Kismet files can't be converted to .csv unless they have a GPS signal attached or included within the files. The likely cause for this is that Kismet hasn't been configured to accept and read GPS signals from GPSD. The steps to properly do so are listed within the Kismet setup.

