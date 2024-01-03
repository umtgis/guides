---
title: "MacOS (Apple Silicon)"
---

## Install UTM

1.  Download UTM from [https://mac.getutm.app](https://mac.getutm.app){target="_blank"}, or install it from the Mac App Store at <https://apps.apple.com/us/app/utm-virtual-machines/id1538878817>{target="_blank"}. UTM is free, but if you install it from the Mac App Store, it will cost you \$9.99. Benefits of installing from the App store include automatic updates, and you will be supporting the continued development of UTM and the QEMU emulator its built upon.

    -   If you install from the direct download, open the `UTM.dmg` disk image file that was downloaded, and drag `UTM.app` into the Applications folder.
    
## Download Windows 11 for ARM Preview VHDX

1. Navigate to <https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewARM64>{target="_blank"}.

2. Sign into `microsoft.com` in the upper right corner of the page using your `first.last@umt.edu` user ID.
    -   If you see, "To access this page, you need to be a member of the Windows Insider program," you'll need to sign up for the "Windows Insider" program.
        -   Navigate to <https://www.microsoft.com/en-us/windowsinsider/register>{target="_blank"}.
        -   Read through the notices, and select the "I accept the terms of this agreement" check box.
        -   **Click "Register now".**
        -   Return <https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewARM64>{target="_blank"} to continue.

3. You should be on a page entitled "Windows Insider Preview Downloads". Click the dropdown menu and select the "Windows 11 Client Arm64 Insider Preview (Beta) - Build xxxxx" option. Disregard the build number; these change often. **Click "Confirm".**

4. A new dropdown will appear inviting you to "Select the product language." English will likely be the only option. Select your language. **Click "Confirm".**

5. A download link for the Windows VHDX should appear. **Click "Download Now".** The download is large (\~10 Gb) and will take some time, especially on a wifi connection. Note where the file downloads to.

## Install a New Virtual Machine with Windows 11 for ARM Preview

1.  Open `UTM.app`, and click the `+` sign at the top of the window to install a new virtual machine.

2.  Select "Virtualize".

3.  Select "Windows"

4.  Select the "Import VHDX Image" check box.

5.  Click the "Browse..." button, and navigate to the downloaded Windows 11 VHDX image. **Click "Continue".**

6.  Select the amount of memory and number of CPU cores for the Windows virtual machine. You can accept the default values, or increase the memory and CPU cores to your liking. It is advisable to not use more than half of your computer's total memory or number of cores. **Click "Continue".**

7.  You may specify a shared directory that will be mapped to the Windows virtual machine from your local machine. This is optional. **Click "Continue".**

8.  Review the Summary, changing the Windows virtual machine's name if you'd like, and **click "Save".**

9. Your new Windows virtual machine should appear in the left column of the UTM window. Click the "play" button (the triangle) to launch the virtual machine. The machine should start up and begin the Windows installation process.

10. Continue through the process of installing Windows in the virtual machine. You may encounter issues; the guide at <https://docs.getutm.app/guides/windows/>{target="_blank"} may be useful. When installing on an M1 MacBook Pro, we ran into trouble with a network check during install. This can be solved by:

    -   Go to the language select screen (you may need to restart the setup if you are past this screen).
    -   Press `Shift + F10` to launch Command Prompt.
    -   Type in `OOBE\BYPASSNRO` and press Enter.
    -   Your VM should reboot and at the setup screen you should see an option for "I don’t have internet." Click that, and then "Continue with limited setup," and you should be able to continue with the installation.

11. Once Windows starts, click the file explorer, and select the CD drive. Click the "spice-guest-tools" installer, which installs important drivers to run windows on a Mac. Reboot when prompted.

12. You may want to adjust the video settings on your Windows VM. To do so, shut down the Windows VM, and in the UTM app, and then, with the Windows VM selected in the left hand menu, click the button that looks like three sliders in the upper right corner. Navigate down to "Display" and click the "Retina Mode" checkbox. Click "Save", and restart the Windows VM. Resolution should be roughly double.

13. At this point, it is good to install any updates to Windows that are available. Click the Start menu and search for "Settings"; go to Settings. Towards the top of the Settings window you should see a "Windows Update" button. Check for updates, and install any that are available.

## Install ArcGIS Pro

Continue your installation from within the new Windows Virtual Machine by following the [Windows install instructions](/Installation/windows.html)
