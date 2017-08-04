# Exploring the Radio Spectrum for News
SRCCON 2017 - Friday August 4, 2017
Minneapolis, MN
-------------------------------------
Jon Keegan   @jonkeegan
Visual Journalist * Senior Research Fellow
Tow Center for Digital Journalism
Columbia University

This repo: http://github.com/jonkeegan/exploring-the-spectrum  
Slides: http://bit.ly/radio-news-slides  
Notes/links: http://bit.ly/radio-news  
Etherpad: https://etherpad.opennews.org/p/SRCCON2017-radio-spectrum
-------------------------------------

### Quick plug for where I work:
The Tow Center for Digital Journalism
* Based at Columbia University’s Graduate School of Journalism
* Provide journalists with skills and knowledge to lead the future of digital journalism
* Serve as a research and development center for journalism
* Explore how technology is changing journalism, its practice, and its consumption
* Research emerging areas, develop teaching methods and courses
* Fellowships for academics, journalists, and technologists
http://facebook.com/towcenter
http://twitter.com/towcenter
http://towcenter.org

-------------------------------------
Whenever I encounter some cool new technology – usually one that has just become very cheap and available – I get very excited about the possibilities and look for ways I can use it in my work. For me this was the case with 3D printing, 3D scanners, cheap thermal cameras and software defined radio. So I am trying to instill in all of you this idea * look for unusual, novel ways to look for story ideas. Sometimes, behind the obvious uses, there are are creative ways technology can be used to tell stories.

### Questions journalists should ask about new technologies
* Who has had access to this technology in the past?
* How has it been used before?
* Can this technology be used to tell a story in a new way?
* What impact will this technology have on society? To my readers?
* How have other journalists used this technology before?
-------------------------------------
So this was exactly what I was thinking when I heard about software defined radio. I first heard about this from my most trusted source for cool technology, my Dad Larry Keegan. He's 88, an electrical engineer, pilot, poet, weather nut and HAM radio operator (WA1PII) among many other things. It immediately struck my imagination, and let me see and understand the radio spectrum in a new, visual way. Because this technology was cheap and pretty easy to use, I now had a very cool lens into this weird invisible world around us – a theme that I keep coming back to in my work.

### Why explore the radio spectrum for news?

* When new technologies fall into the hands of journalists, interesting things can happen
* The radio spectrum is an invisible, crucial national asset that is poorly understood
* We are surrounded by devices that use the radio spectrum, and it is powering our wireless world
-------------------------------------
### FCC Spectrum allocation chart: https://www.ntia.doc.gov/files/ntia/publications/2003-allochrt.pdf

The radio spectrum is huge, confusing and full of mystery. Licenses to use tiny slices of it are auctioned off for billions of dollars by the FCC. It's very tightly regulated and all of this is flying through the air around us. It's pretty crazy to think about. New cars come equipped with dozens of radios aboard, as well as every THING in the Internet of Things. The radio spectrum is powering our futuristic wireless world. This chart shows how carefully these tiny slices are managed so as to not bleed over into one another, which today could have life or death consequences (such as implanted medical devices with radio telemetry, transport navigation and tracking, etc).

Definition: Software defined radio - In a traditional physical radio, hardware components adjust the frequency tuning and modulation of the radio signals for you listening pleasure. In SDR, these components are replaced by software. SDR receivers have an lower and upper tuning frequency limit, and within that, they have a bandwidth of frequency that they can sample all at once. You can slide that bandwidth up or down within the upper and lower limits, and SEE where there is voice or data being transmitted within the swath you are observing.

For a long time, the expensive tools to explore the spectrum were exclusively the domain of technicians, scientists, engineers and HAM radio operators. But with the release of a particular USB TV tuner dongle in Europe (and others like it), things started to change. Hobbyists embraced this cheap ($20) USB stick once they realized they could use its software defined radio capabilities to investigate and visualize a wide swath of the radio spectrum. Open source libraries popped up, waterfall visualizers and signal processing tools quickly appeared on the scene. Today, there is a large, active community of hobbyists and hackers who are using these tools to explore – and sometimes exploit – the radios around us in our daily lives. Many of these spectrum explorers have reversed engineered their garage door openers, or discovered gaping security holes in products designed with the assumption that "civilians" would not have access, nor would they care.

-------------------------------------
### Examples of radio spectrum journalism / journalists using SDR data

Quartz's David Yanofsky built a DIY antenna hooked up to a RaspberryPi to log the ADS-B transmissions from private helicopters flying into the Davos conference in Switzerland.
https://qz.com/600590/we-brought-an-antenna-to-davos-to-track-private-air-travel-and-heres-what-we-found/

