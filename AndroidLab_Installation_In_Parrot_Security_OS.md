# android
Your Own Cyber Forensic Android Audit Lab in Parrot Security OS
#
This idea is based in this great good guide https://guardianproject.info/2017/03/13/build-android-apps-with-debian-apt-install-android-sdk/
#
#
#
#
With Android SDK Manager and Android Studio U 'll be able to emulate Android
#
#
#
#
#
So Just follow the next steps, from your terminal
#
#
# Step 1
#
Set ther password for root
#
    sudo passwd
#
Personalize yor cedentials and memorize in your mind as root
#
    su
#
    cd /root/Desktop
#
#
#
#
## Before you start install these packages first:
#
    apt install curl wget apt-transport-https dirmngr -y
#
Add these 2 lines of Debian Sid repo to the parrot repo.
#
    nano /etc/apt/sources.list.d/parrot.list  
#
#
    #------------------------------------------------------------------------------#
    #                   OFFICIAL DEBIAN REPOS                    
    #------------------------------------------------------------------------------#

    ###### Debian Main Repos
    deb http://deb.debian.org/debian/ unstable main contrib non-free
    deb-src http://deb.debian.org/debian/ unstable main contrib non-free
#
#
save the file
#
    apt update -y
#
    sudo apt install adb android-sdk android-sdk-build-tools-common android-sdk-common android-sdk-platform-tools android-sdk-platform-tools-common androguard apktool aidl anbox diffoscope enjarify libscout repo libatk-adaptor libatk-bridge2.0-0 libatk-bridge2.0-dev google-nexus-tools libandroid-ddms-java android-androresolvd android-framework-res android-libaapt android-libandroidfw android-libadb android-libbacktrace android-libadb-dev android-libbase android-libcutils android-libdex android-libetc1 android-libext4-utils android-libf2fs-utils android-liblog  android-liblog-dev android-libnativehelper android-libselinux android-libsparse android-libunwind android-libutils android-libziparchive android-logtags-tools android-tools-mkbootimg abootimg append2simg apkinfo apksigner apktool dalvik-exchange dex2jar dexdump fdroidcl fdroidserver fastboot android-tools-fastboot android-tools-adb go-mtpfs gradle hprof-conv img2simg jmtpfs libandroid-23-java libandroid-databinding-java libandroid-ddms-java libandroid-dex-java libandroid-layoutlib-api-java libandroid-json-java libandroid-json-java-doc libandroid-layoutlib-api-java libandroid-tools-analytics-library-java libandroid-tools-annotations-java libandroid-tools-common-java libandroid-tools-dvlib-java libandroid-tools-repository-java libsdl2-image-dev libandroid-tools-sdklib-java libandroid-uiautomator-23-java libgradle-android-plugin-java libgradle-core-java libgradle-plugins-java libjacoco-java libkf5kirigami2-5 libscout libsmali-1-java libvo-aacenc0 libvo-amrwbenc0 lime-forensics-dkms python3-pyaxmlparser qml-module-org-kde-kirigami2 split-select volatility zipalign ziptime google-android-build-tools-24-installer build-essential cmake cmake-data debhelper dbus google-mock libboost-dev libboost-filesystem-dev libboost-log-dev libboost-iostreams-dev libboost-program-options-dev libboost-system-dev libboost-test-dev libboost-thread-dev libcap-dev libdbus-1-dev libdbus-cpp-dev libegl1-mesa-dev libgles2-mesa-dev libglib2.0-dev libglm-dev libgtest-dev liblxc1 libproperties-cpp-dev libprotobuf-dev libsdl2-dev lxc-dev libgtk3-nocsd0 pkg-config protobuf-compiler doctorj chaosreader gplaycli libsmali-java smali -y
#
#
#
    wget http://ftp.us.debian.org/debian/pool/main/d/dummydroid/dummydroid_1.2-1_all.deb && sudo dpkg -i dummydroid_1.2-1_all.deb && sudo rm -r dummydroid_1.2-1_all.deb 
#
    snap install --edge --devmode anbox
#
#
# Step 2
#
Let's login as root with the below command
#
    su
#
#
Now is time to open the Android SDK Manager with this command:
#
    android
#
#
Select all the packages of the Android SDK Manager and Install them
#
U 'll receive a message to close and reopen the app, do it multiple times
#
# Step 3
Repeat the step 2 until U see all fully installed, like when where you start to see API 28, P Preview, Android 9, Wear OS, Android TV etc...  :) take a tea...
#
#
# Step 4
#
Let's login as root with the below command for install Android Studio
#
    su
#
    cd /root/Desktop
#
    wget https://dl.google.com/dl/android/studio/ide-zips/3.1.4.0/android-studio-ide-173.4907809-linux.zip && unzip android-studio-ide-173.4907809-linux.zip && cd android-studio/bin/
#
Start the wizard installer
#
    ./studio.sh
#
Select custom installation, choose theme Darcula and mark Android Device and take a tea again, until U see that install the updates.
#
#
#
#
#
# Step 5
Run Android Apps in Parrot Security OS with Anbox 
#
Execute
#
    sudo snap install --devmode --beta anbox
#
    sudo wget -O /var/lib/anbox/android.img https://build.anbox.io/android-images/2018/07/19/android_amd64.img
#
#
    snap refresh --beta --devmode anbox
#
    snap info anbox
#
    sudo systemctl start anbox-container-manager.service
#
    sudo systemctl --user start anbox-session-manager.service
#
    anbox session-manager
#
This command will open the window of Anbox
#
    anbox launch --package=org.anbox.appmgr --component=org.anbox.appmgr.AppViewActivity
#
#
#
#
#
You can same emulate android with GenyMotion, VMware, VirtualBox, BlueStacks, ARChon, Bliss, Droid4X, KoPlayer, MEmu, Nox, Remix OS Player, Xamarin, YouWave...
#
#
#
#
#
If you like install apps in Android execute any of this two options
#
    fdroidcl update
#
    fdroidcl install 'name-of.apk'
#
    adb install 'name-of.apk'
#
#
#
#
# by C4N6
