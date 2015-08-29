# ./vooautoconnect
==============
From VOO_HOMESPOT FAQ:
![faq](http://i.imgur.com/R0RQrnU.png "FAQ")
Very boring...Can't leave the computer downloading/uploading...

Solution
==============
- checks if the SSID you're connected is VOO_HOMESPOT
- checks if you're logged or your session is expired (with an http request to google.be)
- connects with a POST request to wifree.voo.be sending your credentials

Here is what vooautoconnect does.

USAGE
==============
```
chmod +x vooautoconnect
mv vooautoconnect /usr/local/bin
```
then edit your crontab
```
* * * * * autoconnect > /dev/null 2>&1
```
