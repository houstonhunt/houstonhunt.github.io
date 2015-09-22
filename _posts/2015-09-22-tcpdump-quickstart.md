---
layout: post
title: "revisiting tcpdump and similar tools"
---

###Just a collection of thoughts on the overview of net capturing tools...

####Whoa, there are a lot of network capture tools.  Pick one: GUI or terminal, features or straightforward, capture and/or display filters?

Non-exaustive list (not listing any commercial tools), some tools for collecting and analyzing network traffic:

* (recommended) -> tcpdump - 'dump traffic on a network'
* (recommended) -> Wireshark - 'interactively dump and analyze network traffic'
* tshark - 'dump and analyze network traffic'
* ngrep - 'network grep'
* dumpcap - 'dump network traffic'
* ettercap - 'multipurpose sniffer/content filter for MitM attacks'

Other things to note:
* libpcap/winpcap - API libraries for linux and windows respectively ( if you install wireshark on windows you will be prompted to install winpcap in the installer)
* BPF - Berkley Packet Filter - syntax used to filter traffic at capture, used often in tcpdump and in a capture filter in wireshark

I really enjoy using tcpdump because it is a simple terminal interface for capturing network traffic.  I recommend **[this]**(https://danielmiessler.com/study/tcpdump/) as quickstart guide and **[this]**(http://www.wains.be/pub/networking/tcpdump_advanced_filters.txt) when you want to get specific with the fields within a packet.  The man pages are straightforward as well.

Wireshark is not my favorite application because I think the GUI can be a bit clunky, but it has some great features if you navigate it.  *tshark* literally stands for *t*erminal*shark*. It is a bit more annoying and less intuitive in my opinion to use than tcpdump.  'dumpcap' is basically a *dumb*cap program which simply records all network traffic.

ngrep is pretty nifty if you are searching for regex, but will not be very helpful if what you are looking for is not in cleartext or if the string searched for is spread across packets.

**TL;DR:** tcpdump is a good starter tool to pick out traffic of interest (if you know what you're looking for)

