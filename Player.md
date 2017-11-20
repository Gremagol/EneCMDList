# Player guide

In this guide we explain how to use Ene's music module. You can play all sorts of songs from: Youtube, SoundCloud, BandCamp, Twitch, Vimeo, Mixer, Spotify and http (a webpage/url were a music file is presented).

Take in mind that playing songs trough Ene can sometimes take up to a minute depending on the amount of songs you play at the same time.

## How to use Ene's music module
As previously stated you can play from many sources including Youtube Streams and even an .mp3 file that you can upload trough Discord!

Here (link to music commands) you can find all the commands related to music.

To play a song you simpley use `.play <url>`. The url can be from a playlist/stream/video/file from all the above stated sources. Ene will automaticlly join the voice-channel your in when you issue the command.

If you want to skip you can use `.skip`, and to stop the quene you can do `.stop` and Ene will leave the voice channel she was in.

**Don't forget to give Ene the permission to *speak* in the voice channel your in!**

### Music sounds laggy
It's possible that the music your playing doesn't sound as perfect as your normally used to. This can happen to alot of factors like:

- Your connection to the Discord Server is to far.
- Discord is having a decrease in network performance.
- The bot might have a small hiccup (temporarly).

If you experience some lag or issue's with the music module you can issue `.distory` to completely reset the music player. Give it a minute or two and then try again.

### Configure Ene’s Music module!

Ene is also alittle configurable with presenting which music is being played. For example you can type `.config` to see a few options to configure a few things.

The track_announce is an option to announce each track that’s being played. This message is sent in the last channel a music related command is used.

Auto_resume is an option that resume’s playing the song when a user joins the voice channel Ene’s in.

Topic_channel is almost the same as track_announce but displays what’s being played in the topic that the option is configured too.

**Note:** If you dont want Ene to change the topic anymore, take away her Permission to manage the Channel. This way, the topic won't get updated anymore.

## How do I configure these options?

Type in `.config track_announce = true` to set it to true, replace true with false to disable the functionality. Auto_resume works the exact same way.

To enable the topic_channel you type in `.config track_announce <Channel name>`. You don’t add the # in the channel name. When the next song is played the topic will automatically change. Do note that the topic get’s overwritten so back the current name if you plan using this option. Also the topic won’t show *yet* if a song is paused or stopped.
