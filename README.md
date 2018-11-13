authored by
https://github.com/suborb/philips_android_tv

this is my private repo just to store some modifications made by my own.
Great job was made by suborb.

# philips_android_tv
Tools to control Philips 2016 Android TVs

The API is roughly the same as JointSpace (http://jointspace.sourceforge.net/) with the following
differences:

* Uses HTTPS over port 1926
* Uses /6/ instead of /1/ as the API path
* All calls have to have digest auth to be successful
* An initial pairing to determine the user/pass is required
* Channel and Source methods aren't available

Channel status and changes are performed using a different protocol that isn't described here.

The tool here will do the initial pairing. The credentials can then be used in a standard way
(digest) in other tools.
=======
# philiptstvapi
Philips smart tv jointspace api > 2016 
>>>>>>> 5a53537ee14b33a01056b78935c635d5b3b50cdd


Instalation on raspberry pi
======
- apt-get install python-requests
- apt-get install python-pycrypto

First: pair the device

* python philips.py --host XXX.XXX.XXX.XXX pair
where XXX is your tv ip address

* next you'll obtain an username and password. Write them down and use in your scripts.
example: python philips.py --user YOURUSER --pass YOURPASS --host IPADDRESS command.

Available commands:
* standby
* powerstate
* ambion
* ambioff
