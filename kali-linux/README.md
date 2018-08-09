
## Setting up the environment:


* Install VirtualBox/VMWare

* Download the kali .iso file

* Boot the distro 

* Add these from (deb http://http.kali.org/kali kali-rolling main non-free contrib) in `/etc/apt/source.list`
	

	```	
		deb http://http.kali.org/kali kali-rolling main non-free contrib

		deb http://http.kali.org/kali kali-rolling main non-free contrib
	```


* run `apt-get update`

* run `apt-get install -y dkms`

* `apt-get install tor`

* DO NOT RUN BROWSE TOR AS ROOT


## Install Tor

* `apt-get install tor -y`

## proxychains

* Change settings in /etc/proxysettings.config

* Uncomment dynamic_chain. Comment out static_chain

* Add proxy list in the end (default is Tor's)

* Test by running:

	```
		service tor status-all
		
		service start tor

	```

* Run and test if proxychains is working (point to ipchicken.com or dnsleaktest.com)

	```
	proxychains firefox dnsleaktest.com

	```


* 


