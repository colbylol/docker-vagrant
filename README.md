# docker-vagrant

To provision the VM containing the Docker service, run `vagrant up`.

Once completed, you can access the machine via `ssh`:

```
vagrant ssh
```

To shutdown the vagrant machine:

```
vagrant halt
```

To remove the vagrant machine:

```
vagrant destroy
```

To create shared folders for this VM:
```
PS C:\> cd 'C:\Program Files\Oracle\VirtualBox\'
PS C:\Program Files\Oracle\VirtualBox> .\VBoxManage.exe sharedfolder add "docker-vagrant" --name="sharename" --hostpath="C:\test" --automount --auto-mount-point="/test"
```

Refer to the documentation on the [Vagrant](https://www.vagrantup.com) website for more information.

## Local development using VSCode

1. Install the "Remote - SSH" extension by Microsoft.
2. In the repository root, dump the vagrant SSH configuration:

```
vagrant ssh-config
```

3. Create a new SSH host in VSCode, using the configuration from the previous step.

## Local Docker CLI (optional)

To install Docker (server and client) binaries and Docker Compose locally, open Powershell as Administrator and run `install_docker.ps1`.