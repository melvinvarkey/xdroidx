# Introduction #

Instruction on how to upgrade to froyo and keep Froyo.


# Details #
**First**<br>
Install <a href='http://xdroidx.googlecode.com/files/UniversalAndroot-1.6.2-beta.apk'>UniversalAndroot 1.6.2</a> to your phone by clicking link from your Android device.<br>

<b>Next</b><br>
Download & Copy the <a href='http://xdroidx.googlecode.com/files/update.zip'>update.zip</a> to your sdcard.<br>
Download & Copy the <a href='http://xdroidx.googlecode.com/files/Superuser.apk'>Superuser.apk</a> to your tools section of your adb.<br>

<b>Then</b><br>
1. Open command prompt<br>
2. adb push Superuser.apk /sdcard/"<br>
3. adb shell"<br>
4. su"<br>
5. mount -o remount,rw /dev/block/system /system"<br>
6. cp /sdcard/Superuser.apk /system/app/"<br>
7. On the phone, open your launcher, locate Superuser, and open it. You will likely be prompted to allow access then update su.<br>
8. exit<br>
9. exit<br>
10. Proceed to next step.<br>

<b>Finally</b><br>
1. adb shell<br>
2. su<br>
3. mount -o rw,remount /dev/block/system /system<br>
4. cp /system/bin/su /system/xbin/su<br>
5. ls /system/xbin/su" (make sure the results are "/system/xbin/su" and <b>NOT</b> "/system/bin/su": No such file or directory`. If you see this, repeat the previous step.)<br>
6. exit<br>
7. exit<br>
8. adb reboot recovery<br>
9. apply update.zip<br>

<b>Once updated to Froyo</b><br>
1. adb shell<br>
2. system/xbin/su<br>
3. mount -o rw,remount /dev/block/system /system<br>
4. cp /system/xbin/su /system/bin/su<br>
5. chmod 4755 /system/bin/su"<br>
6. ls /system/bin/su" (make sure the results are "/system/bin/su" and NOT "/system/xbin/su" - If you see this, repeat the previous step.)<br>
7. exit<br>
8. exit<br>