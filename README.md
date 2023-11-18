# Installing Kali Linux and Ubuntu on Windows with WSL

This repository provides a guide on how to install Kali Linux and Ubuntu on Windows using the Windows Subsystem for Linux (WSL).

## Prerequisites

- Windows 10 or later.
- Administrative privileges on your Windows machine.

## Enabling WSL

1. **Open PowerShell as Administrator** and run:
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

2. **For WSL 2 (optional):** 
- Enable the Virtual Machine Platform feature:
  ```
  dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
  ```
- Set WSL 2 as the default version:
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

## Usage

- Access your WSL distributions via the Start menu typing ```wsl```
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
