# Auntie's Guide to Installing Windows 11
by Eris "my sweet girl" Ivy, Age 23

![Eris waving gif](/Wave.gif)

**Hi!** This is a guide on how to install and setup **Windows 11** on your new computer. I'm handwriting this guide for you because Windows is a bit of a problem-child and we'll need to take serious precautions to get the 'best' experience out of it.

Unlike MacOS, Windows is notorious for bloatware, ads, telemetry, and overall just an unpleasant user experience; which makes it all the more comforting to know that most of the world's computers run this garbage. My personal gripes aside; it's the only other operating system that officially supports the Adobe creative suite and *the* go-to place for high-end gaming.

The biggest problem with Windows 11 is the mandatory use of a Microsoft account to log in. **We are not going to be doing this**, for a multitude of reasons. On Windows 11, there is a program that auto-backups files to the cloud; similar to MacOS' iCloud. 
Which is nice to have, but the problem is that its the **default** storage. Any file you download will quietly back itself up and a couple weeks down the line you'll be pestered to "**upgrade your OneDrive storage**".

To avoid this entirely we're just not going to log in with a Microsoft account. Luckily people have figured out how to do this, and today we're going to do it too. Friends don't let friends use OneDrive <3

**The install process I've organized into three chapters:**
- 1. Flashing Windows 11 to USB drive
- 2. Installing Windows 11 on your computer
- 3. Bypassing Windows 11 bullshit

Each chapter has step-by-step instructions on how to install Windows 11. First by downloading a Windows 11 image, flashing it to a USB, and running the installer on your computer.

*Before we get started, remember the following:*

- ***DO NOT SIGN IN WITH A MICROSOFT ACCOUNT***
- ***DO NOT CONNECT TO THE INTERNET UNTIL AFTER YOU'VE MADE AN ACCOUNT***
- ***DO NOT GIVE ANY PERSONAL INFORMATION OR DATA TO MICROSOFT***

The best place to get a copy of Windows 11 is from [massgrave.dev](https://massgrave.dev/windows_11_links) which hosts older versions of Windows 11 `.iso` image files and can be verified with [hash-based verification](https://en.wikipedia.org/wiki/File_verification); nerd-speak for "you can compare this file to the original and see no changes have occurred."

Alright cool, let's get started!
### 1. Flashing Windows 11 to USB drive
- Download *Windows 11*
- Download and install [WinDiskWriter](https://github.com/TechUnRestricted/WinDiskWriter/releases/tag/v1.3)
	- You may need to allow this program to run by going into "Privacy & Security" in your system settings. Scroll down to "Security" and click "Open Anyway"
- Plug your USB drive into your Mac
- Choose the `en-us_windows_11(...).iso` file for **"Windows Image"** in WinDiskWriter
- Select your USB drive under **"Target Device"**
	- It may not be necessary as you will be buying brand-new computer parts but check `Patch Installer Requirements` and use the `FAT32` file system
- Click `Start` to flash Windows to the USB drive
- Once finished, eject the USB drive from Finder

### 2. Installing Windows 11 on your computer

- Plug the USB drive into a front USB port
- Power on the computer
- Go through the install as normal for language and keyboard layout
	- If asked for a key, say "I don't have a product key" 
- Choose "Install Windows 11 Home"
	- If asked, install on `WD_Black SN850X` or whatever your SSD shows up as
- Accept the terms and install
Windows will take a few minutes to install, and then reboot into a "getting started menu"

### 3. Bypassing Windows 11 bullshit

You will be met with a screen that says "Is this the right country or region?" after your computer reboots. Do ***not*** click anything here yet.
- Press *Shift* and *F10*
- Click on the terminal window that just opened to *focus* it
- Type `oobe\bypassnro` and then press *Enter*
Windows will restart and load the same "Is this the right country or region?" menu; now you may continue.
- Choose your region and keyboard layout(s)
- When it says "Let's connect you to a network" screen, click "**I don't have internet**"
- Enter your name
This name will also be your computer's name. If you chose "Ava" the path to your videos folder will be `C:\Users\Ava\Videos`
- Enter your password
- Fill out the security questions
- In the "Choose privacy settings for your device" menu, uncheck every single option
Windows will load for a minute and then show your desktop. Congratulations! We're in Windows 11

### Windows 11 post-install tweaks

This part is gonna be a bit messy
