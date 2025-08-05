---
title: 🗜️ Installing a custom recovery
type: docs
weight: 4
---

Software updates can be installed on Android devices using the recovery mode. It is made out of an Linux kernel and ramdisk separate from the main Android OS. When a phone becomes stuck in a bootloop or becomes infected with malware, recovery mode can be helpful.

Just like the bootloader, the recovery that comes with your device only allows official software from the manufacturer to be installed, hence the need to install a custom one in order to install custom firmware.

This portion will guide you in installing the **TeamWin Recovery Project (TWRP)**, a very popular custom recovery for Android devices.



## TWR-what?

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

The TeamWin Recovery Project (TWRP) is an open source, community project aiming to bring custom recoveries to many Android devices. While primarily developed by a few people, support for it on many devices are maintained by members of the Android community. **The Fresh Project unofficially maintains TWRP for Fresh-supported devices.**

TWRP allows one to easily install custom software, back up and restore partitions as necessary, and wipe partitions as needed.



## Installing TWRP for the first time

Installing a custom recovery **for the first time**, or when **the manufacturer's official software is re-installed**, requires the use of the device's **Download Mode**.

With an unlocked bootloader, it is now possible to install software made by third-party developers as well as the manufacturer's official software (if needed be).

> [!CAUTION]
> Following the steps below will **permanently** make Samsung Wallet (Pay and Pass) **inaccessible** even if you **re-install the manufacturer's official software and re-lock your bootloader.**
> 
> If you are not comfortable with this, **stop immediately and** [**re-lock your bootloader**](../unlocking-the-bootloader#re-locking-the-devices-bootloader)**.**

#### What you will need for this step

* A PC, **preferably** running Microsoft Windows(TM)
* A good, supported USB **cable**, make sure the cable does not lose connection immediately when plugged in
* Your device, preferably charged to **at least 60%**.
* The Samsung USB drivers installed. [Get it by clicking here.](https://developer.samsung.com/android-usb-driver)
* Odin, a firmware installation tool from Samsung. [Get it by clicking here.](https://forum.xda-developers.com/t/patched-odin-3-13-1.3762572/)
* The latest available version of TWRP that can be installed using Odin. [Get it by clicking here.](https://github.com/TenSeventy7/android_recovery_exynos9610_ci/releases/download/ci_36/ODIN-TWRP_v3.7.0-Unofficial_a50-1666700569.tar)



### Installing a custom recovery on your device using Odin

1. If not yet done, completely turn off the device by **long-pressing** the **power button** and tapping **Power off**. Tap the **icon again** to confirm.
2. **Extract** the Odin ZIP on **your PC** to an easy to access location. Open the app as **an administrator** by **right-clicking** the `Odin_vxx.x.x_.exe` file and clicking **Run as administrator.**&#x20;
3. **Plug in** the **USB cable** to **your PC.**
4. Once your device has turned off completely, **press both** **volume up and volume down** buttons, and **plug in** the **USB cable** to **your phone**.
5. Your device will turn on to a **teal** screen. This is your device's **download mode**.
6. **Press** the **volume up button** once. Your device's screen will now display multiple lines of text and the Odin will show a green box showing some device information.
7. Click the **AP** button and point it to the **downloaded .tar file for TWRP**.
8. On your device, **long-press** the **volume up button**.
9. On your PC, click **Start**. Ensure you are still **long-pressing** the **volume up button**.
10. Your device will automatically restart. **DO NOT** release the **volume up button.**
11. Your device will automatically start to TWRP. You can now choose to install Fresh, backup data, or install the [Multidisabler Tool](https://forum.xda-developers.com/t/pie-10-11-system-as-root-multidisabler-disables-encryption-vaultkeeper-auto-flash-of-stock-recovery-proca-wsm-cass-etc.3919714/) if you are not planning to install Fresh **immediately**.



## Updating TWRP

TWRP releases updates with new functionality and fixes at least every **1-2 months.** In order to install these new releases, you can choose to install them directly on TWRP, or using Odin.

{{< cards cols="1" >}}
  {{< card link="https://xdaforums.com/t/recovery-official-twrp-3-7-1-0-for-the-galaxy-a50.4735158/" title="Download the latest version of TWRP" subtitle="Get the latest version of TWRP for the Samsung Galaxy A50" >}}
{{< /cards >}}

If you would:

* Like to install using Odin, get the file that **starts** with `ODIN-TWRP`.
* Like to install directly using TWRP, get the file that **starts** with `TWRP`.



## Opening TWRP after installation

Once TWRP is installed using Odin, it can now be accessed directly on your device. Although **starting Android 11**, Samsung now requires the device **to be plugged in to a PC** to be able to access the recovery.

Some firmwares, such as **Fresh** has an easy-to-access shortcut in order to restart to "recovery mode" without using a PC. This is however only accessible if your device successfully turns on and the home screen is accessible.

To access TWRP manually,

1. If not yet done, completely turn off the device by **long-pressing** the **power button** and tapping **Power off**. Tap the **icon again** to confirm.
2. **Long-press** the device's **volume up button**.
3. **Plug in** the **USB cable** to **your PC. DO NOT** release the **volume up button.**
4. TWRP will automatically show up after a couple of seconds.



## Installing custom software using TWRP

TWRP accepts software **compressed in the ZIP (.zip)** format. These can be easily found on forums and groups. **Fresh is also packaged in .zip format.**

> [!IMPORTANT]
> Custom software are developed by developers not associated by the device manufacturer. **Make sure that you trust the developer before proceeding to install custom software.**

1. Copy the .zip file to your device's **SD card**. This is important as your data is **encrypted until a custom firmware is installed.** You can then use the internal storage once a custom firmware is installed.
2. **Restart** your device to "recovery mode". Refer to the [steps above](installing-a-custom-recovery.md#opening-twrp-after-installation) for instructions on how to do it.
3. Tap the **Install** button and navigate to your SD card. You may need to tap **Select storage**, select **SD card**, and tap **OK** in order to access the external storage.
4. Tap the .zip file you would like to install. Confirm if you have selected the correct file.
5. **Slide the blue button** on the **bottom of the screen** to the **right** in order to proceed with the installation.
6. You can choose to restart back to Android by tapping **Reboot System** or tapping the **Back icon** if you wish to do more in TWRP.



## Restarting your device to its normal state

Once you have finished installing custom software, you can now restart back to Android by doing the following steps.

1. Tap **Reboot.**
2. Tap **System**. Your device will now boot back to Android.
