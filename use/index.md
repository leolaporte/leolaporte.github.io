# I Use This 

Just in case you're curious, here's a description of the various hardware and software I use to work and play.
<!--more-->
This is a work in progress, but over time should reflect the entirety of my toolset. My hope is to keep this up-to-date because things change regularly. If there's something you'd like to know and you don't see it here ask in the comments at the bottom of the page!

I realize that the following is a ridiculously large menagerie of gear. That's an occupational hazard. I review more gear than the average bear, but I do keep the stuff that suits me best. One small point, I almost always buy all the gear I use. I generally don't ask for or use review units or loaners. I think it gives me a more realistic idea of what owning this gear is like, and this way I'm not beholden to anyone. Any exceptions are indicated below.

### Home Office

I have a ~300 sq ft home office with several book shelves and a built-in desk in the bay window. There's a comfy armchair and ottoman I've had for years, a less comfy chair from the studio, a couple of side tables.

#### Computers

![My Desk](/images/iusethis/aurora.jpg "My desktop and computers")

Sitting on my desk in the office are:

* Alienware Aurora Ryzen Edition R10 gaming desk top from April 2021  
Ryzen 7 5800 X (8-core, 32MB Cache 4.7GHz)  
Nvidia GeForce RTX 3080 10Gb G DDR6X  
128GB Dual Channel DDR4 XMP at 3400MHz  
2TB M.2 SSD  
2 TB SATA drive  
Dark Side of the Moon chassis with High-Performance CPU Liquid Cooling and 1000W Power Supply
I use a 5TB Drobo Mini for backup. 

