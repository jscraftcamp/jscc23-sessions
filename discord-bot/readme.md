# How to build a discord bot and make it interact with a server and its users

by Gustaf

- Discord.js “best” option for building bots (well known, big community, well documented, easy to learn / use)
- To create a bot, create a bot user account on discord (you get a secret that you use in your code for the bot to “log in”)
- You can customise your bot on the same website (profile pic, description, name, etc)
- Discord Client -> Advanced Settings -> Developer Mode is useful for bot debugging, e. g. getting channel ids, user ids
- To invite a bot to your server: on discord dev site -> OAuth2 -> URL Generator -> Tick permissions the bot needs -> Click the invite link -> Fill out form
- To let Discord know you have a command, you need to “build” a command -> autocoder.com/tools/discord/command/builder helps with that (do it in a separate js file or via HTTP call with postman or whatever)
- Actual functionality like third party apis, etc. are just normal JavaScript like always. You basically just wrap it inside discords api
