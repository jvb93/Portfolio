# The Spotify Experience
[Visit Site](https://spotify-experience.web.app) |
[Github](https://github.com/jvb93/SpotifyExperience)

## What is it?
Do you remember buying physical media? There's something about holding a CD or vinyl in your hands - reading the lyrics or the liner notes as you listen to the album. This feeling of physicality is missing in our current day, where streaming has taken over. 

![Song data from multiple sources](.\img\SpotifyExperience_Main.png)
*Main page showing information about the currewnt song*

The Spotify Experience aims to recreate that feeling by tapping into your now-playing music on Spotify and brings in a ton of additional context about what you're listening to. Detailed artist and song info, analytics, the ability to queue up similar tracks, and more are available through this app.

## Technical
The site is written in Vue and runs almost entirely in your browser. It's hosted on Firebase with a CI pipeline written in Github actions which deploys on every commit to master.

It pulls as much data as it can from the Spotify API and aggregates the rest from the Genius.com API. 

I say it runs *almost entirely* in your browser, because there is a brief exchange of oAuth tokens through a Firebase serverless function in order to preserve client secrets.

