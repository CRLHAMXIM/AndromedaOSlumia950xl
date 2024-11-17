# ANDROMEDAOSLUMIA950XL
- First of all, this is the truth, not something I'm joking about.
# main problem
- I built this AndromedaOS on lumia 950's AndromedaOS and it runs build 17686
- it can work on lumia 950XL. But don't leave it for more than 10 minutes because your device may break uefi and get uefi error 2.
# Quick Guide:
- Download the requested tools
- Connect your Phone using the USB cable
# Phase 1 (Unlock bootloader):
Before start unlocking you have to download
- FFU-file
- Emergency-files
# 1- Open "WPinternals":
# A- Download FFU + Emergency Files:
- 1.Goto "Download"
- 2.Scroll down then click "Search"
- 3.After the results appear Click "Download All"
- 4.It will take some time to download
- 5.If you already have the files scroll to "Repository"
- 6.Click on "Add Existing FFU-file"
- 7.Select your file
# B Unlock bootloader:
- 1.Goto "Unlock bootloader"
- 2.Click "OK" to switch to "Flash-mode"
- 3.When the phone in "Flash-mode", scroll down and click "Unlock" after reading the descriptions
- 4.Multiple reboots expected so you have to wait and don't interrupt the process
- 5.Wait until you see this message "You need to manually reset your phone now!"
- 6.Restart the phone
- 7.Wait until you see this message "Bootloader unlocked successfully"
- 8.If the phone already unlocked expected to boot to Mass storage instead of this message
# Know Problems:
if stuck into Multiple reboots for too long time or you got "Unlock failed", this could happen because of:
- 1.You didn't select FFU-file and Emergency-files
- 2.The FFU-file is different than the current system (maybe you flashed different one before)
- If you bricked the system do the following:
- 1.Boot into Flash-Mode by pressing Power + Volume Down once the phone vibrate hold only Volume Down
- 2.Then open WDRT for possible restore
- If WDRT didn't help check the post below for alternate restore option
- https://xdaforums.com/t/bricked-950xl.3990253/#post-83830313
# C- Switch to Flash-mode:
- Goto "Manual mode"
- Select "Switch to Flash-mode"
- Wait until the phone get in the "Flash-mode"
- Now close "WPinternals"
# Phase 2 (Install the Custom Firmware):
Before flashing if you aware about your files and not sure about the process
Check "Backup Solution" at the end of this post
- Open "WDRT" folder
- Click on "File" at the top left of the window
- Select Open PowerShell
- Select Open As Administrator
- Now run the following command:
- .\thor2 -mode uefiflash -ffufile "D:\Windows_11_MOBILE_TEST1.ffu"
- "D:\.." is an example, use your own location
- Press Enter
- Wait until the process complete
- Now to restart run the following command:
- .\thor2 -mode rnd -reboot
- Note if you are using CMD remove the ".\" from the command at the beginning
- After the restart, expected to see the boot menu
Press on the camera button to select
- done
- ---------------------------------------------------------------------
# Backup Solution:
Usually I use this solution to backup my phone.
# Tool needed:
- MiniTool ShadowMaker (Paid) or trial option for 30 days
- I prefer MiniTool ShadowMaker for these reasons
- 1.Compressed Image
- 2.Faster than other softwares
- 3.You can backup the whole storage not only one partition
# Steps:
- 1.Switch to "Mass Storage mode"
- 2.Close "WPinternals"
- 3.Open "ShadowMaker "
- 4.Click "Connect " Under "This Computer"
- 5.Select "Backup"
- 6.Select "Source"
- 7.Select "Disk and Partitions
- 8.From the "combo box" Select your device "It should be at the end or the space is ~29GB"
- 9.Now select all the partitions one by one (just click on the last one and it will move to the next)
- 10.Click "OK"
- 11.Select "Destination" and set your backup folder
- 12.Click on "Backup Now"
- 13.Wait until the backup finish
- Now you have a mirror of your phone storage.
# Restore:
- 1.If your phone system is not bricked Switch to "Mass Storage mode"
- 2.Close "WPinternals"
- 3.Open "ShadowMaker"
- 4.Goto "Restore"
- 5.Select your "backup copy"
- 6.Click "Restore"
- 7.Click "Next"
- 8.Check if all partitions selected then Click "Next"
- 9.Select your "phone storage" (~29GB)
- 10.Be careful not to select another drive by mistake
- 11.Click "Next"
- 12.Then "Start"
- Note if your system is bricked.. you need to restore the system using WDRT first then do the Restore steps
# After the restore finish:
- 1.Disconnect your phone
- 2.Restart manually
- 3.Done, you have restored your old system as it was exactly.
# .
- I will not give the AndromedaOS lumia 950xl ffu file because there are still many errors like I said in the first paragraph above.

