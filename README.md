# Installing Kali Linux and Ubuntu on Windows with WSL

This repository provides a guide on how to install Kali Linux and Ubuntu on Windows using the Windows Subsystem for Linux (WSL).

## Prerequisites

- Windows 10 or later.
- Administrative privileges on your Windows machine.

## Enabling WSL

1. **Enable WSL through Windows Features:**
   - Open the Start menu and search for “Turn Windows features on or off” and select it.
   - Scroll down in the Windows Features window and check the box next to “Windows Subsystem for Linux”.
   - Click OK and wait for the installation to complete. You might be prompted to restart your computer.

2. **For WSL 2 (optional):** 
   - In the Start menu, search for “Turn Windows features on or off” and open it.
   - Scroll and find “Virtual Machine Platform”, check the box next to it.
   - Click OK and restart your computer when prompted.
   - After restarting, open PowerShell as an administrator and set WSL 2 as the default version:
     ```
     wsl --set-default-version 2
     ```

3. **Restart your computer.**

## Installing Kali Linux and Ubuntu

### Kali Linux

1. **Open Microsoft Store** and search for “Kali Linux”.

2. **Install Kali Linux** by clicking on the ‘Get’ button.

3. **Launch Kali Linux** from the Start menu and follow the on-screen instructions to finish the setup.

### Ubuntu

1. **Open Microsoft Store** and search for “Ubuntu”.

2. **Choose the Ubuntu version** you prefer (e.g., Ubuntu 20.04 LTS) and click ‘Get’ to install.

3. **Launch Ubuntu** from the Start menu and follow the on-screen instructions to complete the installation.

## Post-Installation

- Set up a new user account and password when prompted during the first launch.
- Update your Linux distribution(s) with the following commands:
```
sudo apt update
sudo apt upgrade
```

## Changing Your Hostname in WSL (optional)

To change your hostname in WSL, follow these steps:

1. **Open Your WSL Terminal:**
   - Launch your WSL distribution (Kali Linux or Ubuntu) from the Start menu.

2. **Change the Hostname:**
   - Use a text editor (like `nano` or `vi`) to add this into the `/etc/wsl.conf` file:
     ```bash
     [network]
     hostname = <desire-hostname>
     generateHosts = false
     ```

3. **Edit the Hosts File:**
   - Edit the `/etc/hosts` file:
     ```bash
     sudo vi /etc/hosts
     ```
   - Find the line with your old hostname and replace it with the new one.

4. **Apply the Changes:**
   - Save the changes and exit the editor.
   - To apply the changes, exit WSL and then restart it:
     - Close the WSL terminal.
     - Open PowerShell as Administrator on Windows and run:
       ```
       wsl --shutdown
       ```
     - Reopen your WSL terminal.

5. **Verify the Change:**
   - Check your new hostname by typing `hostname` in your WSL terminal.

Note: In WSL 1, hostname changes are not persistent between restarts. In WSL 2, these changes will persist.

## Usage

- Access your WSL distributions via the Start menu typing ```Ubuntu``` or ```Kali Linux```
- Access your WSL distributions through the CMD by typing the command:
   ```
   wsl -d <distro>
   ```

## Additional Resources

- [WSL Documentation](https://docs.microsoft.com/en-us/windows/wsl/)
- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Ubuntu Documentation](https://ubuntu.com/tutorials/command-line-for-beginners)

## Contributing

Contributions to this guide are welcome! Please feel free to submit pull requests or open issues for any improvements or corrections.
