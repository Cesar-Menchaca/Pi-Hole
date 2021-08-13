# The Pi-Hole: A Network Wide Ad Blocker

## What is Pi-Hole?
Pi-Hole is a Domain Name System (DNS) server that allows users to block advertisements on a network-wide level. For clarification, a DNS server is, at its core, the phonebook or contact list of the internet. DNS servers translates domain names, like google.com, to IP addresses that web browsers can use to access webpages and sites. This makes surfing the web easier because you only have to remember the domain name of a website, instead of a complicated IP address. What makes Pi-Hole different is that when a request is sent from your browser, Pi-Hole will first check if the domain name is not a domain for an ad. If the domain is not for an ad, it will retrieve the IP address and work normally. However, if the domain is for an ad, Pi-Hole will send an invalid IP address, causing the ad to not load.

## Requirements

### Hardware
Contrary to what the name suggests, Pi-Hole does not require a raspberry pi. Pi-Hole can be run in a container, virtual machine, or hardware that can support the OS and code. In this instance, I will be describing how I set up a Pi-Hole using a raspberry pi 4, since that is what I used.
In addition to the raspberry pi, you also need:
* A USB-C power supply that can output 5.1V / 3.0A DC output, which is what the official raspberry pi 4 power supply outputs
* A micro SD card that has at least 4GB of storage
* (Optional) An ethernet cable if you want the raspberry pi to be directly connected to the network

### Software
The OS I used to host the Pi-Hole is [DietPi](https://dietpi.com/), which is a lightweight version of the Raspberry Pi OS. However, you do not need to use DietPi. There is a list of supported Operating Systems at [this link](https://docs.pi-hole.net/main/prerequisites/). All you have to do is download the ISO file of the supported OS you want to use and flash it to the SD card.
