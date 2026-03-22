### Video Downloader

**To check status of Plex:**
systemctl status plexmediaserver

**To upgrade Plex:**
sudo apt upgrade plexmediaserver

**To upgrade YT-DLP:**
sudo apt update
sudo apt upgrade yt-dlp

**To upgrade FFMPEG:**
sudo apt update
sudo apt upgrade ffmpeg

**Downloading yt-dlp Videos**
sudo yt-dlp --merge-output-format mp4 youtube.com/watch?v=-enMGeJF2Dk

**To map a Network share:**
1. Create the directory by: sudo mkdir <directory-name>
2. Edit FSTAB: sudo nano /etc/fstab
3. Add configuration line such as: 
//192.168.1.10/MEDIA /mnt/MEDIA cifs rw,username=plexprxmx,password=password12345 0 0
4. Mount the share by: sudo mount a

**Login Credentials**
User:user
Password:password

**IP ADDR**
192.168.1.#

**Symbolic Link**
Create Symlink for Directory
A symbolic link can point to a directory's absolute or relative path. Use the following syntax to create a symbolic link to a directory in Linux:

ln -s [target-directory] [symlink]

The example below creates a symbolic link named test-link in the home (~/) directory. The link references a directory on a mounted CD.

ln -s /media/marko/VBox_GAs_6.1.38/cert ~/test-link

scp username@remotecomputer:/path/to/file/you/want/to/copy where/to/put/file/on/laptop

```shell
########################################
# 🧠 GENERAL SETTINGS
########################################

# Disable zsh errors for unmatched patterns (optional safety off)
# setopt NO_NOMATCH

########################################
# 📦 PATH SETTINGS
########################################

# Ensure user-installed Python binaries are available (pip installs)
export PATH="$HOME/Library/Python/3.*/bin:$PATH"

# Ensure Homebrew binaries are available
export PATH="/usr/local/bin:/opt/homebrew/bin:$PATH"
export PATH="$HOME/Users/jr/Library/Python/3.9/bin:$PATH"
export PATH="/usr/local/opt/ffmpeg-full/bin:$PATH"

# Enable aliases
alias yt='sudo noglob yt-dlp -f "bestvideo+bestaudio/best"'

########################################
# 📦 PATH SETTINGS
########################################

# Ensure user-installed Python binaries are available (pip installs)
export PATH="$HOME/Library/Python/3.*/bin:$PATH"

# Ensure Homebrew binaries are available
export PATH="/usr/local/bin:/opt/homebrew/bin:$PATH"

########################################
# 🎬 YT-DLP SETTINGS
########################################

# Prevent zsh from interpreting special characters in URLs (VERY IMPORTANT)
alias yt='noglob yt-dlp -f "bestvideo+bestaudio/best"'

# List available formats for a video
alias ytf='noglob yt-dlp -F'

# Download audio only (mp3)
alias yta='noglob yt-dlp -x --audio-format mp3'

# Download playlist/channel safely (respects config throttling)
alias ytpl='noglob yt-dlp --yes-playlist'

########################################
# 📁 NAVIGATION SHORTCUTS
########################################

# Go to your download/media folder (adjust to your setup)
alias dl='cd ~/Downloads/YT'

########################################
# 🍪 COOKIE MANAGEMENT
########################################

# Quick check to confirm cookies file exists
alias cookie='ls -l ~/.config/yt-dlp/cookies.txt'

########################################
# 🧪 DEBUGGING & TESTING
########################################

# Run yt-dlp in verbose mode for troubleshooting
alias ytd='noglob yt-dlp -v'

########################################
# 🔄 RELOAD CONFIG
########################################

# Reload your zsh config without restarting terminal
alias reload='source ~/.zshrc'

########################################
# 📝 NOTES
########################################

# - Always keep cookies fresh to avoid YouTube bot checks
# - If downloads fail, run: ytd "URL" for debug output
# - Use your iMac (residential IP) for best reliability
```

```bash
# Current yt-dlp configuration
-o %(title)s.%(ext)s
# Strips the YouTube Video ID []
--download-archive /Users/jr/.config/yt-dlp/archive.txt
# Adds the downloaded video to a text file should I need to check whether or not the file has already been downloaded
--playlist-end 10

--embed-thumbnail
# Embeds the video thumbail into the downladed video file
--embed-metadata
# Embeds the video metadata into the downloaded video file
--embed-info-json
#
--embed-chapters
# Embeds chapter markers into the downloaded video file
--cookies-from-browser chrome
# Uses cookies from CHROME to authenticate with YouTube to prove that you are not a robot
--sub-langs en
#
--sleep-interval 65
#
--merge-output-format mp4
# Ensures the download video is in the mp4 file container
--default-search ytsearch
#
--user-agent "Mozilla/5.0 (Windows NT 10.0; Win64; x64)"
#
--sleep-requests 5
#
--concurrent-fragments 1
#
--sleep-interval 120
#
--max-sleep-interval 300
#
--limit-rate 500K
#
```
@echo off
GOTO :TopOfCode

This entire section is a comment block,
and can contain any characters without
causing errors because the script execution
jumps right over it.

:TopOfCode
REM Your actual code starts here
...
