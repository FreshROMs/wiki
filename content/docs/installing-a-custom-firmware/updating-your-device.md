---
title: ⬆️ Updating your device
type: docs
weight: 2
---

Ensuring your device is fully-updated before installing custom firmware is important as this reduces the possibility of issues. Most developers have tested custom software using the latest version of the device's official software and as such may not experience issues you may experience when you are using older software.

This portion will guide you in installing updates on your device before installing a custom firmware.


## Updating your device directly

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Updating your device directly is the easiest way in keeping your device updated. Here are the steps in downloading updates directly from your Galaxy device. Ensure your device is **charged to at least 60%** before updating to avoid corruptions due to low battery.

1. Open the **Settings** app.
2. Find and tap **Software updates**.
3. Tap on **Download and install**.
4. If a new software update is available, tap **Download**.
5. Once the download has finished, you can choose to immediately install the update by tapping **Install now** or later by scheduling your update through tapping the **Schedule install** button.
6. Once your device starts updating, it will take a while.
7. Your device will automatically enter Android with a newer version of your device's official software.



## Installing updates manually using a PC

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

A Galaxy device's Download Mode is used to install software **using a PC** with the necessary drivers. This is used by technicians and members of the community to install software directly onto the device without starting the Android OS.

This is useful in the case the device encountered a software corruption and cannot access Android.



#### What you will need for this step

* A PC, **preferably** running Microsoft Windows(TM)
* A good, supported USB **cable**, make sure the cable does not lose connection immediately when plugged in
* Your device, preferably charged to **at least 60%**.
* The Samsung USB drivers installed. [Get it by clicking here.](https://developer.samsung.com/android-usb-driver)
* Odin, a firmware installation tool from Samsung. [Get it by clicking here.](https://forum.xda-developers.com/t/patched-odin-3-13-1.3762572/)



### Getting official firmware for Odin

There are many ways in order to download official firmware for use with Odin. Most may recommend [SamFw](https://samfw.com/) or [SamMobile](https://www.sammobile.com/firmwares/). But this portion will guide you in downloading official firmware using [Bifrost](https://github.com/zacharee/SamloaderKotlin), a faster solution that downloads software updates directly from Samsung servers.



#### Getting your device's region code

Most services will require your device's three-letter region code, also known as the _Open Market Customization (OMC)_ or _Consumer Software Customization (CSC)_. Here are the steps in getting your device's code.

> [!TIP]
> Ensure you are running your device's **official software** before following the steps below.
>
> Some custom firmwares (including Fresh) modifies your device's region code in order to enable certain features not available in your market and **may not** reflect the device's actual region code.

1. Open the **Settings** app.
2. Find and tap **About phone**.
3. Tap **Software information**.
4. Find the **Service provider software version** field.
5. Your three-letter region code is the **first three-letters** at the **bottom-most** caption of the **Service provider software version** field.



#### Getting an official firmware using Bifrost

> [!TIP]
> Some anti-virus software may detect Bifrost as malware due to heuristics.
> 
> As long as you are downloading Bifrost from its official GitHub repository, it is **not** a virus and your anti-virus software may have just detected it as "malware" due to its similarity in name to some certain viruses.

1. Download the latest available version of Bifrost at [this link](https://github.com/zacharee/SamloaderKotlin/releases). Make sure to select the right file for the PC you are using.
2. Extract the entire .zip file to an easily-accessible location.
3. Open the Bifrost file. If using Linux, you may need to set it as "executable".
4. Fill in your device's model (**without** the "/DS", if there is) on the "Model" field.
5. Fill in your device's current region in the "Region" field. This is a **three-letter** code that can be retrieved by [following the steps above](updating-your-device.md#getting-your-devices-region-code).
6. Click **Download** once it has loaded a valid firmware. Save it somewhere with enough space (typically 5-6GB) and can be easily accessed. The download will take a while.
7. Once the download has finished (and it has successfully "decoded" the downloaded file), you should have a .zip file containing the downloaded firmware.
8. Extract the contents of the .zip file to somewhere easily accessible.
9. You are now ready to install official software using Odin.



### Installing official firmware using Odin

1. If not yet done, completely turn off the device by **long-pressing** the **power button** and tapping **Power off**. Tap the **icon again** to confirm.
2. **Extract** the Odin ZIP on **your PC** to an easy to access location. Open the app as **an administrator** by **right-clicking** the `Odin_vxx.x.x_.exe` file and clicking **Run as administrator.**
3. **Plug in** the **USB cable** to **your PC.**
4. Once your device has turned off completely, **press both** **volume up and volume down** buttons, and **plug in** the **USB cable** to **your phone**.
5. Your device will turn on to a **teal** screen. This is your device's **download mode**.
6. **Press** the **volume up button** once. Your device's screen will now display multiple lines of text and the Odin will show a green box showing some device information.
7. Click the **BL** button and point it to the **downloaded .tar.md5 file** that **starts with "BL\_".**
8. Click the **AP** button and point it to the **downloaded .tar.md5 file** that **starts with "AP\_".**
9. Click the **CP** button and point it to the **downloaded .tar.md5 file** that **starts with "CP\_".**
10. Click the **CSC** button and point it to the **downloaded .tar.md5 file** that **starts with "HOME\_CSC\_".**
11. On your device, **long-press** the **volume up button**.
12. On your PC, click **Start**.
13. Your device will automatically restart.
14. Your device will automatically enter Android with a newer version of your device's official software.



