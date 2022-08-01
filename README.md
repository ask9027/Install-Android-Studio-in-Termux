# Install-Android-Studio-in-Termux

## First neet to Login to udroid

Download and install termux from [here.](https://github.com/termux/termux-app/releases)

install ubuntu from [here.](install-ubuntu-on-termux.md)

## Now login to user in ubuntu

## update and install jdk-11

```bash
sudo apt update
sudo apt install openjdk-11-jdk -y
```
## GUI Mode (need to Termux-x11 installed) 
### Install Termux-x11 from [here.](install-termux-x11.md)

#
## Setup Android Studio

### To use android studio in termux need to some files and steps.

download android studio linux tar from [here.](https://developer.android.com/studio)


Download android-sdk for `arm64` from [here](
https://github.com/itsaky/androidide-build-tools/releases/download/v33.0.1/android-sdk-33.0.1-aarch64.tar.xz)

for `arm` from [here](
https://github.com/itsaky/androidide-build-tools/releases/download/v33.0.1/android-sdk-33.0.1-arm.tar.xz)


Now Create `Android` directory in Ubuntu `$HOME` directory
and extract android-studio and android-sdk to ubuntu `$HOME/Android/` directory.


Now open terminal and edit .bashrc file .
```bash
nano ~/.bashrc
```
add these lines to .bashrc

```bash
export ANDROID_SDK_ROOT=$HOME/Android/android-sdk
```
save it.

run this in terminal.
```bash 
source ~/.bashrc
```
## Now run android studio 

`bash ~/Android/android-studio/bin/studio.sh`
(make sure `java --version` is 11)

Cancel setup wizard and uncheck show agin setup wizard.

Now Android Studio setup is completed.

### Note:- there is an error to build apk in this process to fix it use following commands.
```
jar -uvf ~/.gradle/caches/modules-2/files-2.1/com.android.tools.build/aapt2/7.4.0-alpha08-8691043/4d0af64ff88429650487ab88d3ee411a6b5955c6/aapt2-7.4.0-alpha08-8691043-linux.jar ~/Android/Sdk/build-tools/33.0.0/aapt2
```
### Note :- Replace `aapt2-7.4.0-alpha08-8691043` with that you are using and you can also replace build-tools version with another.


### Hope You did it.

If you encounter any error please first google.

**Note:- Layout Manager Not Working.**
**(Tested and Working:- NDK , ADB WI-FI)**

**to use NDK, download from [here](https://github.com/Lzhiyong/termux-ndk/releases)**

## Thanks
