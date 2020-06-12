# Sudo-su-Termux
A bash script to install the sudo functionality in termux.

**Requirements**

The device must be rooted else this will not work.

**Installing sudo**

1. Open termux 
2. Copy this command 
```
wget https://raw.githubusercontent.com/xicor22/Sudo-su-Termux/master/install.sh && chmod +x install.sh && ./install.sh
```
3. Done!

**Features**

- Sets up its environment automatically on first run, no need to do anything but use it
- Creates a root folder ```.suroot``` in the Termux home folder with proper root permissions and ownership
- Creates ```.bashrc``` file in root folder with proper PATH and LD_LIBRARY_PATH variables set so all binaries function correctly
- Bash prompt PS1 variable is also set so you don't have ```bash-4.4#``` as prompt just ```#```
- Automatically creates ```.bash_history``` in root folder when you drop to a root shell so root shell history is preserved
- Can be used like ordinary sudo (but only as root, no other user)
- Can drop to root shell ```sudo su [-]```
- Runs built in Termux binaries and exteral binaries with optional arguments as root in current directory
- Generates output in shell currently using
- Can be used in other bash scripts
- [option] Can turn off colored error messages be editing the variable ```colored``` at the beginning of sudo file

```
Usage:

sudo su [-]  
  Drop to root shell

sudo <command> [<args>]  
  Run command as root with optional arguments
```

**This was inspired by the following:**

https://gitlab.com/st42/termux-sudo
