up:: [[Computer Science MOC]]
tags:: #Programming  
# Linux Commands
Here are some of the most popular and commonly used Linux commands:
## Navigating
- Up and down arrows: shift through commands you recently used
## Common:
- `. ->` file is in the current folder
- `.. -->` file is in the parent folder
	- Running an executable: `./Helloworld`
## Basic Commands

1. `ls` - Shows all of the contents in the directory
   - Example: `ls -la`

2. `cd` - Change directory.
   - Example: `cd /home/user`
   - Current directory `.` , home directory `..`, going from deep all the way back to home just type `cd`

3. `pwd` - Print working directory (where you are)

4. `mkdir` - Make directories.
   - Example: `mkdir new_folder`

5. `rm` - Remove files or directories.
   - Example: `rm file.txt`, `rm -r folder`
	   - Super remover: (recursive remove): `rm -rf`

6. `cp` - Copy files or directories.
   - Example: `cp source_file destination_file`
   - if you have folders within folders, need to do `cp -r sourcefile destinationfile`
	   - -r means recursive -> computer keeps going in folders and copying

7. `mv` - Move or rename files or directories.
   - Example: `mv old_name new_name`

8. `touch` - Create an empty file or update the timestamp of a file.
   - Example: `touch newfile.txt`

9. `cat` - Concatenate and display files.
   - Example: `cat file.txt`

10. `echo` - Display a line of text.
    - Example: `echo "Hello, World!"`

### File Viewing and Editing

1. `nano` - A simple text editor.
   - Example: `nano file.txt`

2. `vi` or `vim` - A powerful text editor.
   - Example: `vim file.txt`

3. `less` - View file contents one screen at a time.
   - Example: `less file.txt`

4. `more` - View file contents with paging.
   - Example: `more file.txt`

### System Information

1. `uname` - Print system information.
   - Example: `uname -a`

2. `top` - Display tasks and system resource usage.

3. `htop` - An interactive process viewer.
   - Example: `htop` (if installed)

4. `df` - Display disk space usage.
   - Example: `df -h`

5. `du` - Estimate file space usage.
   - Example: `du -sh folder`

6. `free` - Display memory usage.
   - Example: `free -h`

### Process Management

1. `ps` - Report a snapshot of current processes.
   - Example: `ps aux`

2. `kill` - Terminate processes by PID.
   - Example: `kill 1234`

3. `killall` - Kill processes by name.
   - Example: `killall processname`

### Networking

1. `ping` - Send ICMP ECHO_REQUEST to network hosts.
   - Example: `ping google.com`

2. `ifconfig` - Configure network interfaces (deprecated, use `ip`).
   - Example: `ifconfig`

3. `ip` - Show/manipulate routing, devices, policy routing, and tunnels.
   - Example: `ip addr`

4. `wget` - Non-interactive network downloader.
   - Example: `wget http://example.com/file.zip`

5. `curl` - Transfer data from or to a server.
   - Example: `curl http://example.com`

### File Permissions

1. `chmod` - Change file modes or Access Control Lists.
   - Example: `chmod 755 file.sh`

2. `chown` - Change file owner and group.
   - Example: `chown user:group file.txt`

### Archiving and Compression

1. `tar` - Store and extract files from a tarball.
   - Example: `tar -cvf archive.tar folder`, `tar -xvf archive.tar`

2. `gzip` - Compress files.
   - Example: `gzip file.txt`

3. `gunzip` - Decompress files.
   - Example: `gunzip file.txt.gz`

4. `zip` - Package and compress (archive) files.
   - Example: `zip archive.zip file1 file2`

5. `unzip` - Extract compressed files.
   - Example: `unzip archive.zip`

### Searching

1. `grep` - Print lines matching a pattern.
   - Example: `grep "search_term" file.txt`

2. `find` - Search for files in a directory hierarchy.
   - Example: `find /path -name "filename"`

3. `locate` - Find files by name.
   - Example: `locate filename`

### System Updates and Package Management

1. `apt-get` - APT package handling utility (Debian-based).
   - Example: `sudo apt-get update`, `sudo apt-get upgrade`

2. `yum` - Package manager for RPM-based distributions.
   - Example: `sudo yum update`

3. `dnf` - Package manager for RPM-based distributions (newer than yum).
   - Example: `sudo dnf update`

4. `pacman` - Package manager utility (Arch Linux).
   - Example: `sudo pacman -Syu`

