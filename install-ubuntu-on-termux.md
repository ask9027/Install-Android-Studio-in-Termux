# Install Ubuntu in Termux
## Open Termux and run following commands

```bash
pkg update -y
apt install x11-repo
apt install proot-distro && pulseaudio
```

## After installation of `proot-distro` install ubuntu by following cammands.

`proot-distro install ubuntu`

## now login to ubuntu
`proot-distro login ubuntu`

## After login run following commands
```bash
apt update -y
apt install sudo gvfs-daemons xfce4 xfce4-terminal thunar-archive-plugin ffmpeg tzdata apt-utils xz-utils vim
```

## After all installed , Create user and password

`adduser username`
### Replace `username` with your username

### Now add user to sudoers
`vim /etc/sudoers`
### add user `username ALL=(ALL:ALL) ALL` below to `root ALL=(ALL:ALL) ALL`
### now logout from ubuntu  by `exit`

## After all set login ubuntu to added user
```
pluseaudio --start --load ="module-native-protocal-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" --exit-idle-time=-1
proot-distro login --user username ubuntu --shared-tmp --bind /dev/null:/proc/sys/kernel/cap_last_cap
```

## That's it for install ubuntu on Termux.

