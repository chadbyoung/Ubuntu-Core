
[//]: # (Created on: August 14, 2017)
[//]: # (Author: Chad Young)
[//]: # (Contact: chad.young@dell.com)


# Mosquitto-snap
This snap is meant to be used as a reference on how-to create snaps for Ubuntu
Core 16 and as such would not be used in a production enviornment. As with 
anything you find on the internet please proceed with caution as you never
know when Gremlins, Goblins, or Trolls will appear.  
  
## Basic information
* At the time of development the version of mosquitto is 1.4.11
* At the time of development the version of snapcraft is 2.29
* At the time of development the version of my snap is 1.0

## Installing the snap

Installing the snap is simple and will require the use of "--devmode". Your 
command line should look like this:  
```
admin@system:~$ sudo snap install <name>.snap --devmode  
```
## Running the broker
In the case of this snap the broker is started as a service as part of the
snap installation and does not need to be started manually. On installation
the broker will start listening on port 1883 (per the mosquitto.conf file).

## Running the Client - Sub/Pub
### Sub
The sub command is as follows:  
```
admin@system:~$ mosquitto-snap.sub -d -t hello/world
```
### Pub
The pub command is as follows:  
```
admin@system:~$ mosquitto-snap.pub -d -t hello/world -m "Hello from terminal #2!"
```

