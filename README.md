# tvmcChromeCastHack

[TVMC website](http://www.tvaddons.ag/tvmc-android/)

I use TVMC for streaming online content on my android mobile and android tablet. TVMC is a flavour of the XBMC Kodi build. TVMC is basically Kodi with all the best plugins/addons pre-installed. 

I initially downloaded Kodi but felt overwhelmed at the amount of reading/searching I had to do to find the best plugins to steam content. TVMC comes with everything included and is basically plug and play!

##Casting from android mobile/tablet to chromecast
There doesn't seem to be a built in way to cast from TVMC to a chromecast but there is a hack!

####Step 1. 
Download a casting app for your device. I use [AllCast](https://play.google.com/store/apps/details?id=com.koushikdutta.cast&hl=en)

You could us a different casting application such as [LocalCast](https://play.google.com/store/apps/details?id=de.stefanpledl.localcast&hl=en)

####Step 2. 
Download the [playercorefactory.xml](playercorefactory.xml) file which is part of this repository. 

This file is already set up to cast using the AllCast app. If you want to change it to a different app for casting, just edit the bottom part of the file. You will need to substitute the "Allcast" key with the name of the casting app which you want to use.

####Step 3. 
You will need to find the TVMC installation directory on your device. We will copy the file above to a certain directory. On my Samsung S5 the directory we need can be found at:

/sdcard/Android/data/ag.tvaddons.tvmc/files/.xbmc/userdata/

Copy the [playercorefactory.xml](playercorefactory.xml) file to the directory above.

I use an app for directory navigation and for copying files:
[ES File Explorer](https://play.google.com/store/apps/details?id=com.estrongs.android.pop&hl=en)

Note: When using a file explorer app the above directory includes the hidden directory ".xbmc". Some file explorer apps will not show this directory by default. [ES File Explorer](https://play.google.com/store/apps/details?id=com.estrongs.android.pop&hl=en) has a "show hidden files" button which shows hidden files! You will need to turn this on in order to find the correct directory.

####Step 4. 
Restart your TVMC app. 

####Step 5. 
Select content to stream, choose AllCast when prompted to choose a player, select your chromecast and sit back and relax!

###Tips and tricks
If the playercorefactory.xml file exists in the directory above, everytime you attempt to stream content, the AllCast app will be opened. If you want to view the content on your device only you will need to remove the playercorefactory.xml file from the above directory.

What I do is store the [playercorefactory.xml](playercorefactory.xml) file in the directory below the /userdata directory. So I store it in here: 
/sdcard/Android/data/ag.tvaddons.tvmc/files/.xbmc/

If I want to watch content on my device I rename the "playercorefactory.xml" file in the "userdata" directory. I usually just add a letter to the ".xml" part to be "playercorefactory.xmlt". If I want to use AllCast for streaming I rename the file to be "playercorefactory.xml" again.

I plan on writing a simple android app for this at some stage but using ES file explorer works ok for now.
