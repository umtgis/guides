---
title: "MacOS (Apple Silicon)"
---

## Install UTM with Windows 11 for ARM Preview

1.  Download UTM from [https://mac.getutm.app](https://mac.getutm.app){target="_blank"}, or install it from the Mac App Store at [https://apps.apple.com/us/app/utm-virtual-machines/id1538878817](https://apps.apple.com/us/app/utm-virtual-machines/id1538878817){target="_blank"}. UTM is free, but if you install it from the Mac App Store, it will cost you \$9.99. Benefits of installing from the App store include automatic updates, and you will be supporting the continued development of UTM and the QEMU emulator its built upon.

    -   If you install from the direct download, open the `UTM.dmg` disk image file that was downloaded, and drag `UTM.app` into the Applications folder.

2.  Open `UTM.app`, and click the `+` sign at the top of the window to install a new virtual machine.

3.  Select "Virtualize".

4.  Select "Windows"

5.  Select the "Import VHDX Image" checkbox, and click the "Download Windows 11 for ARM64 Preview VHDX" link. This will open a new window at [https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewARM64](https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewARM64){target="_blank"}.

    -   Sign into `microsoft.com` in the upper right corner of the page using your `first.last@umt.edu` user ID.
    -   If you see, "To access this page, you need to be a member of the Windows Insider program," you'll need to sign up for the "Windows Insider" program.
        -   Navigate to [https://www.microsoft.com/en-us/windowsinsider/register](https://www.microsoft.com/en-us/windowsinsider/register){target="_blank"}.
        -   Read through the notices, and select the "I accept the terms of this agreement" check box.
        -   **Click "Register now".**
        -   Return to the UTM window and click the "Download Windows 11 for ARM64 Preview VHDX" again, or navigate to [https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewARM64](https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewARM64){target="_blank"}.
    -   You should be on a page entitled "Windows Insider Preview Downloads". Click the dropdown menu and select the "Windows 11 Client Arm64 Insider Preview (Beta) - Build xxxxx" option. Disregard the build number; these change often. **Click "Confirm".**
    -   A new dropdown will appear inviting you to "Select the product language." English will likely be the only option. Select your language. **Click "Confirm".**
    -   A download link for the Windows VHDX should appear. **Click "Download Now".** The download is large (\~10 Gb) and will take some time, especially on a wifi connection. Note where the file downloads to.

6.  Once the Windows 11 for ARM64 Preview VHDX image is downloaded on your computer, return to UTM, click the "Browse..." button, and navigate to the download VHDX image. **Click "Continue".**

7.  Select the amount of memory and number of CPU cores for the Windows virtual machine. You can accept the default values, or increase the memory and CPU cores to your liking. It is advisable to not use more than half of your computer's total memory or number of cores. **Click "Continue".**

8.  You may specify a shared directory that will be mapped to the Windows virtual machine from your local machine. This is optional. **Click "Continue".**

9.  Review the Summary, changing the Windows virtual machine's name if you'd like, and **click "Save".**

10. Your new Windows virtual machine should appear in the left column of the UTM window. Click the "play" button (the triangle) to launch the virtual machine. The machine should start up and begin the Windows installation process.

11. Continue through the process of installing Windows in the virtual machine. You may encounter issues; the guide at [https://docs.getutm.app/guides/windows/](https://docs.getutm.app/guides/windows/){target="_blank"} may be useful. When installing on an M1 MacBook Pro, we ran into trouble with a network check during install. This can be solved by:

    -   Go to the language select screen (you may need to restart the setup if you are past this screen).
    -   Press `Shift + F10` to launch Command Prompt.
    -   Type in `OOBE\BYPASSNRO` and press Enter.
    -   Your VM should reboot and at the setup screen you should see an option for "I don’t have internet." Click that, and then "Continue with limited setup," and you should be able to continue with the installation.

12. Once Windows starts, click the file explorer, and select the CD drive. Click the "spice-guest-tools" installer, which installs important drivers to run windows on a Mac. Reboot when prompted.

13. You may want to adjust the video settings on your Windows VM. To do so, shut down the Windows VM, and in the UTM app, and then, with the Windows VM selected in the lefthand menu, click the button that looks like three sliders in the upper right corner. Navigate down to "Display" and click the "Retina Mode" checkbox. Click "Save", and restart the Windows VM. Resolution should be roughly double.

14. At this point, it is good to install any updates to Windows that are available. Click the Start menu and search for "Settings"; go to Settings. Towards the top of the Settings window you should see a "Windows Update" button. Check for updates, and install any that are available.

## Install .NET SDK 6.0 (x64)

ArcGIS Pro requires .NET SDK 6.0 for x64 processors (*not* for ARM processors!). Follow these instructions to install the correct .NET SDK.

1.  Open a browser and navigate to [https://dotnet.microsoft.com/en-us/download/dotnet/6.0](https://dotnet.microsoft.com/en-us/download/dotnet/6.0){target="_blank"}.

2.  You will see a grid of options for installing the .NET SDK. Under the "Installers" column and "Windows" row, click the "x86" link to begin the download.

3.  Navigate to the downloaded file, and double click to begin the installation process. Follow the instructions in the installer, accepting all defaults.

4.  **Restart the Windows VM.**

## Install ArcGIS Pro

Log in to Windows 11, and follow these instructions:

1.  Download the ArcGIS Pro installer.

    -   Navigate to [https://umontana.maps.arcgis.com](https://umontana.maps.arcgis.com){target="_blank"} and click "Sign In" in the upper right. You will be prompted to sign in with your UM NetID.
    -   Click your name in the upper right and go to My Settings \> Licenses. On the list of product licenses, you'll see a Download link for ArcGIS Pro. Click it to start the download.

2.  Launch the downloaded installer, and follow the instructions to install ArcGIS Pro. Additional instructions are available here: [https://umtqsg.atlassian.net/wiki/spaces/PUB/pages/1478754305/How+to+install+ArcGIS+Pro](https://umtqsg.atlassian.net/wiki/spaces/PUB/pages/1478754305/How+to+install+ArcGIS+Pro){target="_blank"}

3.  Once installed, launch ArcGIS Pro and activate following these instructions: [https://umtqsg.atlassian.net/l/c/1X159Wf2](https://umtqsg.atlassian.net/l/c/1X159Wf2){target="_blank"}
