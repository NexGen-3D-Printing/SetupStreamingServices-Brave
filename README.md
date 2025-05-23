## Setup Streaming Services

1: I really appreciate the original work on this Streaming Service setup, but I fail to understand the use of the worst two browsers for privacy, both do not support Ublock Origin and both are massive data hoarders, so I forked this project to change the browser to Brave instead.

2: I'm unsure if all services will work as intended, as many I don’t use, but the ones I do use are working perfectly.

To Do List:

1. Create Uninstall Script
2. Create Seperate Install for 1080p and 1440p Screens (Non Steam Deck Consoles)
3. Have the SideBar disable in Brave automatically on install


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
6. Once completed, Brave will automatically launch into the new profile, you now need to disable the SideBar: Go to the Hamburger menu and select "Off" for the SideBar menu, once done, you can close Brave again.
7. You can now return to Gamescope (Game Mode/Big Picture Mode), and use the [SteamGridDB](https://github.com/SteamGridDB/decky-steamgriddb) Decky plugin to add images to the new streaming services launchers.

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

### Home Assitant Configuration

I have configured the Home Assistant App to use http://homeassistant.local:8123 but this may not work, so you will need to edit the .desktop file with your specific local IP address.

* The .desktop file is located in ~/Applications/StreamingServices and as an example, change the launch argument from "com.brave.Browser http://homeassistant.local:8123" to "com.brave.Browser http://192.168.0.123:8123"

### Uninstalling (Looking to make a simple script for this)
1. Delete the launchers from Steam.
2. Delete the follwing folder: ~/Applications/StreamingServices. (Home/Applications/StreamingServices)
