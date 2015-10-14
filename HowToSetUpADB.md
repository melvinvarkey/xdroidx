# Introduction #

Instructions on how to setup ADB.


# Details #
**First**<br>
1. Download <a href='http://dl.google.com/android/installer_r11-windows.exe'>Android SDK</a><br>
2. The SDK program will download in a .zip file. Extract the file to your desktop - You should now have a folder on your desktop with a name: android-sdk-windows.<br>
3. Move that folder to your Local Disk ( C: ) > android-sdk-windows<br>
4. Make <b>SURE</b> to install the USB driver package in SDK. This way your device will be recognized when running adb commands later on...<br>

<b>Next</b><br>
In Windows XP/Vista/7<br>

5. Right click on "My Computer" <br>
6. Left click on "Properties"<br>

<b>Vista/Win7</b> (there's is an extra step for these two OS"s ignore this if you are using XP)<br>

7. Click on "Advanced System Settings" in the left hand pane.<br>

<b>IN ALL WINDOWS - Make sure you are on the "Advanced" tab of the System Properties Panel.</b><br>

8. Click on "Environment Variables" button.<br>
9. Click "New..." button.<br>
10. Variable name: adb<br>
11. Variable value: C:android-sdk-windows\tools - location on file<br>
12. Reboot system. :D