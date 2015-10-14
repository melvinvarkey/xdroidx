# Introduction #

Two ways to root your Motorola Droid X Android OS 2.1


# Details #

**First Way - Easy Way!**<br>
Install <a href='http://xdroidx.googlecode.com/files/UniversalAndroot-1.6.2-beta.apk'>UniversalAndroot 1.6.2</a> to your phone by clicking link from your Android device.<br>

<b>Second Way - Hard Way! (for users who like to do stuff the old fashion way.)</b><br>
First Download Root Files - <a href='http://xdroidx.googlecode.com/files/DroidXRoot_v2.zip'>Root Files</a>

(Run means type the command in quotes <a href='but.md'>not the quotes</a> then press the Enter key)<br>

Next follow a list of commands to send to your phone.<br>

1. Download the attached archive and expand it to a folder you can find (eg. c:\DroidXRoot_v2)<br>
2. Set up ADB (If you haven't already follow these instructions here <a href='http://code.google.com/p/xdroidx/wiki/HowToSetUpADB'>HowToSetUpADB</a>)<br>
3. On the phone: Home, Menu Button, Settings, Applications, Development: Make sure the "USB debugging" option is enabled/checked.<br>
4. Status bar, USB connection: Make sure "PC Mode" is selected.<br>
5. Open a command prompt (Start, Run, "cmd", OK;)<br>
6. Run "cd c:\android-sdk-windows\tools"<br>
7. Run "adb devices" - lists your DroidX.<br>
8. Run "cd c:\DroidXRoot" (or where ever you expanded the archive)<br>
9. Run "adb push Superuser.apk /sdcard/Superuser.apk"<br>
10. Run "adb push su /sdcard/su"<br>
11. Run "adb push busybox /sdcard/busybox"<br>
12. Run "adb push exploid /sql<b>"</b><br>
13. Run "adb shell"<br>
14. Run "cd /sql<b>"</b><br>
15. Run "chmod 755 exploid"<br>
16. On your phone, navigate to a screen where you can switch wifi/bluetooth on/off easily (settings, or a home screen with a widget)<br>
17. Run "./exploid" and follow directions on screen. Once this completes you'll be back at a shell prompt.<br>
18. Turn your phone's bluetooth off and on (or on and off)<br>
19. Run "rootshell". You'll be prompted for a password.<br>
20. Type in password "secretlol" and press Enter then you are root! (You'll know because your prompt will now be a "#" instead of "$")<br>
21. Run "cp /sdcard/Superuser.apk /system/app/Superuser.apk"<br>
22. Run "cp /sdcard/su /system/xbin/su"<br>
23. Run "cp /sdcard/busybox /system/xbin/busybox"<br>
24. Run "chmod 4755 /system/xbin/su"<br>
25. Run "chmod 755 /system/xbin/busybox"<br>
26. Run "rm /system/bin/rootshell"<br>
27. Run "reboot"<br>

And your rooted! Yay that wasn't so hard was it? :)