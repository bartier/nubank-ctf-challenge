# Nubank - CTF Challenge

The challenge was found in the [Job Application for Blue Team](https://boards.greenhouse.io/nubank/jobs/1776009?t=b58135231) of Nubank Jobs Page.

![](https://i.imgur.com/IGRqAWv.png)

You can download the file from the link bellow:
[Download file](https://nu-blueteam-hiring.s3.amazonaws.com/36f3e3709766c41204bafcd21a96f691)



Originally the file does not have a explicit extension saying what it is about. So you have to run `file 36f3e3709766c41204bafcd21a96f691` in your terminal to know it is a `tcpdump capture file (little-endian) - version 2.4 (Ethernet, capture length 65535).` 

The file  is now known as a dump of a network traffic. The extensions usually is `.pcap`, associated with Wireshark; a program used for analyzing networks. See more at https://en.wikipedia.org/wiki/Pcap

