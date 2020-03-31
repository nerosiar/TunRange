# Consommi Tounsi  WebApp/Manager

<h1 align="center">
	<br>
	<img src="https://github.com/nerosiar/TunRange/blob/master/logo2rangers.png" alt="Consommi Tounsi Logo">
	<br>
</h1>

<h3 align="center">
	Command Line Version
	<br>
	<a href="https://www.twitch.tv/dowright" target="_blank">
		<img src="https://github.com/ProHackTech/DNX-FWALL-CMD/blob/master/Readme_Social/twitch.png" alt="DOWRIGHTTV" />
	</a>
</h3>

<h2>Before Running</h2>

- [+] Edit data/config.json to reflect your system

- [+] Change environment variable in dnx_run.sh

- [+] Use dnx_run.sh to start the system

<h2>Instructional Demo</h2>

- NOTE: The front end is not included in public/foss version of application yet, but the funcionality of the system is the same.
Edit json files accordingly to implement specific system controls, eg whitelist, blacklist, chat records, etc. CLI is in progress and some settings can be configured using it.


* [x] The "seedling" role can view all public channels
* [x] Move all users into the "seedling" role
* [x] New users to the discord are placed into a "germinating" role
  * [x] All channels are hidden except for "welcome" and "introductions"
  * [x] Only have the ability to post in "introductions"
* [x] To be moved into the "seedling" role
  * [x] MUST emoji react the code of conduct post in "welcome"
  * [x] MUST post an introduction in the "introductions" channel
    * [x] Introduction must be at least 40 characters long.
* [x] Watch code of conduct for emoji reactions and decide if we should move them to seedling role

## TODO
* [x] Setup eslint
* [x] Refactor CONST variables to .env
  * [x] Create a config object, load from .env
* [x] Refactor methods to use a local db like [nedb](https://github.com/louischatriot/nedb/)
  * [x] Listen for new users
    * [x] Add to db with:
      * CodeOfConduct - false
      * Introduction - false
  * [x] Listen for emoji reactions to COC message
    * Update db
  * [x] Listen for messages in introductions
    * [x] Update db when a message recieved for new user with length > 40
* [ ] ON startup
  * [x] Add all germinating users to the db
    * [x] Include COC
    * [x] Include Intro Message
  * [ ] get all users without a role and add them to germinating
* [x] Send a message when a user joins the server.
  * [ ] Log in DB if welcome message has been sent
* [x] Send a message when a user is moved into the seedling group.
* [ ] Move all users that have not yet posted a message into the "germinating" role
* [ ] Deploy!
* [ ] Stream notify channel
  * [ ] Join this channel to be notified when CJ goes live
* [ ] Listen for leave server
  * [ ] Remove COC reactions
* [ ] Listen for role change
  * [ ] Remove from DB

## Resources

### Join a Bot to a server

* Make a request in the browser to:
  * https://discordapp.com/api/oauth2/authorize?client_id=12345&scope=bot&permissions=1

### discord.js docs/examples

* https://discord.js.org/#/docs/main/stable/general/welcome
* https://discordjs.guide/#/popular-topics/miscellaneous-examples

