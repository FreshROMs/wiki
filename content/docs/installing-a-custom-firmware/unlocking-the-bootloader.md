---
title: 📱 Unlocking the bootloader
type: docs
weight: 3
---

Unlocking your device's bootloader is the **first step** to be done in order to install a custom firmware. This is vital as your device's bootloader **normally** disallows installing third-party firmware, unless you unlock it.

You can skip this portion if you have already unlocked your bootloader.



## What is a 'bootloader' anyway?

A bootloader is a vendor-proprietary image responsible for bringing up the kernel on a device. It guards the device state and is responsible for initializing the [Trusted Execution Environment](https://source.android.com/docs/security/features/trusty) and binding its root of trust. The bootloader also verifies the integrity of the device itself before moving execution to the kernel, and displays [boot state](https://source.android.com/docs/security/features/verifiedboot/verified-boot) warnings.

In short terms, **a bootloader checks if the software installed on your device is valid, genuine, and secure before the device attempts to boot.** As the first step in an Android device's boot process, it checks for the signatures and disallows booting if it detects a corrupted or unsigned software.



## Unlocking a Samsung bootloader

> [!TIP]
> Unlocking your bootloader **does not void your warranty immediately.** Your warranty becomes void **once you install custom software on your device**.

If you are uncomfortable with this, **immediately stop proceeding with this guide.**


#### What you will need for this step

* A PC, **preferably** running Microsoft Windows(TM)
* A USB Type-C to Type-C **cable**, make sure the cable does not lose connection immediately when plugged in
* Your device, preferably charged to **at least 60%**.

### Steps in unlocking your device's bootloader

> [!CAUTION]
> Proceeding with this step **will completely wipe your data and remove all files.** Make sure [you have backed up](../backing-up-your-data) all important data before proceeding.

1. &#x20;Enable **developer options** if you haven't enabled it yet. Open the **Settings** app, tap **About phone** then **Software information**, and tap the **Build number** until you see _"Developer options has been turned on."_
2. Open the **Settings** app.
3. If not yet enabled, **turn on** the **OEM unlocking** option. This will allow you to fully unlock the booloader.
4. Completely turn off the device by **long-pressing** the **power button** and tapping **Power off**. Tap the **icon again** to confirm. You can now **plug in** the **USB cable** to **your PC** while your device is shutting down.
5. Once your device has turned off completely, **press both** **volume up and volume down** buttons, and **plug in** the **USB cable** to **your phone**.
6. Your device will turn on to a **teal** screen. This is your device's **download mode**.
7. **Long-press** the **volume up button** until you see a screen titled **"Unlock bootloader**".
8. Press the **volume up button** to confirm the bootloader unlock.
9. Your device will reboot twice while it removes all data completely. It will take a while before it turns on to a **setup screen**.

> [!TIP]
> The **Download Mode** feature of your device is useful in installing custom software, as well as the manufacturer's official software. More on this later.


### Setting up the device after unlocking the bootloader

> [!WARNING]
> This is a **very important** step to do **after unlocking your bootloader** or **re-installing the  manufacturer's official software**. Samsung disallows devices from installing custom software for at least **7 days** if the steps below are **not** done.


1. Set up your device as usual. Ensure **you connect your device to the internet**, this is very important in ensuring Samsung immediately 'unlocks' your device.
2. If needed, enter your existing Google Account's information. You can choose to restore data at this point, **if you're not installing Fresh immediately.**
3. After setting up, go to the **Settings** app.
4. Find and tap **Developer options**.
5. Check if the **OEM unlocking** option is **permanently enabled** (grayed out), with a caption saying _"Device bootloader is unlocked"_.
6. You're ready to install custom software on your device.



## Re-locking the device's bootloader

Here are the steps in the case you decide to re-lock your device's bootloader.

1. Ensure you are running the manufacturer's **official software** for your device. [See the steps here](updating-your-device.md#installing-updates-manually-using-a-pc) for instructions.
2. Completely turn off the device by **long-pressing** the **power button** and tapping **Power off**. Tap the **icon again** to confirm. You can now **plug in** the **USB cable** to **your PC** while your device is shutting down.
3. Once your device has turned off completely, **press both** **volume up and volume down** buttons, and **plug in** the **USB cable** to **your phone**.
4. Your device will turn on to a **teal** screen. This is your device's **download mode**.
5. **Long-press** the **volume up button** until you see a screen titled **"Lock bootloader**".
6. Press the **volume up button** to confirm the bootloader lock.
7. Your device will reboot twice while it removes all data completely. It will take a while before it turns on to a **setup screen**.
8. You have re-locked your device's bootloader.



## For RMM/KG Prenormal-locked devices

Your device is considered to be locked by Samsung's KnoxGuard if **any** of the following criteria matches:

* Your device refuses to install custom software from **Download Mode** and would only install firmware officially released by the manufacturer; or
* The **OEM unlocking** option in the device's **Developer options** menu is missing.

To resolve this issue, you may try doing any of the following:

* Keep your device connected to the internet (either Wi-Fi or mobile data)
* Regularly check for software updates
* Refer to [this guide](https://www.xda-developers.com/fix-missing-oem-unlock-samsung-galaxy-s9-samsung-galaxy-s8-samsung-galaxy-note-8/) by XDA Portal for an alternative way
