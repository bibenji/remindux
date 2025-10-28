# REMINDUX
### Reminder for Linux

## Ports used

```
sudo lsof -i -P -n | grep LISTEN 
sudo netstat -tulpn | grep LISTEN
sudo nmap -sTU -O IP-address-Here
```

## Configuration matérielle

```
cat /proc/cpuinfo
cat /proc/asound/cards
lspci -v|vv|vvv|n|nn|tv
lshw
sudo dmidecode
sudo dmidecode -t memory
sudo dmidecode -t processor 
sudo dmidecode -t slot
sudo dmidecode -t connector
```

# REMINGIT
### Reminder for Git

Git bisect : on démarre, on checke le commit et on répond par git bisect good or git bisect bad
```
git bisect start
git bisect bad
git bisect good d7ffe6a
or:
git bisect start HEAD d7ffe6a
to finish:
git bisect reset
et si on peut pas savoir si y'a le bug :
git bisect skip

git bisect log
git bisect replay
```

Show a file at a specific commit
```
git show d7ffe6a:demo.sh
```

# REMINVIM
### Reminder for Vim

Copy, Cut And Paste :

In visual mode :
```asp
v to select or V to select line (or ctrl-v for blocks?)
d (or y to copy)
P to paste before cursor or p to paste after
```



Copy one line :

In visual mode : yy then p

Copy multi lines :

In visual mode : 2j or v2j then y (for yank) or x (for cut) then p

Delete one line :

In visual mode : dd

Delete multi lines :

In visual mode : 5dd

# AUDIO
### Reminder for audio controllers

libasound lit /proc/asound/cards ou /dev/snd/controlC*

Pour monitorer les events de UDEV + KERNEL
`udevadm monitor --subsystem-match=sound`

```
cat /proc/asound/cards
cat /proc/asound/devices
aplay -l
arecord -l
aconnect -l
```

checker /dev/snd pour voir ce qui est monté par le kernel
