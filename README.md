phaxit
======

Setup
-----

Requires Pythom modules:

- pyphaxio
- configargparse

Usage
-----

One or more options (e.g. api key and secret) can be put in a config file
at ~/.phaxit.conf to avoid having to provide them as options each time.

Then, just use $phaxit -t <phone number> <file> <file> etc. Use multiple -t
options to specify multiple recipients.

Full usage:

	usage: phaxit [-h] [-c CONFIG] -k APIKEY -s APISECRET -t TO file [file ...]
	
	Args that start with '--' (eg. -k) can also be set in a config file
	(~/.phaxit.conf or specified via -c). Config file syntax allows: key=value,
	flag=true, stuff=[a,b,c] (for details, see syntax at https://goo.gl/R74nmi).
	If an arg is specified in more than one place, then commandline values
	override config file values which override defaults.
	
	positional arguments:
	  file                  Files to send
	
	optional arguments:
	  -h, --help            show this help message and exit
	  -c CONFIG, --config CONFIG
	                        Path to config file
	  -k APIKEY, --apikey APIKEY
	                        Phaxio API key
	  -s APISECRET, --apisecret APISECRET
	                        Phaxio API secret
	  -t TO, --to TO        Destination phone numbers, 1<ten digits>

