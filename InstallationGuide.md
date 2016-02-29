### MythTV for iPhone ###
Copyright 2008 Chris Carey (http://chriscarey.com).
This program is distributed under the terms of the GNU General Public License

## Introduction ##

**This software is not a native iPhone app.** It is a web application which is installed on your MythTV server. You access the software by using your iPhone web browser and hitting a URL on your MythTV server.

## Apache Setup ##

You need to set up a /recordings/ Alias for watching videos.

In your apache conf file add:
```
Alias /recordings /var/lib/mythtv/recordings
```

**You must restart apache for the settings to take effect**


## Dependency Install ##

  * Install Smarty on your web server. Download Smarty at: http://www.smarty.net or Debian based systems: **apt-get install smarty**
  * Install php-curl. Debian based systems: **apt-get install php5-curl**
  * Install ffmpeg and it's dependencies. You should be able to run the conversion script by hand via command-line. More info on this in the Transcoding sections below.

## Transcoding Setup ##

Follow this guide below which is the same one I'm using:

http://mythtv.org/wiki/Streaming_to_iPod_touch_or_iPhone

Two changes I made to the mythipod.sh script to make it work:

1) %DIR%/%FILE% should be %DIR% %FILE% (no slash)
2) change libfaac to aac on the last line

YOU MUST HAVE THIS WORKING BEFORE MYTHTV FOR IPHONE WILL WORK! Transcoding is a huge part of this process. For the most part, you are on your own here. You need to get it to the point that the mp4 files are being generated automatically on your MythTV.

You need to set up a "User Job" in MythTV. Mine is called "Convert to iPod". You can initiate this User Job from within MythFrontend, or MythWeb, or soon from within MythTV for iPhone. There is also a setting in Settings->TV->General where you can tell the MythTV to run "User Job #1" every time a show records. You may want this selected.

Getting transcoding working correctly is probably the toughest part of the install.

After upgrading my Ubuntu, I had to install Medibuntu to get the transcoding working. If you run Ubuntu, you probably need to do the same:
http://chriscarey.com/wordpress/?p=26

## Set up Smarty Directories ##

Follow the section SETUP SMARTY DIRECTORIES in the quick start guide
http://www.smarty.net/quick_start.php

## Install Smarty Templates in smarty templates folder ##

  * templates/mythiphone/main.tpl


## Install files in the web app folder on your mythtv box ##

  * mythiphone/i\_db.php
  * mythiphone/i\_functions.php
  * mythiphone/i\_settings.php
  * mythiphone/index.php

## Customize i\_settings.php ##

  * copy i\_settings.php.dist to i\_settings.php

You must edit this file with correct paths and options

## All Done!! ##