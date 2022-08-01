# Install Termux-x11 for GUI Mode in Termux

## Install Termux-x11 by following commands

```
apt update
apt install x11-repo
apt install xwayland
```
## Now Download Termux-x11 from Termux-x11 repor github [actions.](https://github.com/termux/termux-x11/actions/workflows/debug_build.yml) and move to Termux `$Home`

### after download extract download file in Termux `$Home` and run following commands

```
unzip termux-x11.zip
dpkg -i ~/termux-x11.deb
xdg-open ~/app-debug.apk
```

### Note:- You can install termux-x11 on your way. Give apk install permission to termux to install apk.

## Now run following commands to launch termux-11 and give permissions.

```
export XDG_RUNTIME_DIR=${TMPDIR}
termux-11 :1 &
```

## To Run ubuntu in GUI Mode, login to Ubuntu and run following commands
```
unset SESSION_MANAGER
unset DBUS_SESSION_ADDRESS
export PULSE_SERVER=127.0.0.1
clear
env DISPLAY=:1 xfce4-session &
```

## That's it for Termux-x11