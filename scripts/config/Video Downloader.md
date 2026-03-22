### YTDLP - Video Downloader

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

```bash
-o %(title)s.%(ext)s
--download-archive /Users/jr/archive.txt
--playlist-end 10
--embed-thumbnail
--embed-metadata
--embed-info-json
--embed-chapters
--cookies-from-browser chrome
--sub-langs en
--sleep-interval 65
--merge-output-format mp4
--default-search ytsearch
--user-agent "Mozilla/5.0 (Windows NT 10.0; Win64; x64)"
--sleep-requests 5
--concurrent-fragments 1
--sleep-interval 120
--max-sleep-interval 300
--limit-rate 500K
```