* Apple Mac Studio Max
M1 Max
32 GB RAM
1 TB SSD
connected to a 4TB OWC [Express 4M2](https://www.owcdigital.com/products/express-4m2) Thunderbolt 3 external drive

* Xbox Seriex X 1TB

Each connected to a 55" Alienware 120Hz 4K gaming monitor. I switch devices using the remote control that came with the monitor. 

Audio goes to  a pair of [Audioengine 2](https://audioengineusa.com/shop/wirelessspeakers/a2-wireless-computer-speakers/) wired speakers with an Audioengine S8 subwoofer beneath the desk. I use an Alienware 310K Mech. Gaming Keyboard and 510M RGB Gaming Mouse mostly to play Valheim. The Dell dual boots Manjaro Linux and Windows 11. 

When I'm not sitting at my desk, I primarily use one of my more portable devices:
* A 2021 Macbook Pro 14" running Apple's M1 Pro processor with 16 GB RAM and a 512 TB SSD (these days my go-to device)
* A 2021 [Framework DIY Laptop](https://frame.work/laptop-diy-edition) with Intel i7-1185G7, 32GB RAM, 2TB M.2 drive and 1TB USB drive runing Manjaro 
* A 2020 iPad Pro 12.9" with the Magic Keyboard.
* A 2021 iPad Mini 

There's also a 2016 17" [System76 Oryx Pro](https://system76.com/laptops/oryx) i7/32GB/2.5TB/GTX980 laptop. It weighs about 10 pounds but I don't have the heart to give it away. It's running, you guessed it, Manjaro Linux Gnome Edition. 

All my systems have synced Document, Source Code, and dotfile directories using the excellent and free open-source [SyncThing](https://syncthing.net). I keep system build instructions and scripts in [Notion](https://notion.so) which I also use for fancy note-taking. For day-to-day notes, to-dos, and lists I use emacs org-mode.

Because this site is running on a server (cf. [The Beast](https://leolaporte.com/2016/07/21/a-grand-experiment/)) in the studio. I keep logged into it via a tmux session running over mosh on all the systems (even the iPad using the [Blink terminal](https://blink.sh/)).

An emacs daemon is always running on the Beast so it's easy to jump into any post exactly where I left off from any system although right now I'm editing this using Emacs Tramp mode from home on my M1 Pro Macbook.  This web site runs on [hugo](https://gohugo.io/), so I simply save the markdown file, rebuild the site (it takes about 200 milliseconds to rebuild it from scratch with hugo) and jump back into emacs (^XS ^Z hugo fg - it's practically muscle memory). If you see any stray XSs in any of the posts you'll know I accidentally hit the shift key instead of the Control key. To avoid this I always map Caps Lock to the control key. The other tmux panes monitor the five Minecraft instances also running on the server (using Spigot), [WeeChat IRC](https://weechat.org) logged into the TWiT IRC channel, and our [Jitsi videoconferencing](https://jitsi.org/) server. 

#### Smartphones

My daily carry is a two-year old T-Mobile iPhone 12 Pro Max in a red Apple silicon case. I also carry a Fi-based Google Pixel 6 Pro Android phone and a Samsung Galaxy S22 Ultra on Verizon. I'm wearing a Series 6 Apple Watch or, occasionally, a Samsung Galaxy Watch4 and an [Oura 3rd generation smart ring](https://ouraring.com/product/heritage-silver). 

#### Cameras

<img src="/images/iusethis/leica.png" style="float:right" width="200" alt="The Leica Q2" caption="The Leica Q2 with Pelle case" />I use a couple of different camera systems. I shoot stills with the Sony A7RIV mirrorless camera typically with Sony FE 24mm f1.4 GM or [Zeiss Planar T* FE 50mm F1.4 FE](https://www.sony.com/electronics/camera-lenses/sel50f14z) lenses. My daily carry for street photography is a [Leica Q2](https://us.leica-camera.com/Photography/Leica-Q/Leica-Q2) with its fixed 28mm F1.7 lens. I carry the Leica in a beautiful case and strap from [Angelo Pelle](https://www.angelo-pelle.com/product/half-case-for-leica-q2). A beautiful camera deserves a beautiful case. 

#### A/V

For Zoom calls and audio recording on the iMac, I use a [Heil PR-40](https://heilsound.com/products/pr-40/) mic. It's connected via USB using a SoundDevices [MixPre-3](https://www.sounddevices.com/mixpre/). As I do in the studio, I use custom-molded in-ear monitors from [JH Audio](https://jhaudio.com) or [AKG K240](https://www.amazon.com/AKG-K240STUDIO-Semi-Open-Professional-Headphones/dp/B0001ARCFA/ref=sr_1_2?dchild=1&keywords=akg+k240&qid=1610399210&sr=8-2) headphones.

<img style="float: right" src="/images/iusethis/comrex.png" width=150 alt="A Comrex Access2 unit" caption="Comrex Access2"/>When I do radio shows from here, I use the same gear connected to a [Comrex Access2](https://www.comrex.com/products/access-portable-2usb-audio-codec/) audio codec over IP. We've replaced ISDN in the studio with a similar unit. Although these devices use the public Internet instead of direct ISDN lines, they work just as well. 
 
On the other side of the office, there's a 55" curved [Samsung OLED](https://www.samsung.com/uk/tvs/curved-oled-s9c/) which I bought in 2013 for a ridiculous amount of money. It's connected to Denon AVR S910W A/V receiver which feeds it signals from a [HDHomerun Prime](https://www.silicondust.com/product/hdhomerun-prime/) (for cable TV), an Nvidia Shield 2, an Xbox One S, and an Apple TV. I use [Elac Debut 2.0](https://www.elac.com/series/debut-2-0/b6-2/?r=us) bookshelf speakers here. In the living room there's a full Elac surround system paired with a [Hisense 100" short throw projector and screen](https://www.amazon.com/Hisense-100-inch-Ultra-Smart-100L10E/dp/B07NDGM8GF). 

My preferred wired headphones to use with this system are the [HiFiMan HE-560s](https://www.hifiman.com/products/detail/167).

#### Internet

![Ubiquiti Inventory](/images/iusethis/ubiquiti.png "My home networking gear")

I recently upgraded my home network to [Ubiquiti](https://ui.com) gear including the [UDM-Pro router](https://store.ui.com/collections/unifi-network-routing-switching/products/udm-pro), a 48-port PoE switch, and five UniFi AC HD wireless access points connected to Comcast 1000/40 consumer Internet. All the various media centers and computer workstations are hardwired with Ubiquiti PoE managed switches. 

![Home network rack](/images/iusethis/rack.png "My rack")

There's a wine closet in the office, which besides wine, houses a Synology DS1019+ 5-bay NAS with 32TB of storage. It runs a Plex server, along with the usual NAS facilities, including backup for the other computers in the house. The Synology syncs to a Synology DS1515+ NAS at the studio using Hyperbackup.

### Studio A
   
In Studio A at the TWiT Eastside Studios, where we shoot _This Week in Tech_, _MacBreak Weekly_, and _This Week in Google_, I use a Heil PR-40 mic and JH Audio in-ear monitors. The big computer in front of me is a 2019 [Lenovo A940 all-in-one](https://www.lenovo.com/us/en/desktops-and-all-in-ones/ideacentre/yoga-a-series/Yoga-A940-27ICB/p/FFYGF900316) with an 8th Generation Intel® Core™ i7-8700 Processor with a 27" 4K UHD (3840 x 2160) IPS display,  32 GB RAM, and a 256GB SSD. It's running Manjaro Linux with the Gnome desktop.

The [TWiT Wiki](http://wiki.twit.tv/wiki/TWiT_Eastside_Studio_FAQ) has a fairly up-to-date description of the hardware we use to stream the shows. The short version is that we use multiple Canon Vixia consumer grade camcorders, switched with a [Newtek Tricaster 2 Elite](https://newtek.com/twit), streaming live to Twitch, Ustream, and YouTube Live  via an Amazon Elemental. The shows are recorded using decks from Sound Devices. Editors use Adobe Premiere on Dell Precision Workstations. Our audio uses Telos's Axia digital over ethernet. 

### Studio B

Studio B at the TWiT Eastside Studios doubles as my office. I shoot _The Tech Guy_ radio show there, along with _Windows Weekly_ and _Security Now_. While on the air use a 2016 5K iMac desktop and a 2019 System 76 Darter Pro laptop with a 4.9 GHz i7-10510U CPU, 32 GB RAM and a 2 TB SSD running Manjaro Linux with Gnome. 

When I need to record audio I use Twisted Wave on the iMac. My Heil PR-40 mic is connected, as it is at home, using a Blackmagic Designs MixPre-3. I'm wearing [AKG K240 studio headphones](https://www.akg.com/Headphones/Professional%20Headphones/K240-Studio.html).

### Transport

When the weather's nice, I ride to work on a Radpower electric bike, the [Rad City Step Thru](https://www.radpowerbikes.com/pages/ebikes). We own two old-school Segways which we mostly ride for fun. I drive a leased 2021 Ford Mustang Mach-E First Edition and love it. Lisa has a 2022 electric Mini Cooper. We really like electric vehicles. Maybe that's because we generate and store our own electricity with 60 solar panels on the roof and two Tesla Powerwall batteries. Our house is on a well and without electricity we have no water. 

{{< youtube id="03FQZti4vxk" autoplay="false" >}}



