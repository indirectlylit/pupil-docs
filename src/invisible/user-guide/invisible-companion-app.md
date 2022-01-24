---
permalink: /invisible/user-guide/invisible-companion-app
description: Get familiar with Pupil Invisible Companion app!
---

# Invisible Companion App
Get familiar with Pupil Invisible Companion app!

## Home View
<div class="pb-4" style="display:flex;justify-content:center;">
  <v-img
  :src="require('../../media/invisible/invisible-companion-app/invisible-companion-intro.jpg')"
  max-width=80%
  >
  </v-img>
</div>

1. **Scene camera icon**: This icon shows when the scene camera is connected. The color dot will appear only when the scene camera is connected. A color trail will appear along the gray ring during recording. Gaps in the trail signify a disconnect of this camera.
2. **Eye camera icon**: This icon shows when the eye cameras are connected. The color dot will appear only when the eye cameras are connected. A color trail will appear along the inner gray ring during recording. Gaps in the trail signify a disconnect of these cameras.
3. **Recording time**: Display of the elapsed recording time.
4. **Active wearer**: The currently selected wearer.
5. **Active template**: Click this button to fill out the fields of the active template.
6. **Menu**: Main app naviagation. Access recordings, wearers, templates, settings.
7. **Info**: Press this button to see information about remaining recording time, glasses and scene camera info, and the name of your Companion Device.
8. **Record**: Press this button to start or stop a recording.
9. **Preview**: Press this button to see a real-time preview of your scene video with gaze overlay.


## Pupil Cloud Sign Up

Your purchase of Pupil Invisible includes a free membership to [Pupil Cloud](/cloud). First time users need to Sign Up 
using a Google account, or by creating an account with email address and password.

### Automatic uploads to Pupil Cloud

Pupil Cloud enables you to privately and securely upload your recordings from your Companion Device to cloud storage. 
The usage of this feature is **optional***. You can turn this feature on/off during setup, or at any later time in the 
app settings. Learn more about [Pupil Cloud](/cloud).

*200Hz gaze data is provided in Pupil Cloud. On the Companion Device, gaze data is available at 66Hz in real-time.
<v-divider></v-divider>

## OnePlus 6 Companion Device Setup

::: warning
The information in this section is only required for **OnePlus 6** Companion Devices. OnePlus 8 devices do not require the below steps.
:::

### Enable OTG
USB On-The-Go (OTG) must be enabled for Invisible Glasses to connect to your Companion Device.

Check out the video for a demonstration of how to add OTG to quick settings and enable OTG.

<div style="display:flex;flex-direction:row;justify-content:center;" class="pb-4">
    <video style="max-height: 700px;" controls muted>
      <source src="../../media/invisible/invisible-companion-app/videos/usb_otg_oneplus6.mp4" type="video/mp4">
    </video>
</div>


### Enable Application Lock

Lock Pupil Invisible Companion App to the overview to ensure the app keeps running even when your screen is off.

Check out the video to see how to lock the app.

<div style="display:flex;flex-direction:row;justify-content:center;" class="pb-4">
   <video style="max-height: 700px;" controls muted>
     <source src="../../media/invisible/invisible-companion-app/videos/app_lock_oneplus6.mp4" type="video/mp4">
   </video>
</div>

## Time synchronization

The Pupil Invisible Companion App runs its own clock as the source for all data timestamps it generates. To start this clock the App samples the phone’s NTP (Network Time Protocol) synchronized UTC clock.

If more that one device is used and the data is required to be synchronised, make sure all devices have recently been connected to the internet and automatic time setting is active in the operating system settings.

Pupil Monitor will warn you if a device is not in sync.

More info on the technical implementation and quality of NTP synchronisation can be found in the [Pupil Invisible developer docs](/developer/invisible/#time-synchronization "Pupil Invisible developer docs - time synchronization").

## Recording transfer
The recommended way to transfer recordings off of the Companion Device is to upload them to Pupil Cloud. Recordings can be analyzed in Pupil Cloud directly or downloaded to a computer. 

In case usage of Pupil Cloud is not an option, recordings can also be transferred to a computer directly using a USB connection. 

Both options are described in more detail below.

### Pupil Cloud

Pupil Invisible recordings **can only be** uploaded to Pupil Cloud directly from the Invisible Companion App. We recommend using Pupil Cloud for ease of use, stability, robustness, and data security. 

If you made recordings with the Invisible Companion App while the cloud upload was disabled, you can re-enable and upload recordings to Cloud as follows:

1. Enable 'Cloud Upload' in the Companion App settings.
2. Wait until your recording(s) are uploaded to Pupil Cloud. In the recording view, uploaded recordings will show a cloud symbol with a tick
3. Login to [Pupil Cloud](https://cloud.pupil-labs.com "Pupil Cloud") to playback recordings, enrich data, and download.

### Local transfer

:::tip
<v-icon large color="info">info_outline</v-icon>
Recordings transferred locally will contain gaze data at 66 Hz (estimated in real-time on the Companion Device). Only 
recordings uploaded to Pupil Cloud are densified to 200 Hz.
:::

To transfer recordings to a computer using a USB connection you need to first export the recordings to the Android filesystem and then access the filesystem from your computer.

Note that the export process does not delete the recordings from the Invisible Companion App, and you can still upload 
to Pupil Cloud at a later date if required. 

Recordings that are deleted from the Invisible Companion App, e.g. to free up storage space, cannot be transferred back 
to the Invisible Companion App from your backup location (including Pupil Cloud, a laptop/desktop PC, or external HD). 

This means that if you delete the recordings prior to a Pupil Cloud upload, they cannot be uploaded to Pupil Cloud at a 
later date.

**Export from Invisible Companion App**
1. Open recordings view in Invisible Companion App
2. Select desired recording/s
3. Export:
   - For single recordings, the export button is found by clicking on the 3 vertical dots to 
     the right of the cloud symbol
   - For multiple recordings, click the download symbol at the bottom of the screen    
4. Exported recordings will be saved to the `Pupil Invisible Export` folder on the Android filesystem.
    
**Transfer Exported Recordings to a Computer**
1. Connect your OnePlus device to a PC via USB (using the USB cable supplied)
2. Slide down from the top of the device's home-screen and click on 'Android System - USB charging this device'
3. Click on 'Tap for more options'
4. Select 'Transfer Files'
5. Open File Browser on your PC and access the Internal shared storage of your OnePlus device
6. Pupil Invisible recordings can be found in the `Pupil Invisible Export` folder
7. Copy the recordings to your computer before opening them in Pupil Player.

::: tip
<v-icon large color="info">info_outline</v-icon>
On macOS, you require the <a href="https://www.android.com/filetransfer/" alt="Android File Transfer website">Android File Transfer</a> to browse and transfer files between your Mac computer and your Android device.
:::
