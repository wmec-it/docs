![IT Security Header](https://github.com/user-attachments/assets/62e37d9c-74db-4ead-a9e9-7b223b553b9e)

# Linux

## Distrobutions

- [Kali Linux](#kali-linux)

## Essential Linux Commands

### Command-Line Utilities
- **`man`** – View manual pages for commands (e.g., `man ls`).
- **`whatis`** – Get a one-line description of a command (e.g., `whatis ls`).
- **`info`** – Another way to view command documentation (e.g., `info ls`).
- **`--help`** – Get a short help summary for a command (e.g., `ls --help`).
- **`echo`** – Print text to the terminal (e.g., `echo $PATH`).
- **`cat`** – View the contents of a file (e.g., `cat file.txt`).
- **`less` / `more`** – View file contents one page at a time (e.g., `less file.txt`).
- **`head` / `tail`** – View the beginning or end of a file (e.g., `head -n 10 file.txt`).
- **`grep`** – Search for a pattern in a file (e.g., `grep 'error' /var/log/syslog`).
- **`find`** – Search for files in a directory (e.g., `find /home -name "*.txt"`).
- **`awk`** – Process and analyze text (e.g., `awk '{print $1}' file.txt`).
- **`sed`** – Stream editor for text manipulation (e.g., `sed 's/foo/bar/' file.txt`).
- **`cut`** – Cut sections from a file (e.g., `cut -d: -f1 /etc/passwd`).
- **`sort`** – Sort lines of text (e.g., `sort file.txt`).
- **`uniq`** – Report or omit repeated lines in a file (e.g., `uniq file.txt`).
- **`tar`** – Archive files (e.g., `tar -czvf archive.tar.gz /directory`).
- **`zip` / `unzip`** – Compress and decompress files (e.g., `zip file.zip file.txt`, `unzip file.zip`).
- **`rsync`** – Synchronize files and directories (e.g., `rsync -av /source /destination`).

### File and Directory Management
- **`ls`** – List directory contents (e.g., `ls -l`).
- **`cd`** – Change directory (e.g., `cd /var/log`).
- **`pwd`** – Print working directory (e.g., `pwd`).
- **`mkdir`** – Create directories (e.g., `mkdir /newfolder`).
- **`rmdir`** – Remove empty directories (e.g., `rmdir /emptyfolder`).
- **`rm`** – Remove files or directories (e.g., `rm file.txt`, `rm -r folder`).
- **`cp`** – Copy files and directories (e.g., `cp file1.txt file2.txt`).
- **`mv`** – Move or rename files and directories (e.g., `mv file1.txt newfile.txt`).
- **`ln`** – Create hard and symbolic links (e.g., `ln -s /path/to/file symlink`).

### Process Management
- **`ps`** – Show current processes (e.g., `ps aux`).
- **`top`** / **`htop`** – Interactive process viewer.
- **`kill`** – Terminate a process by PID (e.g., `kill 1234`).
- **`killall`** – Kill all processes by name (e.g., `killall firefox`).
- **`pkill`** – Kill processes by name or other attributes (e.g., `pkill -f 'python'`).
- **`bg`** – Resume a suspended job in the background.
- **`fg`** – Bring a background job to the foreground.
- **`nice`** – Run a command with modified scheduling priority (e.g., `nice -n 10 command`).
- **`renice`** – Change the priority of running processes (e.g., `renice 10 -p 1234`).

### File Permissions
- **`chmod`** – Change file permissions (e.g., `chmod 755 file.txt`).
- **`chown`** – Change file owner and group (e.g., `chown user:group file.txt`).
- **`chgrp`** – Change group ownership (e.g., `chgrp group file.txt`).
- **`umask`** – Set default file permissions (e.g., `umask 022`).
- **`stat`** – Display detailed information about a file or directory (e.g., `stat file.txt`).

### Disk Management
- **`df`** – Display disk space usage (e.g., `df -h`).
- **`du`** – Display disk usage of files or directories (e.g., `du -sh /home/user`).
- **`fdisk`** – Partition table manipulator (e.g., `fdisk /dev/sda`).
- **`parted`** – Manage disk partitions (e.g., `parted /dev/sda`).
- **`mkfs`** – Create a file system on a disk partition (e.g., `mkfs.ext4 /dev/sda1`).
- **`mount`** – Mount a file system (e.g., `mount /dev/sda1 /mnt`).
- **`umount`** – Unmount a file system (e.g., `umount /mnt`).
- **`lsblk`** – List information about block devices (e.g., `lsblk`).
- **`vgcreate`, `lvcreate`, `lvextend`, `lvremove`** – LVM commands to manage volumes and groups.

### Networking
- **`ip`** – Show/manipulate IP addresses (e.g., `ip a`, `ip link set eth0 up`).
- **`ifconfig`** – Show or configure network interfaces (e.g., `ifconfig eth0 up`).
- **`ping`** – Send ICMP echo requests to a host (e.g., `ping 8.8.8.8`).
- **`traceroute`** – Trace the path packets take to a network host (e.g., `traceroute google.com`).
- **`nslookup`** – Query DNS information (e.g., `nslookup google.com`).
- **`netstat`** – Network statistics (e.g., `netstat -tuln`).
- **`nmap`** – Network exploration tool (e.g., `nmap 192.168.1.1`).
- **`ss`** – Display socket statistics (e.g., `ss -tuln`).
- **`route`** – Show or manipulate the IP routing table (e.g., `route -n`).
- **`nmcli`** – Manage network connections via command line (e.g., `nmcli device show`).

### User and Group Management
- **`useradd`** – Create a new user (e.g., `useradd john`).
- **`usermod`** – Modify user information (e.g., `usermod -aG sudo john`).
- **`userdel`** – Delete a user (e.g., `userdel john`).
- **`groupadd`** – Create a new group (e.g., `groupadd admin`).
- **`groupdel`** – Delete a group (e.g., `groupdel admin`).
- **`passwd`** – Change a user's password (e.g., `passwd john`).
- **`chage`** – Change user password expiry information (e.g., `chage -l john`).
- **`whoami`** – Display the current logged-in user (e.g., `whoami`).
- **`id`** – Display user and group IDs (e.g., `id john`).
- **`groups`** – Show the groups a user is a member of (e.g., `groups john`).

### System Management
- **`reboot`** – Reboot the system (e.g., `reboot`).
- **`shutdown`** – Shutdown or halt the system (e.g., `shutdown -h now`).
- **`halt`** – Halt the system immediately (e.g., `halt`).
- **`systemctl`** – Manage systemd services (e.g., `systemctl start apache2`).
- **`journalctl`** – View logs collected by systemd (e.g., `journalctl -xe`).
- **`hostnamectl`** – Show or set the system hostname (e.g., `hostnamectl set-hostname newhostname`).
- **`timedatectl`** – Manage system time and date settings (e.g., `timedatectl set-timezone America/New_York`).
- **`uptime`** – Show how long the system has been running (e.g., `uptime`).

### Package Management
- **`apt-get` / `apt`** – Install, update, and remove packages on Debian-based systems (e.g., `apt install package`, `apt remove package`).
- **`dnf`** – Package manager for Red Hat-based systems (e.g., `dnf install package`).
- **`rpm`** – Install, query, and remove RPM packages (e.g., `rpm -ivh package.rpm`).
- **`yum`** – Package manager for older Red Hat-based systems (e.g., `yum install package`).

### Backup and Recovery
- **`tar`** – Create and extract compressed archives (e.g., `tar -czvf archive.tar.gz folder`).
- **`dd`** – Copy and convert data (e.g., `dd if=/dev/sda of=/dev/sdb`).
- **`rsync`** – Sync files and directories (e.g., `rsync -av source/ destination/`).

# Kali Linux

![1Artboard 1kali-header-small](https://github.com/user-attachments/assets/e2ed2fc0-afc1-48ab-8dba-829f7777bf69)

Kali Linux is a very widely used operating system for penetration testing, OSINT, and cyber security in general. Although, like all other linux systems, it is not as user friendly as Windows, or MacOS. We will be learning about it in class, or we may have already learned about it. But Here are gonna be some tips and stuff that I thought I should put on here.	

## Installing

Installing Kali Linux is very easy, especially if you are using a Windows machine, and don’t mind installing it directly to your machine. Using a tool called WSL, you can easily install it with a single command, and access it like a normal app via Windows.

### WSL

![wsl-header-smalller](https://github.com/user-attachments/assets/90cb24fd-7073-4583-a193-5c31aaa03559)

To install it via WSL, open up your Command Prompt (CMD), and type:

```sh
wsl --install -d kali-linux
```

### Microsoft Store

![1Artboard 1msstore-header-smalller](https://github.com/user-attachments/assets/c8215bb0-b0d9-4ff4-803b-755950b68be0)

Kali Linux can also be downloaded from the Microsoft store. Search up Kali Linux, and download the app. You are done!

### Virtual Machine

Using software of your choice (vmware, virtualbox, etc.), you can download the ISO file from Kali Downloads, or you can get the full Virtual Machine already built from Kali Virtual Machines.

#### Downloads

- [vmware](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-vmware-amd64.7z)

- [vmware TORRENT](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-vmware-amd64.7z.torrent)

- [VirtualBox](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-virtualbox-amd64.7z)

- [VirtualBox TORRENT](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-virtualbox-amd64.7z.torrent)

- [Hyper-V](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-hyperv-amd64.7z)

- [Hyper-V TORRENT](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-hyperv-amd64.7z.torrent)

- [QEMU](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-qemu-amd64.7z)

- [QEMU TORRENT](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-qemu-amd64.7z.torrent)

If none of those work, here is the downloads page where they are listed.

[Kali Downloads Page](https://www.kali.org/get-kali/#kali-platforms)

---

## Command Line


The command line is the main area of which Kali Linux is operated, and you should get familiar with it.

### Sudo

Sudo is a command used on every Linux distribution. Sudo gives the command you are running administrative privileges. Running `sudo your-command` will elevate it, and run without restrictions. Adding this to the package commands from before, it would look like this: `sudo apt-get install package-name -y`.
Another use for sudo is elevating every command you run. This can be done by running:

```bashrc
sudo su
```

And then entering in your password. Now you will be running commands as the administrator, instead of just a user.

---

## Packages

Kali Linux has its own packages like every other Linux distribution, and stores the URLs to the server inside of your `sources.list` file (don’t need to worry about this). Kali Linux lists their packages on their main website here.
To install these packages, you need to use `apt install package-name` or `apt-get install package-name`. They will sometimes prompt you to say y/n to a question. To bypass this, add `-y` to the end of your command.

### Search

Finding Kali packages are easy, since they are all listed on the official [tools](https://www.kali.org/tools/) page of the [Kali website](https://www.kali.org/).

You can also add package repositories to your `sources.list` file. This allows you to get packages from other sources such as Ubuntu's packages.

---

## Errors / Debugging / Issues

### (initramfs)

#### Activated on reboot

This issue is usually caused by broken OS files. This can be fixed by running a repair on the `(initramfs)` shell that appears.

***Step 1***

```sh
blkid
```

***Step 2***

Look for the drive with the `PARTLABEL="kali"` in the output of the previous command (it is usually `sda1` or `sda2`).

***Step 3***

Run this command, but replace the `sda1` with whatever drive you have your OS installed on (the one you previously used in the last step).

```sh
fsck /dev/sda1 -y
```

***Step 4***

Restart your computer.

```sh
reboot
```

```sh
exit
```

Or just manually restart it if both commands do not work.

---

## VPN

### OpenVPN

#### Proton VPN

[Geeks for Geeks tutorial](https://www.geeksforgeeks.org/virtual-private-network-vpn-setup-in-kali-linux/)

---

## Common Commands

- `cd`: Move directories
- `ls`: List all files and folders in the current directory
- `mkdir`: Make directory

---

## NetHunter

NetHunter is basically Kali linux made for mobile devices.

### Installation

1. Install [Tow-Bootloader](https://wiki.pine64.org/wiki/PinePhone_Installation_Instructions#Using_Tow-Boot) on your device.
   
2. Write the image to your MicroSD card, e.g.
   
   ```sh
   sudo dd if=IMAGE.img of=/dev/[DEVICE] bs=1M status=progress conv=fsync
   ```
   
3. Insert the MicroSD card into your device.
   
4. Boot your device from MicroSD card (hold Volume down key until the LED turns blue).
   
5. Login with user `kali` and password `1234`.

---

## Bugs

[Bug Tracker](https://bugs.kali.org/view_all_bug_page.php?filter=6740a6fac2841)

---

## Misc
	
### .bashrc

`.bashrc` is a file containing instructions for prefixes in the command line. You can add new ones easily, by just adding a new line like this:

```bashrc
alias cls='clear'
```

This allows you to type in cls to run the clear command. You can do the same with longer commands, therefore expediting the process of running scans, or compiling files.
This is the same throughout all Linux distributions, so remember this.
