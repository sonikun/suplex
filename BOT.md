I use MLTB by Anasty.

# Onedrive Token expired
### 1. Direct Method
- Type the following in VPS terminal
```
rclone config reconnect Onedrive:
```
- Follow the instructions and renew the token

### 2. Local PC Method (recommended)

- Use local computer.
- Download rclone if not already there.
- Locate the downloaded folder, open cmd there and run `rclone` to check if it's running or not.
- If running, then do `rclone config`.
- Create new remotes.
- Locate the newly created rclone.conf in `%APPDATA%/rclone`.
- Upload it to bsetting/private files and usetting/rclone in bot's private chat.
