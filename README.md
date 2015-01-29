# Bandcamp TagPlayer

###What is it?
You pass it a genre, it plays music. It's a [userscript](https://greasyfork.org/en/help/installing-user-scripts). It's a [Last.fm Player](http://www.last.fm/listen/globaltags/delta%20blues)-like genre/tag audio player for the music streaming site [bandcamp.com](http://bandcamp.com). 
(Bandcamp is a pretty neat site where bands can publish and sell their music directly to their fans. You can listen to most music for free before deciding to support the musician and buy it).

###How to use it?
1. [Install a userscript addon](https://greasyfork.org/en/help/installing-user-scripts) for your browser of choice so that you can use userscripts. 
2. [Install](https://github.com/SLLABslevap/bandcamp-tagplayer/raw/master/BCTP.user.js) the Bandcamp TagPlayer userscript either [here](https://github.com/SLLABslevap/bandcamp-tagplayer/raw/master/BCTP.user.js), [here](https://greasyfork.org/en/scripts/7786-bandcamp-tagplayer) or [here](https://openuserjs.org/scripts/SLLABslevap/Bandcamp_TagPlayer).
3. The url of BCTP is https://bandcamp.com/tagplayer/ but you can also  access it via the bandcamp tags pages through links the script inserts. Do either of the followings:
 - go to https://bandcamp.com/tagplayer/ and start using it.
 - go to https://bandcamp.com/tags and select "Open tags in TagPlayer", then click a tag.
 - go to the bandcamp tag page of your tag of choice, eg. https://bandcamp.com/tag/christian-rock or https://bandcamp.com/tag/kawaiicorefartgaze and click the player icon by the tag
 - you can also load a tag in the player via url: https://bandcamp.com/tagplayer/?witchwave or https://bandcamp.com/tagplayer/?electronic


###Screenshots?
Coming

###Browser support?
Last tested with
 - Firefox 35.0 with Greasemonkey 2.3
 - Chrome 40.0 with Tampermonkey  3.9

###Notes
 When loading tags, some tags are interchangeable like *"hip-hop"* *"hip hop"* *"hip/hop"*, since these are all converted into a bandcamp-readable format by bandcamp, in this case into *"hip-hop"*. Generally speaking white spaces and most special characters are replaced with "-", so it doesn't matter if you play the *"hip-hop"* or the *"hip hop"* tag, the same tracks will be played in both cases.
	(To see what the bandcamp-readable format of the currently playing tag is, hover over the tag in the *"currently playing:"* section (top right))
 
 Once a tag is loaded, the page can be bookmarked, so you can return later to listen to the same tag by simply opening the bookmark rather than first opening the player then loading the tag.

 Since the script doesn't have bandcamp database access, a pool of tracks  that are available for playback at bandcamp has to be created. The script will select a random track from this pool each time a track is loaded. Since the tracks for a specific tag are loaded into the pool progressively to avoid hogging the bandcamp servers, when loading a specific tag consecutively multiple times, the first track is selected from a pool of the same 40 albums most of the time. For the second track there are 80 albums in the pool, for the third 120 artist, etc., the larger the number of tracks played, the more artists will be loaded into the pool, so there is less chance of the same track to be played repeatedly.

 New/popular option: after changing this, reloading the currently playing tag is recommended since zhe changes don't have an effect on the tracks already loaded into the album pool.

###TODO / features I might add:
- Last.fm track/artist/album lookup button
- Save for later / bookmark / like functionality for tracks
- Option to play a combination of tags rather than a single tag
- Playlist / song history for the current session
(showing the previously played tracks, option to play them again)
(showing the next track)
- Ignore a song / never play a specific song in the future
- Album/artist/track info, buy link
- Last.fm scrobbling
- Share / embed button
- Option to set a default tag(?)
- Responsive design?
- Skinning?
- Caching

###Links
Primary home of the script is on [github](https://github.com/SLLABslevap/bandcamp-tagplayer). It also on [greasyfork](https://greasyfork.org/en/scripts/7786-bandcamp-tagplayer) and [openuserjs ](https://openuserjs.org/scripts/SLLABslevap/Bandcamp_TagPlayer)
