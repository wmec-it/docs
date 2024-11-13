![IT Security Header](https://github.com/user-attachments/assets/62e37d9c-74db-4ead-a9e9-7b223b553b9e)

# Kali Linux

Kali Linux is a very widely used operating system for penetration testing, OSINT, and cyber security in general. Although, like all other linux systems, it is not as user friendly as Windows, or MacOS. We will be learning about it in class, or we may have already learned about it. But Here are gonna be some tips and stuff that I thought I should put on here.	

## Installing

Installing Kali Linux is very easy, especially if you are using a Windows machine, and don’t mind installing it directly to your machine. Using a tool called WSL, you can easily install it with a single command, and access it like a normal app via Windows.

### WSL

To install it via WSL, open up your Command Prompt (CMD), and type:

```powershell
wsl --install -d kali-linux
```

### Microsoft Store

Kali Linux can also be downloaded from the Microsoft store. Search up Kali Linux, and download the app. You are done!

### Virtual Machine

Using software of your choice (vmware, virtualbox, etc.), you can download the ISO file from Kali Downloads, or you can get the full Virtual Machine already built from Kali Virtual Machines.

## Command Line

The command line is the main area of which Kali Linux is operated, and you should get familiar with it.

## Packages

Kali Linux has its own packages like every other Linux distribution, and stores the URLs to the server inside of your `sources.list` file (don’t need to worry about this). Kali Linux lists their packages on their main website here.
To install these packages, you need to use `apt install package-name` or `apt-get install package-name`. They will sometimes prompt you to say y/n to a question. To bypass this, add `-y` to the end of your command.

## Sudo

Sudo is a command used on every Linux distribution. Sudo gives the command you are running administrative privileges. Running `sudo your-command` will elevate it, and run without restrictions. Adding this to the package commands from before, it would look like this: `sudo apt-get install package-name -y`.
Another use for sudo is elevating every command you run. This can be done by running:

```bashrc
sudo su
```

And then entering in your password. Now you will be running commands as the administrator, instead of just a user.

## Common Commands

- `cd`: Move directories
- `ls`: List all files and folders in the current directory


## Misc
	
### .bashrc

`.bashrc` is a file containing instructions for prefixes in the command line. You can add new ones easily, by just adding a new line like this:

```bashrc
alias cls='clear'
```

This allows you to type in cls to run the clear command. You can do the same with longer commands, therefore expediting the process of running scans, or compiling files.
This is the same throughout all Linux distributions, so remember this.
