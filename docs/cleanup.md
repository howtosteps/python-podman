# Cleanup 

### Stop the container
Stop the container using `podman stop <ContainerID>` command
```
PS C:\Users\aniru\workspace\github\python-podman> podman stop 3bad5052037c
3bad5052037c
```

### Remove the container 
To delete a Podman container, first make sure that the container has been stopped. Then, use the `podman rm` command followed by the container's name or ID.
```

```
###
To stop a running podman machine, use the `podman machine stop` command. 


```
PS C:\Users\aniru\workspace\github\python-podman> podman machine stop
Machine "podman-machine-default" stopped successfully
PS C:\Users\aniru\workspace\github\python-podman> podman machine ls
NAME                     VM TYPE     CREATED      LAST UP             CPUS        MEMORY      DISK SIZE
podman-machine-default*  wsl         6 hours ago  About a minute ago  0           0B          1.777GB
PS C:\Users\aniru\workspace\github\python-podman>
```