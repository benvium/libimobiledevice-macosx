libimobiledevice-macosx
=======================

Binary distribution of the libimobiledevice library for Mac OS X http://www.libimobiledevice.org/

This library allows you to communicate with an iPad or iPhone using command-line tools. Jailbreak is NOT required.

NOTE: This is not an official release. I had a lot of trouble compiling this library for Mac OS X 10.7.4, but found this guy had 
http://blog.boceto.fr/2012/05/05/libimobiledevice-for-macosx/. 
This is just a tidied-up version of his release. Entirely unofficial.
Fink does manage this package for Mac, but a 10.7 release is not available.

Thank you to eAi (https://github.com/eAi/bits-and-pieces) for patching the binaries so that idevicescreenshot now works on iOS 6. 


Installation guide
------------------

Use git to download:
 - git clone GIT-URL /your/path/here
 
OR go to Downloads / Download as Zip on github to use your browser to download. Then extract to /your/path/here.

Set up paths required in Terminal.app
 - nano ~/.bash_profile

Add line at the end that reads:

    export DYLD_LIBRARY_PATH=/your/path/here/imobiledevice-macosx/:$DYLD_LIBRARY_PATH

Add line that reads:

    PATH=${PATH}:/your/path/here/imobiledevice-macosx/

Return to the terminal and type
- source ~/.bash_profile


Examples
--------

Connect an iPhone/iPad

View device log in realtime. Very handy for debugging Phonegap apps - shows WebView output and native messages
 - idevicesyslog

Take screenshot. Puts a TIFF file in the current directory.
 - idevicescreenshot

Install an IPA onto your device
 - ideviceinstaller -i myapp.ipa

Note: Your IPA will need to have a valid code signature and mobileprovision file for the install to succed. This system is NOT
a way around iOSs security!
