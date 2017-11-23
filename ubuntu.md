## ubuntu - Windows bash

### upgrade to latest Ubuntu version

```bash
sudo -S RELEASE_UPGRADER_NO_SCREEN=1 do-release-upgrade
```

### change password

```bash
passwd
```

### get running version

```bash
cat /etc/*-release
```

## windows subsystem

### unsintall

```cmd
lxrun /uninstall /full
```

### install from windows store

```cmd
rem ensure you drop %localappdata%\lxss before installing
lxrun /install /y
sudo -S apt-mark hold sudo
sudo -S apt-mark hold procps
sudo -S apt-mark hold strace
sudo -S RELEASE_UPGRADER_NO_SCREEN=1 do-release-upgrade
```

### set default account

```cmd
lxrun /setdefaultuser root
```
