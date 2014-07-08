# KJ's `hosts` File

This hosts file coalesces hosts from these resources:
 - [Dan Pollock's Hosts File](http://winhelp2002.mvps.org/hosts.htm)
 - [hpHosts' Host File](http://hosts-file.net/)
 - [MDL's Host File](http://http://www.malwaredomainlist.com/hostslist/hosts.txt)
 - [mVPS' Hosts File](http://winhelp2002.mvps.org/hosts.htm)
 - [Peter Lowe's Host File](http://pgl.yoy.org/adservers/)

 I try to keep my amalgamated hosts file as up-to-date as possible with its respective sources; sometimes this happens, sometimes it doesn't. I feel like it usually gets updated every few months or so.

 <hr>

 ### What's it do?
The initial purpose of a hosts file was to map hostnames to IP addresses. This was back in the days before the [DNS](https://en.wikipedia.org/wiki/Dns) was even a thing, meaning that if you wanted to connect to any computer, you had to place its IP and an associated name within your hosts file.
This approach isn't viable in today's age. Could you imagine having to manually place the IP of any server you wanted to visit in your hosts file?
Though this type of hostname assignment is really limited to company intranets today, it still serves as an interesting, out-of-the-box method to block unwanted connections. Instead of having `74.125.225.41 google.com` which will direct you to Google's website, if you wanted to block Google you could write `127.0.0.1 google.com` which says that Google is located right on your computer. Since Google is most definitely not located your computer, it returns with nothing.

### Okay, that's nice and all, but why?
The main thing you will notice while using this hosts file is the stunning lack of ads. (Which is great!) However there are less visible, yet more important advantages. This hosts file contains *actual tens-of-thousands* of sites that are known malware hosts. Containing anything from adware to Java drive-by bots.

Another scary thing this hosts file partially blocks is trackers. Trackers are basically code that follow you and discover your browsing habits (or more accurately the browsing habits of your IP address). This information is sold to ad companies so they can better advertise to you as in individual.

(NB: I said, "partially blocks is trackers," because I feel as though it doesn't do it as well as it should. It is something I am working on.)

### How do I install it?

If you are on Linux/BSD you will need root access. I have no idea how OS X works but you'll probably need root or administrative rights for that as well.

If you are on Windows you will need Administrator access for versions after XP.

Simply copy (and replace) this hosts file over your current one.

#### Windows
The hosts file is located at `C:\System32\drivers\etc\hosts`

#### *NIX
The hosts file is located at `/etc/hosts`
