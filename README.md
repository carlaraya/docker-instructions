# Docker Installation Instructions

### Linux

First of all, if on Linux Mint, run to find out the base Ubuntu version:
```
$ cat /etc/upstream-release/lsb-release
```

An example output is trusty 14.04. This knowledge will be needed during Docker installation.

Follow these installation tutorials, in order.

https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/

https://docs.docker.com/engine/installation/linux/linux-postinstall/

https://docs.docker.com/compose/install/

OPTIONAL: add this line to the end of your `~/.bashrc` file, to deal with file ownership issues:
```
railz() { docker-compose run web rails $@; sudo chown -R $USER:$USER .; }
```

### Windows/Mac

Install Docker Toolbox

Windows: https://docs.docker.com/toolbox/toolbox_install_windows/

Mac: https://docs.docker.com/toolbox/toolbox_install_mac/

For Windows, in the file ~/.docker/config.json, remove this line, if it exists:
```
"credsStore": "wincred"
```
