# Samsung-A52S-bloatware-remove
Just some things to make your phone better and rid of some annoying bloatwares.


1.) Download the latest ADB (Android Debug Bridge) from here: https://dl.google.com/android/repository/platform-tools-latest-windows.zip

2.) Download the Samsung Android USB driver from here: https://developer.samsung.com/android-usb-driver

3.) Enable the Developer mode on you mobile phone and enable the USB debugging mode (***change the screen timeout to 10 minutes, because the adb shell will not work and you are not able to execute commands when the screen is locked***).

4.) Connect your phone to the computer via USB cable (***I have suffered a lot with a faulty USB cable. Sometimes just enought to change a better quality one***).

5.) Open a terminal in you windows system and find the platform tool directory.

For example:
> D:\Samsung>cd platform-tools

6.) Use the following command to check your device is attached an authorized
```
adb devices 
```

> List of devices attached

> ABCDEF12345     unauthorized

****Allow the USB debugging on your phone****

```
adb devices 
```

> List of devices attached

> ABCDEF12345     device

7.) Enter the ADB shell.
```
adb shell 
```
List the Samsung packages
```
pm list packages | grep samsung
```

8.) Uninstall the required bloatware from your phone

```
pm uninstall -k --user 0 NameOfPackage
```

After the command you should recieve the "Success" output
> Success


9.) Make sure the package is removed from your phone

```
pm list packages | grep NameOfPackage
```


****TBD***

Collection

Samsung Free - com.samsung.android.app.spage



Sources:

https://www.xda-developers.com/how-to-remove-bloatware-samsung-galaxy-s22/
