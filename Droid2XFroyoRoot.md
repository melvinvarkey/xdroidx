# Introduction #

Instructions on how to root your Froyo(Android OS 2.2) devices (Droid 2 or Droid X)


# Details #

Setup:<br>
- Install adb <a href='http://code.google.com/p/xdroidx/wiki/HowToSetUpADB'>(here)</a> (only do this if you dont already have adb setup)<br>
- Download<br>
<a href='http://xdroidx.googlecode.com/files/Droid2Root.rar'>Droid2Root</a><br>
- Extract to a directory, I used c:\Droid2Root<br>
- Make sure you have USB degugging enabled<br>
- Change connection to PC Mode<br>

Process:<br>
- Open command prompt<br>
- cd c:/android-sdk-windows\tools<br>
- adb devices (to verify the connection)<br>
- cd c:/Droid2Root<br>
- adb push Superuser.apk /sdcard/Superuser.apk<br>
- adb push su /sdcard/su<br>
- adb push busybox /sdcard/busybox <br>
- adb push rageagainstthecage-arm5.bin /data/local/tmp/rageagainstthecage-arm5.bin<br>
- adb shell<br>
- cd data/local/tmp<br>
- chmod 0755 rageagainstthecage-arm5.bin<br>

- ./rageagainstthecage-arm5.bin<br>
- let the process run until it 'kicks' you out (may take a minute or two)<br>
- adb kill-server<br>
- cd c:/android-sdk-windows\tools<br>
- adb devices (to verify the connection)<br>
- adb shell (you should now have a # prompt, if not return to ./rage step above)<br>

- mount -o rw,remount -t ext3 /dev/block/mmcblk1p21 /system<br>
- cp /sdcard/Superuser.apk /system/app/Superuser.apk<br>
- cp /sdcard/su /system/bin/su<br>
- cp /sdcard/busybox /system/bin/busybox<br>
- chmod 4755 /system/bin/su<br>
- chmod 4755 /system/bin/busybox<br>
- mount -o ro,remount -t ext3 /dev/block/mmcblk1p21 /system<br>
- exit<br>
- exit<br>