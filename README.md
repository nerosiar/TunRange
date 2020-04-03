# Consommi Tounsi  WebApp/Manager

<h1 align="center">
	<br>
	<img src="https://github.com/nerosiar/TunRange/blob/master/logo2rangers.png" alt="Consommi Tounsi Logo">
	<br>
</h1>

<h3 align="center">
	Contact me to get full version from gitlab 
	<br>
	<a href="" target="_blank">
		<img src="https://github.com/ProHackTech/DNX-FWALL-CMD/blob/master/Readme_Social/twitch.png" alt="nerosiar" />
	</a>
</h3>

<h2>Before Running</h2>

- [+] Edit /.idea to reflect your Development environment or create  

- [+] Change environment variable in ConsommiTounsi.iml

- [+] Use wildfly-11.0 to start the system   ()

<h2>Instructional Demo</h2>

- NOTE: The front end is not included in public/foss version of application yet, but the funcionality of the system is the same.
Edit json files accordingly to implement specific system controls, eg Publication , whitelist, blacklist, chat room , etc. REST is in progress and some settings can be configured using it.
The full version of the project is updated Beta-version on gitlab

#### Forum 
######### Post (publication) Management
     * CRUD subject 
     * test subject redandant
     * Automatic deletion of subjects without interaction
     * Topic Display
     * Subject display more appropriate to the profile according to its research and interactions
 ########## Comment Management 
     * CRUD Comment
     * Prohibited word dictionaries
     * the most relevant comments
   ########### Rating 
     * subject evaluation
     * comments evaluation (like / dislike / Emoji)
* [x] The "seedling" role can view all public channels
* [x] Move all users into the "seedling" role
* [x] New users to the App are placed into a "germinating" role
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
  * http://localhost:9090/chatroom/${userToCommunicate}/BeginCommunication

### chat soocket&websocket  docs/examples

* https://koor.fr/Java/TutorialJEE/jee_websocket_chat.wp
* https://mvnrepository.com/artifact/io.socket/engine.io-server



## Infrastructure Security Design Overview
  * Secure Low level Inrastructure :
    - [x] Security of physical Premises 
    - [x] Hardware Design and Provenance 
    - [x] Secure  Boot Stack and Machine Identity
  
  * Secure Service Deployment 
    - [x] Service Identity , Integrity and Isolation 
    - [x] Inter-Service Access Management 
    - [x] Encryption of Inter-Service Communication 
    - [x] Access Management of End User Data 
  
  * Secure Data Storage 
    - [x] Encryption At REST 
    - [x] Delation of Data 
  
  * Secure Internet Communication 
    - [x] Google Front-end Service 
    - [x] Denial of Service (DoS) Protection 
    - [x] User Authentication 
  
  * Operation Security 
    - [x] Safe Software Development 
    - [x] Reducing Insider Risk 
    - [x] Intrusion Detection 