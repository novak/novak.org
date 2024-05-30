+++
title = "GigBeat"
slug = "gigbeat"
date = "2024-05-29"
author = "Michael Novak"
+++

{{< screenshot image="/images/gigbeat_sketches.png" caption="Early sketches of the first GigBeat interface." >}}

GigBeat was a project I started built out of a [Music Hack Day](https://web.archive.org/web/20120201172919/http://musichackday.org/). Like most of the links I'll share pertaining to GigBeat, this website no longer exists. Music Hack Day was a hackathon event going 24 hours and had teams of people building a wide variety of projects related to music. I came across a few presentations from previous events and was planning to attend the New York event in February 2011. I had met Guenther Beyer online through a collection of icons he made available for Android developers. I reached out to him and asked if he would be up for working on an Android project. Initially I pitched him on a different project, an RSS aggregator that pulled in all of your feeds into a single app. His design work for this project was incredible. I kept getting the itch to build something with music. I was using Songbird as a music player on my Linux machines at the time and they had integrated with another company, Songkick, which offered concert data and had an API. I loved how they integrated it into the music player, I could see all my artists tour dates right there. I thought this would be better served as a mobile application, especially with the ability to provide notifications. I reached back out to Guenther and asked if he would be up for working on this with me. Guenther shared my passion for music and was excited to work on it.

The sketches above are the result of a brainstorming session we had over Skype. We set out to build some simple screens that I would be able to implement easily at a Hackathon event. I did not write any code prior to the event, but I was ready to go with all the graphical assets from Guenther.

{{< screenshot image="/images/gigbeat_alpha_screenshots.png" caption="Early implementation of the first GigBeat interface." >}}

These screenshots represent the version I built at the Hackathon over the course of 24 hours. It was a proof of concept and it was exciting to see it functioning on a phone by the end of the event. None of the code from this Hackathon eventually made it into the first version that shipped to the Android Market. In fact, the interface never shipped. Billboard Magazine was in attendance for a piece they ended up running in the magazine covering the event and the projects coming out of it. GigBeat was one of the notable projects they called out in the article. GigBeat also won a prize from Songkick for the implementation of their API. With some of the early excitement surrounding the project Guenther and I set out to build a proper version of the product to ship to the Android Market.

{{< screenshot image="/images/gigbeat_v1_screenshots.png" caption="First version of GigBeat that shipped to the Android Market" >}}

I spent the next several months working towards the first version. Staying up late, getting up early squeezing any amount of time I could building the app. Our goal was to embrace some of the newer trends coming out with Android design, which at this point was not nearly as organized as it would become. We wanted our product to feel like it belonged on the platform, something many apps did not do with Android early on. We shipped this version of the app in September of 2011. We saw a decent number of downloads over the first month. We were at roughly 10,000 downloads by the end of September. We would end up with another roughly 10,000 downloads in October 2011. The first week of November I went up to Boston to attend another Music Hack Day event. I remember sitting at my laptop looking at what I was going to build next when I received a text message from a friend telling me to open up the Android Market on my phone. When I did I saw that GigBeat was front and center at the top of the screen right on the home screen. App promotion on the Android Market at this point in time was huge. This resulted in an explosive number of downloads over the course of the next two months. We began to see websites writing about the app not only from a music perspective but from a design perspective[^1]. 

{{< screenshot image="/images/gigbeat_v12_screenshots.png" caption="Visual refresh for the new Android UI style" >}}

We continued to refine our interface design as the platform changed. It felt like change was moving at warp speed in mobile at this time. This was the beginning of a flatter style design, embracing imagery and typography as core elements of interface design. By this point we were working with Google on taking advantage of new platform features coming out. We were invited to attend Mobile World Congress with Google in 2012 as a partner on the floor with them. We had so many amazing conversations with people walking around the convention floor. We created physical button pins representing each of our dashboard icons from the app. This was quite popular with fans of the app and we ran out of those pretty quick. We shipped the tablet interface for GigBeat prior to the event as it was one of the showcase features of Android at the time. 

{{< screenshot image="/images/gigbeat_feature_screenshots.png" caption="Continual improvements for GigBeat" >}}

We wanted to do more. The ultimate goal was to become a driver of music discovery. The ability for artists to build fan communities was always top of mind for us. We built out a featured section that allowed for highlighting artists. We also began laying the ground work for an artist profile to accompany the tour dates. We were trying to get audio integrated into the experience. Fans going to a show to see the headliner usually don't show up early to see the supporting acts. We felt if we could make it easier for you to experience supporting acts prior to the event you might find them interesting and show up early. We also had plans to support a web portal that artists could use to sell their merch at shows. We wanted to handle the digital experience up through payment and allow the user to pick up their merch at a table.

It should come as no surprise that the music industry doesn't quite work that way. The current situation with Taylor Swift and Ticketmaster is nothing new in the music industry, but they have had such a stronghold on the market that putting up a fight was never going to work. If anyone can do it though, it is probably Taylor[^2]. The Chainsmokers in 2023 at the Upfront Summit spoke on their feelings about the music industry and why they have not invest in music startups[^3].

In June of 2012 we were invited to participate as a speaker at Google I/O[^4], the yearly developer conference that at the time was dominated by Android. This was not a common situation at the time for Google. I don't believe they had any external speakers as part of the I/O conference up to this point. GigBeat was invited along with Square to participate in a session around Android design. Our talk focused on the aspects of our product that we felt best embraced the Android design of the time. It was an incredible experience to be a part of. We were connected with Googlers who worked with us in the weeks leading up to the conference. GigBeat was working with Tim Bray[^5], who gave us absolutely incredible feedback. It was a pleasure getting to work with someone like Tim.

GigBeat ended up with 1,000,000+ downloads on Android, which even today feels unbelievable. The music industry is incredibly tough and I always find myself tempted by going back. Music discovery is not a solved problem and with all the new advances in AI I think we are actually getting further away from it than closer. Regardless, the experience working on this project was so much more than I could have ever hoped for when starting out.

##### GigBeat Press

[Gigbeat Helps Music Fans with Androids See More Shows](https://web.archive.org/web/20190904113523/http://evolver.fm/2011/10/06/gigbeat-helps-music-fans-with-androids-see-more-shows/)

[Is iPhone Losing Its Cool Factor?](https://www.wsj.com/video/is-iphone-losing-its-cool-factor/B3BFEA22-EFC4-4270-AFE1-C12A67B155F9)

[Music Hack Day: Cracking the Code in New York](https://www.billboard.com/music/music-news/music-hack-day-cracking-the-code-in-new-york-472576/)

[^1]: GigBeat - an example of great Android design [Android UI Patterns](https://web.archive.org/web/20111001025956/https://androiduipatterns.com/2011/09/gigbeat-example-of-great-android-design.html)
[^2]: Ticketmaster’s Taylor Swift ticketing fiasco might have just led to a lawsuit from the DOJ [The Verge](https://www.theverge.com/2024/4/16/24131866/doj-ticketmaster-live-nation-antitrust-lawsuit-taylor-swift)
[^3]: From Music to Startups to Venture: The Chainsmokers' Journey to Mantis VC | 2023 Upfront Summit [YouTube](https://www.youtube.com/watch?v=iDTfkBGCMYo)
[^4]: Google I/O 2012 - Playing with Patterns [YouTube](https://www.youtube.com/watch?v=8iUbr8RZKtg)
[^5]: [Tim Bray](https://www.tbray.org/ongoing/)
