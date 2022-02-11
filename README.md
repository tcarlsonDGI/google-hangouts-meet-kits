# Google Hangouts/Meet Kits
Ture Carlson - Feb2022

<!-- 
Everything you didnt know you needed to know but Google didn't tell us for some reason 
-->

## Table of Contents

1. [Overview](#overview)
1. [What you'll need](#whatyoullneed)
1. [Where to Get ChromeOS Images](#images)
1. [How to know what 'mode' the device is in](#mode)
1. [CTL Google Meet Compute System](#ctl)
    - [Creating the recovery USB](#ctl-usb)
    - [Recovering the Meet Compute System](#ctl-recovery)
1. [Asus Chromebox4](#asusChromebox4)
    - [Creating the recovery USB](#asus-chromebox4-usb)
    - [Re-imaging the Chromebox4](#asus-chromebox4-recovery)


## <a name="overview"></a>Overview
For deploying a Google Meet/Hangouts system, there are a few different hardware options that DGI has deployed. This guide will be updated to reflect any new hardware that we run into. 

As of now, we have deployed the following devices: 
- Google Meet Compute System (generally sold as part of a Meet/Hangouts kit)
- Asus Chromebox4 (A standard ChromeOS device that *may* need to be configured for Google Meet/Hangouts)

The purpose of this guide is to assist in the configuration of these systems in the event they are set as a standard ChromeOS device, where they should be in a Hangouts/Meet appliance mode.

## <a name="whatyoullneed"></a>What you'll need
- a USB-A thumb drive (8 GB or larger)
    - **THIS WILL BE WIPED**
- Google Chrome on a separate machine

## <a name="images"></a>Where to get ChromeOS Images (not required for Google Meet Compute System)
Find your device [here](https://cros.tech/), and download the **EARLIEST** available firmware verison.

## <a name="mode"></a>How to know what 'mode' the device is in
 - The device's login screen should **ONLY** show an enterprise login option when in Hangouts/Meet appliance mode
 - **IF** there are other options for login, the device will need to be re-imaged and re-configured

<!-- 
CTL Meet Compute System
-->
# <a name="ctl"></a>CTL Google Meet Compute System
![CTL Meet Compute System](https://cdn.shopify.com/s/files/1/1382/9181/files/on-verticle-base_600x600px2_800x800.png)

If the CTL Meet Compute System is not showing a splash screen that reads something akin to "Your Hangouts/Meet Hardware is ready to use", you need to re-image the device.

## <a name="ctl-usb"></a>Creating the recovery USB
1. If not already installed, install Google Chrome on your machine
2. Install the [Meet Compute System Recovery Utility](https://chrome.google.com/webstore/detail/meet-compute-system-recov/odkacekibiibhidpiopcmgbgebkeoced?hl=en) chrome extension
3. Insert a usb thumb drive into your machine 
    - **This will be wiped** and loaded with a bootable image
4. Click the 'puzzle piece' extensions icon in Google Chrome, and open the Meet Compute System Recovery Utility

*Recovery Utility Step 1 of 3*

5. Click the blue 'Get started' button
6. Click 'Select a model from a list', then select 'CTL' for manufacturer, and 'CTL Meet Compute System' for model

*Step 2 of 3*

7. Select the USB drive you wish to wipe and use to create the recovery USB from the drop-down, and click 'continue'

*Step 3 of 3*

8. Click 'Create now' to wipe your USB, and flash the recovery utility.

## <a name="ctl-recovery"></a>Recovering the Meet Compute System
1. Make sure the Meet Compute System is powered off, and disconnected from ethernet
2. Insert the recovery USB into the device
3. Using a paperclip, hold the recovery button and power on the device.
    - The recovery button is inside the small hole just above the Kensington lock slot
    - Keep holding the button until you see a recovery screen appear on the attached display. You can release the button now.
4. The system should re-image off of the recovery USB, and boot into Meet/Hangouts appliance mode.
    - If the system loads into a standard ChromeOS login, press ```Ctrl-Alt-H``` on an attached USB keyboard to flip the device into Meet/Hangouts mode
5. You should now be safe to connect the System to ethernet and sign-in using enterprise login credentials.

<!--
Asus Chromebox 4
-->
# <a name="asus-chromebox4"></a>Asus Chromebox 4
![Asus Chromebox 4](https://dlcdnwebimgs.asus.com/gain/814d6587-b057-406a-b211-7dcbce1ab97e/w692)
If the Asus Chromebox 4 is not showing a splash screen that reads something akin to "Your Hangouts/Meet Hardware is ready to use", you need to re-image the device.

## <a name="asus-chromebox4-usb"></a>Creating the recovery USB
1. If not already installed, install Google Chrome on your machine
2. Download the recovery image **version 86** for the Asus Chromebox 4
    - Refer to the [Where to Get ChromeOS Images](#images) section of this guide for downloading ChromeOS images
3. Install the [Chromebook Recovery Utility](https://chrome.google.com/webstore/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm?hl=en) chrome extension
4. Insert a usb thumb drive into your machine 
    - **This will be wiped** and loaded with a bootable image
5. Click the 'puzzle piece' extensions icon in Google Chrome, and open the Meet Compute System Recovery Utility

*Recovery Utility Step 1 of 3*

6. Click the blue 'Get started' button
7. Click the 'gear' icon in the upper right corner of the utility window, and select 'Use local image'

*Step 2 of 3*

8. Select the USB drive you wish to wipe and use to create the recovery USB from the drop-down, and click 'continue'

*Step 3 of 3*

9. Click 'Create now' to wipe your USB, and flash the recovery image.

## <a name="asus-chromebox4-recovery"></a>Recovering the Meet Compute System
1. Make sure the Chromebox is powered off, and disconnected from ethernet
2. Insert the recovery USB into the device
3. Using a paperclip, hold the recovery button and power on the device.
    - The recovery button is inside the small hole just above the Kensington lock slot
    - Keep holding the button until you see a recovery screen appear on the attached display. You can release the button now.
4. The system should re-image off of the recovery USB, and boot into Meet/Hangouts appliance mode.
5. Press ```Ctrl-Alt-H``` on an attached USB keyboard to flip the device into Meet/Hangouts mode
6. You should now be safe to connect the System to ethernet and sign-in using enterprise login credentials.







