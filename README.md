RANCID Scripts for Watchguard XTM Firewalls
======

Watchguard scripts for Rancid.  Forked from
https://bitbucket.org/aquerubin/rancid-vyatta, https://github.com/damianfantini/rancid and https://github.com/natecarlson/vyatta-rancid

Includes:

* xtmlogin - basic login script for Watchguard XTMs
* xtm.pm - the Rancid wrapper module to actually grab the configs
* rancid.types.conf - additional device type configuration

To integrate into your RANCID install:

* Copy xtmlogin to your 'bin' directory
* Copy xtm.pm to your PERL5LIB rancid directory
* Append rancid.types.conf to your existing rancid.types.conf file (or create it if it doesn't exist)
* Add a new device to your 'router.db', with the vendor of 'xtm'
* NOTE: You may have to go through the painful process of updating your Perl Installations Socket module to use this package if you are running on RedHat / CentOS 6. If you get a strange error in your rancid error logs like: 
"inet_pton" is not exported by the Socket module
That means that you'll need to update Socket.
