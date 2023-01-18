# docker-vagrant

To install Docker (server and client) binaries and Docker Compose locally, open Powershell as Administrator and run `install_docker.ps1`.

To provision the VM containing the Docker service, run `vagrant up`.

To create shared folders for this VM:
```
PS C:\> cd 'C:\Program Files\Oracle\VirtualBox\'
PS C:\Program Files\Oracle\VirtualBox> .\VBoxManage.exe sharedfolder add "docker-vagrant" --name="sharename" --hostpath="C:\test" --automount --auto-mount-point="/test"
```
