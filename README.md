# ./vooautoconnect

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
modify vooautoconnect with your credentials, then
```
chmod +x vooautoconnect
mv vooautoconnect /usr/local/bin
```
and automatically schedule it (let's say each minute), adding this to your crontab:
```
* * * * * autoconnect > /dev/null 2>&1
```

TODO
==============
- Improve logs
- ARGS? Flags? Options?
- Detect user/password error
- use vooautoconnect on rasperry as AP repeater?
- Support linux (just need to change the SSID detection)
