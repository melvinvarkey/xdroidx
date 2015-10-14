# Introduction #

This is a guide on manually deodexing your phone for custom themes.


# Details #
**I AM NOT RESPONSIBLE FOR WHATEVER HAPPENS TO YOUR PHONE!**<br>

<b>You must be rooted!</b><br>

<b>What you'll need:</b><br>
1. A Windows based machine<br>
2. <a href='http://xdroidx.googlecode.com/files/xUltimate-v2.2.zip'>xUltimate 2.2</a> <br>
3. Patience<br>

<b>Process:</b><br>

1. Unzip xUltimate v2.2, and launch "Main.exe"<br>
2. If everything goes well xUlt should recognize the phone and make a connection. You now should see a list of options.<br>
3. Run option 1. After option 1 is done, run option 2.<br>
4. Now these well take a while. Run option 3.<br>
5. IMPORTANT: After you have run option 3, you MUST navigate to the xUltimate folder and find "origi_frame" folder, and delete "guava.odex". It's a bad file, and interferes with deodexing process.<br>
6. Now run option 4, and wait.<br>
7. Exit xUltimate, and put the phone in "<b>USB Mass Storage</b>".<br>
8. Go back into the xUltimate folder and copy "done_frame", and "done_app", and move them to the root of the sdcard.<br>
9. Switch back to "<b>PC Mode</b>".<br>
9. Open a command prompt, and do the following:<br>

<b>Command:</b><br>
<b>NOTE: THE LITTLE STAR SYMBOL IS REPLACED BY "(star symbol)" DUE TO INCODING INSIDE OF THIS WIKI PAGE</b><br>

adb shell<br>
su<br>
stop<br>
mount -o remount,rw /dev/block/system /system<br>
cp /sdcard/done_app/(star symbol) /system/app/<br>
cp /sdcard/done_frame/(star symbol) /system/framework/<br>
rm /system/app/(star symbol).odex<br>
rm /system/framework/(star symbol).odex<br>
exit<br>
exit<br>
adb reboot<br>

Your phone should now be deodexed and enjoy!<br>

<b>Note: You may notice an increase in speed, and you now have the ability to edit certain files with greater effects. (i.e. services.jar)</b>

<b>If you have any problems visit the XDA Thread:</b><a href='http://forum.xda-developers.com/showthread.php?t=765270'>[HOW-TO] Manually deodex your phone.</a>