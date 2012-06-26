libimobiledevice-macosx
=======================

Binary distribution of the libimobiledevice library for Mac OS X http://www.libimobiledevice.org/

This library allows you to communicate with an iPad or iPhone using command-line tools.

NOTE: This is not an official release. I had a lot of trouble compiling this library for Mac OS X 10.7.4, but found this guy had 
http://blog.boceto.fr/2012/05/05/libimobiledevice-for-macosx/.
This is just a tidied-up version of his release. Entirely unofficial.

Installation guide
------------------

 - git clone GIT-URL /your/path/here
 - nano ~/.bash_profile

Add line at the end that reads:
 export DYLD_LIBRARY_PATH=/your/path/here/imobiledevice-macosx/:$DYLD_LIBRARY_PATH

Add line that reads:
 PATH=${PATH}:/your/path/here/imobiledevice-macosx/

- source ~/.bash_profile


Examples
--------

Connect an iPhone/iPad

View device log in realtime. Very handy for debugging Phonegap apps - shows WebView output and native messages
 - ./idevicesyslog

Take screenshot. Puts a TIFF file in the current directory.
 - ./idevicescreenshot

.. and many others.
 
