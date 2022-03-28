# Install-Android-Studio-in-Termux

## First neet to Login to udroid

Download and install termux from [here.](https://f-droid.org/en/packages/com.termux/)

install ubuntu from [here.](https://github.com/RandomCoderOrg/ubuntu-on-android/)

**Now login to user hippo**

```bash
proot-distro login --user hippo udroid-focal-xfce4 --shared-tmp --bind /dev/null:/proc/sys/kernel/cap_last_cap

```
**update and install jdk-11**
```bash
sudo apt update
sudo apt install openjdk-11-jdk -y
```
**GUI Mode (need to VNC Viewer installed)**
```bash
vncserver :1
```

## Setup Android Studio

**To use android studio in termux need to some files and steps.**

download android studio linux tar from [here.](https://developer.android.com/studio)

download android-sdk, aapt2 from [here](https://androidide.com/) according to your device architecture.
   
and move all files to $HOME directory.

extract all downloaded files *(android studio, android-sdk, aapt2)* in $HOME directory.

Now open terminal and edit .bashrc file .
```bash
nano ~/.bashrc
```
add these lines to .bashrc

```bash
export ANDROID_SDK_ROOT=$HOME/android-sdk
export GRADLE_USER_HOME=$HOME/.gradle
```
save it.

run this in terminal.
```bash 
source ~/.bashrc
```
## Now run android studio 

```bash 
bash android-studio/bin/studio.sh
```
(make sure `java --version` is 11)
   
when android studio ask to select jdk path , choise downloaded openjdk-11-jdk from `/usr/lib/jvm/java-11-openjdk-arm64/`

now it will ask to download emulator , don't download it , uncheck it.

and select android-sdk path from `hippo/home/android-sdk`

now click on next button if all things done correctly it will show downloadable files and it's size. now click on next, this will download all required files.

after downloading click on finish.

Now Android Studio setup is completed.

## Now create new project.
1. Create Project and stop build for now.
2. Now make change in build.gradle(project level) at `classpath "com.android.tools.build:gradle:(version)` to `classpath "com.android.tools.build:gradle:7.0.2"`

Make sure gradle version is 7.3-bin at gradle/wrapper/gradle-wrapper.properties if face some error.

Now build project.

Thats it for Andeoid-Version<12 and Udroid.

**Note:- Make Changes if You want to build project in Termux(use jdk-arm64),Termux at android 12 devices or 32bit Devices use jdk-arm**

need to download jdk [from](https://github.com/itsaky/AndroidIDE/ [to](https://github.com/itsaky/AndroidIDE/)

and extract all files(jdk, android-sdk,aapt2) in Termux `$HOME`.

edit bash.bashrc

```bash
nano ../usr/etc/bash.bashrc

#add these lines
export JAVA_HOME=$HOME/jdk
export PATH=$JAVA_HOME/bin:$PATH
export ANDROID_SDK_ROOT=$HOME/android-sdk
export GRADLE_USER_HOME=$HOME/.gradle

#run
source ../usr/etc/bash.bashrc
```

3. Make change in gradle.properties at `'org.gradle.jvmargs=-Xmx2048m'` to `'org.gradle.jvmargs=-Xmx1024m'`

now Build your project.

Hope You did it. 👍🏻

If you encounter any error please first google.

**Note:- Layout Manager Not Working.**
**(Not Tested :- NDK , ADB WIFI)**

**Thanks**

# Sources : 
**for Android SDK, JDK , AAPT2 [to](https://github.com/itsaky/AndroidIDE/)**

**for ubuntu [to](https://github.com/RandomCoderOrg/ubuntu-on-android/)**

**for termux [to](https://termux.com/)**

**if someone have more idea plesea add in this repo**
