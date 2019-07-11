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
