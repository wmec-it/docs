![IT Security Header](https://github.com/user-attachments/assets/62e37d9c-74db-4ead-a9e9-7b223b553b9e)

# Docs

## Kali Linux

![1Artboard 1kali-header-small](https://github.com/user-attachments/assets/e2ed2fc0-afc1-48ab-8dba-829f7777bf69)

Kali Linux is a very widely used operating system for penetration testing, OSINT, and cyber security in general. Although, like all other linux systems, it is not as user friendly as Windows, or MacOS. We will be learning about it in class, or we may have already learned about it. But Here are gonna be some tips and stuff that I thought I should put on here.	

### Installing

Installing Kali Linux is very easy, especially if you are using a Windows machine, and don’t mind installing it directly to your machine. Using a tool called WSL, you can easily install it with a single command, and access it like a normal app via Windows.

#### WSL

![wsl-header-smalller](https://github.com/user-attachments/assets/90cb24fd-7073-4583-a193-5c31aaa03559)

To install it via WSL, open up your Command Prompt (CMD), and type:

```sh
wsl --install -d kali-linux
```

#### Microsoft Store

![1Artboard 1msstore-header-smalller](https://github.com/user-attachments/assets/c8215bb0-b0d9-4ff4-803b-755950b68be0)

Kali Linux can also be downloaded from the Microsoft store. Search up Kali Linux, and download the app. You are done!

#### Virtual Machine

Using software of your choice (vmware, virtualbox, etc.), you can download the ISO file from Kali Downloads, or you can get the full Virtual Machine already built from Kali Virtual Machines.

##### Downloads

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

### Command Line

The command line is the main area of which Kali Linux is operated, and you should get familiar with it.

### Packages

Kali Linux has its own packages like every other Linux distribution, and stores the URLs to the server inside of your `sources.list` file (don’t need to worry about this). Kali Linux lists their packages on their main website here.
To install these packages, you need to use `apt install package-name` or `apt-get install package-name`. They will sometimes prompt you to say y/n to a question. To bypass this, add `-y` to the end of your command.

#### Search

Finding Kali packages are easy, since they are all listed on the official [tools](https://www.kali.org/tools/) page of the [Kali website](https://www.kali.org/)

You can also add package repositories to your `sources.list` file. This allows you to get packages from other sources such as Ubuntu's packages.

### Sudo

Sudo is a command used on every Linux distribution. Sudo gives the command you are running administrative privileges. Running `sudo your-command` will elevate it, and run without restrictions. Adding this to the package commands from before, it would look like this: `sudo apt-get install package-name -y`.
Another use for sudo is elevating every command you run. This can be done by running:

```bashrc
sudo su
```

And then entering in your password. Now you will be running commands as the administrator, instead of just a user.

### Common Commands

- `cd`: Move directories
- `ls`: List all files and folders in the current directory
- `mkdir`: Make directory

### NetHunter

NetHunter is basically Kali linux made for mobile devices.

#### Installation

1. Install [Tow-Bootloader](https://wiki.pine64.org/wiki/PinePhone_Installation_Instructions#Using_Tow-Boot) on your device
   
2. Write the image to your MicroSD card, e.g.
   
   ```sh
   sudo dd if=IMAGE.img of=/dev/[DEVICE] bs=1M status=progress conv=fsync
   ```
   
3. Insert the MicroSD card into your device
   
4. Boot your device from MicroSD card (hold Volume down key until the LED turns blue
   
5. Login with user "kali" and password "1234"

### Bugs

[Bug Tracker](https://bugs.kali.org/view_all_bug_page.php?filter=6740a6fac2841)

### Misc
	
#### .bashrc

`.bashrc` is a file containing instructions for prefixes in the command line. You can add new ones easily, by just adding a new line like this:

```bashrc
alias cls='clear'
```

This allows you to type in cls to run the clear command. You can do the same with longer commands, therefore expediting the process of running scans, or compiling files.
This is the same throughout all Linux distributions, so remember this.
