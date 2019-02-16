# Modern Development Setup
This is a template that I am slowly refining to modernize my development environment. This is also the template I will be using to teach from and therefore I require it to accomodate the various operating systems that my students will be using.

## OS Agnostic Toolbench
- Docker
- Powershell
- Make
- Firefox
- ngrok
- VSCode
- Terminal Manager

# Windows 10 Home

- Docker : https://github.com/mstraughan86/docker-for-windows10home
- Powershell : https://github.com/powershell/powershell#get-powershell

- Windows Subsystem for Linux : ```(powershell as admin)```
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
- WSL: Ubuntu : https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6
- Chocolatey : 
```
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
- Make : ```(powershell as admin)```
```
choco install make -y
```
- Firefox : ```(powershell as admin)```
```
choco install firefox -y
[Environment]::SetEnvironmentVariable(
    "Path",
    [Environment]::GetEnvironmentVariable("Path", [EnvironmentVariableTarget]::Machine) + ";C:\Program Files\Mozilla Firefox",
    [EnvironmentVariableTarget]::Machine)
```
- ngrok : ```(powershell as admin)```
```
choco install ngrok -y
```
- VSCode : ```(powershell as admin)```
```
choco install vscode -y
```
- Cmder : ```(powershell as admin)```
```
choco install cmder -y
```

# Ubuntu 18.04
- Docker : 
```
sudo apt update
sudo apt upgrade
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update
sudo systemctl status docker
docker -v
sudo usermod -aG docker $USER
```
- Powershell : https://github.com/powershell/powershell#get-powershell
- Make : 
```
sudo apt install build-essential -y
```
- Firefox : 
```
sudo apt install firefox -y
```
- ngrok :
```
wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip
unzip ngrok-stable-linux-amd64.zip
sudo mv ./ngrok /usr/local/bin/ngrok
echo 'PATH=$PATH:/usr/local/bin/ngrok' >> ~/.bashrc
```
- VSCode :
```
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code
```
- Guake : 
```
sudo apt-get install guake -y
```
