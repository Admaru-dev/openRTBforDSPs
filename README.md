# openRTB v2.5(display, video)

This document is openRTB(complies with the OpenRTB 2.5 specificatoin) integration specification for `DSP` that wish to buy Admaru LLC’s inventories.

Kindly check OpenRTB 2.5 specification via below link.

https://www.iab.com/wp-content/uploads/2016/03/OpenRTB-API-Specification-Version-2-5-FINAL.pdf


<br>

# Bid Request 
## Object model


Object | Support | OpenRTB 2.5 Section for Reference 
:--- | :---: | :---: 
BidRequest | O | 3.2.1 
Source | O | 3.2.2 
Regs | O | 3.2.3 
Imp | O | 3.2.4
Metric | X | 3.2.5
Banner | O | 3.2.6
Video | O | 3.2.7 
Native | X | 3.2.9 
Format | O | 3.2.10
PMP | X | 3.2.11 
Deal | X | 3.2.12 
Site | O | 3.2.13 
App | X | 3.2.14 
Publisher | O | 3.2.15 
Content | O | 3.2.16
Producer | X | 3.2.17
Device | O | 3.2.18
Geo | O | 3.2.19 
User | O | 3.2.20
Data | X | 3.2.21
Segment | X | 3.2.22 
Native Markup | X | - | 4.1
Asset | O | - | 4.2 
Title | O | - | 4.3 
Image | O | - | 4.4 
Video | O | - | 4.5 
Data | O | - | 4.6 


## Request sample

## Banner
	{ "id": "80ce30c53c16e6ede735f123ef6e32361bfc7b22", 
	   "at": 1, 
	  "cur": [ "USD" ], 
	  "imp": [ { "id": "1", "bidfloor": 0.03, "banner": { "h": 250, "w": 300, "pos": 0 } } ], 
	  "site": { "id": "102855", "cat": [ "IAB3-1" ], "domain": "www.foobar.com", "page": "http://www.foobar.com/1234.html ", 
	  "publisher": { "id": "8953", "name": "foobar.com", "cat": [ "IAB3-1" ], "domain": "foobar.com" } }, 
	  "device": {"ua": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/537.13 (KHTML, like Gecko) Version/5.1.7 Safari/534.57.2", "ip": "123.145.167.10" }, 
	  "user": { "id": "55816b39711f9b5acf3b90e313ed29e51665623f" } 
	}

## Video
	{ "id": "1234567893", 
	  "at": 2, 
	  "tmax": 120, 
	  "imp": [ { "id": "1", "bidfloor": 0.03, "video": { "w": 640, "h": 480, "pos": 1, "startdelay": 0, "minduration": 5, "maxduration": 30,"maxextended": 30, "minbitrate": 300, "maxbitrate": 1500, "api": [ 1, 2 ], "protocols": [ 2, 3 ], "mimes": [ "video/x-flv", "video/mp4", "application/x-shockwave-flash", "application/javascript" ], "linearity": 1, "boxingallowed": 1, "playbackmethod": [ 1, 3 ], "delivery": [ 2 ], "battr": [ 13, 14 ], "companionad": [ { "id": "1234567893-1", "w": 300, "h": 250, "pos": 1, "battr": [ 13, 14 ], "expdir": [ 2, 4 ] }, { "id": "1234567893-2", "w": 728, "h": 90, "pos": 1, "battr": [ 13, 14 ] } ], "companiontype": [ 1, 2 ] } } ], 
	  "site": { "id": "1345135123", "name": "Site ABCD", "domain": "siteabcd.com", "cat": [ "IAB2-1", "IAB2-2" ], "page": "http://siteabcd.com/page.htm", "ref": "http://referringsite.com/referringpage.htm", "privacypolicy": 1, 
	  "publisher": { "id": "pub12345", "name": "Publisher A" }, 
	  "content": { "id": "1234567", "series": "All About Cars", "season": "2", "episode": 23, "title": "Car Show", "cat": [ "IAB2-2" ], "keywords": "keyword-a,keyword-b,keyword-c" } }, 
	  "device": { "ip": "64.124.253.1", "ua": "Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10.6; en-US; rv:1.9.2.16) Gecko/20110319 Firefox/3.6.16","os": "OS X", "flashver": "10.1", "js": 1 }, 
	  "user": { "id": "456789876567897654678987656789", "buyeruid": "545678765467876567898765678987654", "data": [ { "id": "6", "name": "Data Provider 1", "segment": [ { "id": "12341318394918", "name": "auto intenders" }, { "id": "1234131839491234", "name": "auto enthusiasts" } ] } ] 
	  } 
	}


