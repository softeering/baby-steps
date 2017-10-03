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
lxrun /install /y
```

### set default account

```cmd
lxrun /setdefaultuser root
```
