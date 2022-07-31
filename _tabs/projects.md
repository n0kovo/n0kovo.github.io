---
title: Projects
icon: fas fa-file-code
order: 1
---

### A bunch of stuff I've made:

* ### [OpenRandonaut](https://github.com/openrandonaut/openrandonaut-bot)
	An attempt at open-sourcing the functionality of the app Randonatica, which is based on software by the [Fatum Project](https://github.com/anonyhoney/fatum-en). Written in Python.<br><br> The script uses the [quantumrandom](https://github.com/lmacken/quantumrandom) library to interface with the [ANU Quantum Random Number Generator](https://qrng.anu.edu.au/), where it gets a list of [truly random](https://en.wikipedia.org/wiki/Hardware_random_number_generator#Quantum_random_properties) numbers, converts them to coordinates and then uses [SciPy](https://github.com/scipy/scipy) to compute the gaussian kernel density estimate of those coordinates. The script can be interacted with through a Telegram-bot. <br><br>If you're unfamiliar with The Fatum Project and the concepts of Probability Blind-Spots and Quantum Randomness, I recommend reading [fatum_theory.txt](https://github.com/anonyhoney/fatum-en/blob/master/docs/fatum_theory.txt) which shipped with the original Fatum bot. [This video](https://www.youtube.com/watch?v=6C6aXta3m1M) gives a lot of great background info too. If you have no idea what any of this is about, watch [this video](https://www.youtube.com/watch?v=nDX81AUm8yE) and/or read [this article](https://medium.com/swlh/randonauts-how-a-random-number-generator-can-set-you-free-dfc2a2413e15).<br><br>Technologies used: [SciPy](https://scipy.org/), [NumPy](https://numpy.org/), [Matplotlib](https://matplotlib.org/), [Pandas](https://pandas.pydata.org/), [Seaborn](https://github.com/mwaskom/seaborn).

* ### [FB Friend List Scraper](https://github.com/narkopolo/fb_friend_list_scraper)

   An OSINT tool I wrote to scrape names and usernames off large friend lists on Facebook, without being rate limited. Written in Python, the script uses [Selemium](https://pypi.org/project/selenium/) to interact with the mobile version of facebook.com, which is less dynamic than the desktop version, and then parses the HTML using [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/). Built in proxy support, progress bar and very pretty output. [Featured on kitploit.com](https://www.kitploit.com/2022/05/fbfriendlistscraper-osint-tool-to.html).

* ### [Danish Wordlists](https://github.com/narkopolo/danish-wordlists)
	A collection of various Danish base wordlists to aid in password security research and fuzzing of Danish targets. With tools like Hashcat, in combination with word mangling rules, Markov chains etc. these wordlists can be a very effective in cracking Danish passwords. Lists include all legal Danish first and last names, street names, town and city names, company names, Danish bible translations, scrape of the Danish language Wikipedia and passwords from publicly available data leaks from Danish websites.
	
* ### [Hashcat Rules Collection](https://github.com/narkopolo/hashcat-rules-collection)
	A huge collection of Hashcat rule files. Probably the largest publicly available anywhere.

* ### [SSID Keyspace Table](https://github.com/narkopolo/ssid-keyspace-table)
	A lookup table of common (Danish) WiFi router SSIDs with their corresponding router model, WPA key examples, keyspace, format, estimated cracking time and default web interface credentials. **Example**: Seeing *Telenor3225CF* in the wild? Consulting this table will reveal that it's probably a Technicolor TG788vn v2 router using a default WPA keyspace of A-F0-9 and a length of 11 characters, which is crackable in under 40 hours using hashcat on an EC2 GPU instance. The data was sourced from pictures of used routers for sale on [www.dba.dk](https://www.dba.dk).
	
* ### [Danish Phone Wordlist Generator](https://github.com/narkopolo/danish_phone_wordlist_generator)
	A tool for generating wordlists of Danish phone numbers by area and/or usage (Mobile, landline etc.) Useful for password cracking or fuzzing Danish targets.

* ### [CVE-2021-39174 PoC](https://github.com/narkopolo/CVE-2021-39174-PoC)
	A quick exploit I wrote for an Information Exposure vulnerability in Cachet, an open source status page system, while doing the Catch box on HTB. The script was [used by Ippsec while doing the same box](https://youtu.be/XAZI361XgRU?t=1164) 😎

* ### [cURL to SQLMap](https://github.com/narkopolo/curl_to_sqlmap)
	A Python script to quickly convert cURL command syntax into SQLMap command syntax. Extremely handy when used in combination with the "Copy as cURL" option in Dev Tools.
	
	
* ### [Jensens Grinder](https://github.com/narkopolo/jensens_grinder/blob/main/jensens_grinder.py)
	A *very* old (and terribly written) Python script I once wrote as a Proof of Concept, back when the Danish restaurant chain [Jensens Bøfhus](https://jensens.com/da/) had a... let's say "poorly thought out" referral program. The script automated the process of registering new accounts with random names and addresses on the webbsite using disposable emails, and refering these accounts from a central account to gain points. These points could then be used in restaurants to pay for food. In a matter of minutes, the script could earn you several hundred dollars worth of points. Included for historic reasons, novelty and lulz-factor. Please don't judge my old code.
	


* ### [Dialect Map](https://github.com/narkopolo/dialektkort) 
The Royal Danish Library maintains a collection of historic sound recordings of  different Danish dialects. I wrote a scraper too pull the data from that collection and plot them on a map by querying location data from the [Danish Agency for Data Supply and Infrastructure](https://eng.sdfe.dk/) API and mapping it on an [interactive Leaflet.js map](https://narkopolo.github.io/dialektkort/) using [Folium](https://github.com/python-visualization/folium).	