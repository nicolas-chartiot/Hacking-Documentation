# Hacking

#### "Understand computers so well that you can make them do things they were not supposed to"

# Table of Contents
* [Network](#network)
	* [Address Resolution Protocol (ARP)](#address resolution protocol (arp))
	* [ARP Poisoning](#arp poisoning)

***
# Network

## Address Resolution Protocol (ARP)

When a computer wants to send a package to another device, it needs it's **IP address** and **Mac address**. To get the device's Mac address, it broadcasts and ARP request to the network, asking devices for the Mac address of that specific IP.

The device will get that request and send a response, specifying the data needed. These values are stored in an **ARP Table**

**Request:**
~~~
Who has 192.168.1.2? Tell 192.168.1.1
~~~

**Response**:
~~~
192.168.1.2 is at 00:0a:95:9d:68:16
~~~

## ARP Poisoning

## This will be another header
