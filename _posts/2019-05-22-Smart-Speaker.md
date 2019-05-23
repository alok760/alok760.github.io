---
title:        "Make Your own Smart Speaker with SUSI.AI (In Progress article)"
description:  "Learn to make your own smart speaker with a raspberry pi"
image:        "smart_speaker.jpg"
author:       "Alok"
---

![susi.ai smart speaker](/assets/smart_speaker.jpg)

If you're worried about privacy concerns when using smart assistants or just want to build your own one with complete freedom then this guide will help you. SUSI.AI provides Artificial Intelligence for Smart Speakers, Personal Assistants, Robots, Help Desks and Chatbots. SUSI.AI is a completely free and open source software.

In this guide we will be building our own smart speaker assistant which will talk to the user just like Alexa or Google home. The keyword will be "SUSI".

Things you will need
- Raspberry Pi
- Respeaker 2-mics Hat / usb mic / usb sound card
- sd card
- speaker
- 3.5mm Aux cable/ JST PH2.0 connector

![components](/assets/components.jpeg)

#### Step 1 Download and flash the image
1. Download the latest Susibian image from https://github.com/fossasia/susi_installer/releases.
   The downloaded image will look something like susibian-xxxxxxxxxxxx.img.xz
2. Insert the SD card in your PC
3. If you're on linux open up a terminal and go to your downloads folder(or the place where the image is downloaded) and type the following commands


<b> Extract the image </b> <br>
`tar xvf susibian-<timestamp>.img.xz` <br>
Example <br>
`tar xvf susibian-201905170311.img.xz`

<b> Write the image to sd-card </b> <br>
`sudo dd if=<path_to_downloaded_image_file> of=/dev/sdX bs=4M status=progress`<br>
Example <br> `sudo dd if=/home/alok/Downloads/susibian-201905150334.img of=/dev/sdc bs=4M status=progress` <br>
(find the diskname of your sd card by typing `lsblk`)


#### Step 2 Choosing the required hardware
- As this is a smart speaker we will need both a microphone and a speaker
- Setting up using respeaker hat
  - ReSpeaker 2-Mics Pi HAT is a dual-microphone expansion board for Raspberry Pi designed for AI and voice applications. - - http://wiki.seeedstudio.com/ReSpeaker_2_Mics_Pi_HAT/
