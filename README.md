# Install-Android-Studio-in-Termux

## First need to Login to Ubuntu.

Download and install termux from [here.](https://github.com/termux/termux-app/releases)

install ubuntu from [here.](install-ubuntu-on-termux.md)

## Now login to user in ubuntu

## update and install jdk-11

```bash
sudo apt update
sudo apt install openjdk-11-jdk -y # or openjdk-17-jdk
```
## GUI Mode (need to Termux-x11 installed) 
### Install Termux-x11 from [here.](https://github.com/termux/termux-x11.git)

#
## Setup Android Studio

### To use android studio in termux need to some files and steps.

download android studio linux tar from [here.](https://developer.android.com/studio)


Download android-sdk and cmdline-tools from [here](https://github.com/AndroidIDEOfficial/androidide-tools/releases/tag/sdk).

Also Download build-tools and platform-tools from [here](https://github.com/AndroidIDEOfficial/androidide-tools/releases/tag/v33.0.3) according to your devices `arch`.


Now Create `Android` directory in Ubuntu `$HOME` directory
and extract android-studio,android-sdk into ubuntu `$HOME/Android/` directory
and extract cmdline-tools, build-tools and platform-tools in `$HOME/Android/android-sdk/` dir.

#
Now open terminal and edit .bashrc file .
```bash
nano ~/.bashrc
```
add these lines to .bashrc

```bash
export ANDROID_HOME=$HOME/Android/android-sdk
```
save it.

run this in terminal.
```bash 
source ~/.bashrc
```
#
## Now run android studio 

`bash ~/Android/android-studio/bin/studio.sh`

Cancel setup wizard and uncheck show agin setup wizard.

Now Android Studio setup is completed.

### Note:- there is an error to build apk in this process to fix it use following commands.

### to fix aapt2 error go to [this](https://github.com/Lzhiyong/termux-ndk/issues/106#issuecomment-1133898302) link.


### Hope You did it.

If you encounter any error please first google.
#
**Note:- Layout Manager Not Working.**
**(Tested and Working:- NDK , ADB WI-FI)**

**to use NDK, download from [here](https://github.com/Lzhiyong/termux-ndk/releases)**
#
## $Thanks$
