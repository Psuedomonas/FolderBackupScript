# FolderBackupScript
Initial Code from
http://teamtutorials.com/windows-tutorials/create-a-windows-daily-backup-script 
May 9, 2007
Author Johnathan Ward

xcopy c:\test\* x:\backup\%date:~0,3%\* /Y /Q /S

The xcopy commands will copy files and folders. The syntax for the command is xcopy [destination] [arguments]. Where source is the folder that you want to backup and destination is the backup on the network drive. The arguments tell xcopy how to handle certain situations. For my script I used /Y to suppress prompting when overwriting files. If you do not include this the script will ask you before copying each file, that wouldn’t be automated. /Q doesn’t display the file names while copying. /S copies directories and sub directories. You can find more arguments by opening the command windows and typing xcopy /?.

Where you see \%date:~0,3%\ is the name of the destination folder. If you didn’t want to change the name daily you could simple call it \backup\ or something like that. The %date% is a variable. If you type %date at the command line, you will get the current date and time output. The :~0,3 tells the command line to return the first three letters of that date (0-3) and trim off the rest.

----
See 
https://www.lifewire.com/xcopy-command-2618103 And 
https://support.microsoft.com/en-us/help/289483/switches-that-you-can-use-with-xcopy-and-xcopy32-commands
For additional commands

---
Purpose:
Create a batch script for Dexis and Dentrix database backup executable by Scheduled Tasks

Progress:
A demo version I have created is having unknown issues at the moment. I was trying to impliment mmddyyyy filenames usings additional scripts but have had no success in implimenting these. Furthermore attempts to returning to the iniatial script have failed to successfully execute. I am not sure if there is an infinite loop or a strange syntax error I am overlooking due to its simplicity. In any case I cannot be sure if the current implimentation will work untill tested. It would be ideal to be able to adjust the target directory as well.
