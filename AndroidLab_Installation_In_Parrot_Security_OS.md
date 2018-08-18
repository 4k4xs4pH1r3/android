# android
Your Own Android Lab in Parrot Security OS
#
This idea is based in this great good guide https://guardianproject.info/2017/03/13/build-android-apps-with-debian-apt-install-android-sdk/
#
#Just follow the next steps, from your terminal
#
#
# Step 1
sudo apt install adb android-sdk android-sdk-build-tools-common android-sdk-common android-sdk-platform-tools android-sdk-platform-tools-common androguard apktool aidl anbox diffoscope enjarify libscout repo libatk-bridge2.0-0 libatk-bridge2.0-dev google-nexus-tools libandroid-ddms-java android-androresolvd android-framework-res android-libaapt android-libandroidfw android-libadb android-libbacktrace android-libadb-dev android-libbase android-libcutils android-libdex android-libetc1 android-libext4-utils android-libf2fs-utils android-liblog  android-liblog-dev android-libnativehelper android-libselinux android-libsparse android-libunwind android-libutils android-libziparchive android-logtags-tools android-tools-mkbootimg abootimg append2simg apkinfo apksigner apktool dalvik-exchange dex2jar dexdump fdroidcl fdroidserver fastboot go-mtpfs gradle hprof-conv img2simg jmtpfs libandroid-23-java libandroid-databinding-java libandroid-ddms-java libandroid-dex-java libandroid-layoutlib-api-java libandroid-json-java libandroid-json-java-doc libandroid-layoutlib-api-java libandroid-tools-analytics-library-java libandroid-tools-annotations-java libandroid-tools-common-java libandroid-tools-dvlib-java libandroid-tools-repository-java libandroid-tools-sdklib-java libandroid-uiautomator-23-java libgradle-android-plugin-java libgradle-core-java libgradle-plugins-java libjacoco-java libkf5kirigami2-5 libscout libsmali-1-java libvo-aacenc0 libvo-amrwbenc0 lime-forensics-dkms python3-pyaxmlparser qml-module-org-kde-kirigami2 split-select volatility zipalign ziptime google-android-build-tools-24-installer doctorj chaosreader gplaycli libsmali-java smali -y
#
#
#
wget http://ftp.us.debian.org/debian/pool/main/d/dummydroid/dummydroid_1.2-1_all.deb
#
sudo dpkg -i dummydroid_1.2-1_all.deb
#
sudo rm -r dummydroid_1.2-1_all.deb
#
#
#
# Step 2
#
Let's login as root with the bwelow command
su
#
#
Now itś time to open the Android SDK Manager with this command:
#
android
#
#
Install all the packages of the Android SDK Manager
#
U 'll receive a message to close and reopen the app, do it multiple times
#
# Step 3
Repeat the step 2 until U see all fully installed :)
#
#
#
# by C4N6





