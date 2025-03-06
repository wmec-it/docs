# West-Mec IT Security Docs

![IT Security Header](https://github.com/user-attachments/assets/62e37d9c-74db-4ead-a9e9-7b223b553b9e)

## Table of Contents
- [Essential Linux Commands](#essential-linux-commands)
  - [Command-Line Utilities](#command-line-utilities)
  - [File and Directory Management](#file-and-directory-management)
  - [Process Management](#process-management)
  - [File Permissions](#file-permissions)
  - [Disk Management](#disk-management)
  - [Networking](#networking)
  - [User and Group Management](#user-and-group-management)
  - [System Management](#system-management)
  - [Package Management](#package-management)
  - [Backup and Recovery](#backup-and-recovery)
- [Kali Linux](#kali-linux)
  - [Installation Methods](#installation-methods)
  - [Command Line Basics](#command-line-basics)
  - [Package Management](#package-management)
  - [Troubleshooting](#troubleshooting)
  - [Advanced Configuration](#advanced-configuration)
  - [Mobile Applications](#mobile-applications)

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

## Kali Linux

![Kali Linux Header](https://github.com/user-attachments/assets/e2ed2fc0-afc1-48ab-8dba-829f7777bf69)

Kali Linux is a specialized Linux distribution designed for penetration testing, security auditing, and digital forensics. It comes preinstalled with numerous security tools and utilities that make it the preferred choice for cybersecurity professionals. While it shares the same foundational principles as other Linux distributions, it specifically caters to security-oriented tasks.

### Installation Methods

Kali Linux can be installed through several methods depending on your requirements and existing setup:

#### Windows Subsystem for Linux (WSL)

![WSL Header](https://github.com/user-attachments/assets/90cb24fd-7073-4583-a193-5c31aaa03559)

WSL allows Windows users to run a Linux environment directly on Windows without the overhead of a virtual machine. To install Kali Linux via WSL:

1. Open Command Prompt (CMD) as Administrator
2. Execute the following command:
   ```sh
   wsl --install -d kali-linux
   ```

#### Microsoft Store

![Microsoft Store Header](https://github.com/user-attachments/assets/c8215bb0-b0d9-4ff4-803b-755950b68be0)

For a simplified installation process:

1. Open the Microsoft Store
2. Search for "Kali Linux"
3. Download and install the application

#### Virtual Machine Installation

For a more isolated and complete Kali Linux experience, you can install it as a virtual machine using virtualization software such as VMware, VirtualBox, or Hyper-V.

##### Download Links

Official Virtual Machine Images:

- **VMware**:
  - [Direct Download](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-vmware-amd64.7z)
  - [Torrent](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-vmware-amd64.7z.torrent)

- **VirtualBox**:
  - [Direct Download](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-virtualbox-amd64.7z)
  - [Torrent](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-virtualbox-amd64.7z.torrent)

- **Hyper-V**:
  - [Direct Download](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-hyperv-amd64.7z)
  - [Torrent](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-hyperv-amd64.7z.torrent)

- **QEMU**:
  - [Direct Download](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-qemu-amd64.7z)
  - [Torrent](https://cdimage.kali.org/kali-2024.3/kali-linux-2024.3-qemu-amd64.7z.torrent)

For additional installation options, refer to the [Official Kali Linux Downloads Page](https://www.kali.org/get-kali/#kali-platforms).

### Command Line Basics

The command line interface is the primary method of interaction with Kali Linux. Mastering key commands will significantly enhance your productivity.

#### Elevating Privileges with Sudo

The `sudo` command allows you to execute commands with administrative privileges:

```sh
sudo command-name
```

To maintain elevated privileges for multiple commands, use:

```sh
sudo su
```

This will prompt for your password once and then allow you to run all subsequent commands with administrative privileges.

#### Essential Navigation Commands

- `cd` - Change directory
- `ls` - List files and directories in the current location
- `mkdir` - Create new directories

### Package Management

Kali Linux uses the APT package management system for installing, updating, and removing software packages.

#### Installing Packages

To install a package:

```sh
sudo apt install package-name
```

or

```sh
sudo apt-get install package-name
```

To automatically confirm all prompts during installation, add the `-y` flag:

```sh
sudo apt install package-name -y
```

#### Finding Packages

Browse available packages on the [official Kali Linux Tools page](https://www.kali.org/tools/).

You can also configure additional package repositories by modifying the `/etc/apt/sources.list` file to access packages from other Linux distributions.

### Troubleshooting

#### Resolving (initramfs) Boot Issues

If your system boots to an `(initramfs)` prompt, follow these steps to repair the filesystem:

1. At the `(initramfs)` prompt, identify your system partitions:
   ```sh
   blkid
   ```

2. Locate the partition with `PARTLABEL="kali"` (typically `/dev/sda1` or `/dev/sda2`)

3. Repair the filesystem:
   ```sh
   fsck /dev/sda1 -y
   ```
   (Replace `sda1` with your actual system partition)

4. Restart your system:
   ```sh
   reboot
   ```
   or
   ```sh
   exit
   ```

### Advanced Configuration

#### Customizing Shell with .bashrc

The `.bashrc` file allows you to customize your command line environment. Add command aliases to simplify complex operations:

```sh
# Add to your ~/.bashrc file:
alias cls='clear'
```

After editing the file, apply changes with:

```sh
source ~/.bashrc
```

### VPN Configuration

#### Setting Up OpenVPN with Proton VPN

For detailed instructions on configuring a VPN in Kali Linux, refer to the [Geeks for Geeks tutorial](https://www.geeksforgeeks.org/virtual-private-network-vpn-setup-in-kali-linux/).

### Mobile Applications

#### NetHunter

NetHunter is the mobile variant of Kali Linux designed for Android devices and specialized hardware.

##### Installation Instructions

1. Install [Tow-Bootloader](https://wiki.pine64.org/wiki/PinePhone_Installation_Instructions#Using_Tow-Boot) on your device

2. Write the NetHunter image to your MicroSD card:
   ```sh
   sudo dd if=IMAGE.img of=/dev/[DEVICE] bs=1M status=progress conv=fsync
   ```

3. Insert the MicroSD card into your device

4. Boot from the MicroSD card by holding the Volume Down key until the LED turns blue

5. Login with default credentials:
   - Username: `kali`
   - Password: `1234`

### Additional Resources

#### Bug Tracking and Support

Report and track bugs via the [Official Kali Linux Bug Tracker](https://bugs.kali.org/view_all_bug_page.php?filter=6740a6fac2841).
