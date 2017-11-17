#ReactNative Installation Guide

## :arrow_up: How to Setup React and it's related stuff

**Installing Dependencies:**
You will need Node.js, the React Native command line interface, and Android Studio.

**Step 1: Nodejs**

        $ curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash -
        $ sudo apt-get install -y nodejs

- optional – To compile and install native addons from npm  you may also need to install build tools:
        `$ sudo apt-get install -y build-essential`

**Step 2: The React Native CLI**

- `$ sudo npm install -g react-native-cli`

- If you get an error like Cannot find module 'npmlog',  try installing npm directly:
        `$ curl -0 -L https://npmjs.org/install.sh | sudo sh`

**Step 3: Installing java**

        $ sudo apt-get install python-software-properties
        $ sudo add-apt-repository ppa:webupd8team/java
        $ apt-get update
        $ sudo apt-get -y install oracle-java8-installer

- optional: run `$ sudo update-alternatives --config java` if needed (to set default jdk)

**Step 4: Android Studio**

    Required libraries for 64-bit machines:
    $ sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386


- Download [Android Studio](https://developer.android.com/studio/install.html)

**Installation and Configuration**
1. Unpack the .zip file to `/opt/`
2. Launch Android Studio, open a terminal, navigate to the `android-studio/bin/` directory, and execute `./studio.sh` - don’t use sudo with it
3. Go with the installation wizard and download SDK make sure you include the AVD during installation,  choose *-Custom-* installation.

**To configure AVD:**
https://developer.android.com/studio/run/emulator-acceleration.html#vm-linux

**To make Android Studio available in your list of applications, select [ Tools > Create Desktop Entry ] from the Android Studio menu bar.**

**Set up the ANDROID_HOME environment variable:**
- Add the following lines to your sudo nano `~/.profile` (or equivalent) config file:

        export ANDROID_HOME=${HOME}/Android/Sdk
        export PATH=${PATH}:${ANDROID_HOME}/tools
        export PATH=${PATH}:${ANDROID_HOME}/platform-tools

- Type source `~/.profile` to load the config into your current shell.

*Please make sure you export the correct path for ANDROID_HOME, if you did not install the Android SDK using Android Studio.Check using this cmd: `echo $ANDROID_HOME`*

##Some Useful Links:
- [**Iginte**](https://github.com/infinitered/ignite) as a react native dependency manager.
- [**Native Base**](https://github.com/GeekyAnts/NativeBase) as an App base theme.
- [**Reactotron**](https://github.com/infinitered/reactotron) for debugging.
