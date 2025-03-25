I use MLTB by Anasty.

### Onedrive Token expired
Creating rclone.conf from local computer and replacing it with the one in bot is easier than doing rclone config reconnect Onedrive: in server, then using local computer to generate token, then entering it in the terminal. If later is done, then 99% chances that it will fail.
Use local computer.
Download rclone if not already there.
Locate the downloaded folder, open cmd there and run rclone to check if it's running or not.
If running, then do rclone config.
Create new remotes.
Locate the newly created rclone.conf in %APPDATA%/rclone.
Upload it to bsetting/private files and usetting/rclone in bot's private chat.