BuzzFeed's Peter Aldhous didn't use SDR hardware himself, but he did use ADS-B data from FlightAware to find FBI and DHS surveillance aircraft circling over American cities, and just this week published another story showing how the US Marshals used aircraft mounted Stingrays to locate narco kingpin "El Chapo" in Mexico.
https://www.buzzfeed.com/peteraldhous/spies-in-the-skies?utm_term=.kbkjgKvb2#.egQ2qNnyG
https://www.buzzfeed.com/peteraldhous/us-marshals-spy-plane-over-mexico?utm_term=.eiA2DawBp8
http://buzzfeednews.github.io/2016-04-federal-surveillance-planes/analysis.html

ProPublica collaborated with Gizmodo to peer through the radio spectrum around President Trump's Mar-a-Lago resort in Florida. Using an external directed antenna, they were able to surveil the Wi-Fi network of the resort, and found weak security, and a number of unsecured networked devices that could be compromised and used for surveillance by adversaries or malicious hackers.
https://www.propublica.org/article/any-half-decent-hacker-could-break-into-mar-a-lago

While not used in a specific story, ProPublica's Jeremy Merrill created a cool SDR setup to identify the planes flying over his home in Brooklyn, and answering on a LED display his question of "I wonder where that plane is coming from?".
http://jeremybmerrill.com/blog/2016/01/flyover.html

-------------------------------------
### RTL-SDR Dongle (RTL2832U)

* Tune Low (MHz): 24 MHz
* Tune Max (MHz): 1766 MHz
* RX Bandwidth (MHz): 3.2 MHz
* ADC Resolution (Bits): 8 bits/sample
* Max sample rate: 3.2 MS/s
* Transmit?: No
* Price: $20

-------------------------------------

### Some of the things you can observe using SDR (depending on your device / antenna):

* AM/FM radio
* CB radio
* Amateur radio
* Shortwave radio
* IoT devices
* Aircraft ADS-B transponders
* Air traffic control tower communications
* Maritime AIS transponders * Ships at sea
* Train transponders (Front, middle, end of train)
* NOAA Weather forecasts
* NOAA Meteor-M Satellites
* GPS satellites
* Amateur radio satellites
* Emergency responder radio traffic
* Pagers
* Garage door openers
* Remote control cars and drones controller signals

Source: Hobbyists Guide to the RTL-SDR
https://www.amazon.com/Hobbyists-Guide-RTL-SDR-Software-Defined-ebook/dp/B00KCDF1QI

-------------------------------------

### Popular SDR Clients

GQRX - Linux / Windows / Mac  / RaspberryPi SDR client
http://gqrx.dk/
http://gqrx.dk/download/gqrx-sdr-for-the-raspberry-pi
http://gqrx.dk/doc/practical-tricks-and-tips

CubicSDR - Linux / Windows / Mac SDR client
http://cubicsdr.com/
http://cubicsdr.com/wp-content/uploads/2015/02/CubicSDR-MainWindow1-Annotated.png

dump1090 - For logging and mapping aircraft ADS-B transponder data (Linux / Mac)
https://github.com/mutability/dump1090

SDR# - Windows
http://airspy.com/download/

WebSDR - Browser-based remote SDR server browser. Watch signals from around the world
http://websdr.org/
-------------------------------------
### Related: Amateur radio (aka HAM radio)

If you are geeking out over this and want more, get your Amateur Radio (HAM) license!

* I did. My callsign: KE3GAN
* Technician class license (basic)
* Lasts 10 years
* You don't need to know morse code (but you used to need to)
* Costs ~$15 or so
* You have to take an exam. You can practice here: https://www.qrz.com/hamtest/
* Allows you to transmit (talk) on all amateur bands above 30 MHz
* You don’t need a license to listen!

HAM radio license info
http://www.arrl.org/getting-your-technician-license

Buy this book to prepare for the exam, and learn everything you need to know:
https://www.amazon.com/ARRL-Ham-Radio-License-Manual/dp/1625950136/ref=sr_1_1?ie=UTF8&qid=1501256686&sr=8-1&keywords=arrl+3rd+edition
-------------------------------------
### Buy this cheap Chinese radio for $25
* BaoFeng UV-5R Dual Band Two Way Radio
* Covers most Amateur bands
* DON’T: Transmit on Police/Fire/EMS frequencies* Very illegal
* DO: Talk to the International Space Station with a handheld, homemade Yagi antenna

