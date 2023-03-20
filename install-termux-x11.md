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

## Now run following commands to make termux-11 usable.

```
DISPLAY=:0 termux-x11 &
```

## To Run ubuntu in GUI Mode, login to Ubuntu and run following commands
before ubuntu in GUI Mode install `xvfb` in ubuntu.
`sudo apt install xvfb`
Now you good to go 
```
export PULSE_SERVER=127.0.0.1
export DISPLAY=:0
Xvfb :0 -ac -screen 0 4090x4090x24 &
dbus-launch --exit-with-session startxfce4 &
```

### ***Note:-*** Don't try to change screen height or width otherwise display don't work properly.

## That's it for Termux-x11
