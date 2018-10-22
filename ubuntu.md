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

### execute a command on multiple boxes via sshpass

* apt install sshpass [if not already done]

```
#!/bin/bash
read -s -p "Type in your password [then press enter]:" pass
COMMAND="$1"
for i in `seq 11 20 ; seq 51 60`;
do
        HOST="boxname$i"
        echo "Connecting to $HOST exec command $COMMAND"
        #ssh -t $HOST $COMMAND
        sshpass -p $pass ssh -q -t $HOST $COMMAND
Done
```

* and call it this way:

```
./execboxes.sh COMMAND
```
