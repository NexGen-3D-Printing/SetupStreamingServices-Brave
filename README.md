## Setup Streaming Services

1: I really appreciate the original work on this Streaming Service setup, but I fail to understand the use of the worst two browsers for privacy, both do not support Ublock Origin and both are massive data hoarders, so I forked this project to change the browsers used to Brave instead.

2: I'm unsure if all services will work as intended, as many I don’t use, but the ones I do use are working perfectly, you may need to open Brave and set it up how you like it first, maybe install Sponsor Block and De-arrow, I will need to work on this script still as I don’t think the apps are opening in their own separate profile, which I highly recommend.


This script will provide a UI to select any URLs found in the `data/links.index` source file, and will create desktop icons and add them to Steam.  It is compatible with all devices running SteamOS.

<table>
  <tr>
    <td><img src="https://raw.githubusercontent.com/NexGen-3D-Printing/SetupStreamingServices-Brave/main/.images/20240709.jpg"/></td>
  </tr>
</table>

### Supported URLs
The list below is based on the index found in the source tree and may not contain the full list.  Review [data/links.index](/data/links.index) for the most up-to-date data.

* [ABC IView](https://iview.abc.net.au)
* [AirGPU](https://app.airgpu.com)
* [Amazon Luna](https://luna.amazon.com/)
* [Amazon Prime Video](https://www.amazon.com/video)
* [Angry Birds TV](https://www.angrybirds.com/series/)
* [Antstream](https://live.antstream.com/)
* [Apple TV](https://tv.apple.com/)
* [BBC iPlayer](https://www.bbc.co.uk/iplayer/)
* [BritBox](https://britbox.com)
* [Binge](https://binge.com.au)
* [Blacknut](https://www.blacknut.com/en-gb/games)
* [Boosteroid](https://cloud.boosteroid.com)
* [CBBC](https://www.bbc.co.uk/cbbc)
* [CBeebies](https://www.bbc.co.uk/cbeebies)
* [Channel 4](https://www.channel4.com/)
* [Crave](https://www.crave.ca/)
* [Criterion Channel](https://www.criterionchannel.com)
* [Crunchyroll](https://www.crunchyroll.com/)
* [Curiosity Stream](https://curiositystream.com)
* [Daily Wire](https://www.dailywire.com/watch)
* [Discord](https://discord.com/app)
* [Disney+](https://www.disneyplus.com/)
* [DocPlay](https://www.docplay.com)
* [Dropout](https://www.dropout.tv/browse)
* [Emby Theater](https://emby.media/)
* [Fox](https://www.fox.com/)
* [Fubo TV](https://www.fubo.tv)
* [GeForce Now](https://play.geforcenow.com/mall/)
* [GBNews Live](https://www.gbnews.com/watch/live)
* [GlobalComix](https://globalcomix.com/)
* [Google Play Books](https://play.google.com/store/books)
* [HBO Max](https://www.max.com/)
* [Home Assistant](https://demo.home-assistant.io/)
* [Hulu](https://www.hulu.com/)
* [Internet Archive Movies](https://archive.org/details/movies)
* [ITV X](https://www.itv.com/)
* [Kanopy](https://www.kanopy.com)
* [Microsoft Movies and TV](https://apps.microsoft.com/movies)
* [My5](https://www.channel5.com/)
* [Nebula](https://nebula.tv/)
* [Netflix](https://www.netflix.com/)
* [Newgrounds Movies](https://www.newgrounds.com/movies)
* [Newgrounds Games](https://www.newgrounds.com/games)
* [Kogama](https://www.kogama.com/)
* [Paramount+](https://www.paramountplus.com/)
* [Peacock TV](https://www.peacocktv.com/)
* [POP Player](https://player.pop.co.uk/)
* [Puffer](https://puffer.stanford.edu/player/)
* [Plex](https://app.plex.tv/)
* [Pocket Casts](https://play.pocketcasts.com)
* [Poki](https://poki.com/)
* [Reddit](https://www.reddit.com/r/all/)
* [SBS Ondemand](https://www.sbs.com.au/ondemand/)
* [Scratch](https://scratch.mit.edu/explore/projects/all)
* [Sling TV](https://www.sling.com)
* [Spotify](https://open.spotify.com/)
* [Stan](https://www.stan.com.au)
* [Steam Broadcasts](https://steamcommunity.com/?subsection=broadcasts)
* [Squid TV](https://www.squidtv.net/)
* [TikTok](https://www.tiktok.com/)
* [Threads](https://www.threads.net/)
* [Twitch](https://www.twitch.tv/)
* [Twitter](https://twitter.com/)
* [Vimeo](https://vimeo.com/)
* [Virgin TV Go](https://virgintvgo.virginmedia.com/en/home)
* [VK Play](https://cloud.vkplay.ru/)
* [Xbox Game Pass Streaming](https://www.xbox.com/play)
* [Xiaohongshu (RedNote)](https://www.xiaohongshu.com/explore)
* [YouTube Music](https://music.youtube.com/)
* [YouTube TV](https://tv.youtube.com/)
* [YouTube](https://www.youtube.com/)
* [WebRcade](https://play.webrcade.com/)

### Installation

1. Switch to desktop mode
2. Open the Discovery App
3. Install Brave Browser
4. Open then close Brave (This will create your main profile, usualy will be called "Work" but you can rename this later if you want)
5. Paste the following into your Konsole

```
curl -L https://github.com/NexGen-3D-Printing/SetupStreamingServices-Brave/raw/main/install.sh | bash
```
6. Once completed, launch Brave again, you will see a profile selection window with a new profile called "Your Brave" select this one and Brave will launch.
7. Go to the Hamburger menu and "Off" for the SideBar menu, once done, you can close Brave again
8. Return to Gamescope, and use the [SteamGridDB](https://github.com/SteamGridDB/decky-steamgriddb) Decky plugin to add images to the new streaming services launchers.

### Enabling Native Touch Support

After opening a shortcut, enable native touch support to improve the user experience.

* Open controller settings for the platform.
* Select `Edit Layout`.
* Select `Action Sets`.
* Select the `Default Settings` gear.
* Select `Add Always-On command`.
* Select `Add command`.
* Select `System`.
* Select `Touchscreen Native Support`.

Return to your application screen, and use touch input.

### Uninstalling
1. Delete the launchers from Steam.
2. Remove the related .desktop files from ~/Applications.
3. Delete steam-browser-open from ~/bin.
