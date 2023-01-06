# Initial setup 
Describe all steps 

### Install podman
Follow installation instructions at [Podman for Windows](https://github.com/containers/podman/blob/main/docs/tutorials/podman-for-windows.md)

### Podman machine init process
```
PS C:\Users\aniru> podman machine init
Extracting compressed file
Importing operating system into WSL (this may take a few minutes on a new WSL install)...
Configuring system...
Generating public/private ed25519 key pair.
Your identification has been saved in podman-machine-default
Your public key has been saved in podman-machine-default.pub
The key fingerprint is:
Machine init complete
To start your machine run:

        podman machine start
```

### Podman machine start
```
PS C:\Users\aniru> podman machine start
Starting machine "podman-machine-default"

This machine is currently configured in rootless mode. If your containers
require root permissions (e.g. ports < 1024), or if you run into compatibility
issues with non-podman clients, you can switch using the following command:

        podman machine set --rootful

API forwarding listening on: npipe:////./pipe/podman-machine-default

Another process was listening on the default Docker API pipe address.
You can still connect Docker API clients by setting DOCKER HOST using the
following powershell command in your terminal session:

        $Env:DOCKER_HOST = 'npipe:////./pipe/podman-machine-default'

Or in a classic CMD prompt:

        set DOCKER_HOST = 'npipe:////./pipe/podman-machine-default'

Alternatively terminate the other process and restart podman machine.
Machine "podman-machine-default" started successfully
```

### Test podman
We test podman installation by running a micro image from redhat that runs the `date` command
```
PS C:\Users\aniru> podman run ubi8-micro date
Resolved "ubi8-micro" as an alias (/etc/containers/registries.conf.d/000-shortnames.conf)
Trying to pull registry.access.redhat.com/ubi8-micro:latest...
Getting image source signatures
Check`ing if image destination supports signatures
Copying blob sha256:fdb82fb306d5fe8a181e0c0703110bd192c0bbb8ab32a727d4e268f22a3e3262
Copying config sha256:655e3818c6df1519b648e932994e941985699873946fd12ac8ff250dfca2d6bf
Writing manifest to image destination
Storing signatures
Fri Jan  6 03:01:52 UTC 2023
```

### Check podman machine status
```
PS C:\Users\aniru\workspace\github\python-podman> podman machine ls
NAME                     VM TYPE     CREATED      LAST UP            CPUS        MEMORY      DISK SIZE
podman-machine-default*  wsl         6 hours ago  Currently running  8           920.3MB     1.542GB
```