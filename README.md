# Discord-Music-Bot

This bot allows you to play audio tracks in a Discord voice channel
of your choice:

<img src="./readme/gallery/1-play-track.png" style="max-width: 60%">

It also contains a simple system for queueing tracks in advance:

<img src="./readme/gallery/2-enqueue-track.png" style="max-width: 60%">

You can search for tracks or enter a direct YouTube link via the chat box (how you would usually send messages to another user)

# Setup

The only required setup is to get the ID of a voice channel you would like to
designate as your server's "radio channel". You can find this id by right
clicking a voice channel in your server with developer mode enabled:

<img src="./readme/gallery/4-copy-voice-channel-id.png" style="max-width: 60%">


Otherwise, you just need to pick a prefix for your bot, and you're all set!

# Prefix Commands

All commands are shown with `!` as a prefix, but you can set whatever you'd like
during setup or afterwards by modifying the `PREFIX` variable.

- `!play <query>`: Play or search for a track
- `!play` Resume a paused track or play the latest track from the queue if the player is disconnected
- `!pause`: Pause the currently playing track
- `!leave`: Disconnect the bot from the voice channel
- `!nowplaying`: Retrieve the current track and queued tracks
- `!queue`: Same as `!nowplaying`
- `!addqueue <query>`: Add a track to the queue
- `!skip`: Skip currently playing track and play the next track in the queue
- `!clearqueue`: Clear the current queue
- `!help`: Bring up help menu

Queued tracks automatically play when the last track finishes.

# Troubleshooting

This app uses the [ytdl-core](https://github.com/fent/node-ytdl-core) npm package
to stream from YouTube, which is frequently updated as YouTube makes changes. 
If your bot has issues downloading a particular track, try again later or check 
for an updated version of the dependency.