BaoFeng UV-5R transceiver (Cheap Ham radio):
https://www.amazon.com/BaoFeng-UV-5R-Dual-Radio-Black/dp/B007H4VT7A
-------------------------------------
### More links and resources

SDR People to follow

https://twitter.com/lemonodor
https://twitter.com/brianabelson
https://twitter.com/csete

Crowdsourced UNFILTERED ADS-B data:
https://www.adsbexchange.com/

FCC Radio spectrum chart:
https://www.ntia.doc.gov/files/ntia/publications/2003-allochrt.pdf

SDR Links:
http://www.rtl-sdr.com/
https://www.reddit.com/r/RTLSDR/

Identify weird signals you encounter:
http://www.sigidwiki.com/wiki/Database
https://www.reddit.com/r/signalidentification/

Lookup the frequencies licensed for use in your area:
https://www.radioreference.com/

Jeremy Merrill's code he used for his "flyover" project:
https://github.com/jeremybmerrill/flyover

Database of flight routes to be used in conjunction with ADS-B data:
http://www.virtualradarserver.co.uk/FlightRoutes.aspx

-------------------------------------
### Minneapolis Ham repeaters
https://www.repeaterbook.com/repeaters/location_search.php?state_id=27&type=city&loc=Minneapolis
```
53.37/52.37
This repeater is a split site system with a transmit power of 75 watts and uses 1/2 wavelength antennas for both receive and transmit. Be sure to remember you will need a 100 Hz CTCSS tone for access. Give it a try!

147.21/147.81
This repeater is now a single site system with a transmit power of 80 watts and a 100Hz CTCSS (PL) tone required for access. Full tone squelch is enabled (100 Hz CTCSS tone is both encoded and decoded)

224.54/222.94
Access with a PL tone of 100.0 Hz, a surprisingly wide-coverage single-site machine.

444.30/449.30
With a PL tone of 114.8 Hz, on the 70cm band, this repeater has been replaced with a Yaesu System Fusion FM/C4FM DR-1 machine.
```
-------------------------------------

### Minneapolis frequencies:
https://www.radioreference.com/apps/db/?ctid=1336
https://www.radioreference.com/apps/db/?aid=2541

```
NOAA Weather 162.540

Frequency	Tone	Location	County	Call	 Use	Operational status
145.1100-	PKT	Minneapolis	Hennepin	N0TL	OPEN	Unknown status
145.1100-	DSTR	Minneapolis	Hennepin	KD0JOU	OPEN	ON-AIR
145.3700-	107.2	Minneapolis	Hennepin	K0MSP	OPEN	ON-AIR
146.7000-	127.3	Minneapolis	Hennepin	WC0HC	OPEN	ON-AIR
147.0300+	114.8	Minneapolis	Hennepin	KD0JOU	OPEN	ON-AIR
147.1500+	100.0	Minneapolis	Hennepin	W0YC	OPEN	OFF-AIR
147.2700+	114.8	Minneapolis	Hennepin	WB0ZKB	OPEN	ON-AIR
223.9000-	100.0	Minneapolis	Hennepin	KE0NA	OPEN	ON-AIR
442.4000+	DMR	Minneapolis	Hennepin	KB0SVW	OPEN	ON-AIR
442.4250+	DMR	Minneapolis, University of Minnesota	Hennepin	NH7CY	OPEN	ON-AIR
442.6500+	DMR	Minneapolis, Riverview apartments	Hennepin	N0BVE	OPEN	ON-AIR
443.0000+	118.8	Minneapolis, East Bank Univ. of MN	Hennepin	N0YNT	OPEN	OFF-AIR
443.3000+	DMR	Minneapolis	Hennepin	N0NKI	OPEN	Testing
443.5750+	114.8	Minneapolis	Hennepin	KD0WIL	OPEN	ON-AIR
444.4250+	114.8	Minneapolis, U of Minn	Hennepin	KA0KMJ	OPEN	ON-AIR
444.6500+	114.8	Minneapolis	Hennepin	N0BVE	OPEN	ON-AIR
444.7250+	100.0	Minneapolis	Hennepin	KD5DLJ	OPEN	OFF-AIR
444.8750+	DSTR	Minneapolis	Hennepin	KD0JOU	OPEN	ON-AIR
1283.3000-	DSTR	Minneapolis	Hennepin	KD0JOU	OPEN	ON-AIR
```

dump1090 snippet for logging flights to CSV (courtesy of @schwanksta):
```
# first start dump1090
./dump1090 --aggressive --interactive --net --net-sbs-port 30003
# log data to a CSV
nc 127.0.0.1 30003 >> airplanes.csv
```
