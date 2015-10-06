# SSHTunnel
Android Quasi-VPN App to circumvent the GFW through SOCKS and SSH

SSHTunnel
http://code.google.com/p/sshtunnel/

## What I did in this fork
* took some patches from around the internet
** [Nils Durner](https://github.com/ndurner)
** [intika](https://github.com/intika)
* removed analytics library
* upgraded ormlite to latest JARs from http://ormlite.com/releases/
* upgraded trilead-ssh2 to latest version from https://github.com/jenkinsci/trilead-ssh2
* upgraded iptables to 1.4.20 binary copied from AFWall+ (from FDroid, so presumably it's safe)
* published APK - see Releases tab: https://github.com/gjedeer/sshtunnel/releases

## HOWTO
To build it, just set your paths to android dev environment, create ant.properties file:

```
key.store=/path/to/your/android-apk-keystore/signkey
key.alias=name_of_your_key
version-name=1.5.7
```

and type `ant` in the project directory.

## TODO
* build [redsocks](https://github.com/gjedeer/sshtunnel/blob/master/assets/redsocks) from [source](http://darkk.net.ru/redsocks/)
* upgrade SSH library to http://svn.svnkit.com/repos/3rdparty/com.trilead.ssh2/ ?
* upgrade [bouncy castle files](https://github.com/gjedeer/sshtunnel/tree/master/src/com/trilead/ssh2/crypto) inside SSH library?
* make it a reproducible build for f-droid (haha yeah right, i'll have time for this after i'm dead)
