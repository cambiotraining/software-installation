---
pagetitle: "Software installation"
---

# WSL

The **Windows Subsystem for Linux (WSL2)** is a compatibility layer within Windows that enables users to run a Linux "core" alongside the Windows operating system. 
It is available for Windows 11 and recent versions of Windows 10. 

WSL2 provides a seamless integration between Windows and Linux environments, allowing users to execute native Linux commands and run Linux applications directly on a Windows machine. 
WSL2 is designed to be compatible with the Windows filesystem, allowing you to easily interact with your Windows files.


## Installing WSL2

There are detailed instructions on how to install WSL on the [Microsoft documentation page](https://learn.microsoft.com/en-us/windows/wsl/install). 
But briefly:

- Click the Windows key and search for  _Windows PowerShell_, right-click on the app and choose **Run as administrator**. 
- Answer "Yes" when it asks if you want the App to make changes on your computer. 
- A terminal will open; run the command: `wsl --install`.  
  Progress bars will show while installing "Virtual Machine Platform", "Windows Subsystem for Linux" and finally "Ubuntu" (this process can take a long time).
- After installation completes, restart your computer.
- After restart, a terminal window will open asking you to create a username and password.  
  If it doesn't, click the Windows key and search for _Ubuntu_, click on the App and it should open a new terminal. 
  - You can use the same username and password that you have on Windows, or a different one - it's your choice. Spaces and other special characters are not allowed for your Ubuntu username.
  - **Note:** when you type your password nothing seems to be happening as the cursor doesn't move. However, the terminal is recording your password as you type. You will be asked to type the new password again to confirm it, so you can always try again if you get it wrong the first time.

You should now have access to a Ubuntu Linux terminal. 
This behaves very much like a regular Ubuntu server. 


## Directory shortcuts

After installation, it is useful to **create shortcuts to your directories on Windows**. 
Your main `C:\` drive is located in `/mnt/c/` and other drives will be equally available based on their letter. 
To create shortcuts to commonly-used directories you use _symbolic links_. 

The following commands automatically create shortcuts to your Windows "Documents", "Desktop" and "Downloads" folders (copy/paste these commands on the terminal):

```bash
ln -s $(wslpath $(powershell.exe '[environment]::getfolderpath("MyDocuments")' | tr -d '\r')) ~/Documents
ln -s $(wslpath $(powershell.exe '[environment]::getfolderpath("Desktop")' | tr -d '\r')) ~/Desktop
ln -s $(wslpath $(powershell.exe '[environment]::getfolderpath("UserProfile")' | tr -d '\r'))/Downloads ~/Downloads
```

After running these commands, if you list the files in your home directory (`ls -l`), you should see the shortcuts just created. 


## Default terminal

You can **configure the Windows terminal to automatically open _WSL2_** (instead of the default Windows Command Prompt or Powershell):

- Search for and open the "<i class="fa-solid fa-terminal"></i> Terminal" application.
- Click on the down arrow <i class="fa-solid fa-chevron-down"></i> in the toolbar.
- Click on "<i class="fa-solid fa-gear"></i> Settings".
- Under "Default Profile" select "<i class="fa-brands fa-linux"></i> Ubuntu".


## Visual Studio Code

Visual Studio Code is a text editor which integrates very well with WSL2. 
Instructions to install it are given on a [separate page](vscode.md).


