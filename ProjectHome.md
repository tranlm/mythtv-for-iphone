MythTV for iPhone allows you to watch your TV shows on your MythTV DVR on your iPhone (or iPod Touch). It has been suggested that I rename the software to something more generic, since the iPod Touch is also fully supported. Something like "MythTV for Apple Touch", or "MythTVStream". Thoughts?

The software allows you to browse your recorded shows, and look at show details. You can stream any recorded show to the iPhone (or iPod Touch) wirelessly.

The technology behind it is MythTV (The Open-Source DVR), PHP for the backend, Smarty and iUI for the frontend.

### Update: ###

**2008-05-16** - I just did a fresh install of myth for iphone on a fresh ubuntu 8.04 box. I found a lot of changes that I need to update in the install guide when possible. Also like i said below, I'm going to include smarty directories and update i\_settings.php to have all the correct options to work on the ubuntu system.

**2008-05-10** - Released version 0.04. I'm considering including the smarty directory folders into the project which should make setup much easier. I think getting smarty set up is confusing for a lot of people. This will be included on version 0.05 which should come out next week. Also, I want to get the conversion script to tie into mythweb or somehow trigger the "Convert to iPod" background job in MythTV. Right now, the software just calls the conversion script manually. Lame. If we get it creating the background job in mythtv, then it will queue properly.

**2008-05-09** - Updated my servers to Ubuntu 8.04 and having issues with the mythipod.sh conversion script. aac codec error. Once I work through this I will polish up a new version .04 and release to Google Code - **Adding Medibuntu repositories to my Ubuntu install fixed this problem!**