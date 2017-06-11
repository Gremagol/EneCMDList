##Custom Reactions
###Important
*	For modifying **global** custom reactions, the ones which will work across all the servers your bot is connected to, you **must** be a Bot Owner.  
You must also use the commands for adding, deleting and listing these reactions in a direct message with the bot.  
*	For modifying **local** custom reactions, the ones which will only work on the server that they are added on, it is required to have the **Administrator** permission.  
You must also use the commands for adding, deleting and listing these reactions in the server you want the custom reactions to work on.  

###Commands and Their Use
| Command Name | Description | Example |
|:------------:|-------------|---------|
|`acr` | Add a custom reaction with a trigger and a response. Running this command in a server requries the Administrator permission. Running this command adds a new global custom reaction. **Gremagol only** | `.acr "hello" Hi there %user%`
|`lcr` | Lists global or server custom reactions (20 commands per page). Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions. Specifying `all` argument instead of the number will DM you a text file with a list of all custom reactions.  | `.lcr 1` or `.lcr all`
|`lcrg` | Lists global or server custom reactions (20 commands per page) grouped by trigger, and show a number of responses for each. Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions.  | `.lcrg 1`
|`scr` | Shows a custom reaction's response on a given ID.  | `.scr 1`
|`dcr` | Deletes a custom reaction on a specific index. If ran in DM, it deletes a global custom reaction. **Gremagol only**. If ran in a server, it requires Administration privileges and removes server custom reaction.  | `.dcr 5`
|`crdm` | Toggles whether the response message of the custom reaction will be sent as a direct message.  | `.crdm 44`
|`crad` | Toggles whether the message triggering the custom reaction will be automatically deleted.  | `.crad 59`
|`crstatsclear` | Resets the counters on `.crstats`. You can specify a trigger to clear stats only for that trigger. **Gremagol only** | `.crstatsclear` or `.crstatsclear rng`
|`crstats` | Shows a list of custom reactions and the number of times they have been executed. Paginated with 10 per page. Use `.crstatsclear` to reset the counters.  | `.crstats` or `.crstats 3`


####Now that we know the commands let's take a look at an example of adding a command with `.acr`,  
`.acr "Nice Weather" It sure is, %user%!`  

This command can be split into two different arguments:  

* 	 The trigger, `"Nice Weather"`  
* 	 And the response, `It sure is, %user%!`  

An important thing to note about the triger is that, to be more than one word, we had to wrap it with quotation marks, `"Like this"` otherwise, only the first word would have been recognised as the trigger, and the second word would have been recognised as part of the response.  

There's no special requirement for the formatting of the response, so we could just write it in exactly the same way we want it to respond, albeit with a placeholder - which will be explained in this next section.  

Now, if that command was ran in a server, anyone on that server can make the bot mention them, saying `It sure is, @Username` anytime they say "Nice Weather". If the command is ran in a direct message with the bot, then the custom reaction can be used on every server the bot is connected to.  

###Block global Custom Reactions
If you want to disable some global custom reactions which you do not like, and you do not want to remove them or you are not the bot owner you can do so by adding a new Custom Reaction with the same trigger on your server, and set the response to `-`.

For example:
`.acr /o/ -`

Now if you try to trigger `/o/`, it won't print anything.

###Placeholders!
There are currently three different placeholders which we will look at, with more placeholders potentially coming in the future.  

| Placeholder | Description | Example Usage | Usage |
|:-----------:|-------------|---------------|-------|
|`%mention%`|The `%mention%` placeholder is triggered when you type `@BotName` - It's important to note that if you've given the bot a custom nickname, this trigger won't work!|```.acr "Hello %mention%" I,  %mention%, also say hello!```|Input: "Hello @BotName" Output: "I, @BotName, also say hello!"|
|`%user%`|The `%user%` placeholder mentions the person who said the command|`.acr "Who am I?" You are %user%!`|Input: "Who am I?" Output: "You are @Username!"|
|`%rng%`|The `%rng%` placeholder generates a random number between 0 and 10. You can also specify a custom range (%rng1-100%) even with negative numbers: `%rng-9--1%` (from -9 to -1) . |`.acr "Random number" %rng%`|Input: "Random number" Output: "2"|
|`%rnduser%`|The `%rnduser%` placeholder mentions a random user from the server. |`.acr "Random user" %rnduser%`|Input: "Random number" Output: @SomeUser|
|`%target%`|The `%target%` placeholder is used to make Shinoa Mention another person or phrase, it is only supported as part of the response|`.acr "Say this: " %target%`|Input: "Say this: I, @BotName, am a parrot!". Output: "I, @BotName, am a parrot!".|

