##Table Of Contents
- [Help](#help)
- [Administration](#administration)
- [CustomReactions](#customreactions)
- [Gambling](#gambling)
- [Games](#games)
- [Music](#music)
- [NSFW](#nsfw)
- [Permissions](#permissions)
- [Pokemon](#pokemon)
- [Searches](#searches)
- [Utility](#utility)
- [Xp](#xp)


### Administration  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Administration | `.delmsgoncmd` | Toggles the automatic deletion of the user's successful command message to prevent chat flood. You can use it either as a server toggle, channel whitelist, or channel blacklist, as channel option has 3 settings: Enable (always do it on this channel), Disable (never do it on this channel), and Inherit (respect server setting). Use `list` parameter to see the current states. **Requires Administrator server permission.** | `.delmsgoncmd` or `.delmsgoncmd channel enable` or `.delmsgoncmd channel inherit` or `.delmsgoncmd list`
 Administration | `.deafen` `.deaf` | Deafens mentioned user or users. **Requires DeafenMembers server permission.** | `.deaf "@Someguy"` or `.deaf "@Someguy" "@Someguy"`
 Administration | `.undeafen` `.undef` | Undeafens mentioned user or users. **Requires DeafenMembers server permission.** | `.undef "@Someguy"` or `.undef "@Someguy" "@Someguy"`
 Administration | `.delvoichanl` `.dvch` | Deletes a voice channel with a given name. **Requires ManageChannels server permission.** | `.dvch VoiceChannelName`
 Administration | `.creatvoichanl` `.cvch` | Creates a new voice channel with a given name. **Requires ManageChannels server permission.** | `.cvch VoiceChannelName`
 Administration | `.deltxtchanl` `.dtch` | Deletes a text channel with a given name. **Requires ManageChannels server permission.** | `.dtch TextChannelName`
 Administration | `.creatxtchanl` `.ctch` | Creates a new text channel with a given name. **Requires ManageChannels server permission.** | `.ctch TextChannelName`
 Administration | `.settopic` `.st` | Sets a topic on the current channel. **Requires ManageChannels server permission.** | `.st My new topic`
 Administration | `.setchanlname` `.schn` | Changes the name of the current channel. **Requires ManageChannels server permission.** | `.schn NewName`
 Administration | `.edit` | Edits bot's message, you have to specify message ID and new text. Supports embeds. **Requires ManageMessages server permission.** | `.edit 7479498384 Hi :^)`
 AutoAssignRoleCommands | `.autoassignrole` `.aar` | Automaticaly assigns a specified role to every user who joins the server. Provide no parameters to disable. **Requires ManageRoles server permission.** | `.aar` or `.aar RoleName`
 DangerousCommands | `.execsql` | Executes an sql command and returns the number of affected rows. Dangerous. **Bot Owner Only** | `.execsql UPDATE DiscordUser SET CurrencyAmount=CurrencyAmount+1234`
 DangerousCommands | `.deletewaifus` | Deletes everything from WaifuUpdates and WaifuInfo tables. **Bot Owner Only** | `.deletewaifus`
 DangerousCommands | `.deletecurrency` | Deletes everything from Currency and CurrencyTransactions. **Bot Owner Only** | `.deletecurrency`
 DangerousCommands | `.deleteplaylists` | Deletes everything from MusicPlaylists. **Bot Owner Only** | `.deleteplaylists`
 DangerousCommands | `.deleteexp` | deleteexp **Bot Owner Only** | `deleteexp`
 GameChannelCommands | `.gvc` | Toggles game voice channel feature in the voice channel you're currently in. Users who join the game voice channel will get automatically redirected to the voice channel with the name of their current game, if it exists. Can't move users to channels that the bot has no connect permission for. One per server. **Requires Administrator server permission.** | `.gvc`
 LocalizationCommands | `.languageset` `.langset` | Sets this server's response language. If bot's response strings have been translated to that language, bot will use that language in this server. Reset by using `default` as the locale name. Provide no parameters to see currently set language.  | `.langset de-DE ` or `.langset default`
 LocalizationCommands | `.langsetdefault` `.langsetd` | Sets the bot's default response language. All servers which use a default locale will use this one. Setting to `default` will use the host's current culture. Provide no parameters to see currently set language.  | `.langsetd en-US` or `.langsetd default`
 LocalizationCommands | `.languageslist` `.langli` | List of languages for which translation (or part of it) exist atm.  | `.langli`
 LogCommands | `.logserver` | Enables or Disables ALL log events. If enabled, all log events will log to this channel. **Requires Administrator server permission.** | `.logserver enable` or `.logserver disable`
 LogCommands | `.logignore` | Toggles whether the `.logserver` command ignores this channel. Useful if you have hidden admin channel and public log channel. **Requires Administrator server permission.** | `.logignore`
 LogCommands | `.logevents` | Shows a list of all events you can subscribe to with `.log` **Requires Administrator server permission.** | `.logevents`
 LogCommands | `.log` | Toggles logging event. Disables it if it is active anywhere on the server. Enables if it isn't active. Use `.logevents` to see a list of all events you can subscribe to. **Requires Administrator server permission.** | `.log userpresence` or `.log userbanned`
 MuteCommands | `.setmuterole` | Sets a name of the role which will be assigned to people who should be muted. Default is ene-mute. **Requires ManageRoles server permission.** | `.setmuterole Silenced`
 MuteCommands | `.mute` | Mutes a mentioned user both from speaking and chatting. You can also specify time string for how long the user should be muted. **Requires ManageRoles server permission.** **Requires MuteMembers server permission.** | `.mute @Someone` or `.mute 1h30m @Someone`
 MuteCommands | `.unmute` | Unmutes a mentioned user previously muted with `.mute` command. **Requires ManageRoles server permission.** **Requires MuteMembers server permission.** | `.unmute @Someone`
 MuteCommands | `.chatmute` | Prevents a mentioned user from chatting in text channels. **Requires ManageRoles server permission.** | `.chatmute @Someone`
 MuteCommands | `.chatunmute` | Removes a mute role previously set on a mentioned user with `.chatmute` which prevented him from chatting in text channels. **Requires ManageRoles server permission.** | `.chatunmute @Someone`
 MuteCommands | `.voicemute` | Prevents a mentioned user from speaking in voice channels. **Requires MuteMembers server permission.** | `.voicemute @Someone`
 MuteCommands | `.voiceunmute` | Gives a previously voice-muted user a permission to speak. **Requires MuteMembers server permission.** | `.voiceunmute @Someguy`
 PlayingRotateCommands | `.rotateplaying` `.ropl` | Toggles rotation of playing status of the dynamic strings you previously specified. **Bot Owner Only** | `.ropl`
 PlayingRotateCommands | `.addplaying` `.adpl` | Adds a specified string to the list of playing strings to rotate. You have to pick either 'Playing', 'Watching' or 'Listening' as the first parameter. Supported placeholders: `%servers%`, `%users%`, `%playing%`, `%queued%`, `%time%`, `%shardid%`, `%shardcount%`, `%shardguilds%`. **Bot Owner Only** | `.adpl Playing with you` or `.adpl Watching you sleep`
 PlayingRotateCommands | `.listplaying` `.lipl` | Lists all playing statuses with their corresponding number. **Bot Owner Only** | `.lipl`
 PlayingRotateCommands | `.removeplaying` `.rmpl` `.repl` | Removes a playing string on a given number. **Bot Owner Only** | `.rmpl`
 PrefixCommands | `.prefix` | Sets this server's prefix for all bot commands. Provide no parameters to see the current server prefix. **Setting prefix requires Administrator server permission.**  | `.prefix +`
 PrefixCommands | `.defprefix` | Sets bot's default prefix for all bot commands. Provide no parameters to see the current default prefix. This will not change this server's current prefix. **Bot Owner Only** | `.defprefix +`
 ProtectionCommands | `.antiraid` | Sets an anti-raid protection on the server. Provide no parameters to disable. First parameter is number of people which will trigger the protection. Second parameter is a time interval in which that number of people needs to join in order to trigger the protection, and third parameter is punishment for those people (Kick, Ban, Mute) **Requires Administrator server permission.** | `.antiraid 5 20 Kick` or `.antiraid`
 ProtectionCommands | `.antispam` | Stops people from repeating same message X times in a row. Provide no parameters to disable. You can specify to either mute, kick or ban the offenders. If you're using mute, you can add a number of seconds at the end to use a timed mute. Max message count is 10. **Requires Administrator server permission.** | `.antispam 3 Mute` or `.antispam 4 Kick` or `.antispam`
 ProtectionCommands | `.antispamignore` | Toggles whether antispam ignores current channel. Antispam must be enabled. **Requires Administrator server permission.** | `.antispamignore`
 ProtectionCommands | `.antilist` `.antilst` | Shows currently enabled protection features.  | `.antilist`
 PruneCommands | `.prune` `.clear` | `.prune` removes all Ene's messages in the last 100 messages. `.prune X` removes last `X` number of messages from the channel (up to 100). `.prune @Someone` removes all Someone's messages in the last 100 messages. `.prune @Someone X` removes last `X` number of 'Someone's' messages in the channel.  | `.prune` or `.prune 5` or `.prune @Someone` or `.prune @Someone X`
 SlowModeCommands | `.slowmode` | Toggles slowmode. Disable by specifying no parameters. Slowmode deletes any excess messages users type over the specified limit of messages per X seconds. To enable, specify a number of messages each user can send, followed by an interval in seconds. For example 1 message every 5 seconds. **Requires ManageMessages server permission.** | `.slowmode 1 5` or `.slowmode`
 SlowModeCommands | `.slowmodewl` | Ignores a role or a user from the slowmode feature. **Requires ManageMessages server permission.** | `.slowmodewl SomeRole` or `.slowmodewl AdminDude`
 RoleCommands | `.reactionroles` `.rero` | Specify role names and server emojis with which they're represented, the bot will then add those emojis to the previous message in the channel, and users will be able to get the roles by clicking on the emoji. You can set 'excl' as the first parameter to make them exclusive. You can have up to 5 of these enabled on one server at a time. **Requires ManageRoles server permission.** | `.reactionroles Gamer :SomeServerEmoji: Streamer :Other: Watcher :Other2:` or `.reactionroles excl Horde :Horde: Alliance :Alliance:`
 RoleCommands | `.reactionroleslist` `.reroli` | Lists all ReactionRole messages on this channel and their indexes. **Requires ManageRoles server permission.** | `.reactionroleslist`
 RoleCommands | `.reactionrolesremove` `.rerorm` | Removed a ReactionRole message on the specified index. **Requires ManageRoles server permission.** | `.reactionrolesrm 1`
 RoleCommands | `.setrole` `.sr` | Sets a role for a given user. **Requires ManageRoles server permission.** | `.sr @User Guest`
 RoleCommands | `.removerole` `.rr` | Removes a role from a given user. **Requires ManageRoles server permission.** | `.rr @User Admin`
 RoleCommands | `.renamerole` `.renr` | Renames a role. The role you are renaming must be lower than bot's highest role. **Requires ManageRoles server permission.** | `.renr "First role" SecondRole`
 RoleCommands | `.removeallroles` `.rar` | Removes all roles from a mentioned user. **Requires ManageRoles server permission.** | `.rar @User`
 RoleCommands | `.createrole` `.cr` | Creates a role with a given name. **Requires ManageRoles server permission.** | `.cr Awesome Role`
 RoleCommands | `.deleterole` `.dr` | Deletes a role with a given name. **Requires ManageRoles server permission.** | `.dr Awesome Role`
 RoleCommands | `.rolehoist` `.rh` | Toggles whether this role is displayed in the sidebar or not. **Requires ManageRoles server permission.** | `.rh Guests` or `.rh "Space Wizards"`
 RoleCommands | `.rolecolor` `.roleclr` | Set a role's color using its hex value. Provide no color in order to see the hex value of the color of the specified role.  | `.roleclr Admin` or `.roleclr Admin ffba55`
 RoleCommands | `.mentionrole` `.menro` | Mentions a role. If the role is not mentionable, bot will make it mentionable for a moment. **Requires MentionEveryone server permission.** | `.menro RoleName`
 SelfAssignedRolesCommands | `.adsarm` | Toggles the automatic deletion of confirmations for `.iam` and `.iamn` commands. **Requires ManageMessages server permission.** | `.adsarm`
 SelfAssignedRolesCommands | `.asar` | Adds a role to the list of self-assignable roles. You can also specify a group. If 'Exclusive self-assignable roles' feature is enabled, users will be able to pick one role per group. **Requires ManageRoles server permission.** | `.asar Gamer` or `.asar 1 Alliance` or `.asar 1 Horde`
 SelfAssignedRolesCommands | `.rsar` | Removes a specified role from the list of self-assignable roles. **Requires ManageRoles server permission.** | `.rsar`
 SelfAssignedRolesCommands | `.lsar` | Lists self-assignable roles. Shows 20 roles per page.  | `.lsar` or `.lsar 2`
 SelfAssignedRolesCommands | `.togglexclsar` `.tesar` | Toggles whether the self-assigned roles are exclusive. While enabled, users can only have one self-assignable role per group. **Requires ManageRoles server permission.** | `.tesar`
 SelfAssignedRolesCommands | `.rolelevelreq` `.rlr` | Set a level requirement on a self-assignable role. **Requires ManageRoles server permission.** | `.rlr 5 SomeRole`
 SelfAssignedRolesCommands | `.iam` | Adds a role to you that you choose. Role must be on a list of self-assignable roles.  | `.iam Gamer`
 SelfAssignedRolesCommands | `.iamnot` `.iamn` | Removes a specified role from you. Role must be on a list of self-assignable roles.  | `.iamn Gamer`
 SelfCommands | `.scadd` | Adds a command to the list of commands which will be executed automatically in the current channel, in the order they were added in, by the bot when it startups up. **Bot Owner Only** | `.scadd .stats`
 SelfCommands | `.autocmdadd` | Adds a command to the list of commands which will be executed automatically every X seconds. **Bot Owner Only** | `.autocmdadd 60 .prune 1000`
 SelfCommands | `.sclist` | Lists all startup commands in the order they will be executed in. **Bot Owner Only** | `.sclist`
 SelfCommands | `.autocmds` `.autolist` `.autocmdlist` | Lists all auto commands and the intervals in which they execute. **Bot Owner Only** | `.autolist`
 SelfCommands | `.wait` | Used only as a startup command. Waits a certain number of miliseconds before continuing the execution of the following startup commands. **Bot Owner Only** | `.wait 3000`
 SelfCommands | `.scrm` | Removes a startup or auto command with the provided index. **Bot Owner Only** | `.scrm 3`
 SelfCommands | `.scclr` | Removes all startup commands. **Bot Owner Only** | `.scclr`
 SelfCommands | `.fwmsgs` | Toggles forwarding of non-command messages sent to bot's DM to the bot owners **Bot Owner Only** | `.fwmsgs`
 SelfCommands | `.fwtoall` | Toggles whether messages will be forwarded to all bot owners or only to the first one specified in the credentials.json file **Bot Owner Only** | `.fwtoall`
 SelfCommands | `.shardstats` | Stats for shards. Paginated with 25 shards per page.  | `.shardstats` or `.shardstats 2`
 SelfCommands | `.restartshard` | Try (re)connecting a shard with a certain shardid when it dies. No one knows will it work. Keep an eye on the console for errors. **Bot Owner Only** | `.restartshard 2`
 SelfCommands | `.leave` | Makes Ene leave the server. Either server name or server ID is required. **Bot Owner Only** | `.leave 123123123331`
 SelfCommands | `.sleep` | Shuts the bot down. **Bot Owner Only** | `.sleep`
 SelfCommands | `.nap` | Restarts the bot. Might not work. **Bot Owner Only** | `.nap`
 SelfCommands | `.setname` `.newnm` | Gives the bot a new name. **Bot Owner Only** | `.newnm BotName`
 SelfCommands | `.setnick` | Changes the nickname of the bot on this server. You can also target other users to change their nickname. **Requires ManageNicknames server permission.** | `.setnick BotNickname` or `.setnick @SomeUser New Nickname`
 SelfCommands | `.setstatus` | Sets the bot's status. (Online/Idle/Dnd/Invisible) **Bot Owner Only** | `.setstatus Idle`
 SelfCommands | `.setavatar` `.setav` | Sets a new avatar image for the EneBot. Parameter is a direct link to an image. **Bot Owner Only** | `.setav http://i.imgur.com/xTG3a1I.jpg`
 SelfCommands | `.game` | Sets the bots game status to either Playing, Listening, or Watching. **Bot Owner Only** | `.setgame Playing with snakes.` or `.setgame Watching anime.` or `.setgame Listening music.`
 SelfCommands | `.setstream` | Sets the bots stream. First parameter is the twitch link, second parameter is stream name. **Bot Owner Only** | `.setstream TWITCHLINK Hello`
 SelfCommands | `.send` | Sends a message to someone on a different server through the bot.  Separate server and channel/user ids with `|` and prefix the channel id with `c:` and the user id with `u:`. **Bot Owner Only** | `.send serverid|c:channelid message` or `.send serverid|u:userid message`
 SelfCommands | `.imagesreload` | Reloads images bot is using. Safe to use even when bot is being used heavily. **Bot Owner Only** | `.imagesreload`
 SelfCommands | `.botconfigreload` | Reloads bot configuration in case you made changes to the BotConfig table either with .execsql or manually in the .db file. **Bot Owner Only** | `.botconfigreload`
 ServerGreetCommands | `.greetdel` `.grdel` | Sets the time it takes (in seconds) for greet messages to be auto-deleted. Set it to 0 to disable automatic deletion. **Requires ManageServer server permission.** | `.greetdel 0` or `.greetdel 30`
 ServerGreetCommands | `.greet` | Toggles anouncements on the current channel when someone joins the server. **Requires ManageServer server permission.** | `.greet`
 ServerGreetCommands | `.greetmsg` | Sets a new join announcement message which will be shown in the server's channel. Type `%user%` if you want to mention the new member. Using it with no message will show the current greet message. You can use embed json from <https://gremagol.com/embed-generator> instead of a regular text, if you want the message to be embedded. **Requires ManageServer server permission.** | `.greetmsg Welcome, %user%.`
 ServerGreetCommands | `.greetdm` | Toggles whether the greet messages will be sent in a DM (This is separate from greet - you can have both, any or neither enabled). **Requires ManageServer server permission.** | `.greetdm`
 ServerGreetCommands | `.greetdmmsg` | Sets a new join announcement message which will be sent to the user who joined. Type `%user%` if you want to mention the new member. Using it with no message will show the current DM greet message. You can use embed json from <https://gremagol.com/embed-generator> instead of a regular text, if you want the message to be embedded. **Requires ManageServer server permission.** | `.greetdmmsg Welcome to the server, %user%`
 ServerGreetCommands | `.bye` | Toggles anouncements on the current channel when someone leaves the server. **Requires ManageServer server permission.** | `.bye`
 ServerGreetCommands | `.byemsg` | Sets a new leave announcement message. Type `%user%` if you want to show the name the user who left. Type `%id%` to show id. Using this command with no message will show the current bye message. You can use embed json from <https://gremagol.com/embed-generator> instead of a regular text, if you want the message to be embedded. **Requires ManageServer server permission.** | `.byemsg %user% has left.`
 ServerGreetCommands | `.byedel` | Sets the time it takes (in seconds) for bye messages to be auto-deleted. Set it to `0` to disable automatic deletion. **Requires ManageServer server permission.** | `.byedel 0` or `.byedel 30`
 TimeZoneCommands | `.timezones` | Lists all timezones available on the system to be used with `.timezone`.  | `.timezones`
 TimeZoneCommands | `.timezone` | Sets this guilds timezone. This affects bot's time output in this server (logs, etc..)  | `.timezone` or `.timezone GMT Standard Time`
 UserPunishCommands | `.warn` | Warns a user. **Requires BanMembers server permission.** | `.warn @b1nzy Very rude person`
 UserPunishCommands | `.warnlog` | See a list of warnings of a certain user. **Requires BanMembers server permission.** | `.warnlog @b1nzy`
 UserPunishCommands | `.warnlogall` | See a list of all warnings on the server. 15 users per page. **Requires BanMembers server permission.** | `.warnlogall` or `.warnlogall 2`
 UserPunishCommands | `.warnclear` `.warnc` | Clears all warnings from a certain user. You can specify a number to clear a specific one. **Requires BanMembers server permission.** | `.warnclear @PoorDude 3` or `.warnclear @PoorDude`
 UserPunishCommands | `.warnpunish` `.warnp` | Sets a punishment for a certain number of warnings. You can specify a time string after 'Ban' or 'Mute' punishment to make it a temporary mute/ban. Provide no punishment to remove. **Requires BanMembers server permission.** | `.warnp 5 Ban` or `.warnp 3` or `.warnp 5 Mute 2d12h`
 UserPunishCommands | `.warnpunishlist` `.warnpl` | Lists punishments for warnings.  | `.warnpunishlist`
 UserPunishCommands | `.ban` `.b` | Bans a user by ID or name with an optional message. You can specify a time string before the user name to ban the user temporarily. **Requires BanMembers server permission.** | `.b "@some Guy" Your behaviour is toxic.` or `.b 1d12h @b1nzy Come back when u chill`
 UserPunishCommands | `.unban` | Unbans a user with the provided user#discrim or id. **Requires BanMembers server permission.** | `.unban kwoth#1234` or `.unban 123123123`
 UserPunishCommands | `.softban` `.sb` | Bans and then unbans a user by ID or name with an optional message. **Requires KickMembers server permission.** **Requires ManageMessages server permission.** | `.sb "@some Guy" Your behaviour is toxic.`
 UserPunishCommands | `.kick` `.k` | Kicks a mentioned user. **Requires KickMembers server permission.** | `.k "@some Guy" Your behaviour is toxic.`
 UserPunishCommands | `.masskill` | Specify a new-line separated list of `userid reason`. You can use Username#discrim instead of UserId. Specified users will be banned from the current server, blacklisted from the bot, and have all of their flowers taken away. **Requires BanMembers server permission.** **Bot Owner Only** | `.masskill BadPerson#1234 Toxic person`
 VcRoleCommands | `.vcrole` | Sets or resets a role which will be given to users who join the voice channel you're in when you run this command. Provide no role name to disable. You must be in a voice channel to run this command. **Requires ManageRoles server permission.** | `.vcrole SomeRole` or `.vcrole`
 VcRoleCommands | `.vcrolelist` | Shows a list of currently set voice channel roles.  | `.vcrolelist`

###### [Back to ToC](#table-of-contents)

### CustomReactions  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 CustomReactions | `.addcustreact` `.acr` | Add a custom reaction with a trigger and a response. Running this command in server requires the Administration permission. Running this command in DM is Bot Owner only and adds a new global custom reaction. Guide here: <http://enecmdlist.readthedocs.io/en/latest/Custom%20Reactions/>  | `.acr "hello" Hi there %user%`
 CustomReactions | `.editcustreact` `.ecr` | Edits the custom reaction's response given its ID.  | `.ecr 123 I'm a magical girl`
 CustomReactions | `.listcustreact` `.lcr` | Lists global or server custom reactions (20 commands per page). Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions. Specifying `all` parameter instead of the number will DM you a text file with a list of all custom reactions.  | `.lcr 1` or `.lcr all`
 CustomReactions | `.listcustreactg` `.lcrg` | Lists global or server custom reactions (20 commands per page) grouped by trigger, and show a number of responses for each. Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions.  | `.lcrg 1`
 CustomReactions | `.showcustreact` `.scr` | Shows a custom reaction's response on a given ID.  | `.scr 1`
 CustomReactions | `.delcustreact` `.dcr` | Deletes a custom reaction on a specific index. If ran in DM, it is bot owner only and deletes a global custom reaction. If ran in a server, it requires Administration privileges and removes server custom reaction.  | `.dcr 5`
 CustomReactions | `.crca` | Toggles whether the custom reaction will trigger if the triggering message contains the keyword (instead of only starting with it).  | `.crca 44`
 CustomReactions | `.crdm` | Toggles whether the response message of the custom reaction will be sent as a direct message.  | `.crdm 44`
 CustomReactions | `.crad` | Toggles whether the message triggering the custom reaction will be automatically deleted.  | `.crad 59`
 CustomReactions | `.crstatsclear` | Resets the counters on `.crstats`. You can specify a trigger to clear stats only for that trigger. **Bot Owner Only** | `.crstatsclear` or `.crstatsclear rng`
 CustomReactions | `.crstats` | Shows a list of custom reactions and the number of times they have been executed. Paginated with 10 per page. Use `.crstatsclear` to reset the counters.  | `.crstats` or `.crstats 3`
 CustomReactions | `.crclear` | Deletes all custom reactions on this server. **Requires Administrator server permission.** | `.crclear`

###### [Back to ToC](#table-of-contents)

### Gambling  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Gambling | `.daily` `.timely` | Use to claim your 'timely' currency. Bot owner has to specify the amount and the period on how often you can claim your currency.  | `.daily .timely`
 Gambling | `.timelyreset` | Resets all user timeouts on `.timely` command. **Bot Owner Only** | `.timelyreset`
 Gambling | `.timelyset` | Sets the 'timely' currency allowance amount for users. Second parameter is period in hours, default is 24 hours. **Bot Owner Only** | `.timelyset 100` or `.timelyset 50 12`
 Gambling | `.raffle` | Prints a name and ID of a random online user from the server, or from the online user in the specified role.  | `.raffle` or `.raffle RoleName`
 Gambling | `.raffleany` | Prints a name and ID of a random user from the server, or from the specified role.  | `.raffleany` or `.raffleany  RoleName`
 Gambling | `.$` `.currency` `.$$` `.$$$` `.cash` `.cur` | Check how much currency a person has. (Defaults to yourself)  | `.$` or `.$ @SomeGuy`
 Gambling | `.curtrs` | Shows your currency transactions on the specified page. Bot owner can see other people's transactions too.  | `.curtrs 2` or `.curtrs @SomeUser 2`
 Gambling | `.give` | Give someone a certain amount of currency. You can specify the reason after the mention.  | `.give 1 @SomeGuy` or `.give 5 @CootGurl Ur so pwetty`
 Gambling | `.award` | Awards someone a certain amount of currency. You can specify the reason after the Username. You can also specify a role name to award currency to all users in a role. **Bot Owner Only** | `.award 100 @person` or `.award 5 Role Of Gamblers`
 Gambling | `.take` | Takes a certain amount of currency from someone. **Bot Owner Only** | `.take 1 @SomeGuy`
 Gambling | `.rollduel` | Challenge someone to a roll duel by specifying the amount and the user you wish to challenge as the parameters. To accept the challenge, just specify the name of the user who challenged you, without the amount.  | `.rollduel 50 @SomeGuy` or `.rollduel @Challenger`
 Gambling | `.betroll` `.br` | Bets a certain amount of currency and rolls a dice. Rolling over 66 yields x2 of your currency, over 90 - x4 and 100 x10.  | `.br 5`
 Gambling | `.leaderboard` `.lb` | Displays the bot's currency leaderboard.  | `.lb`
 Gambling | `.rps` | Play a game of Rocket-Paperclip-Scissors with Ene. You can bet on it. Multiplier is the same as on betflip.  | `.rps r 100` or `.rps scissors`
 AnimalRacingCommands | `.race` | Starts a new animal race.  | `.race`
 AnimalRacingCommands | `.joinrace` `.jr` | Joins a new race. You can specify an amount of currency for betting (optional). You will get YourBet*(participants-1) back if you win.  | `.jr` or `.jr 5`
 BlackJackCommands | `.blackjack` `.bj` | Start or join a blackjack game. You must specify the amount you're betting. Use `.hit`, `.stand` and `.double` commands to play. Game is played with 4 decks. Dealer hits on soft 17 and wins draws.  | `.bj 50`
 BlackJackCommands | `.hit` | In the blackjack game, ask the dealer for an extra card.  | `.hit`
 BlackJackCommands | `.stand` | Finish your turn in the blackjack game.  | `.stand`
 BlackJackCommands | `.double` | In the blackjack game, double your bet in order to receive exactly one more card, and your turn ends.  | `.double`
 Connect4Commands | `.connect4` `.con4` | Creates or joins an existing connect4 game. 2 players are required for the game. Objective of the game is to get 4 of your pieces next to each other in a vertical, horizontal or diagonal line. You can specify a bet when you create a game and only users who bet the same amount will be able to join your game.  | `.connect4`
 CurrencyEventsCommands | `.event` | Starts one of the events seen on public Ene. Events: `reaction` **Bot Owner Only** | `.eventstart reaction` or `.eventstart reaction -d 1 -a 50 --pot-size 1500`
 CurrencyRaffleCommands | `.rafflecur` | Starts or joins a currency raffle with a specified amount. Users who join the raffle will lose the amount of currency specified and add it to the pot. After 30 seconds, random winner will be selected who will receive the whole pot. There is also a `mixed` mode in which the users will be able to join the game with any amount of currency, and have their chances be proportional to the amount they've bet.  | `.rafflecur 20` or `.rafflecur mixed 15`
 DiceRollCommands | `.roll` | Rolls 0-100. If you supply a number `X` it rolls up to 30 normal dice. If you split 2 numbers with letter `d` (`xdy`) it will roll `X` dice from 1 to `y`. `Y` can be a letter 'F' if you want to roll fate dice instead of dnd.  | `.roll` or `.roll 7` or `.roll 3d5` or `.roll 5dF`
 DiceRollCommands | `.rolluo` | Rolls `X` normal dice (up to 30) unordered. If you split 2 numbers with letter `d` (`xdy`) it will roll `X` dice from 1 to `y`.  | `.rolluo` or `.rolluo 7` or `.rolluo 3d5`
 DiceRollCommands | `.nroll` | Rolls in a given range. If you specify just one number instead of the range, it will role from 0 to that number.  | `.nroll 5` or `.nroll 5-15`
 DrawCommands | `.draw` | Draws a card from this server's deck. You can draw up to 10 cards by supplying a number of cards to draw.  | `.draw` or `.draw 5`
 DrawCommands | `.drawnew` | Draws a card from the NEW deck of cards. You can draw up to 10 cards by supplying a number of cards to draw.  | `.drawnew` or `.drawnew 5`
 DrawCommands | `.deckshuffle` `.dsh` | Reshuffles all cards back into the deck.  | `.dsh`
 FlipCoinCommands | `.flip` | Flips coin(s) - heads or tails, and shows an image.  | `.flip` or `.flip 3`
 FlipCoinCommands | `.betflip` `.bf` | Bet to guess will the result be heads or tails. Guessing awards you 1.95x the currency you've bet (rounded up). Multiplier can be changed by the bot owner.  | `.bf 5 heads` or `.bf 3 t`
 FlowerShopCommands | `.shop` | Lists this server's administrators' shop. Paginated.  | `.shop` or `.shop 2`
 FlowerShopCommands | `.buy` | Buys an item from the shop on a given index. If buying items, make sure that the bot can DM you.  | `.buy 2`
 FlowerShopCommands | `.shopadd` | Adds an item to the shop by specifying type price and name. Available types are role and list. **Requires Administrator server permission.** | `.shopadd role 1000 Rich`
 FlowerShopCommands | `.shoplistadd` | Adds an item to the list of items for sale in the shop entry given the index. You usually want to run this command in the secret channel, so that the unique items are not leaked. **Requires Administrator server permission.** | `.shoplistadd 1 Uni-que-Steam-Key`
 FlowerShopCommands | `.shoprem` `.shoprm` | Removes an item from the shop by its ID. **Requires Administrator server permission.** | `.shoprm 1`
 SlotCommands | `.slotstats` | Shows the total stats of the slot command for this bot's session. **Bot Owner Only** | `.slotstats`
 SlotCommands | `.slottest` | Tests to see how much slots payout for X number of plays. **Bot Owner Only** | `.slottest 1000`
 SlotCommands | `.slot` | Play Ene slots. Max bet is 10 mil. 1.5 second cooldown per user.  | `.slot 5`
 WaifuClaimCommands | `.waifureset` | Resets your waifu stats, except current waifus.  | `.waifureset`
 WaifuClaimCommands | `.claimwaifu` `.claim` | Claim a waifu for yourself by spending currency.  You must spend at least 10% more than her current value unless she set `.affinity` towards you.  | `.claim 50 @Himesama`
 WaifuClaimCommands | `.waifutransfer` | Transfer the ownership of one of your waifus to another user. You must pay 10% of your waifu's value.  | `.waifutransfer @ExWaifu @NewOwner`
 WaifuClaimCommands | `.divorce` | Releases your claim on a specific waifu. You will get some of the money you've spent back unless that waifu has an affinity towards you. 6 hours cooldown.  | `.divorce @CheatingSloot`
 WaifuClaimCommands | `.affinity` | Sets your affinity towards someone you want to be claimed by. Setting affinity will reduce their `.claim` on you by 20%. Provide no parameters to clear your affinity. 30 minutes cooldown.  | `.affinity @MyHusband` or `.affinity`
 WaifuClaimCommands | `.waifus` `.waifulb` | Shows top 9 waifus. You can specify another page to show other waifus.  | `.waifus` or `.waifulb 3`
 WaifuClaimCommands | `.waifuinfo` `.waifustats` | Shows waifu stats for a target person. Defaults to you if no user is provided.  | `.waifuinfo @MyCrush` or `.waifuinfo`
 WaifuClaimCommands | `.waifugift` `.gift` `.gifts` | Gift an item to someone. This will increase their waifu value by 50% of the gifted item's value if they don't have affinity set towards you, or 100% if they do. Provide no parameters to see a list of items that you can gift.  | `.gifts` or `.gift Rose @Himesama`
 WheelOfFortuneCommands | `.wheeloffortune` `.wheel` | Bets a certain amount of currency on the wheel of fortune. Wheel can stop on one of many different multipliers. Won amount is rounded down to the nearest whole number.  | `.wheel 10`

###### [Back to ToC](#table-of-contents)

### Games  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Games | `.choose` | Chooses a thing from a list of things  | `.choose Get up;Sleep;Sleep more`
 Games | `.8ball` | Ask the 8ball a yes/no question.  | `.8ball Is b1nzy a nice guy?`
 Games | `.rategirl` | Use the universal hot-crazy wife zone matrix to determine the girl's worth. It is everything young men need to know about women. At any moment in time, any woman you have previously located on this chart can vanish from that location and appear anywhere else on the chart.  | `.rategirl @SomeGurl`
 Games | `.linux` | Prints a customizable Linux interjection  | `.linux Spyware Windows`
 AcropobiaCommands | `.acrophobia` `.acro` | Starts an Acrophobia game.  | `.acro` or `.acro -s 30`
 ChatterBotCommands | `.cleverbot` | Toggles cleverbot session. When enabled, the bot will reply to messages starting with bot mention in the server. Custom reactions starting with %mention% won't work if cleverbot is enabled. **Bot Owner Only** | `.cleverbot`
 HangmanCommands | `.hangmanlist` | Shows a list of hangman term types.  | `.hangmanlist`
 HangmanCommands | `.hangman` | Starts a game of hangman in the channel. Use `.hangmanlist` to see a list of available term types. Defaults to 'all'.  | `.hangman` or `.hangman movies`
 HangmanCommands | `.hangmanstop` | Stops the active hangman game on this channel if it exists.  | `.hangmanstop`
 LeetCommands | `.leet` | Converts a text to leetspeak with 6 (1-6) severity levels  | `.leet 3 Hello`
 NunchiCommands | `.nunchi` | Creates or joins an existing nunchi game. Users have to count up by 1 from the starting number shown by the bot. If someone makes a mistake (types an incorrect number, or repeats the same number) they are out of the game and a new round starts without them.  Minimum 3 users required.  | `.nunchi`
 PlantPickCommands | `.pick` | Picks the currency planted in this channel. 60 seconds cooldown.  | `.pick`
 PlantPickCommands | `.plant` | Spend an amount of currency to plant it in this channel. Default is 1. (If bot is restarted or crashes, the currency will be lost)  | `.plant` or `.plant 5`
 PlantPickCommands | `.gencurrency` `.gc` | Toggles currency generation on this channel. Every posted message will have chance to spawn currency. Chance is specified by the Bot Owner. (default is 2%) **Requires ManageMessages server permission.** | `.gc`
 PollCommands | `.poll` `.ppoll` | Creates a public poll which requires users to type a number of the voting option in the channel command is ran in. **Requires ManageMessages server permission.** | `.ppoll Question?;Answer1;Answ 2;A_3`
 PollCommands | `.pollstats` | Shows the poll results without stopping the poll on this server. **Requires ManageMessages server permission.** | `.pollstats`
 PollCommands | `.pollend` | Stops active poll on this server and prints the results in this channel. **Requires ManageMessages server permission.** | `.pollend`
 SpeedTypingCommands | `.typestart` | Starts a typing contest.  | `.typestart`
 SpeedTypingCommands | `.typestop` | Stops a typing contest on the current channel.  | `.typestop`
 SpeedTypingCommands | `.typeadd` | Adds a new article to the typing contest. **Bot Owner Only** | `.typeadd wordswords`
 SpeedTypingCommands | `.typelist` | Lists added typing articles with their IDs. 15 per page.  | `.typelist` or `.typelist 3`
 SpeedTypingCommands | `.typedel` | Deletes a typing article given the ID. **Bot Owner Only** | `.typedel 3`
 TicTacToeCommands | `.tictactoe` `.ttt` | Starts a game of tic tac toe. Another user must run the command in the same channel in order to accept the challenge. Use numbers 1-9 to play.  | `.ttt`
 TriviaCommands | `.trivia` `.t` | Starts a game of trivia. You can add `nohint` to prevent hints. First player to get to 10 points wins by default. You can specify a different number. 30 seconds per question.  | `.t` or `.t --timeout 5 -p -w 3 -q 10`
 TriviaCommands | `.tl` | Shows a current trivia leaderboard.  | `.tl`
 TriviaCommands | `.tq` | Quits current trivia after current question.  | `.tq`

###### [Back to ToC](#table-of-contents)

### Help  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Help | `.modules` `.mdls` | Lists all bot modules.  | `.modules`
 Help | `.commands` `.cmds` | List all of the bot's commands from a certain module. You can either specify the full name or only the first few letters of the module name.  | `.cmds Admin` or `.cmds Admin --view 1`
 Help | `.help` `.h` | Either shows a help for a single command, or DMs you help link if no parameters are specified.  | `.h .cmds` or `.h`
 Help | `.hgit` | Generates the commandlist.md file. **Bot Owner Only** | `.hgit`
 Help | `.readme` `.guide` | Sends a readme and a guide links to the channel.  | `.readme` or `.guide`
 Help | `.donate` | Instructions for helping the project financially.  | `.donate`
 Help | `.invite` | Sends invite links to your current channel.  | `.invite`

###### [Back to ToC](#table-of-contents)

### NSFW  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 NSFW | `.autohentai` | Posts a hentai every X seconds with a random tag from the provided tags. Use `|` to separate tags. 20 seconds minimum. Provide no parameters to disable. **Requires ManageMessages channel permission.** | `.autohentai 30 yuri|tail|long_hair` or `.autohentai`
 NSFW | `.autoboobs` | Posts a boobs every X seconds. 20 seconds minimum. Provide no parameters to disable. **Requires ManageMessages channel permission.** | `.autoboobs 30` or `.autoboobs`
 NSFW | `.autobutts` | Posts a butts every X seconds. 20 seconds minimum. Provide no parameters to disable. **Requires ManageMessages channel permission.** | `.autobutts 30` or `.autobutts`
 NSFW | `.hentai` | Shows a hentai image from a random website (gelbooru or danbooru or konachan or atfbooru or yandere) with a given tag. Tag is optional but preferred. Only 1 tag allowed.  | `.hentai yuri`
 NSFW | `.hentaibomb` | Shows a total 5 images (from gelbooru, danbooru, konachan, yandere and atfbooru). Tag is optional but preferred.  | `.hentaibomb yuri`
 NSFW | `.yandere` | Shows a random image from yandere with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `.yandere tag1+tag2`
 NSFW | `.konachan` | Shows a random hentai image from konachan with a given tag. Tag is optional but preferred.  | `.konachan yuri`
 NSFW | `.e621` | Shows a random hentai image from e621.net with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `.e621 yuri+kissing`
 NSFW | `.rule34` | Shows a random image from rule34.xx with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `.rule34 yuri+kissing`
 NSFW | `.danbooru` | Shows a random hentai image from danbooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `.danbooru yuri+kissing`
 NSFW | `.gelbooru` | Shows a random hentai image from gelbooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `.gelbooru yuri+kissing`
 NSFW | `.derpibooru` `.derpi` | Shows a random image from derpibooru with a given tag. Tag is optional but preferred.  | `.derpi yuri+kissing`
 NSFW | `.boobs` | Real adult content.  | `.boobs`
 NSFW | `.butts` `.ass` `.butt` | Real adult content.  | `.butts` or `.ass`
 NSFW | `.nsfwtagbl` `.nsfwtbl` | Toggles whether the tag is blacklisted or not in nsfw searches. Provide no parameters to see the list of blacklisted tags.  | `.nsfwtbl poop`
 NSFW | `.nsfwcc` | Clears nsfw cache. **Bot Owner Only** | `.nsfwcc`

###### [Back to ToC](#table-of-contents)

### Music  
Submodule | Commands and aliases | Description | Usage
----------|------------|-----------------|-------
 Config | `.config` | Gives you various options like announce the song that's currently playing in the selected channel. | `.config topic_channel = music` `.config auto_resume = true` `.cfg`
 Config | `.mprefix` | Set a Prefix of the Musicmodule for your Server. **Note:** If you forgot the prefix, you can do `@Ene mprefix` | `.mprefix +` `+smp .`
 Config | `.mlanguage` | Ene supports several user-contributed languages that you can select with this command. | `.mlang` `.mlang de_DE`
 Perms | `.admin` | Allows whitelisting members and roles for the Admin rank. Guide here: http://enecmdlist.readthedocs.io/en/latest/Permissions/ | `.admin add Staff` `.admin del DjRole` `.admin list`
 Perms | `.dj` | Allows whitelisting members and roles for the DJ rank. Guide here: http://enecmdlist.readthedocs.io/en/latest/Permissions/ | `.dj add @DjRole` `.dj del everyone` `.dj list`
 Perms | `.user` | Allows whitelisting members and roles for the User rank. Guide here: http://enecmdlist.readthedocs.io/en/latest/Permissions/ | `.user add @everyone` `.user del everyone` `.user list`
 Control | `.stop` | Stop the player and clear the playlist. | `.stop` `.s`
 Control | `.join` | Makes Ene join your current voice channel. | `.join` `.j`
 Control | `.disconnect` | Make Ene leave the current voice channel. | `.disconnect` `.lv`
 Control | `.play <url>` or `.play <search-term>` | Play music from the given URL or search for a track. | `.q` `.play`
 Control | `.pause` | Pause the player. | `.pause`
 Control | `.unpause` | Unpause the player. | `.unpause` `.resume`
 Control | `.split <url>` | Split a YouTube video into a tracklist provided in its description. | `.split <url>`
 Control | `.select 1` or `.play 4` | Select one of the offered tracks after a search to play. | `.select 4` `.play 4`
 Control | `.songrepeat single|all|off` | Toggle between repeat modes. | `.srp`
 Control | `.shuffle` | Toggle shuffle mode for the current queue. | `.shuffle`
 Control | `.reshuffle` | Reshuffle the current queue. | `reshuffle`
 Control | `.skip` or `skip 2` | Skip the current song, the nth song in the queue, all songs from n to m, or all songs from mentioned users. Please use in moderation. | `.skip 10` `.skip`
 Control | `.volume <0-150>` | Changes the volume. Values are 0-150 and 100 is the default. | `.volume`
 Control | `.destroy` | Reset the player and clear the playlist. | `.d` `.destory`
 Info | `.nowplaying` | Display the currently playing song. | `.np` `nowplaying`
 Info | `.list` | Display a list of the current songs in the playlist. | `.lq` `.list` 
 Info | `.export` | Export the current queue to a hastebin link, can be later used as a playlist. | `.export` `.ex`
 Info | `.gensokyo` | Show the current song played on gensokyoradio.net | `.gensokyo`
 Info | `.history` | Display a list of the songs in playlist history. | `.h` `.history`
 Seeking | `.forward [[hh:]mm:]ss` | Forward the track by a given amount of time. | `.forward 2:30`
 Seeking | `.rewind [[hh:]mm:]ss` | Rewind the track by a given amount of time. | `.rewind 30`
 Seeking | `.seek [[hh:]mm:]ss` | Set the position of the track to the given time. | `.seek 2:45:00`
 Seeking | `.restart` | Restart the currently playing track. | `.restart`

###### [Back to ToC](#table-of-contents)

### Permissions  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Permissions | `.verbose` `.v` | Sets whether to show when a command/module is blocked.  | `.verbose true`
 Permissions | `.permrole` `.pr` | Sets a role which can change permissions. Supply no parameters to see the current one. Type 'reset' instead of the role name to reset the currently set permission role. Users with Administrator server permissions can use permission commands regardless of whether they have the specified role. There is no default permission role. **Requires Administrator server permission.** | `.pr Some Role` or `.pr reset`
 Permissions | `.listperms` `.lp` | Lists whole permission chain with their indexes. You can specify an optional page number if there are a lot of permissions.  | `.lp` or `.lp 3`
 Permissions | `.removeperm` `.rp` | Removes a permission from a given position in the Permissions list.  | `.rp 1`
 Permissions | `.moveperm` `.mp` | Moves permission from one position to another in the Permissions list.  | `.mp 2 4`
 Permissions | `.srvrcmd` `.sc` | Sets a command's permission at the server level.  | `.sc "command name" disable`
 Permissions | `.srvrmdl` `.sm` | Sets a module's permission at the server level.  | `.sm ModuleName enable`
 Permissions | `.usrcmd` `.uc` | Sets a command's permission at the user level.  | `.uc "command name" enable SomeUsername`
 Permissions | `.usrmdl` `.um` | Sets a module's permission at the user level.  | `.um ModuleName enable SomeUsername`
 Permissions | `.rolecmd` `.rc` | Sets a command's permission at the role level.  | `.rc "command name" disable MyRole`
 Permissions | `.rolemdl` `.rm` | Sets a module's permission at the role level.  | `.rm ModuleName enable MyRole`
 Permissions | `.chnlcmd` `.cc` | Sets a command's permission at the channel level.  | `.cc "command name" enable SomeChannel`
 Permissions | `.chnlmdl` `.cm` | Sets a module's permission at the channel level.  | `.cm ModuleName enable SomeChannel`
 Permissions | `.allchnlmdls` `.acm` | Enable or disable all modules in a specified channel.  | `.acm enable #SomeChannel`
 Permissions | `.allrolemdls` `.arm` | Enable or disable all modules for a specific role.  | `.arm [enable/disable] MyRole`
 Permissions | `.allusrmdls` `.aum` | Enable or disable all modules for a specific user.  | `.aum enable @someone`
 Permissions | `.allsrvrmdls` `.asm` | Enable or disable all modules for your server.  | `.asm [enable/disable]`
 BlacklistCommands | `.ubl` | Either [add]s or [rem]oves a user specified by a Mention or an ID from a blacklist. **Bot Owner Only** | `.ubl add @SomeUser` or `.ubl rem 12312312313`
 BlacklistCommands | `.cbl` | Either [add]s or [rem]oves a channel specified by an ID from a blacklist. **Bot Owner Only** | `.cbl rem 12312312312`
 BlacklistCommands | `.sbl` | Either [add]s or [rem]oves a server specified by a Name or an ID from a blacklist. **Bot Owner Only** | `.sbl add 12312321312` or `.sbl rem SomeTrashServer`
 CmdCdsCommands | `.cmdcooldown` `.cmdcd` | Sets a cooldown per user for a command. Set it to 0 to remove the cooldown.  | `.cmdcd "some cmd" 5`
 CmdCdsCommands | `.allcmdcooldowns` `.acmdcds` | Shows a list of all commands and their respective cooldowns.  | `.acmdcds`
 FilterCommands | `.fwclear` | Deletes all filtered words on this server. **Requires Administrator server permission.** | `.fwclear`
 FilterCommands | `.srvrfilterinv` `.sfi` | Toggles automatic deletion of invites posted in the server. Does not affect the Bot Owner.  | `.sfi`
 FilterCommands | `.chnlfilterinv` `.cfi` | Toggles automatic deletion of invites posted in the channel. Does not negate the `.srvrfilterinv` enabled setting. Does not affect the Bot Owner.  | `.cfi`
 FilterCommands | `.srvrfilterwords` `.sfw` | Toggles automatic deletion of messages containing filtered words on the server. Does not affect the Bot Owner.  | `.sfw`
 FilterCommands | `.chnlfilterwords` `.cfw` | Toggles automatic deletion of messages containing filtered words on the channel. Does not negate the `.srvrfilterwords` enabled setting. Does not affect the Bot Owner.  | `.cfw`
 FilterCommands | `.fw` | Adds or removes (if it exists) a word from the list of filtered words. Use`.sfw` or `.cfw` to toggle filtering.  | `.fw poop`
 FilterCommands | `.lstfilterwords` `.lfw` | Shows a list of filtered words.  | `.lfw`
 GlobalPermissionCommands | `.listglobalperms` `.lgp` | Lists global permissions set by the bot owner. **Bot Owner Only** | `.lgp`
 GlobalPermissionCommands | `.globalmodule` `.gmod` | Toggles whether a module can be used on any server. **Bot Owner Only** | `.gmod nsfw`
 GlobalPermissionCommands | `.globalcommand` `.gcmd` | Toggles whether a command can be used on any server. **Bot Owner Only** | `.gcmd .stats`
 ResetPermissionsCommands | `.resetperms` | Resets the bot's permissions module on this server to the default value. **Requires Administrator server permission.** | `.resetperms`
 ResetPermissionsCommands | `.resetglobalperms` | Resets global permissions set by bot owner. **Bot Owner Only** | `.resetglobalperms`

###### [Back to ToC](#table-of-contents)

### Pokemon  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Pokemon | `.attack` | Attacks a target with the given move. Use `.movelist` to see a list of moves your type can use.  | `.attack "vine whip" @someguy`
 Pokemon | `.movelist` `.ml` | Lists the moves you are able to use  | `.ml`
 Pokemon | `.heal` | Heals someone. Revives those who fainted. Costs one Currency.   | `.heal @someone`
 Pokemon | `.type` | Get the poketype of the target.  | `.type @someone`
 Pokemon | `.settype` | Set your poketype. Costs one Currency. Provide no parameters to see a list of available types.  | `.settype fire` or `.settype`

###### [Back to ToC](#table-of-contents)

### Searches  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Searches | `.lolban` | Shows top banned champions ordered by ban rate.  | `.lolban`
 Searches | `.crypto` `.c` | Shows basic stats about a cryptocurrency from coinmarketcap.com. You can use either a name or an abbreviation of the currency.  | `.c btc` or `.c bitcoin`
 Searches | `.rip` | rip  | `rip`
 Searches | `.say` | Bot will send the message you typed in this channel. Supports embeds.  | `.say hi`
 Searches | `.weather` `.we` | Shows weather data for a specified city. You can also specify a country after a comma.  | `.we Moscow, RU`
 Searches | `.time` | Shows the current time and timezone in the specified location.  | `.time London, UK`
 Searches | `.youtube` `.yt` | Searches youtubes and shows the first result  | `.yt query`
 Searches | `.imdb` `.omdb` | Queries omdb for movies or series, show first result.  | `.imdb Batman vs Superman`
 Searches | `.randomcat` `.meow` | Shows a random cat image.  | `.meow`
 Searches | `.randomdog` `.woof` | Shows a random dog image.  | `.woof`
 Searches | `.image` `.img` | Pulls the first image found using a search parameter. Use `.rimg` for different results.  | `.img cute kitten`
 Searches | `.randomimage` `.rimg` | Pulls a random image using a search parameter.  | `.rimg cute kitten`
 Searches | `.lmgtfy` | Google something for an idiot.  | `.lmgtfy query`
 Searches | `.shorten` | Attempts to shorten an URL, if it fails, returns the input URL.  | `.shorten https://google.com`
 Searches | `.google` `.g` | Get a Google search link for some terms.  | `.google query`
 Searches | `.magicthegathering` `.mtg` | Searches for a Magic The Gathering card.  | `.magicthegathering about face` or `.mtg about face`
 Searches | `.hearthstone` `.hs` | Searches for a Hearthstone card and shows its image. Takes a while to complete.  | `.hs Ysera`
 Searches | `.yodify` `.yoda` | Translates your normal sentences into Yoda styled sentences!  | `.yoda my feelings hurt`
 Searches | `.urbandict` `.ud` | Searches Urban Dictionary for a word.  | `.ud Pineapple`
 Searches | `.define` `.def` | Finds a definition of a word.  | `.def heresy`
 Searches | `.aq` | Searches Tagdef.com for a hashtag.  | `.# ff`
 Searches | `.catfact` | Shows a random catfact from <http://catfacts-api.appspot.com/api/facts>  | `.catfact`
 Searches | `.revav` | Returns a Google reverse image search for someone's avatar.  | `.revav @SomeGuy`
 Searches | `.revimg` | Returns a Google reverse image search for an image from a link.  | `.revimg Image link`
 Searches | `.safebooru` | Shows a random image from safebooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `.safebooru yuri+kissing`
 Searches | `.wikipedia` `.wiki` | Gives you back a wikipedia link  | `.wiki query`
 Searches | `.color` `.clr` | Shows you pictures of colors which correspond to the inputed hex values. Max 10.  | `.color 00ff00` or `.color f00 0f0 00f`
 Searches | `.videocall` | Creates a private <http://www.appear.in> video call link for you and other mentioned people. The link is sent to mentioned people via a private message.  | `.videocall "@the First" "@Xyz"`
 Searches | `.avatar` `.av` | Shows a mentioned person's avatar.  | `.av @SomeGuy`
 Searches | `.wikia` | Gives you back a wikia link  | `.wikia mtg Vigilance` or `.wikia mlp Dashy`
 Searches | `.bible` | Shows bible verse. You need to supply book name and chapter:verse  | `.bible genesis 3:19`
 AnimeSearchCommands | `.novel` | Searches for a novel on `http://novelupdates.com/`. You have to provide an exact name.  | `.novel the nine cauldrons`
 AnimeSearchCommands | `.mal` | Shows basic info from a MyAnimeList profile.  | `.mal straysocks`
 AnimeSearchCommands | `.anime` `.ani` `.aq` | Queries anilist for an anime and shows the first result.  | `.ani aquarion evol`
 AnimeSearchCommands | `.manga` `.mang` `.mq` | Queries anilist for a manga and shows the first result.  | `.mq Shingeki no kyojin`
 FeedCommands | `.feed` `.feedadd` | Subscribes to a feed. Bot will post an update up to once every 10 seconds. You can have up to 10 feeds on one server. All feeds must have unique URLs. **Requires ManageMessages server permission.** | `.feed https://www.rt.com/rss/`
 FeedCommands | `.feedremove` `.feedrm` `.feeddel` | Stops tracking a feed on the given index. Use `.feeds` command to see a list of feeds and their indexes. **Requires ManageMessages server permission.** | `.feedremove 3`
 FeedCommands | `.feeds` `.feedlist` | Shows the list of feeds you've subscribed to on this server. **Requires ManageMessages server permission.** | `.feeds`
 JokeCommands | `.yomama` `.ym` | Shows a random joke from <http://api.yomomma.info/>  | `.ym`
 JokeCommands | `.randjoke` `.rj` | Shows a random joke from <http://tambal.azurewebsites.net/joke/random>  | `.rj`
 JokeCommands | `.chucknorris` `.cn` | Shows a random Chuck Norris joke from <http://api.icndb.com/jokes/random/>  | `.cn`
 JokeCommands | `.wowjoke` | Get one of Kwoth's penultimate WoW jokes.  | `.wowjoke`
 JokeCommands | `.magicitem` `.mi` | Shows a random magic item from <https://1d4chan.org/wiki/List_of_/tg/%27s_magic_items>  | `.mi`
 MemegenCommands | `.memelist` | Pulls a list of memes you can use with `.memegen` from http://memegen.link/templates/  | `.memelist`
 MemegenCommands | `.memegen` | Generates a meme from memelist with top and bottom text.  | `.memegen biw "gets iced coffee" "in the winter"`
 OsuCommands | `.osu` | Shows osu stats for a player.  | `.osu Name` or `.osu Name taiko`
 OsuCommands | `.osub` | Shows information about an osu beatmap.  | `.osub https://osu.ppy.sh/s/127712`
 OsuCommands | `.osu5` | Displays a user's top 5 plays.  | `.osu5 Name`
 OverwatchCommands | `.overwatch` `.ow` | Show's basic stats on a player (competitive rank, playtime, level etc) Region codes are: `eu` `us` `cn` `kr`  | `.ow us Battletag#1337` or `.overwatch eu Battletag#2016`
 PathOfExileCommands | `.pathofexile` `.poe` | Searches characters for a given Path of Exile account. May specify league name to filter results.  | `.poe "Zizaran"`
 PathOfExileCommands | `.pathofexileleagues` `.poel` | Returns a list of the main Path of Exile leagues.  | `.poel`
 PathOfExileCommands | `.pathofexilecurrency` `.poec` | Returns the chaos equivalent of a given currency or exchange rate between two currencies.  | `.poec Standard "Mirror of Kalandra"`
 PathOfExileCommands | `.pathofexileitem` `.poei` | Searches for a Path of Exile item from the Path of Exile GamePedia.  | `.poei "Quill Rain"`
 PlaceCommands | `.placelist` | Shows the list of available tags for the `.place` command.  | `.placelist`
 PlaceCommands | `.place` | Shows a placeholder image of a given tag. Use `.placelist` to see all available tags. You can specify the width and height of the image as the last two optional parameters.  | `.place Cage` or `.place steven 500 400`
 PokemonSearchCommands | `.pokemon` `.pkmn` | Searches for a pokemon.  | `.poke Sylveon`
 PokemonSearchCommands | `.pokemonability` `.pokeab` | Searches for a pokemon ability.  | `.pokeab overgrow`
 StreamNotificationCommands | `.smashcast` `.hb` | Notifies this channel when the specified user starts streaming. **Requires ManageMessages server permission.** | `.smashcast SomeStreamer`
 StreamNotificationCommands | `.twitch` `.tw` | Notifies this channel when the specified user starts streaming. **Requires ManageMessages server permission.** | `.twitch SomeStreamer`
 StreamNotificationCommands | `.picarto` `.pa` | Notifies this channel when the specified user starts streaming. **Requires ManageMessages server permission.** | `.picarto SomeStreamer`
 StreamNotificationCommands | `.mixer` `.bm` | Notifies this channel when the specified user starts streaming. **Requires ManageMessages server permission.** | `.mixer SomeStreamer`
 StreamNotificationCommands | `.streamadd` `.stadd` | Notifies this channel when the user's stream on the specified URL goes online or offline. **Requires ManageMessages server permission.** | `.stadd twitch.tv/someguy`
 StreamNotificationCommands | `.streamremove` `.strm` | Removes notifications of a specified stream on the specified platform on this channel. You can also just specify an url. **Requires ManageMessages server permission.** | `.strm Twitch SomeGuy` or `.strm twitch.tv/someguy`
 StreamNotificationCommands | `.streamsclear` | Deletes all followed streams on this server. **Requires Administrator server permission.** | `.streamsclear`
 StreamNotificationCommands | `.liststreams` `.ls` | Lists all streams you are following on this server.  | `.ls`
 StreamNotificationCommands | `.streamoff` `.stoff` | Toggles whether the bot will notify about streams going offline. **Requires ManageMessages server permission.** | `.stoff`
 StreamNotificationCommands | `.streammsg` | Specify an url of a stream you're already following, and a message in order to set a stream notification message which will show up every time stream comes online. **Requires ManageMessages server permission.** | `.streammsg https://www.twitch.tv/trolhamonas/ Hello world`
 StreamNotificationCommands | `.checkstream` `.cs` | Checks if a user is online on a certain streaming platform.  | `.cs twitch MyFavStreamer`
 TranslateCommands | `.translate` `.trans` | Translates from>to text. From the given language to the destination language.  | `.trans en>fr Hello`
 TranslateCommands | `.autotrans` `.at` | Starts automatic translation of all messages by users who set their `.atl` in this channel. You can set "del" parameter to automatically delete all translated user messages. **Requires Administrator server permission.** **Bot Owner Only** | `.at` or `.at del`
 TranslateCommands | `.autotranslang` `.atl` | Sets your source and target language to be used with `.at`. Specify no parameters to remove previously set value.  | `.atl en>fr`
 TranslateCommands | `.translangs` | Lists the valid languages for translation.  | `.translangs`
 XkcdCommands | `.xkcd` | Shows a XKCD comic. Specify no parameters to retrieve a random one. Number parameter will retrieve a specific comic, and "latest" will get the latest one.  | `.xkcd` or `.xkcd 1400` or `.xkcd latest`

###### [Back to ToC](#table-of-contents)

### Utility  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Utility | `.togethertube` `.totube` | Creates a new room on <https://togethertube.com> and shows the link in the chat.  | `.totube`
 Utility | `.whosplaying` `.whpl` | Shows a list of users who are playing the specified game.  | `.whpl Overwatch`
 Utility | `.inrole` | Lists every person from the specified role on this server. You can use role ID, role name.  | `.inrole Some Role`
 Utility | `.checkperms` | Checks yours or bot's user-specific permissions on this channel.  | `.checkperms me` or `.checkperms bot`
 Utility | `.userid` `.uid` | Shows user ID.  | `.uid` or `.uid @SomeGuy`
 Utility | `.roleid` `.rid` | Shows the id of the specified role.  | `.rid Some Role`
 Utility | `.channelid` `.cid` | Shows current channel ID.  | `.cid`
 Utility | `.serverid` `.sid` | Shows current server ID.  | `.sid`
 Utility | `.roles` | List roles on this server or roles of a user if specified. Paginated, 20 roles per page.  | `.roles 2` or `.roles @Someone`
 Utility | `.channeltopic` `.ct` | Sends current channel's topic as a message.  | `.ct`
 Utility | `.createinvite` `.crinv` | Creates a new invite which has infinite max uses and never expires. **Requires CreateInstantInvite channel permission.** | `.crinv`
 Utility | `.stats` `.info` | Shows some basic stats for Ene.  | `.stats`
 Utility | `.showemojis` `.se` | Shows a name and a link to every SPECIAL emoji in the message.  | `.se A message full of SPECIAL emojis`
 Utility | `.listservers` | Lists servers the bot is on with some basic info. 15 per page. **Bot Owner Only** | `.listservers 3`
 Utility | `.savechat` | Saves a number of messages to a text file and sends it to you. **Bot Owner Only** | `.savechat 150`
 Utility | `.ping` | Ping the bot to see if there are latency issues.  | `.ping`
 BotConfigCommands | `.botconfigedit` `.bce` | Sets one of available bot config settings to a specified value. Use the command without any parameters to get a list of available settings. **Bot Owner Only** | `.bce CurrencyName b1nzy` or `.bce`
 CalcCommands | `.calculate` `.calc` | Evaluate a mathematical expression.  | `.calc 1+1`
 CalcCommands | `.calcops` | Shows all available operations in the `.calc` command  | `.calcops`
 CommandMapCommands | `.aliasesclear` `.aliasclear` | Deletes all aliases on this server. **Requires Administrator server permission.** | `.aliasclear`
 CommandMapCommands | `.alias` `.cmdmap` | Create a custom alias for a certain Ene command. Provide no alias to remove the existing one. **Requires Administrator server permission.** | `.alias allin .bf all h` or `.alias "linux thingy" >loonix Spyware Windows`
 CommandMapCommands | `.aliaslist` `.cmdmaplist` `.aliases` | Shows the list of currently set aliases. Paginated.  | `.aliaslist` or `.aliaslist 3`
 InfoCommands | `.serverinfo` `.sinfo` | Shows info about the server the bot is on. If no server is supplied, it defaults to current one.  | `.sinfo Some Server`
 InfoCommands | `.channelinfo` `.cinfo` | Shows info about the channel. If no channel is supplied, it defaults to current one.  | `.cinfo #some-channel`
 InfoCommands | `.userinfo` `.uinfo` | Shows info about the user. If no user is supplied, it defaults a user running the command.  | `.uinfo @SomeUser`
 InfoCommands | `.activity` | Checks for spammers. **Bot Owner Only** | `.activity`
 PatreonCommands | `.parewrel` | Forces the update of the list of patrons who are eligible for the reward. **Bot Owner Only** | `.parewrel`
 PatreonCommands | `.clparew` `.claparew` | Claim patreon rewards. If you're subscribed to bot owner's patreon you can use this command to claim your rewards - assuming bot owner did setup has their patreon key.  | `.clparew`
 QuoteCommands | `.listquotes` `.liqu` | Lists all quotes on the server ordered alphabetically or by ID. 15 Per page.  | `.liqu 3` or `.liqu 3 id`
 QuoteCommands | `..` | Shows a random quote with a specified name.  | `.. abc`
 QuoteCommands | `.qsearch` | Shows a random quote for a keyword that contains any text specified in the search.  | `.qsearch keyword text`
 QuoteCommands | `.quoteid` `.qid` | Displays the quote with the specified ID number. Quote ID numbers can be found by typing `.liqu [num]` where `[num]` is a number of a page which contains 15 quotes.  | `.qid 123456`
 QuoteCommands | `.quotedel` `.qdel` | Deletes a quote with the specified ID. You have to be either server Administrator or the creator of the quote to delete it.  | `.qdel 123456`
 QuoteCommands | `.delallq` `.daq` | Deletes all quotes on a specified keyword. **Requires Administrator server permission.** | `.delallq kek`
 RemindCommands | `.remind` | Sends a message to you or a channel after certain amount of time. First parameter is `me`/`here`/'channelname'. Second parameter is time in a descending order (mo>w>d>h>m) example: 1w5d3h10m. Third parameter is a (multiword) message.  | `.remind me 1d5h Do something` or `.remind #general 1m Start now!`
 RemindCommands | `.remindlist` `.remindl` `.remindlst` | Lists all reminders you created. Paginated.  | `.remindlist 1`
 RemindCommands | `.reminddel` `.remindrm` | Deletes a reminder on the specified index.  | `.remindrm 3`
 RemindCommands | `.remindtemplate` | Sets message for when the remind is triggered.  Available placeholders are `%user%` - user who ran the command, `%message%` - Message specified in the remind, `%target%` - target channel of the remind. **Bot Owner Only** | `.remindtemplate %user%, do %message%!`
 RepeatCommands | `.repeatinvoke` `.repinv` | Immediately shows the repeat message on a certain index and restarts its timer. **Requires ManageMessages server permission.** | `.repinv 1`
 RepeatCommands | `.repeatremove` `.reprm` | Removes a repeating message on a specified index. Use `.repeatlist` to see indexes. **Requires ManageMessages server permission.** | `.reprm 2`
 RepeatCommands | `.repeat` | Repeat a message every specified number of minutes in the current channel. You can instead specify time of day for the message to be repeated at daily (make sure you've set your server's timezone). You can have up to 5 repeating messages on the server in total. **Requires ManageMessages server permission.** | `.repeat -i 5 -m "Hello there" -n` or `.repeat 17:30 -m "tea time"`
 RepeatCommands | `.repeatlist` `.replst` | Shows currently repeating messages and their indexes. **Requires ManageMessages server permission.** | `.repeatlist`
 StreamRoleCommands | `.streamrole` | Sets a role which is monitored for streamers (FromRole), and a role to add if a user from 'FromRole' is streaming (AddRole). When a user from 'FromRole' starts streaming, they will receive an 'AddRole'. Provide no parameters to disable **Requires ManageRoles server permission.** | `.streamrole "Eligible Streamers" "Featured Streams"`
 StreamRoleCommands | `.streamrolekw` `.srkw` | Sets keyword which is required in the stream's title in order for the streamrole to apply. Provide no keyword in order to reset. **Requires ManageRoles server permission.** | `.srkw` or `.srkw PUBG`
 StreamRoleCommands | `.streamrolebl` `.srbl` | Adds or removes a blacklisted user. Blacklisted users will never receive the stream role. **Requires ManageRoles server permission.** | `.srbl add @b1nzy#1234` or `.srbl rem @b1nzy#1234`
 StreamRoleCommands | `.streamrolewl` `.srwl` | Adds or removes a whitelisted user. Whitelisted users will receive the stream role even if they don't have the specified keyword in their stream title. **Requires ManageRoles server permission.** | `.srwl add @b1nzy#1234` or `.srwl rem @b1nzy#1234`
 UnitConverterCommands | `.convertlist` | List of the convertible dimensions and currencies.  | `.convertlist`
 UnitConverterCommands | `.convert` | Convert quantities. Use `.convertlist` to see supported dimensions and currencies.  | `.convert m km 1000`
 VerboseErrorCommands | `.verboseerror` `.ve` | Toggles whether the bot should print command errors when a command is incorrectly used. **Requires ManageMessages server permission.** | `.ve`

###### [Back to ToC](#table-of-contents)

### Xp  
Submodule | Command and aliases | Description | Usage
----------|----------------|--------------|-------
 Xp | `.experience` `.xp` | Shows your xp stats. Specify the user to show that user's stats instead.  | `.xp`
 Xp | `.xplvluprewards` `.xprews` `.xpcrs` `.xprrs` `.xprolerewards` `.xpcurrewards` | Shows currently set level up rewards.  | `.xprews`
 Xp | `.xprolereward` `.xprr` | Sets a role reward on a specified level. Provide no role name in order to remove the role reward. **Requires ManageRoles server permission.** | `.xprr 3 Social`
 Xp | `.xpcurreward` `.xpcr` | Sets a currency reward on a specified level. Provide no amount in order to remove the reward. **Bot Owner Only** | `.xpcr 3 50`
 Xp | `.xpnotify` `.xpn` | Sets how the bot should notify you when you get a `server` or `global` level. You can set `dm` (for the bot to send a direct message), `channel` (to get notified in the channel you sent the last message in) or `none` to disable.  | `.xpn global dm` or `.xpn server channel`
 Xp | `.xpexclude` `.xpex` | Exclude a channel, role or current server from the xp system. **Requires Administrator server permission.** | `.xpex Role Excluded-Role` or `.xpex Server`
 Xp | `.xpexclusionlist` `.xpexl` | Shows the roles and channels excluded from the XP system on this server, as well as whether the whole server is excluded.  | `.xpexl`
 Xp | `.xpleaderboard` `.xplb` | Shows current server's xp leaderboard.  | `.xplb`
 Xp | `.xpgleaderboard` `.xpglb` | Shows the global xp leaderboard.  | `.xpglb`
 Xp | `.xpadd` | Adds xp to a user on the server. This does not affect their global ranking. You can use negative values. **Requires Administrator server permission.** | `.xpadd 100 @b1nzy`
 Club | `.clubtransfer` | Transfers the ownership of the club to another member of the club.  | `.clubtransfer @b1nzy`
 Club | `.clubadmin` | Assigns (or unassigns) staff role to the member of the club. Admins can ban, kick and accept applications.  | `.clubadmin`
 Club | `.clubcreate` | Creates a club. You must be at least level 5 and not be in the club already.  | `.clubcreate b1nzy's friends`
 Club | `.clubicon` | Sets the club icon.  | `.clubicon https://i.imgur.com/htfDMfU.png`
 Club | `.clubinfo` | Shows information about the club.  | `.clubinfo b1nzy's friends#123`
 Club | `.clubbans` | Shows the list of users who have banned from your club. Paginated. You must be club owner to use this command.  | `.clubbans 2`
 Club | `.clubapps` | Shows the list of users who have applied to your club. Paginated. You must be club owner to use this command.  | `.clubapps 2`
 Club | `.clubapply` | Apply to join a club. You must meet that club's minimum level requirement, and not be on its ban list.  | `.clubapply b1nzy's friends#123`
 Club | `.clubaccept` | Accept a user who applied to your club.  | `.clubaccept b1nzy#1337`
 Club | `.clubleave` | Leaves the club you're currently in.  | `.clubleave`
 Club | `.clubkick` | Kicks the user from the club. You must be the club owner. They will be able to apply again.  | `.clubkick b1nzy#1337`
 Club | `.clubban` | Bans the user from the club. You must be the club owner. They will not be able to apply again.  | `.clubban b1nzy#1337`
 Club | `.clubunban` | Unbans the previously banned user from the club. You must be the club owner.  | `.clubunban b1nzy#1337`
 Club | `.clublevelreq` | Sets the club required level to apply to join the club. You must be club owner. You can't set this number below 5.  | `.clublevelreq 7`
 Club | `.clubdesc` | Sets the club description. Maximum 150 characters. Club owner only.  | `.clubdesc This is the best club please join.`
 Club | `.clubdisband` | Disbands the club you're the owner of. This action is irreversible.  | `.clubdisband`
 Club | `.clublb` | Shows club rankings on the specified page.  | `.clublb 2`
 ResetCommands | `.xpreset` | Resets specified user's XP, or the XP of all users in the server. You can't reverse this action. **Requires Administrator server permission.** | `.xpreset @b1nzy` or `.xpreset`
