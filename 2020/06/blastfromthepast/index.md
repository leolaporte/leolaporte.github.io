# Five Years Later: The TWiT.tv Web Site

Exactly five years ago, we debuted the "new" [TWiT web site](https://twit.tv). I wrote the following post shortly after. It's buried somewhere on the site (that's one part of the design I wish we'd done better) so I wanted to "resurrect" it here. The annotations are from today.
<!--more-->
**Originally Posted 12 June 2015**

### Some History

The Internet is changing. And so are we. The way web sites look seems to change every few months, but even the way they work, and the very reason they exist has shifted since the first pages at twit.tv went up in 2005. 

I designed and implemented that original site by myself, choosing Drupal 4 as the content management system. It didn't take long, as we added more shows and more hosts, for TWiT to outgrow that very simple original design. I asked Amber MacArthur, host of *Inside The Net* on TWiT, and her brother Jeff, to redesign the site. Their company, MGImedia Communications, crafted a new look and user interface for us and I hired the best Drupal programmers I knew, Lullabot, to implement it.  TWiT.tv v2.0, engineered chiefly by Ted Serbinski, went live in 2007 and served us well for four years. But changes in our business and intense growth prompted another redesign by ImageX in 2011. By the end of 2014 I had decided it was time for another re-design, but this time I wanted to undertake something more ambitious.

In talks about new media for more than 10 years I've been saying that our job was to provide content for our audience  *when they wanted, where they wanted, in any form they wanted, without limitations on how they could consume it.*

(I remember telling that to a convention of HBO employees in 2004 and almost being shown the door. But even HBO is coming around.) One of the reasons I've always made TWiT ad-supported is because it let us do that. It was in our interest to serve up our shows live or on-demand, in audio or video, and everywhere you wanted to watch.

In the early days of TWiT that meant a web site to provide you with a directory of shows and RSS feeds. Most people, once they found out about TWiT, went to iTunes to subscribe. And that was how 90% of our audience listened for years. 

### Fast Forward to the Present 

Today the market is much more fragmented. iTunes downloads are down to about 16% of the total. Another 10% of our audience watches the live stream either on the web site or by plugging the URL into a video player like VLC. 30% download pre-recorded shows via the web site.  All the rest, nearly half, use apps to watch or listen on their mobile phones, tablets, Rokus, TiVOs, Samsung TVs, many other platforms.[^1] I consider this a success. We've put TWiT in front of our audiences wherever they want it. But it means that our web site plays a very different role. And mobile apps are becoming increasingly important. 

[^1]: Five years later this trend is even more pronounced. The most significant trend is towrd using an app to stream shows. Most people don't download at all anymore. 

As I began to appreciate this drastic change in how you watch and listen, I came to the realization that we needed to pay more attention to mobile while not ignoring the web. I, and many others, began to think of what we do as not broadcasting, or podcasting, but content as a service, or CaaS.[^2] That's a pretty high-falutin' term, but it does describe what we're trying to do. 

[^2]: OK that name didn't catch on, but conceptually that's still what's happening behind the scenes.

RSS feeds were a step in this direction, making it possible for readers and listeners to subscribe to a feed and get content in any manner they wanted. Instead of forcing you to read the news in a newspaper or on a web page, RSS feeds let you decide how you'd read and in what form. But RSS doesn't go far enough. We are taking it a step farther and creating a full-blown API that can deliver our content, all the meta-data associated with it, and additional information about our hosts, sponsors, and events on demand to any app that wants it. [^3]

[^3]: This didn't happen, alas. RSS is still totally dominant. We use the API and a few other apps do, but an API is far harder to use than RSS, and doesn't really offer much more. 

Our new web site is just once consumer of this API. We're developing new apps on iOS, Android, and Windows that will also use the API.[^4] And we're inviting anyone who knows how to make a JSON call to create their own sites and apps. What we're unveiling today is much more than a new web site, it's a new way to deliver content that empowers my dream to give our audience the shows when they want, where they want, how they want without limits. 

[^4]: After spending $75,000 on these apps with a third-party developer we abandoned them as unusable. The development team attempted to use a cross-platform app framework. It didn't work. Today we would probably have created the site as a [Progressive Web App](https://en.wikipedia.org/wiki/Progressive_web_application) which would have eliminated the need for dedicated apps entirely. 

### Headless Drupal 

We met with several great Drupal design teams late last year to begin the process of creating a new site. One, Four Kitchens out of Austin, told us about an exciting new technique they had developed for a couple of their big media clients. This technique, called "Headless Drupal," used the robust Drupal content management system for data entry (I'm writing this in a Drupal form right now) [^5] and to serve the API calls. 

[^5]:And I'm writing these notes in markdown with emacs. So I think I'm actually going back in time. But sometimes the oldest things are the best!

### The Front End

But Four Kitchens didn't use Drupal for the web site. Instead they recommended a more modern and flexible tool called node.js. Unlike previous web sites, the site itself wouldn't be a content management system, it would only be a representation of the content via the API.  I liked the idea for several reasons.

First, Drupal's presentation is looking a little old and staid next to the spiffy, responsive sites other media companies are using. I liked the idea of being able to use a more modern tool like node.js. 

Second, by decoupling the backend from the presentation, it would be easier and faster to create new sites. Web design styles change faster than high fashion, so it's nice to be able to update the site without re-doing all the hard work on the backend.[^6]

[^6]: And, in fact, we've changed the original, elegant, design considerably to reflect the needs of our marketing department. Honestly, I thought the original design was perfect, but over time we wanted to make it easier to discover our shows. The flexibility designed into the front end has definitely paid off.

### The Apps

Third, having a complete API would make it easier to do apps. The app, just like the web site, would have access to everything there is to know about TWiT, in a simple, orderly fashion.

Finally, by making the API public, we encourage members of our audience to create new things, things we might never have thought of. You could even design a web site you like better. Abstracting the content from the presentation seems like a big win.[^7]

[^7]:And there have been some fantastic apps using the API fully - like Patrick Hickey's [MyTWiT](https://twit.tv/posts/picks/ios-pick-mytwit) (no longer available). There's a list of current apps on the site, https://twit.tv/apps. I'm not sure how many of them use the API - frankly RSS is much easier.

So while you may think we're unveiling a new web site here, we're really just showing you the tip of the iceberg. Most of the work was done on the backend and is invisible to you. 

### The Site

Let me talk about the various pieces that go into this new twit.tv.

We asked the Four Kitchens design team to create something very visual and clean. We feel that people come to the web site for two reasons: first because they googled one of us or were looking for tech information. Those people need to get a quick idea of what twit is and what we do. The front page is designed to do that with the big hero images, quick statements of purpose, and a gallery of recent shows in our three main categories: tech news, help and how-tos, and reviews.[^8]

[^8]:As I mentioned, this is how the site *used* to look. It has changed considerably since then. 

The second reason people come to the site is to find content. These people already know about TWiT, but they want to quickly find and download a show, watch the live stream, or seach for information they heard on a show. The top navigation reflects those primary purposes: Live, Shows, Apps, Search and More... (where we stick everything else). We're using Apache Solr search and I think it's a major upgrade to our old search. 

The site is fully mobile responsive and looks great on every size screen. You can see for yourself by resizing the page and refreshing. We think the site might even look best on mobile - and that's good because that's how most people surf these days!

### Roll the Credits

My deepest thanks to Four Kitchens' designer Jared John for the look and feel (and the lovely Verlag font up front). Kevin Lamping did the dust programming. Peter Sieg was the node.js lead. Any missing or broken features are not their fault - they're ours. We had a strict budget and weren't abe to add many of the cool features we all wanted. But we have an ongoing support contract with Four Kitchens and hope to add the most requested missing features over time. We have a backlog of well over 100 features we didn't have the time or money to implement in version 1.0 I also suspect we'll be ready to do a second phase with Four Kitchens when everybody recovers from this one. In about a year.[^9]

[^9]:And lots of credit to our in house engineer, Patrick Delahanty, who has maintained the site and overseen many changes to make it more usable. We didn't get to add a lot of those 100 features (web engineering is damn expensive) but I think we've got a very useful and functional site. 

The stuff you don't see is even more amazing. Four Kitchens' Drupal dev David Diers took the lead here and worked many long hours (and weekends, too) to get us to launch. Matt Grill played the part of the cavalry, swooping in to make sure SSL worked right, and backing David on getting the API up and running. The two of them worked miracles, and if you enjoy the API, buy them a beer the next time you're in Austin or San Diego (that's where Matt is). I want to buy them a whole brewery.[^10]

[^10]: We still use the Drupal backend, mostly unchanged, throughout our workflow. Once a show is edited it's published to the endpoints, including Cachefly and YouTube, by Drupal. Producers create the show notes in Drupal, and editors put relevant metadata into the Drupal backend where it propagates to everywhere else.

The entire process used the Agile methodology, and our project leaders, Paul Benjamin and Suzy Bates, kept the Jira log humming through 279 user stories and 730 points in nine sprints over the past six months. And if you know Agile you'll know what that means. 

On the TWiT Team, credit to Patrick Delahanty who re-coded our workflow engine, Elroy, to interface with Drupal so that our editors and producers could move their entire data entry workflow to the Drupal backend. And he did it in about a month. Patrick is the official first API user. I managed the project with help from our CEO Lisa Laporte, Engineering Manager, Bruce Chezem, and analyst Jeff Needles. 

The Drupal 7.0 backend is running on Acquia servers[^11] using memcache and Varnish to speed things up. The web front end is running on Heroku. The API is documented at Apiary with key service from 3Scale. Node.js caching is provided by RedisLabs. Video and audio playback on the site is from JW Player. All TWiT shows and RSS feeds are stored and served by Cachefly. 

[^11]:Now on Blackmesh from [Contegix](https://www.contegix.com/)

Many of the pictures you see on the site were shot by Jason Guy at JasonGuyPhotography.com.[^12]

[^12]:And since then, Michael O'Donnell, Moises Luna, John "jammerb" Slanina, Masako Watanabe, and myself.

I hope you like the new TWiT.tv 4.0. Please give me your feedback at leo@leoville.com. We'll fix the bugs as fast as we can, and adjust the interface to better suit your needs when we can afford it. Meanwhile, brush up on your RESTful API calls. I can't wait to see what you do with it. 

For more information about our developer program and the public API visit https://twit.tv/about/developer-program




