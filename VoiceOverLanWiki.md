# Introduction #

This project is about creating an android application that shows the power and how to properly use sockets in android environment.



# Details #

This application is about having an audio streaming between two android devices, like having a call but you don't need any internet all you need is a wireless network.


# Installation #

All you have to do is get the apk file from the bin folder and install it on one, two or multiple android devices and once you're connected to a wifi network open the application, select an ip from the spinner and press call, the device you're calling will have a prompt (the only option there is "ok" since the application is only for testing purposes but it's easy to do some improvement to this application).

# How it works #

The basics of how this application works is that when you open the application, There will be a thread starting that broadcasts a packet containing the ip of the device. The other devices will do a scan every 10 seconds getting all the ips on the network and if it doesn't have the ip in the spinner it will add it. There's also another thread opened when starting the application this one awaits a connection. When you select an ip from the spinner (from device A for example) and call (B), A tcp connection happens between A and B, when B receives this connection it will prompt B that A is calling , B presses ok and a message (1) is being sent to A.
When this tcp connection is established between A and B, a check for the proper buffer size, channel ... happens to check for the proper configuration for the voice data for each device, a datagram socket opens and the audio data streams on the network and that's how you can speak and hear on your device what's been said on the other one.

# Issues #

This application is still on the first version and it still requires some testing, enhancements and some bug fixing so excuse me if you found some bugs, but the main purpose of the application is served.

Enjoy and thank you