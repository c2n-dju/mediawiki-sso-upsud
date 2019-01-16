CASAuth(entication) Extension for Mediawiki, using U-PSud SSO
=============================================================

A CAS Authentication extension for Mediawiki 1.31 (and possibly earlier)

Introduction
------------

This code is customized towards usage for private wikis, with the ability to
restrict access to the wiki to specific usernames.

This extension is currently written for and tested against Mediawiki 1.31.
However, if you find it works well against a different
version of Mediawiki, please feel free to let me know and I will
keep track of it in this README.

Installation
------------

Assuming a working CAS system, installation should take under 2 minutes.
Assume $WIKI is the directory for your wiki.

1.  Go to folder $WIKI/extensions

2.  Download this source code into that directory
    ```bash
    git clone https://github.com/c2n-dju/mediawiki-sso-upsud
    cd mediawiki-sso-upsud
    git submodule init
    git submodule update
    cd submodules/CASAuth
    ln -s ../../CASAuthSettings.php 
    ```

3.  Add the following line to your LocalSettings.php

    ```php
    require_once( "$IP/extensions/mediawiki-sso-upsud/CASAuth.php" );
    ```

4.  You should now have working CAS U-PSud SSO authentication for your wiki!

