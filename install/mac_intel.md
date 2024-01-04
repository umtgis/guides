---
title: "MacOS (Intel)"
---

## Install UTM

UTM employs Apple's Hypervisor virtualization framework to run other operating systems on Mac processors at near native speeds. It is a free alternative to virtualization software such as [Parallels](https://www.parallels.com){target="_blank"}, with impressive performance.

There are three ways to install UTM:

  - Download UTM from [https://mac.getutm.app](https://mac.getutm.app){target="_blank"}. Click the "Download" link. Open the `UTM.dmg` disk image file that was downloaded, and drag `UTM.app` into the Applications folder.
  - Install UTM from the [Mac App Store](https://apps.apple.com/us/app/utm-virtual-machines/id1538878817){target="_blank"}. UTM is free, but if you install it from the Mac App Store, it will cost you \$9.99. Benefits of installing from the App store include automatic updates, and you will be supporting the continued development of UTM and the QEMU emulator its built upon.
  - If you use [Homebrew](https://brew.sh){target="_blank"} for app management on your Mac, install UTM via homebrew in Terminal: `brew install utm`.
    
## Download Windows 11 Preview ISO

1. Navigate to <https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewiso>{target="_blank"}.

2. Sign into `microsoft.com` in the upper right corner of the page using your `first.last@umt.edu` user ID.
    -   If you see, "To access this page, you need to be a member of the Windows Insider program," you'll need to sign up for the "Windows Insider" program.
        -   Navigate to <https://www.microsoft.com/en-us/windowsinsider/register>{target="_blank"}.
        -   Read through the notices, and select the "I accept the terms of this agreement" check box.
        -   **Click "Register now".**
        -   Return <https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewiso>{target="_blank"} to continue.

3. You should be on a page entitled "Windows Insider Preview Downloads". Toward the bottom of the page, click the drop down menu and select the "Windows 11 Insider Preview (Release Preview Channel) - Build xxxxx" option. Disregard the build number; these change often. **Click "Confirm".**

4. A new drop down will appear inviting you to "Select the product language." Select your language. **Click "Confirm".**

5. A download link for the Windows ISO should appear. **Click "64-bit Download".** The download is large (\~6.6 Gb) and will take some time, especially on a wifi connection. Note where the file downloads to.

## Install a New Virtual Machine with Windows 11 Preview

1.  Open `UTM.app`, and click the `+` sign at the top of the window to install a new virtual machine.

2.  Select "Virtualize".

3.  Select "Windows"

4.  Click the "Browse..." button, and navigate to the downloaded Windows 11 Preview ISO image that you downloaded above. **Click "Continue".**

5.  Select the amount of memory and number of CPU cores for the Windows virtual machine. You can accept the default values, or increase the memory and CPU cores to your liking. It is advisable to not use more than half of your computer's total memory or number of cores. **Click "Continue".**

6.  You may specify a shared directory that will be mapped to the Windows virtual machine from your local machine. This is optional. **Click "Continue".**

7.  Review the Summary, changing the Windows virtual machine's name if you'd like, and **click "Save".**

8. Your new Windows virtual machine should appear in the left column of the UTM window. Click the "play" button (the triangle) to launch the virtual machine. The machine should start up and begin the Windows installation process. **When prompted, "press any key to boot from CD or DVD..."**; this will start the installer.

9. Continue through the process of installing Windows in the virtual machine. You may encounter issues; the guide at <https://docs.getutm.app/guides/windows/>{target="_blank"} may be useful. When prompted to activate windows with a product key, select "I don't have a product key" at the bottom of the window to continue (or, enter one if you have one on hand). I've found activating Windows is unnecessary, at least for the short term.

10. Once Windows starts, click the file explorer, and select the CD drive. Click the "spice-guest-tools" installer, which installs important drivers to run windows on a Mac. Reboot when prompted.

11. You may want to adjust the video settings on your Windows VM. To do so, shut down the Windows VM, and in the UTM app, and then, with the Windows VM selected in the left hand menu, click the button that looks like three sliders in the upper right corner. Navigate down to "Display" and click the "Retina Mode" check box. Click "Save", and restart the Windows VM. Resolution should be roughly double.

12. At this point, it is good to install any updates to Windows that are available. Click the Start menu and search for "Settings"; go to Settings. Towards the top of the Settings window you should see a "Windows Update" button. Check for updates, and install any that are available.

## Install ArcGIS Pro

Continue your installation from within the new Windows Virtual Machine by following the [Windows install instructions](/Installation/windows.html).