# Nubank - CTF Challenge

*Disclaimer: I'm just an enthusiast in Security Area/Capture The Flags Challenges. I don't know the answer of this challenge. 
This repository is only to gather all information I have about it.*

The challenge was found in the [Job Application for Blue Team](https://boards.greenhouse.io/nubank/jobs/1776009?t=b58135231) of Nubank Jobs Page.

![](https://i.imgur.com/IGRqAWv.png)

You can download the file from the link bellow:
[Download file](https://nu-blueteam-hiring.s3.amazonaws.com/36f3e3709766c41204bafcd21a96f691)

# What do We know so far?

##### 1. The file name is a MD5 hash.
The string `36f3e3709766c41204bafcd21a96f691` is a MD5 hash generated with the content of the file, you can see this running the command below:

`cat 36f3e3709766c41204bafcd21a96f691 | md5sum`

Output is the MD5 hash like the file name:

`36f3e3709766c41204bafcd21a96f691  -`

##### 2. The file is dump of a network traffic.

Originally the file does not have a explicit extension saying what it is about. So you have to run `file 36f3e3709766c41204bafcd21a96f691` in your terminal to know it is a `tcpdump capture file (little-endian) - version 2.4 (Ethernet, capture length 65535).` 

The extensions usually is `.pcap`, associated with Wireshark; a program used for analyzing networks. See more at https://en.wikipedia.org/wiki/Pcap

##### 3. Statics of the dump of network traffic using Wireshark

1. Install Wireshark and open the file `36f3e3709766c41204bafcd21a96f691`.
2. Go to Statistics > Protocol Hierarchy in the menu.
3. The following appears:

![Wireshark Protocol Hierarchy Statistics](https://i.imgur.com/f6dqLkC.png)
There is 53.9% of SSH encrypted packets in the dump. Is this a distraction or something helpful?

## Contributors

Would like to help? Feel free to open an issue or send a PR.




