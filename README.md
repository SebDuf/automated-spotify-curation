## [THE SPOTIFY PLAYLIST](https://open.spotify.com/playlist/6rag6XjWQKCEMxnWOEEVtS?si=s1aiweigRouRSVAMAXXTBA)

## The Idea

Music curation is hard to automate and still relies a lot on human input. Luckily, finding and curating music is also a passion for many people who share their work for others to enjoy.

Therefore, if we curate a list of curators that we like, we could automatically scrap their selections and put them in a single Spotify playlist.

## The Architecture

Key points to keep in mind:
* Laziness is critical; everything else is secondary. Automate as much as possible.
* Music curators live on various platforms (Youtube, Reddit, Spotify itself) and new sources might appear tomorrow. Each scrapper must be independent from one another, but the output must be normalized to a single format and sent to a single location.


## The Architecture

The output of this "system" is tracks added to a Spotify playlist. When a new song appears in a playlist, we have succedeed.

> WIP: Diagram with playlist as end result

Spotify's API allows us to do pretty much any operation we can do in the deskptop or mobile application. When a human wants to add a track to a playlist, it will search for it and then add the result to the playlist.

From Spotify's point of view, everything has a unique identifier (a URI): an album has a URI, a song has a URI, a playlist has a URI, a user has a URI. To add a song to a playlist, we need the playlists' URI and the track URI. We have the former, how do we get the latter?

> WIP: Diagram with playlist/URI and a track/URI going to playlist

A search allows us to transform human text to a list of URIs

> WIP: Diagram with text transforming to track/URI
