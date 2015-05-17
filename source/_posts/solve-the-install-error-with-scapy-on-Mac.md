title: solve the install error with scapy on Mac
date: 2015-01-23 16:10:07
categories: 
- research
tags:
- mac
- scapy
---

Today there are some errors when I run scapy on Mac system. I installed scapy with pip (pip install scapy). it catchs some errors:
<!-- more -->	

	Traceback (most recent call last):
	File "/usr/local/bin/scapy", line 25, in 
	interact()
	File "/usr/local/lib/python2.7/site-packages/scapy/main.py", line 278, in interact
	scapy_builtins = import("all",globals(),locals(),".").dict
	File "/usr/local/lib/python2.7/site-packages/scapy/all.py", line 25, in 
	from route import *
	File "/usr/local/lib/python2.7/site-packages/scapy/route.py", line 162, in 
		conf.route=Route()
	File "/usr/local/lib/python2.7/site-packages/scapy/route.py", line 22, in init
	self.resync()
	File "/usr/local/lib/python2.7/site-packages/scapy/route.py", line 31, in resync
	self.routes = read_routes()
	File "/usr/local/lib/python2.7/site-packages/scapy/arch/unix.py", line 86, in read_routes
	ifaddr = scapy.arch.get_if_addr(netif)
	File "/usr/local/lib/python2.7/site-packages/scapy/arch/init.py", line 36, in get_if_addr
	return socket.inet_ntoa(get_if_raw_addr(iff))
	File "/usr/local/lib/python2.7/site-packages/scapy/arch/pcapdnet.py", line 187, in get_if_raw_addr
	i = dnet.intf()
	AttributeError: 'module' object has no attribute 'intf'
	
I have search from Google, seems many guys have come across the same problem with me. I have solved this problem with the follow steps:

1.remove the previous scapy.
	
	sudo pip install pyrex --allow-all-external --allow-unverified pyrex
	
2.reinstall the scapy with brew.
	
	brew reinstall scapy 
	
The whole steps are all above.